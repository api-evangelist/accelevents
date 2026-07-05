# Accelevents (accelevents)

Accelevents is an all-in-one event management and ticketing platform for in-person, virtual, and hybrid events - covering registration, ticketing, agenda and sessions, speakers, exhibitors, networking, and engagement. The **Accelevents Open API** is a REST API (base `https://api.accelevents.com/rest`) authenticated with an organization API key generated from the account Integrations tab (Edit Enterprise → Integrations → API Key) and passed in a request header. It exposes event details, attendees, ticketing orders and sales, ticket holders, sessions, speakers, and attendee networking.

**Access model (honest note):** the Open API is documented publicly at [developer.accelevents.com](https://developer.accelevents.com/docs/accelevents-api-documentation), but exercising it requires an API key that only an owner-level user on a qualifying paid plan can generate. Per the pricing page, **API & Webhooks are bundled from the Business tier and above** (Professional does not list API access; Enterprise and White Label are custom-quoted). Three endpoints below are **confirmed** directly against the public API reference (event details, all attendees, ticketing orders); the remaining operations are **named in the public reference object catalog** (Session, Speaker, Ticket Holder, Portal People) but their exact request paths are **modeled** here and flagged with `x-endpoint-modeled: true` in the OpenAPI and as `MODELED` in the collections. The authentication header name (`AUTHENTICATION`) is likewise modeled from the getting-started guide - confirm it on the reference before use.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/accelevents/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/accelevents/refs/heads/main/apis.yml)

## Tags

- Event Management
- Ticketing
- Events
- Registration
- Virtual Events
- Sessions

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Accelevents Events API

Retrieve event and design details for an event by its unique event URL, and check recurring-event status. The event URL is the unique identifier used across the rest of the API. *Event details retrieval is confirmed; recurring-event paths are modeled.*

- **Human URL:** [https://developer.accelevents.com/reference/event-and-design-details](https://developer.accelevents.com/reference/event-and-design-details)
- **Base URL:** `https://api.accelevents.com/rest`

### Accelevents Attendees API

List and search event attendees with pagination, filter people by company, job title, and interests, and add attendees to an event. *The all-attendees listing endpoint is confirmed; people-filter and add-attendee paths are modeled.*

- **Human URL:** [https://developer.accelevents.com/reference/get-all-attendees](https://developer.accelevents.com/reference/get-all-attendees)
- **Base URL:** `https://api.accelevents.com/rest`

### Accelevents Ticketing Orders API

Retrieve ticketing and add-on orders for an event with search, date, and pagination filters, pull dashboard sales data, and export ticket buyer data. *The ticketing-orders endpoint is confirmed; sales-data and CSV-export paths are modeled.*

- **Human URL:** [https://developer.accelevents.com/reference/get-ticketing-orders](https://developer.accelevents.com/reference/get-ticketing-orders)
- **Base URL:** `https://api.accelevents.com/rest`

### Accelevents Tickets API

Manage individual ticket holders - update ticket-holder attributes by barcode ID, exchange a ticket type for an attendee, and export ticket-holder data. *Named in the public reference object catalog; exact request paths are modeled.*

- **Base URL:** `https://api.accelevents.com/rest`

### Accelevents Sessions API

List and update event sessions, manage an attendee's registered/bookmarked sessions, create session tags and tracks, and create and list speakers. *Named in the public reference object catalog (Session, Speaker); exact request paths are modeled.*

- **Base URL:** `https://api.accelevents.com/rest`

## Artifacts

- [OpenAPI](openapi/accelevents-openapi.yml)
- [Postman Collection](collections/accelevents.postman_collection.json)
- [Open Collection](collections/accelevents.opencollection.json)
- [Plans](plans/accelevents-plans-pricing.yml)
- [Rate Limits](rate-limits/accelevents-rate-limits.yml)
- [FinOps](finops/accelevents-finops.yml)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/accelevents)
- [Website](https://www.accelevents.com)
- [Documentation](https://developer.accelevents.com/docs/accelevents-api-documentation)
- [API Reference](https://developer.accelevents.com/reference)

## WebSocket Review

Accelevents does **not** expose a documented public WebSocket API. The documented developer surface is request/response REST (the Open API) plus outbound webhooks (a bundled paid-plan feature). In-event real-time features (live streams, chat, networking) are delivered through the hosted application, not a public streaming API. See [review.yml](review.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
