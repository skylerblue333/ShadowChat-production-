# ShadowChat Production — Archived Integration Stub

**Portfolio status: ARCHIVED.**

This repository is retained for historical reference only. It is not a production deployment, runnable ShadowChat application, or canonical source of ShadowChat behavior.

## Why it is archived

The repository contains deployment/integration metadata but no application source tree or Dockerfile. Its previous `package.json` scripts reported successful build/test/lint results without executing meaningful verification, and `docker-compose.yml` referenced a local image build that this repository cannot perform as-is.

Keeping this repository active would duplicate and blur the canonical ShadowChat work. Useful deployment ideas should be migrated deliberately into the canonical ShadowChat repository or the integrated SKYCOIN4444 application rather than developed independently here.

## Canonical direction

Use the maintained canonical ShadowChat implementation for application code and verified runtime behavior. Treat this repository only as historical evidence of an earlier deployment-boundary concept.

Potential integration contracts preserved from the earlier design include:

- realtime messaging over WebSocket/Socket.IO-compatible interfaces;
- external database and Redis dependencies;
- a separate authentication boundary;
- queue-backed background work.

These are architecture notes, not verified capabilities of this archived repository.

## Historical deployment stub

`docker-compose.yml` is retained to preserve history. It references `DATABASE_URL`, `REDIS_URL`, and `AUTH_SERVICE_URL`, but there is no Dockerfile or application source in this repository, so the compose definition is **not a verified deployable stack**.

## Preservation policy

Do not delete useful history. If a file or idea from this repository is still valuable, port it through a reviewed change into the canonical implementation and verify it there.

## Authorship

Developed by Skyler Blue Spillers with human, open-source, and AI-assisted engineering. AI assistance does not imply solely AI-authored work.
