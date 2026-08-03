# ArcBest (arcbest)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ArcBest is a logistics company offering less-than-truckload (LTL) freight, truckload, moving, and supply chain management services. The ArcBest API platform provides integration capabilities for freight rating, booking, tracking, and supply chain visibility.

**URL:** [https://www.arcbest.com/](https://www.arcbest.com/)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Logistics, Freight, LTL, Supply Chain, Shipping, Transportation

## Timestamps

- **Created:** 2026-03-23
- **Modified:** 2026-04-19

## APIs

### ArcBest API
The ArcBest API provides programmatic access to freight services including LTL rate quotes, shipment booking, tracking, BOL generation, and supply chain visibility. Access is by invitation only.

**Human URL:** [https://www.arcbest.com/](https://www.arcbest.com/)

#### Tags:

 - LTL Freight, Rate Quote, Shipment Tracking, BOL, Supply Chain

#### Properties

- [Documentation](https://www.arcbest.com/)
- [OpenAPI](openapi/arcbest-api.yaml)

## Common Properties

- [Portal](https://www.arcbest.com/)
- [SignUp](https://www.arcbest.com/)

## Features

| Name | Description |
|------|-------------|
| LTL Rate Quotes | Real-time less-than-truckload freight rate quotes with transit time estimates. |
| Shipment Booking | API-based shipment booking and scheduling for LTL and truckload freight. |
| Shipment Tracking | Real-time tracking of freight shipments with status updates and delivery notifications. |
| BOL Generation | Electronic Bill of Lading generation and management through API integration. |
| Pickup Scheduling | Automated pickup scheduling and confirmation for outbound freight. |
| Supply Chain Visibility | End-to-end supply chain visibility across ArcBest freight and logistics services. |

## Use Cases

| Name | Description |
|------|-------------|
| E-Commerce Shipping | Integrate ArcBest freight rates and booking into e-commerce platforms for automated shipping. |
| ERP Integration | Connect ArcBest freight services to ERP systems for automated freight procurement and accounting. |
| TMS Integration | Integrate with Transportation Management Systems for multi-carrier freight optimization. |
| Warehouse Management | Connect ArcBest pickup scheduling with warehouse management systems for outbound logistics automation. |

## Integrations

| Name | Description |
|------|-------------|
| SAP | Integration with SAP ERP for freight cost allocation and logistics management. |
| Oracle | Connect to Oracle ERP and WMS systems for automated freight operations. |
| Salesforce | Integrate shipment tracking and freight data with Salesforce CRM. |
| ShipStation | Multi-carrier shipping management platform integration. |
| Shopify | E-commerce platform integration for LTL freight rate display and booking. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [ArcBest API](openapi/arcbest-api.yaml)

### JSON Schema

- [Shipment](json-schema/arcbest-api-shipment-schema.json)
- [Tracking Status](json-schema/arcbest-api-tracking-status-schema.json)
- [Rate Request](json-schema/arcbest-api-rate-request-schema.json)
- [Rate Response](json-schema/arcbest-api-rate-response-schema.json)
- [Address](json-schema/arcbest-api-address-schema.json)
- [Freight Item](json-schema/arcbest-api-freight-item-schema.json)

### JSON-LD

- [ArcBest API Context](json-ld/arcbest-api-context.jsonld)

## Vocabulary

- [ArcBest Vocabulary](vocabulary/arcbest-vocabulary.yaml) — Unified taxonomy mapping 4 resources, 5 actions, 0 workflows, and 3 personas

## Rules

- [ArcBest Spectral Rules](rules/arcbest-spectral-rules.yml) — 18 rules across 8 categories enforcing ArcBest API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
