# Source Code

Application source code lives here. The Rust Harness CLI lives separately in `crates/harness-cli/`.

## Structure (proposed)

```
src/
├── domain/          ← entities, value objects, repositories, services
├── application/     ← commands, queries, handlers
├── infrastructure/  ← database, logging, notifications
├── interface/       ← controllers, DTOs, presenters, routes, middlewares
└── surfaces/        ← browser, mobile, desktop, CLI
```

This follows the architecture described in `docs/ARCHITECTURE.md`. Create real folders only when a story enters implementation and the selected stack needs them.
