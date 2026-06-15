# HipChat (hipchat)

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
