# Project Context

Shared domain language for this repository. AI agents use this glossary to stay consistent with business terms, module naming, and architectural decisions.

## Language

**Harness**:
The operating framework that agents interact with — intake, story, trace, audit, backlog, and the Rust CLI at `scripts/bin/harness-cli`. Not the application itself.
_Avoid_: framework, scaffold

**Intake**:
The entry gate where every implementation prompt is classified by type (new spec, spec slice, change request, etc.) and risk lane (tiny, normal, high-risk).
_Avoid_: ticket, request

**Story**:
A story-sized work packet with classification, status, validation proof, and trace linkage. Stored in `docs/stories/` and the durable layer (`harness.db`).
_Avoid_: task, ticket, issue

**Trace**:
A durable record of what was done in a session — intake, decisions, friction, and outcome — scored for quality. Stored via `scripts/bin/harness-cli trace`.
_Avoid_: log, record

**Durable Layer**:
The SQLite database (`harness.db`) + Rust CLI (`scripts/bin/harness-cli`) that stores operational state: intakes, stories, decisions, backlog, traces, interventions, and tool registrations.
_Avoid_: database, backend, store

**Proof**:
Validation evidence (unit, integration, e2e, platform) recorded against a story via `scripts/bin/harness-cli story update --unit 1 --integration 1`.
_Avoid_: test, verification

**Backlog**:
Harness improvement items — friction-driven, with predicted vs actual outcomes. Managed via `scripts/bin/harness-cli backlog add`.
_Avoid_: todo, issue

**Decision**:
A durable architectural or process decision, recorded in `docs/decisions/` and the durable layer via `scripts/bin/harness-cli decision add`.
_Avoid_: ADR (use sparingly — only for architecture-specific decisions)

**Intervention**:
A correction, override, escalation, or approval from a human, reviewer, CI, or another agent. Recorded separately from traces.
_Avoid_: correction, review

**Capability**:
A named purpose (e.g. `deploy-verification`) that optional external tools can provide. Absent capability = clean skip, never a failure.
_Avoid_: feature, tool

**Lane**:
Risk classification tier: `tiny`, `normal`, or `high-risk`. Determines process depth.
_Avoid_: level, tier, priority
