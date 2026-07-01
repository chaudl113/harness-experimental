# Domain Model

No application domain is currently defined. This document is the placeholder for the project's domain model — the core business concepts, their relationships, and the ubiquitous language that the code, docs, and agent instructions share.

## When to populate

Populate this document when a product spec arrives. During the first buildout, use `/grill-with-docs` to:

1. Extract domain terms from the spec
2. Challenge fuzzy language and pick canonical terms
3. Record decisions that shape the domain in `docs/ADR/`

## Structure

Once populated, this document should cover:

### Bounded Contexts

The product areas with stable names and contracts. Example for an e-commerce system:

- **Ordering**: receives and tracks customer orders
- **Inventory**: manages stock levels and warehouse allocation
- **Billing**: generates invoices and processes payments
- **Fulfillment**: manages picking, packing, and shipping

### Core Entities

The key domain objects with their identity and lifecycle:

| Entity | Context | Identity | Lifecycle |
|--------|---------|----------|-----------|
| Order | Ordering | Order ID | Created → Confirmed → Paid → Fulfilled → Completed |

### Relationships

Cross-context relationships and integration patterns:

- **Ordering → Inventory**: reserves stock on order placement
- **Ordering → Billing**: triggers invoice generation on order confirmation
- **Fulfillment → Inventory**: decrements stock on shipment

### State Machines

Non-trivial state transitions for core entities should be documented as diagrams or tables.

## Before implementation

1. Run `/grill-with-docs` on the product spec to define the domain vocabulary.
2. Update `docs/CONTEXT.md` with the glossary terms.
3. Update this document with bounded contexts, entities, and relationships.
4. Record architecture decisions in `docs/ADR/` as they crystallize.
5. Validate: can an agent read `CONTEXT.md` + `DOMAIN.md` + `docs/ADR/*.md` and understand what to build without guessing?
