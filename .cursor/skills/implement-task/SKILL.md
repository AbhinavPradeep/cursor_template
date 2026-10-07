---
name: implement-task
description: Implement one already-defined bounded task while preserving agreed contracts, state ownership and reviewability.
---

# Implement one bounded task

Before editing, read the task, linked requirements/invariants/contracts, existing implementation/tests, expected files/areas, and any shared contract impact. If an unplanned architecture/shared-contract change is needed, report it first.

Defaults:
- explicit typed data and straightforward transformations;
- expected domain failures as explicit results/events;
- preserve state ownership;
- immutable boundary messages where practical;
- no concurrency without a requirement;
- no new layers/packages without concrete pressure;
- no unrelated refactors.

Add the simplest tests that protect the behaviour. Run focused tests during iteration and the full deterministic gate at completion.
