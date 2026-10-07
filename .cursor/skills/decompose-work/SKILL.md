---
name: decompose-work
description: Turn agreed architecture and contracts into a dependency-aware task DAG suitable for independent or parallel work.
---

# Decompose work

Before creating tasks, verify explicit answers exist for major dataflow, invariants, state ownership, component boundaries, contracts, and concurrency/ordering/idempotency decisions where relevant. If not, report the missing design decision rather than inventing tasks.

Each task should state:
- task ID and behavioural goal;
- requirement/invariant IDs;
- owner/workstream;
- dependencies;
- referenced contracts;
- in scope / out of scope;
- expected files/areas (advisory only);
- acceptance criteria;
- tests/verification;
- shared-contract impact.

Prefer tasks with small blast radius that can be fully human-reviewed and tested independently.

Parallel tasks are valid when state ownership does not overlap, the connecting contract is agreed, fakes/stubs allow independent progress, and neither side routinely edits the other's internals.

Update `docs/TASKS.md`.
