# Accelevents (accelevents)

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
