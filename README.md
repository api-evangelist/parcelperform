# Parcel Perform (parcelperform)

Parcel Perform is a Singapore-headquartered Data & Delivery Experience Platform that aggregates real-time tracking data across hundreds of carriers worldwide into one standardized event model, then layers post-purchase tracking pages, proactive notifications, logistics performance analytics, and returns management on top. The Parcel Perform API (developer portal at developer.parcelperform.com) lets merchants and platforms create and retrieve shipments and their tracking events, manage returns, and receive outgoing webhooks for tracking-status changes, authenticated with OAuth2 client-credentials bearer tokens.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/parcelperform/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/parcelperform/refs/heads/main/apis.yml)

## Tags

- Logistics
- Shipment Tracking
- Post-Purchase
- Delivery Experience
- Returns
- E-Commerce

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Parcel Perform Shipments API

Create, retrieve, list, and update shipments in a Parcel Perform account. A shipment carries the carrier/courier code, tracking number, sender and recipient details, and (in the v5.2.0 response) related returns, rating, line item, and collection point objects. This is the system of record that ties a merchant order to a trackable parcel across Parcel Perform's carrier network.

- **Human URL:** [https://developers.parcelperform.com/docs/api-guides-reference/5unzr17vbxlxd-list-shipments](https://developers.parcelperform.com/docs/api-guides-reference/5unzr17vbxlxd-list-shipments)
- **Base URL:** `https://api.parcelperform.com/v5`

#### Tags

- Shipments
- Tracking
- Carriers

#### Properties

- [Documentation](https://developers.parcelperform.com/docs/api-guides-reference/8e768e6831f6c-overview)
- [API Reference](https://developers.parcelperform.com/docs/api-guides-reference/6f5f7fedef593-create-a-shipment)
- [OpenAPI](openapi/parcelperform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelperform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelperform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Parcel Perform Tracking Events API

Retrieve the normalized tracking event timeline captured for a shipment, or manually create events on an existing outbound or return shipment. Parcel Perform standardizes carrier-specific status codes from its carrier network into a single event and milestone model (with location and timestamp) so consuming applications don't have to parse each carrier's raw tracking feed themselves.

- **Human URL:** [https://developers.parcelperform.com/docs/api-guides-reference/ee4c914fc83bf-create-events-for-an-existing-shipment](https://developers.parcelperform.com/docs/api-guides-reference/ee4c914fc83bf-create-events-for-an-existing-shipment)
- **Base URL:** `https://api.parcelperform.com/v5`

#### Tags

- Tracking
- Events
- Milestones

#### Properties

- [Documentation](https://www.parcelperform.com/insights/tracking-api)
- [API Reference](https://developers.parcelperform.com/docs/api-guides-reference/blfc895yi4bx3-create-events)
- [OpenAPI](openapi/parcelperform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelperform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelperform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Parcel Perform Returns API

Create a return, or create a return together with its associated return shipment, in a Parcel Perform account (one return per request). Return shipments flow through the same shipment and tracking-event model as outbound parcels, giving merchants a single system for forward and reverse logistics visibility.

- **Human URL:** [https://developers.parcelperform.com/docs/api-guides-reference/3d66ap56pfly7-create-return](https://developers.parcelperform.com/docs/api-guides-reference/3d66ap56pfly7-create-return)
- **Base URL:** `https://api.parcelperform.com/v5`

#### Tags

- Returns
- Reverse Logistics
- RMA

#### Properties

- [API Reference](https://developers.parcelperform.com/docs/api-guides-reference/1bd1a948e1eb3-create-a-return)
- [OpenAPI](openapi/parcelperform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelperform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelperform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Parcel Perform Webhooks API

Register a callback URL to automatically receive Shipment Tracking Update events as outgoing webhooks whenever Parcel Perform ingests a new carrier tracking event, in either the v5.0.0 or v5.2.0 payload format. This is Parcel Perform's push notification surface - there is no public WebSocket or streaming endpoint.

- **Human URL:** [https://developers.parcelperform.com/docs/api-guides-reference/e8adbc8a2da19-outgoing-webhooks-version-5-format](https://developers.parcelperform.com/docs/api-guides-reference/e8adbc8a2da19-outgoing-webhooks-version-5-format)
- **Base URL:** `https://api.parcelperform.com/v5`

#### Tags

- Webhooks
- Notifications
- Outgoing Webhooks

#### Properties

- [Documentation](https://developers.parcelperform.com/docs/api-guides-reference/ba66787fe87e7-outgoing-webhooks-version-5-2-0-format)
- [API Reference](https://developers.parcelperform.com/docs/api-guides-reference/e8adbc8a2da19-outgoing-webhooks-version-5-format)
- [OpenAPI](openapi/parcelperform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelperform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelperform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Parcel Perform Couriers API

Modeled reference-data surface for the carrier/courier network Parcel Perform aggregates - reported between roughly 900 and 1,000+ carriers worldwide, added weekly, each identified by a courier code used on shipment creation. Parcel Perform publishes a marketing directory of supported carriers, but the public API Guides & Reference does not document a standalone GET /couriers list endpoint as of this review; carrier codes are otherwise surfaced only as a field on Shipment resources, so the endpoints below are modeled rather than confirmed.

- **Human URL:** [https://www.parcelperform.com/integrations/carriers](https://www.parcelperform.com/integrations/carriers)
- **Base URL:** `https://api.parcelperform.com/v5`

#### Tags

- Couriers
- Carriers
- Reference Data

#### Properties

- [Documentation](https://www.parcelperform.com/integrations/carriers)
- [OpenAPI](openapi/parcelperform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelperform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelperform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Parcel Perform Analytics API

Modeled reporting surface behind Parcel Perform's Analyze product, which turns aggregated delivery-experience data (carrier SLA/on-time performance, exception rates, estimated-delivery-date accuracy) into dashboards and AI-generated insights. Analyze is documented as a product within the Parcel Perform app, not as a standalone endpoint set in the public API Guides & Reference, so the endpoints below are modeled on the metrics the product describes rather than confirmed against a published reference.

- **Human URL:** [https://www.parcelperform.com/products/analyze](https://www.parcelperform.com/products/analyze)
- **Base URL:** `https://api.parcelperform.com/v5`

#### Tags

- Analytics
- Insights
- Performance

#### Properties

- [Documentation](https://www.parcelperform.com/products/analyze)
- [OpenAPI](openapi/parcelperform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelperform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelperform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/ParcelPerform)
- [LinkedIn](https://www.linkedin.com/company/parcel-perform)
- [Website](https://www.parcelperform.com/)
- [Documentation](https://developers.parcelperform.com/)
- [Plans](plans/parcelperform-plans-pricing.yml)
- [Rate Limits](rate-limits/parcelperform-rate-limits.yml)
- [Fin Ops](finops/parcelperform-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
