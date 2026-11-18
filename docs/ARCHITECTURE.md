# Architecture principles

This document describes the responsibilities intended for the current folders. It does not choose implementation languages or claim the target game's integration method is known.

## Client

`source/client/game/` is the client multiplayer runtime: message/event handlers, local and remote player state, entity/world updates, synchronization, and client lifecycle. `source/client/network/` handles connection and transport. `source/client/scripting/` contains Lua execution boundaries. `source/client/launcher/` handles player startup and server selection.

## Server

`source/server/game/` is the authoritative multiplayer runtime: client-message handlers, player/session state, entities/world state, events, and synchronization. `source/server/network/` handles connections and transport. `source/server/scripting/` owns Lua execution areas. Treat every client message and script input as untrusted.

## Shared and SDK

`source/shared/` contains common models and rules used by both sides. `source/shared/sdk/` is the shared game-function library boundary consumed by project code; record evidence and target version for its declarations in `docs/research/game-sdk/`. Keep it separate from Lua runtimes and do not put game files or proprietary game source in the repository.

## Principles

1. Keep the client game handlers and server authority clearly separated.
2. Validate all network and script input at trust boundaries.
3. Version shared message and data contracts deliberately.
4. Bound script capabilities and resource usage before running untrusted code.
5. Record game-facing function provenance, target build, confidence, and limitations.
6. Keep external dependencies and vendored source traceable and license-reviewed.
7. Record significant technical choices as dated ADRs.

## Open decisions

The game-state model, exact multiplayer handlers, network message format, Lua version/runtime, script package format, SDK declarations, build system, and supported platforms remain undecided. Define these from concrete requirements and verifiable technical information.
