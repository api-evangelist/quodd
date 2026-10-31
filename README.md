# QUODD

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

QUODD is a cloud-native market data provider delivering real-time, delayed, historical, end-of-day, and point-in-time pricing, plus reference data, a security master, fundamentals, estimates, corporate actions, ESG, and news across global equities, ETFs, options, fixed income, FX, funds, and indices. The QUODD Developer Platform (developer.quodd.com) exposes market data through REST and gRPC snapshot APIs, token-based authentication, and cloud delivery options - Cloud APIs, Cloud Streaming, Cloud Alerts, Cloud Search, and Cloud Files. QUODD advertises more than 250 billion data points across 150-plus global exchanges. Developer documentation is public, but production access is gated behind trial or firm credentials and enterprise contact-sales agreements; exact REST base URLs and full endpoint paths are not published openly.

**Areas:** Market Data · Real-Time Data · Financial Data · Streaming · Historical Data · Reference Data · Quotes · Fintech

## QUODD on APIs.io

Everything profiled for QUODD is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/quodd/](https://apis.io/providers/quodd/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [QUODD Snap API](https://apis.io/apis/quodd/quodd-snap-api/) — Single-ticker real-time or delayed pricing snapshot (Snap). Returns the current quote and trade fields - last price, bid/ask, volume, and related market…
- [QUODD Batch Snaps API](https://apis.io/apis/quodd/quodd-batch-snaps-api/) — Batch snapshot retrieval for many tickers in a single request, via GET (query list) or POST (ticker array). Returns real-time or delayed pricing for each…
- [QUODD Options Snaps API](https://apis.io/apis/quodd/quodd-options-snaps-api/) — Real-time or delayed options pricing snapshots for single contracts (Options Snap) and for many contracts at once (Batch Options Snaps, GET and POST).…
- [QUODD Authentication Token API](https://apis.io/apis/quodd/quodd-authentication-token-api/) — Token generation for trial and firm users. Exchanges username and password credentials for an access token that is appended to REST requests as the _token…
- [QUODD Ticker Search API](https://apis.io/apis/quodd/quodd-ticker-search-api/) — Ticker and symbol lookup for discovering securities across asset classes and identifiers (Cloud Search). Listed as Beta Access on the QUODD Developer…
- [QUODD Historical Prices API](https://apis.io/apis/quodd/quodd-historical-prices-api/) — End-of-day and historical market data across 80-plus global exchanges - US equities and ETFs from 1994, global markets from 2000 - as OHLCV time series or…
- [QUODD Reference Data & Security Master API](https://apis.io/apis/quodd/quodd-reference-data-security-master-api/) — Global reference data and security master (Global Master) - intra-day global equity descriptive data, funds, corporate actions, dividends, and fixed income…
- [QUODD Fundamentals & Estimates API](https://apis.io/apis/quodd/quodd-fundamentals-estimates-api/) — Company fundamentals, metrics, ratios, and analyst estimates on global securities for fundamental analysis. Described in QUODD product documentation;…
- [QUODD Snap gRPC API](https://apis.io/apis/quodd/quodd-snap-grpc-api/) — gRPC delivery of pricing snapshots (Snap) and ticker information (Ticker Info) for high-performance, low-overhead integrations. Documented on the QUODD…
- [QUODD Cloud Streaming API](https://apis.io/apis/quodd/quodd-cloud-streaming-api/) — Cloud Streaming pushes changing quote and trade fields continuously rather than requiring repeated REST polling, for live market data in servers, web, and…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [quodd](https://apis.io/servers/quodd/quodd/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Quodd Agentic Access](https://apis.io/agentic-access/quodd/quodd-agentic-access/)

#### Collections (3)

Postman and Open Collection request collections.

- [QUODD Market Data API (Modeled) Authentication API](https://apis.io/collections/quodd/open-quodd-authentication-api/)
- [QUODD Market Data API (Modeled) Authentication Options API](https://apis.io/collections/quodd/open-quodd-options-api/)
- [QUODD Market Data API (Modeled) Authentication Snapshots API](https://apis.io/collections/quodd/open-quodd-snapshots-api/)

#### Overlays (3)

OpenAPI overlays, including conversational phrasing for each operation.

- [Quodd Authentication Api Overlay](https://apis.io/overlays/quodd/quodd-authentication-api-overlay/)
- [Quodd Options Api Overlay](https://apis.io/overlays/quodd/quodd-options-api-overlay/)
- [Quodd Snapshots Api Overlay](https://apis.io/overlays/quodd/quodd-snapshots-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Quodd Authentication](https://apis.io/security/quodd/quodd-authentication/)
- [Quodd Domain Security](https://apis.io/security/quodd/quodd-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Quodd Plans Pricing](https://apis.io/plans/quodd/quodd-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Quodd Rate Limits](https://apis.io/rate-limits/quodd/quodd-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Quodd Finops](https://apis.io/finops/quodd/quodd-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.quodd.com)
- [Documentation](https://developer.quodd.com)
- [Support](https://www.quodd.com/support)
- [Blog](https://www.quodd.com/insights)
- [Terms of service](https://www.quodd.com/terms-of-use)
- [Privacy policy](https://www.quodd.com/privacy-policy)

## API Evangelist rating

**Kin Score 36.2** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 48.4 |
| Contract governance | 4.5 |
| Operational transparency | 7.9 |
| Developer ergonomics | 47.0 |
| Access clarity | 26.3 |

**Agent readiness 19.5** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 28.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/quodd/](https://apis.io/providers/quodd/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for QUODD: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/quodd/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
