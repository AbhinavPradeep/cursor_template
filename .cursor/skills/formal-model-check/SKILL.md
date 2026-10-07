---
name: formal-model-check
description: Optional workflow for a small concurrency-critical protocol only after simpler reasoning/tests are insufficient.
---

# Formal model check

Do not use by default.

Use only for a deliberately selected small protocol whose interleavings are difficult to reason about with ownership, types, tests and stateful PBT alone.

Potential tools include TLA+/PlusCal or SPIN/Promela.

Model protocol state variables, independently scheduled actors, transitions, ordering/idempotency semantics, safety invariants, and only essential liveness properties.

Do not model Python class layout, helpers, logging, or unrelated application details.

Workflow:
1. state the concrete risk;
2. define smallest abstract state;
3. define actions;
4. define invariants;
5. run checker if available;
6. inspect counterexamples;
7. translate meaningful traces into Python regression/stateful tests;
8. reconcile requirements/model/contracts/implementation;
9. document under `docs/formal/`.
