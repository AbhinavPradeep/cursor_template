---
name: strengthen-tests
description: Strengthen tests using properties, stateful testing, contract tests, regressions or selective mutation testing without chasing coverage for its own sake.
---

# Strengthen tests

Map each proposed test to a requirement, invariant, contract, edge case, or discovered defect. Record that link in `docs/TEST_STRATEGY.md` for substantial work. Prefer tests that would fail for a plausible incorrect implementation.

Use Pytest for example unit/transition, contract, integration, and minimal regression tests. Choose the lightest effective test for the behaviour:
- an example test for a specific outcome or boundary;
- a contract test with shared behavioural assertions for a seam;
- a small integration test for important wiring/dataflow;
- a regression test for a discovered defect.

Use Hypothesis `@given` for a meaningful general or metamorphic property. Use Hypothesis stateful testing when correctness depends on operation sequences. State the property or invariant before adding either kind of test; do not add property tests solely because Hypothesis is available.

During iteration, run focused Pytest tests with `python -m pytest <test-path>`. Before declaring a bounded task complete, run `./scripts/check.sh`, which checks Ruff, Pyright, and Pytest. Report the test-to-requirement links, commands and results, and any remaining gaps.

Mutmut is an optional late quality probe for stable critical domain logic. Inspect meaningful surviving mutants; do not chase mutation score or coverage targets.
