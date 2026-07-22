---
name: Stream and query market data over gRPC
description: Use QUODD's published proto3 services for streaming snapshots, ticker fundamentals, and option lookup at api.quodd.com:443.
api: grpc/quodd-grpc.yml
operations: [GetSnapsStream, GetSnaps, GetTickerInfo, GetOptionTickers, GetOptionExpirations]
generated: '2026-07-22'
method: generated
---

# Stream and query market data over gRPC

1. **Use the real protos.** QUODD publishes proto3 definitions saved verbatim in this repo: `grpc/quodd-snap.proto` (SnapService), `grpc/quodd-info.proto` (TickerInfoService), `grpc/quodd-optionlookup.proto` (OptionLookupService). All are served at `api.quodd.com:443`.
2. **Authenticate via metadata.** Add `authorization: Bearer <JWT>` to every request's metadata. For SnapService also set `AssetType: Equities` or `AssetType: Options` to match the data requested.
3. **Snapshots.** `GetSnaps` (request/response) returns a `SnapResponse` for a ticker list; `GetSnapsStream` returns a server stream of `SnapMessage` updates.
4. **Manage the stream lifecycle.** The stream stays open while market data flows and is terminated automatically after 30 minutes without active data — implement reconnection logic; expiring JWTs also require re-auth.
5. **Fundamentals.** `GetTickerInfo` takes `tickers` plus a repeated `fields` selector (e.g. `name`, `market_cap`, `price_to_earnings`) — request only the fields you need. Per-ticker failures come back as `ErrorInfoMessage { ticker, error, message }`.
6. **Option discovery.** `GetOptionExpirations` lists expiration dates for an underlying; `GetOptionTickers` lists contracts, optionally filtered by `option_type` and `expiration_date`.
7. **Quick test.** The docs demonstrate `grpcurl -H 'authorization: Bearer TOKEN' -H 'AssetType: Equities' -proto 'snap.proto' -d '{"tickers":["AAPL"]}' api.quodd.com:443 snap.SnapService/GetSnaps`.

Each service requires the matching active subscription (streaming, ticker info, option lookup) on your QUODD agreement.
