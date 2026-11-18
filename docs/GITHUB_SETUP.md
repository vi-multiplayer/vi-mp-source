# GitHub repository setup

Repository: [vi-multiplayer/vi-mp-source](https://github.com/vi-multiplayer/vi-mp-source). The repository is public. This checklist records the selected community workflow and which settings still need to be applied.

## Issues

- Keep Issues enabled and allow the public to file issues.
- Use `.github/ISSUE_TEMPLATE/` forms for bug reports, feature/design proposals, and documentation fixes.
- Create and maintain these labels: `bug`, `enhancement`, `documentation`, `question`, `good first issue`, `help wanted`, `status:triage`, `status:blocked`, `area:client`, `area:server`, `area:lua`, and `area:sdk`.
- Route broad questions and early ideas to Discussions; keep Issues for actionable work.

## Pull requests

- Keep Pull Requests enabled and allow public contributions.
- Use the repository pull request template. Require a summary, related issue, verification notes, and compatibility impact.
- Prefer squash or rebase merging for focused project history. Delete merged head branches automatically.
- Add branch protection after the initial `main` branch is present. Protect against force-push and deletion; require a pull request, but do not require CI checks until stable checks exist.

## Discussions

Enable Discussions and use categories:

- **Announcements** — maintainer-only release and project news.
- **General** — open conversation.
- **Ideas** — early product and architecture ideas; use `.github/DISCUSSION_TEMPLATE/ideas.yml`.
- **Polls** — community preference checks.
- **Q&A** — project and contributor questions; use `.github/DISCUSSION_TEMPLATE/q-a.yml`.
- **Show and tell** — original experiments and community contributions.

Discussion form filenames must match the category slugs (`ideas` and `q-a`). GitHub allows maintainers to create and edit category names, formats, and slugs from the Discussions page.

## Repository identity and access

- Keep the description clear that this is an independent, pre-development project.
- Use original branding; do not use publisher logos or game assets.
- Keep the wiki off while `docs/` is the canonical documentation source.
- Do not add a license until project owners choose reuse and contribution terms.
- Enable private vulnerability reporting when available and point users to `SECURITY.md`.

## Automation and releases

- Keep GitHub Actions disabled or read-only until workflows have stable project checks. Grant write permissions only to a workflow that needs them.
- Add formatting/build checks once the project chooses its toolchain.
- Do not publish releases or claim game compatibility until the project scope gate is satisfied.
- Add release signing and artifact provenance before distributing executable builds.
