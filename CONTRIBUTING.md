# Contributing

Thanks for helping shape the project. This repository is in pre-development, so start with documentation and proposals before adding game-specific code.

## Before you start

1. Read the [project scope](docs/PROJECT_SCOPE.md), [repository structure](docs/STRUCTURE.md), [architecture principles](docs/ARCHITECTURE.md), and [code style](docs/CODE_STYLE.md).
2. Search existing issues and pull requests to avoid duplicate work.
3. For a significant feature or architectural change, open an issue first and describe the problem, evidence, options, and risks.
4. Work only with material you have the right to contribute. Do not submit proprietary game files, leaked source, extracted assets, or copied code from other multiplayer projects.

## Proposing changes

- Keep each pull request focused and explain the user or developer problem it solves.
- Link related issues and record important design choices as an ADR in `docs/decisions/`.
- Include relevant documentation updates and explain how a reviewer can verify the change.
- Do not claim compatibility with an unreleased or undocumented game interface.
- Do not add dependencies, generated binaries, secrets, or game data without explaining their source, license, and necessity.
- Keep implementation in the agreed `source/client`, `source/server`, `source/shared`, or `source/vendor` area; place contributor utilities in `tools/` and documentation in `docs/`.

## Development workflow

1. Create a branch from the default branch.
2. Make the smallest coherent change.
3. Run the checks documented for the affected component. During this documentation-only stage, there are no software build or test commands.
4. Review your diff for unrelated edits, sensitive information, licensing, and accidental binary files.
5. Open a pull request using the repository template.

## Code review

Reviewers assess correctness, clarity, maintainability, security, provenance, and whether the change stays within project scope. Be open to revisions and keep discussion focused on the work.

## Contributions and licensing

The project has not selected a repository license or contributor terms. Until those are published, limit contributions to discussion and proposed documentation changes; do not treat contribution as granting broad reuse rights. A maintainer must establish the licensing policy before accepting implementation contributions.

By participating, you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).
