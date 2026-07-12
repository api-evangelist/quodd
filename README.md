# QUODD (quodd)

QUODD is a cloud-native market data provider delivering real-time, delayed, historical, end-of-day, and point-in-time pricing, plus reference data, a security master, fundamentals, estimates, corporate actions, ESG, and news across global equities, ETFs, options, fixed income, FX, funds, and indices. The QUODD Developer Platform ([developer.quodd.com](https://developer.quodd.com)) exposes market data through REST and gRPC snapshot APIs with token-based authentication, alongside cloud delivery options — Cloud APIs, Cloud Streaming, Cloud Alerts, Cloud Search, and Cloud Files. QUODD advertises more than 250 billion data points across 150-plus global exchanges.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/quodd/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/quodd/refs/heads/main/apis.yml)

## Access Model (Read This First)

QUODD's developer documentation is publicly readable, but production access is **gated**:

- **Token-based auth.** Trial or firm users exchange a username and password for an access token (`POST` token-for-trial-user / token-for-firm-user). The token is appended to REST requests as the `_token` query parameter and **expires after 24 hours**.
- **Enterprise / contact-sales.** There is **no public, self-serve pricing**. Commercial access, dataset entitlements, and exchange licensing are arranged per customer.
- **Exact REST base URL and paths are not published openly.** `api.quodd.com` is referenced for the gRPC Snap service. The OpenAPI in this entry is therefore **honestly modeled** (`endpointsModeled`) from the documented operation list — Snap, Batch Snaps, Options Snap, Batch Options Snaps, and the token endpoints — and may differ from the live routes.

## Tags

- Market Data
- Real-Time Data
- Financial Data
- Streaming
- Historical Data
- Reference Data
- Quotes
- Fintech

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### QUODD Snap API

Single-ticker real-time or delayed pricing snapshot (Snap) — last price, bid/ask, volume, and related fields for one instrument across QUODD's global asset-class coverage. Endpoint paths are modeled.

- **Documentation:** [https://developer.quodd.com/docs/rest-api](https://developer.quodd.com/docs/rest-api)
- **Base URL (modeled):** `https://api.quodd.com`

### QUODD Batch Snaps API

Batch snapshot retrieval for many tickers in a single request, via `GET` (query list) or `POST` (ticker array). Documented as Batch Snaps in the QUODD REST API reference.

- **API Reference:** [https://developer.quodd.com/docs/rest-api/post-batch-snaps](https://developer.quodd.com/docs/rest-api/post-batch-snaps)

### QUODD Options Snaps API

Real-time or delayed options pricing snapshots for single contracts (Options Snap) and for many contracts at once (Batch Options Snaps, `GET` and `POST`).

- **API Reference:** [https://developer.quodd.com/docs/rest-api/post-batch-options-snaps](https://developer.quodd.com/docs/rest-api/post-batch-options-snaps)

### QUODD Authentication Token API

Token generation for trial and firm users. Exchanges credentials for a 24-hour access token passed as the `_token` query parameter.

- **API Reference:** [https://developer.quodd.com/docs/rest-api/post-token-for-trial-user](https://developer.quodd.com/docs/rest-api/post-token-for-trial-user)

### QUODD Ticker Search API

Ticker and symbol lookup for discovering securities across asset classes and identifiers (Cloud Search). Listed as Beta Access on the Developer Platform; endpoints modeled.

- **Documentation:** [https://developer.quodd.com/](https://developer.quodd.com/)

### QUODD Historical Prices API

End-of-day and historical market data across 80-plus global exchanges — US equities and ETFs from 1994, global markets from 2000 — as OHLCV time series or point-in-time snapshots, with adjusted/unadjusted series and automatic corporate-action adjustments. Concrete endpoints are modeled, not published.

- **Documentation:** [https://www.quodd.com/historical-stock-prices-api-global-market-data](https://www.quodd.com/historical-stock-prices-api-global-market-data)

### QUODD Reference Data & Security Master API

Global reference data and security master (Global Master) — intra-day equity descriptive data, funds, corporate actions, dividends, and fixed income terms and conditions. Concrete endpoints are modeled, not published.

- **Documentation:** [https://www.quodd.com/financial-data-apis](https://www.quodd.com/financial-data-apis)

### QUODD Fundamentals & Estimates API

Company fundamentals, metrics, ratios, and analyst estimates on global securities. Concrete endpoints are modeled, not published.

- **Documentation:** [https://www.quodd.com/financial-data-apis](https://www.quodd.com/financial-data-apis)

### QUODD Snap gRPC API

gRPC delivery of pricing snapshots (Snap) and ticker information (Ticker Info) for high-performance, low-overhead integrations. Documented on the Developer Platform alongside the REST API.

- **Documentation:** [https://developer.quodd.com/docs/snap-grpc-api](https://developer.quodd.com/docs/snap-grpc-api)

### QUODD Cloud Streaming API

Cloud Streaming pushes changing quote and trade fields continuously rather than requiring repeated REST polling. **QUODD's own developer platform does not publicly document the streaming transport** (no `wss://` endpoint is published); third-party WebSocket access to QUODD feeds is documented via Intrinio's Real-Time SDK. Access is gated behind enterprise agreements.

- **Documentation:** [https://www.quodd.com/advanced-api-delivery](https://www.quodd.com/advanced-api-delivery)

## WebSocket / Streaming Review

**Does QUODD expose a documented public WebSocket API? No.** QUODD's own developer platform documents token-authenticated REST and gRPC snapshot APIs (request/response) and markets a "Cloud Streaming" delivery option whose transport is not publicly specified. The only documented WebSocket access to QUODD market-data feeds lives on a third-party platform (Intrinio's Real-Time SDK), not on QUODD's own API surface. No AsyncAPI document was created because there is no first-party server-push transport publicly documented to model. See `review.yml`.

## Common Properties

- [Authentication](authentication/quodd-authentication.yml)
- [LinkedIn](https://www.linkedin.com/company/quodd-financial-information-services)
- [Website](https://www.quodd.com)
- [Documentation](https://developer.quodd.com)
- [Plans](plans/quodd-plans-pricing.yml)
- [Rate Limits](rate-limits/quodd-rate-limits.yml)
- [Fin Ops](finops/quodd-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
