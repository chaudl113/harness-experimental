# Agent Instructions

Add project-specific agent instructions here.

<!-- HARNESS:BEGIN -->
## Harness

This repo uses Harness. Before work, read:

- `README.md`
- `docs/HARNESS.md`
- `docs/FEATURE_INTAKE.md`
- `docs/ARCHITECTURE.md`
- `docs/CONTEXT_RULES.md`
- `docs/CONTEXT.md` (domain glossary)
- `docs/DOMAIN.md` (domain model)
- `docs/TOOL_REGISTRY.md`
- `docs/TEST_MATRIX.md`
- `scripts/bin/harness-cli query matrix` on macOS/Linux, or `.\scripts\bin\harness-cli.exe query matrix` on Windows

Use the Rust Harness CLI at `scripts/bin/harness-cli` on macOS/Linux or
`scripts/bin/harness-cli.exe` on Windows as the main operational tool. Before a
step that could use an external tool, run `scripts/bin/harness-cli query tools
--capability <name> --status present` to see what is equipped; an absent
capability is a clean skip.

## Project Docs

- `docs/ADR/` — architecture decision records (application-level)
- `docs/decisions/` — Harness infrastructure decisions
- `docs/API/` — API contracts (OpenAPI, GraphQL, gRPC)
- `docs/RUNBOOK/` — operational procedures

## Skills

Skills live in `.claude/skills/`:

| Category | User-invoked (type `/name`) | Model-invoked (auto) |
|---|---|---|
| Engineering | `grill-with-docs`, `to-prd`, `to-issues`, `improve-codebase-architecture`, `setup-matt-pocock-skills`, `triage` | `tdd`, `diagnosing-bugs`, `codebase-design`, `domain-modeling`, `prototype`, `code-review` |
| Productivity | `handoff` | `grilling` |
| Project | (add project-specific skills here) | — |
<!-- HARNESS:END -->
