---
name: Authenticate and get a pricing snapshot
description: Generate a QUODD access token and fetch a real-time or delayed quote snapshot for one ticker.
api: openapi/quodd-snapshots-api-openapi.yml
operations: [createTrialToken, createFirmToken, getSnap]
generated: '2026-07-22'
method: generated
---

# Authenticate and get a pricing snapshot

1. **Get a token.** Call `createTrialToken` (trial users) or `createFirmToken` (firm users) in `openapi/quodd-authentication-api-openapi.yml` with your `username` and `password` (the published reference documents these as header parameters). The response contains a `token`.
2. **Cache it for up to 24 hours.** Tokens expire after 24 hours. On a `401`, regenerate the token and retry — do not retry with the same token.
3. **Fetch the snapshot.** Call `getSnap` with the `ticker` path parameter (e.g. `MSFT`) and append the token as the `_token` query parameter.
4. **Read the payload carefully.**
   - `IsDelayed: true` means prices are 15 minutes delayed. Symbology extensions also signal the feed: `.D` delayed, `.NB` Nasdaq Basic, `.NB.D` Nasdaq Basic delayed.
   - Timestamps (`LastTimestamp`, `QuoteTimestamp`) are EST, format `YYYY-MM-DDTHH:MM:SS.sssssss`.
   - A `200` can still carry a per-instrument failure: check the `Error` field on the snapshot object (see `errors/quodd-problem-types.yml`).

Notes: endpoint paths in the spec are honestly modeled — QUODD does not publish literal REST paths; production access requires trial or firm credentials. No idempotency keys or pagination exist on this surface (`conventions/quodd-conventions.yml`).
