---
name: arcbest-tms-book-and-document-load
description: Run the full ArcBest Expedite Third Party TMS flow from a transportation management system — quote, book, poll status, pull the Bill of Lading, and attach PO and customer reference numbers.
api: arcbest:arcbest-expedite-tms-api
operations:
  - quoteCreate
  - bookingCreate
  - bookingGetStatus
  - orderBol
  - orderUpdateRefs
generated: '2026-09-04'
method: generated
source: openapi/arcbest-expedite-tms-api-openapi.yml, docs/arcbest-expedite-tms-quote-book-instructions-2024-08.pdf
---

# Book and document an ArcBest Expedite load from a TMS

Base URL: `https://api.arcb.com/expedite/digital` (test: `https://test.api.arcb.com/expedite/digital`).
Auth is **HTTP Basic** — username and password issued by the ArcBest Expedite team. This is a
different scheme from the Customer API; do not send a bearer token here.

## Steps

1. **Quote** — `quoteCreate`: `POST /quote`. Body carries `Source`, `UserName`,
   `ArcBestCustomerId`, `Payer`, `Shipper`, `Consignee`, `PickupDate`, `Commodities[]`
   (`Length`, `Width`, `Height`, `Weight`, `Quantity`, `PackageType`, `FreightClass`, `NMFCNumber`,
   `NMFCSub`), `NotifyBeforeDelivery` and `Accessorials[]`.

   The response carries `ExpediteQuoteId`, `Charge`, `ItemizedCharges`, `AdvertisedTransitDays`,
   `AdvertisedDueDate`, `PickupDate`, `Notes` and `Errors`. **Check `Errors[]` even on a 200** —
   rejections (dimensions or weight beyond limits, incompatible scheduling, rejected accessorials,
   a lane whose mileage is not valid for ArcBest expedite) arrive inside a 200 with every other field
   null.

   Show the customer the returned `Notes` and the returned earliest `PickupDate`; seed the
   confirmation step from that date rather than from what they originally asked for.

2. **Book** — `bookingCreate`: `PUT /booking`, once the customer has finalised pickup and delivery
   windows and provided contacts and pickup/dropoff instructions.

   **No idempotency key and no cancel operation exist on this API.** A repeated `PUT /booking` is a
   repeated physical tender. If a call times out, go to step 3 before retrying.

3. **Poll** — `bookingGetStatus`: `GET /booking/status?quoteids=P000…&quoteids=P000…` (repeat the
   parameter per quote). The response is keyed by quote id with `Status`, `StatusString`
   (`BOOKINGINPROGRESS`, `SHIPMENTBOOKED`, …), `ExpediteOrderNo` and `ArcBestOrderNo`. Operators book
   within minutes. Consume both order numbers on `SHIPMENTBOOKED`.

4. **Bill of Lading** — `orderBol`: `GET /order/bol/{expediteOrderNo}`. Use the **expedite** order
   number here — it is the BOL number.

5. **References** — `orderUpdateRefs`: `POST /order/refs/{arcbOrderNo}` with a JSON array of
   `{"type": "PO" | "CUSTREF", "value": "…"}`. Use the **ArcBest** order (pro) number here, not the
   expedite order number. Swapping the two is the most common error on this surface.

6. **Receive milestones.** ArcBest POSTs the full order history to a tracking endpoint you build and
   register with them, on every milestone and location ping. Refresh your history from each push
   (in full, or by appending entries newer than your last timestamp). Model and sequence are in
   `json-schema/arcbest-expedite-tracking-model.json` and
   `asyncapi/arcbest-track-and-trace-webhooks.yml`. There is no published signature on these pushes —
   authenticate them with whatever credential you gave ArcBest for your endpoint.
