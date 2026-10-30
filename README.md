# HipChat

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

> **No longer operating.** This company or product has shut down, been discontinued, or been deprecated. This profile is kept as a historical record and is not maintained or rated.

**Status:** HipChat has been discontinued. Retained for historical reference.

HipChat was Atlassian's team chat platform, providing persistent group chat, video, file sharing, and an extensive integration ecosystem. Atlassian discontinued HipChat Cloud, Stride, HipChat Server, and HipChat Data Center on February 15, 2019 after selling the IP to Slack in July 2018 and committing to a joint migration path for customers. This profile preserves the historical API surface (REST API v2, Webhooks, Connect add-on framework) for archival and migration-pattern research; no live endpoints remain.

**Areas:** Chat · Messaging · Collaboration · Team Communication · Sunset · Historical · Atlassian · Webhook · Defunct

## HipChat on APIs.io (historical record)

Everything profiled for HipChat is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/hipchat/](https://apis.io/providers/hipchat/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [HipChat REST API v2](https://apis.io/apis/hipchat/hipchat-rest-api-v2/) — The HipChat REST API v2 was the primary developer surface for the team chat platform, exposing rooms, users, messages, notifications, emoticons, OAuth…
- [HipChat Webhooks API](https://apis.io/apis/hipchat/hipchat-webhooks-api/) — Event-driven webhook delivery from HipChat rooms. Webhooks could be registered via the REST API or declared in an add-on descriptor. Each delivery included…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [HipChat Webhooks API](https://apis.io/asyncapis/hipchat/hipchat-webhooks-asyncapi/)

#### Event channels (10)

Individual events and webhooks the provider emits.

- [/webhook/room_archived](https://apis.io/channels/hipchat/webhook-room-archived/)
- [/webhook/room_created](https://apis.io/channels/hipchat/webhook-room-created/)
- [/webhook/room_deleted](https://apis.io/channels/hipchat/webhook-room-deleted/)
- [/webhook/room_enter](https://apis.io/channels/hipchat/webhook-room-enter/)
- [/webhook/room_exit](https://apis.io/channels/hipchat/webhook-room-exit/)
- [/webhook/room_file_upload](https://apis.io/channels/hipchat/webhook-room-file-upload/)
- [/webhook/room_message](https://apis.io/channels/hipchat/webhook-room-message/)
- [/webhook/room_notification](https://apis.io/channels/hipchat/webhook-room-notification/)
- [/webhook/room_topic_change](https://apis.io/channels/hipchat/webhook-room-topic-change/)
- [/webhook/room_unarchived](https://apis.io/channels/hipchat/webhook-room-unarchived/)

#### JSON Schema (4)

The data models the API reads and writes.

- [HipChat Message](https://apis.io/schemas/hipchat/hipchat-message/)
- [HipChat Room](https://apis.io/schemas/hipchat/hipchat-room/)
- [HipChat User](https://apis.io/schemas/hipchat/hipchat-user/)
- [HipChat Webhook](https://apis.io/schemas/hipchat/hipchat-webhook/)

#### JSON Structure (2)

Data models expressed in JSON Structure.

- [Hipchat Message Structure](https://apis.io/json-structure/hipchat/hipchat-message-structure/)
- [Hipchat Room Structure](https://apis.io/json-structure/hipchat/hipchat-room-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Hipchat Context](https://apis.io/jsonld/hipchat/hipchat-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [HipChat Vocabulary](https://apis.io/vocabularies/hipchat/hipchat-vocabulary/)

#### Examples (4)

Example requests and responses.

- [Hipchat Room Example](https://apis.io/examples/hipchat/hipchat-room-example/)
- [Hipchat Room Message Webhook Example](https://apis.io/examples/hipchat/hipchat-room-message-webhook-example/)
- [Hipchat Send Notification Example](https://apis.io/examples/hipchat/hipchat-send-notification-example/)
- [Hipchat User Example](https://apis.io/examples/hipchat/hipchat-user-example/)

#### Governance rules (3)

Spectral rulesets for the provider's contracts.

- [HipChat — asyncapi rules](https://apis.io/rules/hipchat/hipchat-asyncapi-spectral-rules/)
- [HipChat — jsonschema rules](https://apis.io/rules/hipchat/hipchat-jsonschema-spectral-rules/)
- [HipChat — rest api rules](https://apis.io/rules/hipchat/hipchat-rest-api-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Hipchat Domain Security](https://apis.io/security/hipchat/hipchat-domain-security/)
- [Hipchat Trust Center](https://apis.io/security/hipchat/hipchat-trust-center/)
- [Hipchat Vulnerability Disclosure](https://apis.io/security/hipchat/hipchat-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Hipchat Plans Pricing](https://apis.io/plans/hipchat/hipchat-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Hipchat Rate Limits](https://apis.io/rate-limits/hipchat/hipchat-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Hipchat Finops](https://apis.io/finops/hipchat/hipchat-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.atlassian.com/)
- [Documentation](https://developer.atlassian.com/server/hipchat/)
- [Blog](https://www.atlassian.com/blog/announcements/new-atlassian-slack-partnership)
- [GitHub](https://github.com/hipchat)

## API Evangelist rating

**Not rated** — this company is recorded as no longer operating, so no score is published. If it is in fact operating, say so on this repository and it will be re-profiled.

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for HipChat: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/hipchat/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
