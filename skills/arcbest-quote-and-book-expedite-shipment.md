---
name: arcbest-quote-and-book-expedite-shipment
description: Quote an ArcBest Expedite time-critical freight shipment, present the options to a human, tender a booking request, and poll until ArcBest confirms it and returns the order number.
api: arcbest:arcbest-expedite-customer-api
operations:
  - authorizePost
  - quotesSubmitQuote
  - quotesBookExpediteQuote
  - quotesGetBookingStatus
generated: '2026-09-04'
method: generated
source: openapi/arcbest-expedite-customer-api-openapi.yml, docs/arcbest-expedite-customer-quote-book-instructions-2024-08.pdf
---

# Quote and book an ArcBest Expedite shipment

Base URL: `https://api.arcb.com/expedite/customer`. Start against the test host
`https://test.api.arcb.com/expedite/customer` — ArcBest asks integrators to.

## Before you start

Credentials are not self-serve. A `ClientId` (32 chars) and `ClientSecret` (64 chars) are issued by
ArcBest support (api@arcb.com). If you do not have them, stop and say so — there is no signup flow.

## Steps

1. **Authorize** — `authorizePost`: `POST /authorize` with `{"ClientId": "...", "ClientSecret": "..."}`.
   The response is `{"AccessToken": "..."}` (~1000 characters). Send it on every later call as
   `Authorization: Bearer <accesstoken>`. Token lifetime is not published, so re-authorize on a 401
   rather than caching indefinitely.

2. **Quote** — `quotesSubmitQuote`: `POST /quotes`. Build the body from
   `json-schema/arcbest-expedite-quote-request-model.json`. ArcBest's own rules, verbatim:
   - `Origin.ReadyDate` must be in the future, and `ReadyDate` must precede `ByDate` — the pair is
     the window in which the load is ready and by when it must be processed.
   - 2-character `State`, 5-digit `PostalCode`, 3-character `Country` (`"USA"`).
   - Freight class goes in `ShipUnits[].Class`; hazardous loads need a full `HazmatItem`
     (ProperShippingName, Nos, Class, Id, PackingGroup, EmergencyPhone).

3. **Read the envelope, not the status.** A rejected quote comes back as HTTP 200 with every payload
   field null and `Errors[]` populated with `{Code, Message}` objects. Treat a non-empty `Errors[]`
   as a failure. See `errors/arcbest-problem-types.yml`.

4. **Show the options to a human.** Present `QuoteResponse.Products.ExpediteOptions`, the returned
   notes, and the returned earliest pickup date. Do not book on your own judgement — the next step
   commits a truck.

5. **Book** — `quotesBookExpediteQuote`: `POST /quotes/booking-request/expedite` with the chosen
   option's `UnifiedQuoteNo` (a `P000…` string) and `ResponseNo`. For a time-critical forwarding
   quote use `quotesBookTimeCriticalForwardingQuote` (`POST /quotes/booking-request/time-critical-forwarding`)
   instead.

   **This is the dangerous call.** There is no idempotency key and there is no cancel operation on
   this API. A duplicate request is a duplicate physical tender, and ArcBest's booking request terms
   charge a truck-ordered-but-not-used fee if a shipment is cancelled within 24 hours of the
   scheduled pickup once a driver is dispatched. Never retry this call blind — go to step 6 first.

6. **Poll** — `quotesGetBookingStatus`: `GET /quotes/booking-request/status?quoteNo=P000…`.
   Statuses: `Quoted` (a quote exists, no booking request), `Booking`, `Booking in Progress`
   (received, being processed), `Shipment Booked` (success — the order number is returned as
   `yyyymm12345`), `Unable to Fulfill`, `Unknown`. ArcBest operators confirm within minutes. Poll
   with backoff; this endpoint is also your replay guard — if it already reports
   `Booking in Progress` or `Shipment Booked`, a retry of step 5 is a duplicate, not a repair.

7. Handle `Unable to Fulfill` by re-quoting, not by re-booking.
