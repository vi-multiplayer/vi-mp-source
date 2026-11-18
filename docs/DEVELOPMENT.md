# Developer guide

## Current state

This repository is a documentation and structure foundation. It has no production code, selected implementation language, build system, or runnable client/server. The folders below reflect the current tree; see [STRUCTURE.md](STRUCTURE.md) for the complete listing.

## Where to work

- `source/client/`: launcher, player-side networking, Lua sandbox, and multiplayer game behavior.
- `source/server/`: server startup, networking, Lua runtime areas, and authoritative multiplayer game behavior.
- `source/shared/`: common models, extensions metadata, validation, and the shared game-function SDK.
- `source/vendor/`: approved third-party source only; record provenance and license.
- `tests/`: tests grouped by client, server, shared code, SDK, and integration.
- `tools/`: scripts, developer helpers, code generation, and release utilities.
- `docs/`: scope, architecture, research, guides, and decision records.
- `.github/`: issue, pull request, and discussion templates; future automation.

## Contribution flow

1. Read [CONTRIBUTING.md](../CONTRIBUTING.md), [the project scope](PROJECT_SCOPE.md), [the structure guide](STRUCTURE.md), and [code style](CODE_STYLE.md).
2. Open a Discussion for an early idea or question. Use an Issue when the work is ready to be scoped.
3. Make a focused branch and pull request. Explain affected modules, verification, and compatibility impact.
4. Do not add code, APIs, game-specific claims, or dependencies without describing their evidence and source.

## When implementation begins

Choose the language, Lua version, build system, network format, and test runner from documented requirements. Then add exact local build and verification commands, matching CI checks, and dependency provenance. Until then, do not invent placeholder code or claim game compatibility.
