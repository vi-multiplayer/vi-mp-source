# Current repository structure

This guide matches the folders currently present in the repository. It does not list folders that were removed. The README files inside each area explain its responsibility; implementation and technology choices remain open.

```text
.
├── .github/
│   ├── DISCUSSION_TEMPLATE/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
├── source/
│   ├── client/
│   │   ├── bootstrap/
│   │   ├── core/
│   │   ├── game/
│   │   ├── launcher/
│   │   ├── network/
│   │   │   ├── connection/
│   │   │   └── transport/
│   │   └── scripting/
│   │       └── lua/
│   │           └── sandbox/
│   ├── server/
│   │   ├── bootstrap/
│   │   ├── core/
│   │   ├── game/
│   │   ├── network/
│   │   │   ├── connection/
│   │   │   └── transport/
│   │   └── scripting/
│   │       └── lua/
│   │           ├── api/
│   │           ├── bindings/
│   │           ├── runtime/
│   │           └── sandbox/
│   ├── shared/
│   │   ├── config/
│   │   ├── extensions/
│   │   ├── game/
│   │   ├── sdk/
│   │   ├── types/
│   │   └── validation/
│   └── vendor/
├── tests/
│   ├── client/
│   ├── fixtures/
│   ├── integration/
│   ├── sdk/
│   ├── server/
│   └── shared/
├── tools/
│   ├── codegen/
│   ├── dev/
│   ├── release/
│   └── scripts/
└── docs/
    ├── decisions/
    └── research/
        └── game-sdk/
```

Root files include `README.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `SUPPORT.md`, `CHANGELOG.md`, `.editorconfig`, `.gitattributes`, and `.gitignore`. A license has not been selected.

## Client and server game code

`source/client/game/` is for the client's multiplayer behavior: message/event handlers, player and entity state, game-state synchronization, and client-side lifecycle. It is not merely a game integration adapter.

`source/server/game/` is for the server's authoritative multiplayer behavior: client-message handlers, player/session state, entity/world state, event handling, and synchronization decisions. Client input is untrusted. Both folders describe project behavior; they do not contain game files.

## Lua

Lua-related code is grouped under `source/client/scripting/` and `source/server/scripting/`. The server currently separates runtime, API, bindings, and sandbox areas. The client currently keeps a Lua sandbox area. The exact Lua version, API, execution model, and package format still need decisions.

## Shared SDK

`source/shared/sdk/` is the shared game-function library boundary used by project code. Keep its contents project-owned and record function provenance, version, confidence, and constraints in `docs/research/game-sdk/`. It is not a server scripting SDK. No SDK subfolders are listed because they are not present in the current tree.

## Other folders

- `source/client/launcher/`: player-facing startup and server-selection workflows.
- `source/client/network/` and `source/server/network/`: connection lifecycle and transport boundaries.
- `source/shared/game/`: common multiplayer state models.
- `source/shared/extensions/`: shared extension metadata/contracts, if needed.
- `source/vendor/`: approved third-party source only, with provenance and license recorded.
- `tests/`: client, server, shared, SDK, integration, and synthetic fixture areas.
- `tools/`: repository scripts, development helpers, code generation, and release tools.
- `.github/`: issue, pull request, discussion templates, and future automation.

## Technology choices

No programming language for the client/server, build system, network protocol, Lua version, SDK binding strategy, or CI checks has been selected. Add implementation only after requirements and supported interfaces are established.
