---
name: design-system
description: Design the smallest understandable architecture after requirements analysis and before task decomposition.
---

# Design system

Goal: produce an architecture sufficient for safe independent/parallel work without overengineering.

1. Describe major dataflows first, without inventing classes.
2. Identify important mutable state and assign one authoritative owner.
3. Group coherent responsibilities into the minimum useful component/module boundaries.
4. Define dependency direction and external boundaries.
5. Default to immutable boundary messages plus controlled mutation inside owners.
6. Define failure policy: expected domain outcomes as explicit result/event types; unexpected/programming/infrastructure failures as exceptions.
7. For retryable/duplicable inputs, define stable identity and duplicate semantics.
8. Define only the ordering guarantees needed to protect invariants.
9. Assess concurrency: synchronous by default; introduce async/threads/processes only when justified.
10. Identify seams needing explicit contracts/Protocols.
11. Apply the module-promotion rule: no package/layer without real ownership/responsibility/dependency pressure.
12. Record important tradeoffs and excluded complexity.
13. Update `docs/ARCHITECTURE.md`.

Do not decompose implementation tasks yet.
