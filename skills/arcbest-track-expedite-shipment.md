---
name: arcbest-track-expedite-shipment
description: Look up the status of a booked ArcBest Expedite shipment by reference number, and resolve the status codes it returns.
api: arcbest:arcbest-expedite-customer-api
operations:
  - authorizePost
  - shipmentsGetShipmentsByReferenceNumbers
  - shipmentsGetShipmentStatusCodes
generated: '2026-09-04'
method: generated
source: openapi/arcbest-expedite-customer-api-openapi.yml, docs/arcbest-expedite-customer-quote-book-instructions-2024-08.pdf
---

# Track a booked ArcBest Expedite shipment

Base URL: `https://api.arcb.com/expedite/customer` (test: `https://test.api.arcb.com/expedite/customer`).

All operations here are reads. Nothing in this skill changes state or costs money.

## Steps

1. **Authorize** — `authorizePost`: `POST /authorize`, then send `Authorization: Bearer <accesstoken>`.

2. **Resolve the vocabulary once** — `shipmentsGetShipmentStatusCodes`: `GET /shipments/status-codes`.
   Cache the result; tracking responses carry numeric status codes, not labels.

3. **Search** — `shipmentsGetShipmentsByReferenceNumbers`: `POST /shipments/search` with the
   reference numbers to look up. ArcBest's instructions say to use this once
   `/quotes/booking-request/status` has returned the pro number.

4. **Read the payload** against `json-schema/arcbest-expedite-tracking-model.json`. Key fields:
   `Shipment.ProNumber`, `Shipment.ProductType`, `Shipment.ServiceLevel`, and the `Shipper`,
   `Consignee` and `ThirdParty` parties, each with an `Account` and a `Location` address.

5. **Know which number you are holding.** Three identifiers travel together and are easy to confuse:
   - `UnifiedQuoteNo` / `ExpediteQuoteId` — `P000…`, identifies the quote.
   - `ExpediteOrderNo` — `yyyymm12345`, the BOL number.
   - `ArcBestOrderNo` / `ProNumber` — the ArcBest pro number.

6. **Prefer the push feed for live updates.** ArcBest posts full order history to an endpoint you
   register with them on every milestone and location ping — polling this search endpoint in a loop
   is not the intended pattern. See `asyncapi/arcbest-track-and-trace-webhooks.yml`.
