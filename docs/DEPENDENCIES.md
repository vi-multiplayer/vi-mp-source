# Dependency policy

No runtime dependencies have been selected. Keep `source/vendor/` empty until there is a concrete need to vendor source directly.

Before adding a dependency:

1. Describe why the project needs it and whether a standard library or existing dependency can meet the need.
2. Check the upstream's maintenance, security history, and license compatibility.
3. Record its exact version and source in the relevant package manifest and update the lockfile where the ecosystem uses one.
4. If source is copied into `source/vendor/`, record the upstream URL, exact version or commit, license, local changes, and update procedure.
5. Do not copy source, tools, or assets from FiveM, MTA, or another project.

The repository license and contribution terms must be chosen before accepting implementation contributions.
