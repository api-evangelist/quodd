---
name: Batch snapshots for equities and options
description: Retrieve pricing snapshots for many tickers or option contracts in a single request instead of polling one by one.
api: openapi/quodd-snapshots-api-openapi.yml
operations: [listSnaps, batchSnaps, getOptionsSnap, listOptionsSnaps, batchOptionsSnaps]
generated: '2026-07-22'
method: generated
---

# Batch snapshots for equities and options

1. **Authenticate first** (see the authenticate-and-snap skill); every call takes the `_token` query parameter.
2. **Prefer batch over loops.** QUODD's rate limits are contractual, not published — reduce call volume by requesting many tickers at once:
   - `listSnaps` — GET with a query list of tickers.
   - `batchSnaps` — POST with an array of tickers (use for long lists).
3. **Options contracts** use the parallel operations in `openapi/quodd-options-api-openapi.yml`: `getOptionsSnap` for one contract, `listOptionsSnaps` / `batchOptionsSnaps` for many. Option snapshots add `UnderlyingTicker`, `OptionType`, `ExpirationDate`, `StrikePrice`.
4. **Discover contracts before snapping them.** Option tickers and expirations come from the Option Lookup gRPC service (`grpc/quodd-optionlookup.proto`: `GetOptionTickers`, `GetOptionExpirations`).
5. **Handle partial failures.** Batch responses succeed as a whole while individual instruments fail in-payload — inspect each object's `Error` field and never treat a `200` as all-clear.
