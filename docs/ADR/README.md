# Architecture Decision Records

Durable decisions that shape architecture, integration patterns, technology choices, and scope boundaries.

## Current ADRs

No application ADRs yet — the project is in Harness v0 with no application code. When ADRs are created, they follow the format defined in `docs/templates/decision.md` and `.claude/skills/engineering/domain-modeling/ADR-FORMAT.md`.

Existing Harness infrastructure decisions live in `docs/decisions/` (the original Harness decision log).

## When to create an ADR

All three conditions must be true:

1. **Hard to reverse** — the cost of changing your mind later is meaningful
2. **Surprising without context** — a future reader will wonder "why did they do it this way?"
3. **The result of a real trade-off** — there were genuine alternatives and you picked one for specific reasons

## Numbering

Sequential: `0001-slug.md`, `0002-slug.md`, etc. Increment from the highest existing number in this directory.
