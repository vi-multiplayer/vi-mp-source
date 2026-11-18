# Roadmap

This roadmap lists investigation gates, not promised features or dates. Later stages depend on verified information and a permitted technical path.

## 0. Project foundation

- [x] Establish project scope and contributor guidance.
- [x] Adopt the `source/client`, `source/server`, `source/shared`, `source/vendor`, `tools`, and `docs` structure.
- [ ] Select a repository license and contribution terms.
- [ ] Confirm repository ownership, default branch, and GitHub settings.
- [ ] Choose independent project branding.

## 1. Research and requirements

- [ ] Track official public information about platform availability, technical interfaces, and modding terms.
- [ ] Keep dated sources and mark claims as confirmed, uncertain, or unknown.
- [ ] Define goals and needs for players, server operators, and developers without assuming game internals.
- [ ] Decide whether game-specific integration is supported and permitted.

## 2. Technical proposal

- [ ] Select a language and build approach based on requirements and supported interfaces.
- [ ] Define deployment, trust boundaries, update model, and threat model.
- [ ] Decide what client, server, and shared responsibilities actually require.
- [ ] Establish evidence, version support, and provenance for each proposed game SDK function before implementation.
- [ ] Decide separately whether a community-facing extension SDK is needed; do not conflate it with the shared game SDK.
- [ ] Record major choices in ADRs and track unresolved risks.

## 3. Game-independent foundation

- [ ] Add source code only for components with a concrete, independent use case.
- [ ] Add build, formatting, and verification automation once the source toolchain exists.
- [ ] Document how contributors build and review the project.

## 4. Supported game integration (conditional)

- [ ] Pass the scope gate in `PROJECT_SCOPE.md` before any game-specific implementation.
- [ ] Build and document a minimal integration against supported interfaces.
- [ ] Publish compatibility limits, installation guidance, and security practices.
- [ ] Arrange independent review before distributing builds.

## Not decided

There is no release date, compatibility promise, client integration method, server protocol, scripting system, or selected implementation stack.
