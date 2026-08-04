# HipChat (hipchat)

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

HipChat was Atlassian's team chat platform, providing persistent group chat, video, file sharing, and an extensive integration ecosystem. Atlassian discontinued HipChat Cloud, Stride, HipChat Server, and HipChat Data Center on February 15, 2019 after selling the IP to Slack in July 2018 and committing to a joint migration path for customers. This profile preserves the historical API surface (REST API v2, Webhooks, Connect add-on framework) for archival and migration-pattern research; no live endpoints remain.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hipchat/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hipchat/refs/heads/main/apis.yml)

## Tags

- Chat
- Messaging
- Collaboration
- Team Communication
- Sunset
- Historical
- Atlassian
- Webhooks

## Timestamps

- **Created:** Sun Dec 31 2023 19:00:00 GMT-0500 (Eastern Standard Time)
- **Modified:** 2026-05-23

## APIs

### HipChat REST API v2

The HipChat REST API v2 was the primary developer surface for the team chat platform, exposing rooms, users, messages, notifications, emoticons, OAuth sessions, add-on capabilities, and webhook management. Authentication supported four token types (add-on tokens, user tokens, personal access tokens, and room notification tokens) passed as either an auth_token query parameter or an Authorization Bearer header. The API was retired on February 15, 2019 alongside the rest of the HipChat product line.

- **Human URL:** [https://developer.atlassian.com/server/hipchat/about-the-hipchat-rest-api/](https://developer.atlassian.com/server/hipchat/about-the-hipchat-rest-api/)

#### Tags

- Chat
- Rooms
- Messages
- Users
- Notifications
- Webhooks
- OAuth
- Sunset

#### Properties

- [Documentation](https://developer.atlassian.com/server/hipchat/about-the-hipchat-rest-api/)
- [API Reference](https://www.hipchat.com/docs/apiv2)
- [OpenAPI](openapi/hipchat-rest-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Authentication](https://developer.atlassian.com/server/hipchat/auth/)
- [Rate Limits](https://developer.atlassian.com/server/hipchat/hipchat-rest-api-rate-limits/)
- [Rate Limits](rate-limits/hipchat-rate-limits.yml)
- [Security](https://developer.atlassian.com/server/hipchat/hipchat-rest-api-scopes/)
- [Getting Started](https://developer.atlassian.com/server/hipchat/getting-started-with-atlassian-connect-for-hipchat/)
- [SDK](https://github.com/hipchat/hipchat-php)
- [SDK](https://github.com/hipchat/hipchat-rb)
- [SDK](https://github.com/hipchat/hubot-hipchat)
- [C L I](https://github.com/hipchat/hipchat-cli)
- [Integrations](https://github.com/hipchat/redmine_hipchat)
- [Integrations](https://github.com/hipchat/triatomic)
- [GitHub Organization](https://github.com/hipchat)
- [JSON Schema](json-schema/hipchat-room-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hipchat-user-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hipchat-message-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hipchat-webhook-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/hipchat-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Versioning](https://developer.atlassian.com/server/hipchat/hipchat-connect-versioning/)
- [Sunset](https://www.atlassian.com/blog/announcements/new-atlassian-slack-partnership)
- [Sunset](https://www.atlassian.com/migration/move-from-hipchat-to-slack)

### HipChat Webhooks API

Event-driven webhook delivery from HipChat rooms. Webhooks could be registered via the REST API or declared in an add-on descriptor. Each delivery included a JWT-signed signed_request query parameter that the receiving service was expected to verify. The room_message event was the primary integration pattern, with additional events covering room enter, exit, topic change, archive, notification, and file upload. The webhook surface was retired with the rest of HipChat on February 15, 2019.

- **Human URL:** [https://developer.atlassian.com/server/hipchat/webhooks/](https://developer.atlassian.com/server/hipchat/webhooks/)

#### Tags

- Webhooks
- Events
- Chat
- Sunset

#### Properties

- [Documentation](https://developer.atlassian.com/server/hipchat/webhooks/)
- [AsyncAPI](asyncapi/hipchat-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Authentication](https://developer.atlassian.com/server/hipchat/understanding-jwt-for-apps/)
- [JSON Schema](json-schema/hipchat-webhook-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Sunset](https://www.atlassian.com/migration/move-from-hipchat-to-slack)

## Common Properties

- [Documentation](https://developer.atlassian.com/server/hipchat/)
- [Developer Portal](https://developer.atlassian.com/server/hipchat/)
- [GitHub Organization](https://github.com/hipchat)
- [Blog](https://www.atlassian.com/blog/announcements/new-atlassian-slack-partnership)
- [Sunset](https://www.atlassian.com/migration/move-from-hipchat-to-slack)
- [Integrations](https://www.atlassian.com/partnerships/slack)
- [Pricing](plans/hipchat-plans-pricing.yml)
- [Rate Limits](rate-limits/hipchat-rate-limits.yml)
- [Fin Ops](finops/hipchat-finops.yml)

## Maintainers

**FN:** API Evangelist
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
