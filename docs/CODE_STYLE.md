# Code and documentation style

No production language or build tool has been selected. This guide sets language-neutral rules; add language-specific formatting and lint rules when a real implementation is chosen.

## General

- Prefer clear names, small functions, and reviewable changes over clever abstractions.
- Keep client, server, and shared responsibilities explicit.
- Validate untrusted input at boundaries and return useful errors without exposing secrets.
- Document public interfaces, configuration, compatibility, and security assumptions.
- Add dependencies only for a clear need; check maintenance status and license first.
- Never commit credentials, personal data, game files, leaked material, or generated binaries.

## Formatting

- UTF-8 text, LF line endings, and a final newline.
- Four spaces for indentation by default; YAML uses two spaces.
- Use descriptive Markdown headings, ordered levels, and language-tagged fenced code blocks.
- Keep prose readable and avoid reformatting unrelated sections.

## Source boundaries

- Put player-side project code in `source/client/` and hosting code in `source/server/`.
- Put only deliberately shared contracts and small common definitions in `source/shared/`.
- Put approved vendored third-party source in `source/vendor/`, with its upstream, version, license, and local modifications documented.
- Put contributor-facing scripts in `tools/`; document prerequisites and effects.
- Treat serialized data and network messages as versioned interfaces.

## Review checklist

- Is the change scoped, understandable, and documented?
- Are invalid input, errors, concurrency, and resource limits handled where relevant?
- Are dependency and content origins clear, and are their licenses compatible?
- Can a reviewer verify the change using documented steps?
