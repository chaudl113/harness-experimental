# Project Rules

<!-- HARNESS:BEGIN -->
## Harness

Claude Code loads this file into every session, but it does not auto-load
`AGENTS.md`. The bare `@` lines below import the always-required harness
context (the "Must in all lanes" set from `docs/CONTEXT_RULES.md`) at
context-load time. Never wrap them in backticks; that disables the import.

@AGENTS.md

@docs/FEATURE_INTAKE.md

@docs/CONTEXT.md

Also run `scripts/bin/harness-cli query matrix` before starting work.

Lane-dependent context (`README.md`, `docs/HARNESS.md`, `docs/ARCHITECTURE.md`,
`docs/DOMAIN.md`, `docs/CONTEXT_RULES.md`, product docs, stories, decisions) is
intentionally not imported — read it per lane, as `docs/CONTEXT_RULES.md`
prescribes.

## Skills

Engineering skills live in `.claude/skills/engineering/`. User-invoked skills
(type `/skill-name`) are: `grill-with-docs`, `to-prd`, `to-issues`,
`improve-codebase-architecture`, `setup-matt-pocock-skills`, `triage`.
Model-invoked skills (agent auto-selects) are: `tdd`, `diagnosing-bugs`,
`codebase-design`, `domain-modeling`, `prototype`, `code-review`.

Productivity skills in `.claude/skills/productivity/`: `grill-me`, `handoff`.
Project-specific skills in `.claude/skills/project/`.
<!-- HARNESS:END -->
