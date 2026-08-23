# ShadowChat Production

Production integration boundary for SKYCOIN4444 ShadowChat. Application behavior remains in the canonical ShadowChat implementation; this repository owns deployment and runtime integration concerns.

## Integration contract
- Realtime transport: Socket.IO/WebSocket-compatible gateway
- Events: `message`, `presence`, `typing`
- Persistence: canonical SKYCOIN4444 database service
- Queue: `TypeScript-Message-Queue` / BullMQ
- Authentication: `TS-Auth-Service`
- Canonical integration target: `skycoin4444-canonical`

## Deployment configuration

`docker-compose.yml` defines the runtime contract and requires `DATABASE_URL`, `REDIS_URL`, and `AUTH_SERVICE_URL`.

The compose file does **not** create or imply a production database, Redis deployment, authentication service, TLS certificate, or public URL. Those dependencies must be provisioned and verified separately.

## Readiness gate

Do not label this service production-ready until database connectivity, authentication, realtime messaging, deployment, TLS/live URL, and authenticated smoke tests all pass.

## Current limitation

This repository is currently an integration/deployment boundary rather than a complete ShadowChat implementation. Existing ShadowChat repositories must be compared before consolidation.

## Preservation rule

Preserve working behavior and migrate capabilities into the canonical ecosystem rather than replacing code solely for architectural consistency.

## Domains

- https://skycoin4444.com
- https://skycoin4444.net
- https://skycoin4444.shop
- https://skycoin44.token

## Authorship

Developed by Skyler Blue Spillers with human, open-source, and AI-assisted engineering. AI assistance does not imply solely AI-authored work.
