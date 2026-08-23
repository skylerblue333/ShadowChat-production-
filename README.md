# ShadowChat Production

Production service boundary for SKYCOIN4444 ShadowChat. Application behavior remains in the canonical ShadowChat implementation; this repository owns production integration/deployment concerns.

## Integration contract
- Realtime transport: Socket.IO/WebSocket-compatible gateway
- Events: `message`, `presence`, `typing`
- Persistence: canonical SKYCOIN4444 database service
- Queue: `TypeScript-Message-Queue` / BullMQ
- Authentication: `TS-Auth-Service`
- Canonical integration target: `skycoin4444-canonical`

## Readiness gate
Do not label this service production-ready until database connectivity, authentication, realtime messaging, deployment, TLS/live URL, and authenticated smoke tests all pass.

## Preservation rule
Existing ShadowChat implementations must be compared before consolidation. Preserve working behavior and migrate capabilities into the canonical ecosystem rather than replacing code solely for architectural consistency.
