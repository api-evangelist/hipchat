# HipChat (hipchat)

> **Status: SUNSET / DISCONTINUED.** HipChat Cloud, HipChat Server, HipChat Data Center, and Stride were
> all discontinued by Atlassian on **February 15, 2019**. The IP was acquired by Slack on
> **July 26, 2018** ("Slack has acquired the IP for Stride and Hipchat Cloud, both of which we will
> discontinue. We will also be discontinuing Hipchat Server and Hipchat Data Center."). No HipChat REST
> API v2 endpoints remain reachable. This profile preserves the historical API surface for archival,
> migration-pattern research, and adapter scaffolding.

API and integration profile for HipChat, Atlassian's former team chat platform.

## Lifecycle

| Field | Value |
| --- | --- |
| Score label | `SUNSET` |
| Lifecycle | `discontinued` |
| End-of-sale | 2018-07-26 (Slack acquisition announcement) |
| End-of-life | **2019-02-15** |
| Replacement | [Slack](https://slack.com) (joint migration path) |
| Migration page | https://www.atlassian.com/migration/move-from-hipchat-to-slack |
| Original API reference | `https://www.hipchat.com/docs/apiv2` (offline; use archive.org snapshots) |
| Atlassian developer docs (mirror) | https://developer.atlassian.com/server/hipchat/ |

## APIs documented

| API | Surface | Base URL (historical) | Spec |
| --- | --- | --- | --- |
| HipChat REST API v2 | REST | `https://api.hipchat.com/v2` | [`openapi/hipchat-rest-api-openapi.yml`](openapi/hipchat-rest-api-openapi.yml) |
| HipChat Webhooks API | Event delivery (JWT-signed) | `https://api.hipchat.com/v2/room/{id_or_name}/webhook` | [`asyncapi/hipchat-webhooks-asyncapi.yml`](asyncapi/hipchat-webhooks-asyncapi.yml) |

### Authentication (historical)

Four token types, passed via `Authorization: Bearer {token}` or `?auth_token={token}`:

- Add-on token (issued via `POST /oauth/token`)
- User token
- Personal access token
- Room notification token

### OAuth scopes

`admin_group`, `admin_room`, `manage_rooms`, `send_message`, `send_notification`, `view_group`,
`view_messages`, `view_room`.

### Rate limits

- **500 requests / 5 minutes** overall (`X-Ratelimit-*` headers).
- **30 messages / minute / room** flood control on notification and message-send endpoints
  (`X-FloodControl-*` headers).

## Artifacts in this repo

| Folder | Files |
| --- | --- |
| `openapi/` | `hipchat-rest-api-openapi.yml` |
| `asyncapi/` | `hipchat-webhooks-asyncapi.yml` |
| `json-schema/` | `hipchat-room-schema.json`, `hipchat-user-schema.json`, `hipchat-message-schema.json`, `hipchat-webhook-schema.json` |
| `json-structure/` | `hipchat-room-structure.json`, `hipchat-message-structure.json` |
| `json-ld/` | `hipchat-context.jsonld` |
| `examples/` | `hipchat-room-example.json`, `hipchat-user-example.json`, `hipchat-send-notification-example.json`, `hipchat-room-message-webhook-example.json` |
| `rules/` | `hipchat-rest-api-rules.yml` (Spectral) |
| `capabilities/` | `hipchat-rooms.yaml`, `hipchat-users.yaml`, `hipchat-messages.yaml`, `hipchat-webhooks.yaml`, `hipchat-emoticons.yaml` |
| `vocabulary/` | `hipchat-vocabulary.yml` |
| `plans/` | `hipchat-plans-pricing.yml` (historical pricing) |
| `rate-limits/` | `hipchat-rate-limits.yml` |
| `finops/` | `hipchat-finops.yml` |

## Historical SDK and tooling ecosystem (github.com/hipchat)

| Repo | Language | Purpose | Stars |
| --- | --- | --- | --- |
| [`hubot-hipchat`](https://github.com/hipchat/hubot-hipchat) | CoffeeScript | Hubot chat-bot adapter | 661 |
| [`hipchat-cli`](https://github.com/hipchat/hipchat-cli) | Shell | CLI scripts for the REST API | 341 |
| [`hipchat-rb`](https://github.com/hipchat/hipchat-rb) | Ruby | REST wrapper with Capistrano hooks | 334 |
| [`hipchat-php`](https://github.com/hipchat/hipchat-php) | PHP | REST wrapper | 167 |
| [`redmine_hipchat`](https://github.com/hipchat/redmine_hipchat) | Ruby | Redmine notification plugin | 64 |
| [`curler`](https://github.com/hipchat/curler) | Python | Gearman worker that cURLs | 51 |
| [`triatomic`](https://github.com/hipchat/triatomic) | CoffeeScript | Starter Hubot config for Heroku | 29 |

Plus forks/infrastructure: `strophejs`, `punjab`, `SleekXMPP`/`slixmpp`, `phpredis`, `honcho`,
`oauthd`, `linkify`, `Caja-HTML-Sanitizer`, `python-client` (LaunchDarkly), `php-client` (LaunchDarkly),
`ZipArchive`, `three20`, `InAppSettingsKit`, `asap-authentication-python`, `pusher`, `mixpanel_proxy`,
`x2js`, `alchimia`, and the `sleuthman` Pac-Man clone.

## Why this profile exists

HipChat is a worked example of a complete platform sunset: a four-product line, a healthy add-on
marketplace (HipChat Connect), and a robust XMPP/REST/webhook stack, all decommissioned together.
The artifacts here serve three purposes:

1. **Migration-pattern reference** — for teams documenting their own chat-platform sunsets.
2. **Adapter scaffolding** — Naftiko capabilities and OpenAPI specs that downstream tools can
   re-target at modern equivalents (Slack, Microsoft Teams, Mattermost).
3. **Historical record** — a single canonical map of the HipChat API surface as it existed, even
   after the developer.atlassian.com pages start to bit-rot.

## Source verification

Every claim in `apis.yml` and the artifacts here traces to one of:

- `https://www.atlassian.com/blog/announcements/new-atlassian-slack-partnership` (sunset announcement, July 26 2018)
- `https://www.atlassian.com/migration/move-from-hipchat-to-slack` (official migration page)
- `https://developer.atlassian.com/server/hipchat/about-the-hipchat-rest-api/` (auth, base URL, token types)
- `https://developer.atlassian.com/server/hipchat/hipchat-rest-api-scopes/` (8 OAuth scopes)
- `https://developer.atlassian.com/server/hipchat/hipchat-rest-api-rate-limits/` (500/5min + 30/min flood control)
- `https://developer.atlassian.com/server/hipchat/webhooks/` (signed_request JWT)
- `https://en.wikipedia.org/wiki/HipChat` (founding 2009, Atlassian acquisition 2012-03-07, sunset 2019-02-15)
- `gh api orgs/hipchat/repos` (live GitHub org enumeration as of 2026-05-23)
