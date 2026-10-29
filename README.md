# ArcBest

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ArcBest is a multibillion-dollar freight and logistics provider operating ABF Freight (LTL), Panther Premium Logistics (expedite), MoLo (truckload brokerage) and U-Pack (moving), with managed transportation, warehousing and international forwarding alongside. Its integration surface is published on arcb.com in two forms: REST APIs covering rate quote, volume quote, tracking, document retrieval, transit times, pickup request and Bill of Lading, whose documentation sits behind a customer login; and ANSI X12 EDI, where ArcBest publishes downloadable 204, 210 and 214 mapping specifications openly. The one API surface documented publicly is ArcBest Expedite - a Customer API and a third-party TMS API, each shipped as a downloadable Swagger-Codegen reference with worked JSON examples, live at api.arcb.com with a test environment at test.api.arcb.com.

**Areas:** Logistics · Freight · LTL · Supply Chain · Shipping · Transportation · Expedite · Truckload · EDI · Bill of Lading · Rate Quote · Shipment Tracking

## ArcBest on APIs.io

Everything profiled for ArcBest is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/arcbest/](https://apis.io/providers/arcbest/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [ArcBest Pickups API](https://apis.io/apis/arcbest/arcbest-pickups-api/) — Pickup scheduling and management
- [ArcBest Rates API](https://apis.io/apis/arcbest/arcbest-rates-api/) — Freight rate quote services
- [ArcBest Shipments API](https://apis.io/apis/arcbest/arcbest-shipments-api/) — Shipment booking and management
- [ArcBest Tracking API](https://apis.io/apis/arcbest/arcbest-tracking-api/) — Shipment tracking and visibility
- [ArcBest Authorize API](https://apis.io/apis/arcbest/arcbest-authorize-api/) — Exchange a ClientId and ClientSecret for a bearer access token.
- [ArcBest Booking API](https://apis.io/apis/arcbest/arcbest-booking-api/) — Booking requests placed against a quote, and their asynchronous status.
- [ArcBest Order API](https://apis.io/apis/arcbest/arcbest-order-api/) — Bill of Lading retrieval and reference-number updates on a booked order.
- [ArcBest Quote API](https://apis.io/apis/arcbest/arcbest-quote-api/) — Rate quote requests for expedite loads.
- [ArcBest Quotes API](https://apis.io/apis/arcbest/arcbest-quotes-api/) — Submit expedite rate quotes, request bookings against them, and poll booking status.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Arcbest Track And Trace Webhooks](https://apis.io/asyncapis/arcbest/arcbest-track-and-trace-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [arcbest-mcp.yml](https://apis.io/servers/arcbest/arcbest-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Arcbest Agentic Access](https://apis.io/agentic-access/arcbest/arcbest-agentic-access/)

#### JSON Schema (14)

The data models the API reads and writes.

- [Address](https://apis.io/schemas/arcbest/arcbest-api-address/)
- [ErrorResponse](https://apis.io/schemas/arcbest/arcbest-api-error-response/)
- [FreightItem](https://apis.io/schemas/arcbest/arcbest-api-freight-item/)
- [PickupConfirmation](https://apis.io/schemas/arcbest/arcbest-api-pickup-confirmation/)
- [PickupRequest](https://apis.io/schemas/arcbest/arcbest-api-pickup-request/)
- [RateRequest](https://apis.io/schemas/arcbest/arcbest-api-rate-request/)
- [RateResponse](https://apis.io/schemas/arcbest/arcbest-api-rate-response/)
- [Shipment](https://apis.io/schemas/arcbest/arcbest-api-shipment/)
- [ShipmentList](https://apis.io/schemas/arcbest/arcbest-api-shipment-list/)
- [ShipmentRequest](https://apis.io/schemas/arcbest/arcbest-api-shipment-request/)
- [TrackingEvent](https://apis.io/schemas/arcbest/arcbest-api-tracking-event/)
- [TrackingStatus](https://apis.io/schemas/arcbest/arcbest-api-tracking-status/)
- [Arcbest Expedite Quote Request Model](https://apis.io/schemas/arcbest/arcbest-expedite-quote-request-model/)
- [Arcbest Expedite Quote Response Model](https://apis.io/schemas/arcbest/arcbest-expedite-quote-response-model/)

#### JSON Structure (12)

Data models expressed in JSON Structure.

- [Arcbest Api Address Structure](https://apis.io/json-structure/arcbest/arcbest-api-address-structure/)
- [Arcbest Api Error Response Structure](https://apis.io/json-structure/arcbest/arcbest-api-error-response-structure/)
- [Arcbest Api Freight Item Structure](https://apis.io/json-structure/arcbest/arcbest-api-freight-item-structure/)
- [Arcbest Api Pickup Confirmation Structure](https://apis.io/json-structure/arcbest/arcbest-api-pickup-confirmation-structure/)
- [Arcbest Api Pickup Request Structure](https://apis.io/json-structure/arcbest/arcbest-api-pickup-request-structure/)
- [Arcbest Api Rate Request Structure](https://apis.io/json-structure/arcbest/arcbest-api-rate-request-structure/)
- [Arcbest Api Rate Response Structure](https://apis.io/json-structure/arcbest/arcbest-api-rate-response-structure/)
- [Arcbest Api Shipment List Structure](https://apis.io/json-structure/arcbest/arcbest-api-shipment-list-structure/)
- [Arcbest Api Shipment Request Structure](https://apis.io/json-structure/arcbest/arcbest-api-shipment-request-structure/)
- [Arcbest Api Shipment Structure](https://apis.io/json-structure/arcbest/arcbest-api-shipment-structure/)
- [Arcbest Api Tracking Event Structure](https://apis.io/json-structure/arcbest/arcbest-api-tracking-event-structure/)
- [Arcbest Api Tracking Status Structure](https://apis.io/json-structure/arcbest/arcbest-api-tracking-status-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Arcbest Api Context](https://apis.io/jsonld/arcbest/arcbest-api-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Arcbest Vocabulary](https://apis.io/vocabularies/arcbest/arcbest-vocabulary/)

#### Examples (12)

Example requests and responses.

- [Arcbest Api Address Example](https://apis.io/examples/arcbest/arcbest-api-address-example/)
- [Arcbest Api Error Response Example](https://apis.io/examples/arcbest/arcbest-api-error-response-example/)
- [Arcbest Api Freight Item Example](https://apis.io/examples/arcbest/arcbest-api-freight-item-example/)
- [Arcbest Api Pickup Confirmation Example](https://apis.io/examples/arcbest/arcbest-api-pickup-confirmation-example/)
- [Arcbest Api Pickup Request Example](https://apis.io/examples/arcbest/arcbest-api-pickup-request-example/)
- [Arcbest Api Rate Request Example](https://apis.io/examples/arcbest/arcbest-api-rate-request-example/)
- [Arcbest Api Rate Response Example](https://apis.io/examples/arcbest/arcbest-api-rate-response-example/)
- [Arcbest Api Shipment Example](https://apis.io/examples/arcbest/arcbest-api-shipment-example/)
- [Arcbest Api Shipment List Example](https://apis.io/examples/arcbest/arcbest-api-shipment-list-example/)
- [Arcbest Api Shipment Request Example](https://apis.io/examples/arcbest/arcbest-api-shipment-request-example/)
- [Arcbest Api Tracking Event Example](https://apis.io/examples/arcbest/arcbest-api-tracking-event-example/)
- [Arcbest Api Tracking Status Example](https://apis.io/examples/arcbest/arcbest-api-tracking-status-example/)

#### Collections (4)

Postman and Open Collection request collections.

- [ArcBest Pickups API](https://apis.io/collections/arcbest/open-arcbest-pickups-api/)
- [ArcBest Pickups Rates API](https://apis.io/collections/arcbest/open-arcbest-rates-api/)
- [ArcBest Pickups Shipments API](https://apis.io/collections/arcbest/open-arcbest-shipments-api/)
- [ArcBest Pickups Tracking API](https://apis.io/collections/arcbest/open-arcbest-tracking-api/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Arcbest Expedite Customer Api Overlay](https://apis.io/overlays/arcbest/arcbest-expedite-customer-api-overlay/)
- [Arcbest Expedite Tms Api Overlay](https://apis.io/overlays/arcbest/arcbest-expedite-tms-api-overlay/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [ArcBest — jsonschema rules](https://apis.io/rules/arcbest/arcbest-jsonschema-spectral-rules/)
- [ArcBest API Rules](https://apis.io/rules/arcbest/arcbest-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Arcbest Authentication](https://apis.io/security/arcbest/arcbest-authentication/)
- [Arcbest Domain Security](https://apis.io/security/arcbest/arcbest-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Arcbest Plans Pricing](https://apis.io/plans/arcbest/arcbest-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Arcbest Rate Limits](https://apis.io/rate-limits/arcbest/arcbest-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Arcbest Finops](https://apis.io/finops/arcbest/arcbest-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://arcb.com/)
- [Documentation](https://arcb.com/technology/shippers/API)
- [Getting started](https://arcb.com/technology/shippers/API/expedite-setup-documentation-download)
- [API reference](https://arcb.com/technology/shippers/API/expedite-setup-documentation-download)
- [Sign up](https://arcb.com/registration/customer)
- [Support](https://support.arcb.com/en)
- [Blog](https://arcb.com/blog)
- [Terms of service](https://arcb.com/terms-of-use)
- [Privacy policy](https://arcb.com/privacy-policy)
- [GitHub](https://github.com/ArcBest-Technologies)

## API Evangelist rating

**Kin Score 42.4** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 29.1 |
| Contract governance | 45.5 |
| Operational transparency | 10.5 |
| Developer ergonomics | 66.1 |
| Access clarity | 34.2 |

**Agent readiness 34.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 22.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/arcbest/](https://apis.io/providers/arcbest/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ArcBest: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/arcbest/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
