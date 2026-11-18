# VI Multiplayer

An independent, community-led project exploring whether multiplayer software can be built for a future game release using supported and permitted interfaces.

> This project is not affiliated with, endorsed by, or sponsored by Rockstar Games or Take-Two Interactive. It currently contains no game code, game assets, reverse-engineered material, or compatibility claims.

## Status

**Pre-development.** We do not yet have verified public technical interfaces, supported platforms, or applicable modding terms for the target game. This repository currently provides project organization and developer documentation. It does not contain a working client or server.

Game-specific implementation depends on public, verifiable technical information and a lawful, technically supported integration path. Until then, work stays in documentation, requirements, and game-independent research.

## Repository layout

```text
.
├── source/
│   ├── client/  # Launcher and player-side multiplayer behavior
│   ├── server/  # Authoritative multiplayer server behavior
│   ├── shared/  # Common models, config, validation, and game SDK
│   └── vendor/  # Approved vendored source only, if needed
├── tests/      # client, server, shared, integration, synthetic fixtures
├── tools/      # scripts, dev helpers, code generation, release tooling
├── docs/       # scope, architecture, decisions, research, and guides
└── .github/    # contribution templates and future automation
```

These folders describe the current repository organization; see [the structure guide](docs/STRUCTURE.md) for the exact current tree. `source/client/game/` and `source/server/game/` hold the multiplayer handlers and state logic for their respective sides. The shared game-function library boundary is `source/shared/sdk/`.

## Project boundaries

- Create original code, names, documentation, and designs.
- Do not copy code, assets, tools, or distinctive designs from FiveM, MTA, or other projects.
- Do not distribute game files, proprietary assets, leaked material, or circumvention tools.
- Do not claim compatibility or features without verifiable support.
- Reassess technical scope against public information and applicable terms before game-specific implementation.

## Contributing

Start with [CONTRIBUTING.md](CONTRIBUTING.md), [the project scope](docs/PROJECT_SCOPE.md), and [the developer guide](docs/DEVELOPMENT.md). At this stage, useful contributions include requirements, public-source research, documentation, and carefully scoped design proposals.

## Project documents

- [Roadmap](docs/ROADMAP.md)
- [Architecture principles](docs/ARCHITECTURE.md)
- [Code style](docs/CODE_STYLE.md)
- [Dependency policy](docs/DEPENDENCIES.md)
- [Shared game SDK](docs/SDK.md)
- [Support](SUPPORT.md)
- [Changelog](CHANGELOG.md)
- [GitHub setup checklist](docs/GITHUB_SETUP.md)
- [Architecture decision records](docs/decisions/README.md)

## Licensing

No license or contribution terms have been selected yet. Until they are published, do not assume the contents are licensed for reuse. Maintainers must decide these terms before accepting implementation contributions.

## Name and trademarks

“VI Multiplayer” is a working project name. Product names and trademarks belong to their respective owners. The project will use its own branding and will not suggest official affiliation.
