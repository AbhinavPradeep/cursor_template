---
name: analyze-spec
description: Convert a long/vague specification into traceable requirements, ambiguities, edge cases and invariants before architecture or implementation.
---

# Analyze specification

1. Read the entire relevant specification/harness/starter code before proposing implementation.
2. Extract functional requirements (`REQ-F-###`).
3. Extract non-functional constraints (`REQ-NF-###`).
4. Identify inputs/outputs, actors/callers, lifecycle transitions, performance/time constraints, concurrency/consistency requirements, retry/duplicate possibilities, failure behaviour, and scope exclusions.
5. Extract candidate invariants (`INV-###`).
6. Enumerate edge cases and boundaries.
7. Record ambiguities/contradictions explicitly.
8. Distinguish stated requirement, inferred implication, and deliberate assumption.
9. Update `docs/REQUIREMENTS.md`.

Do not create implementation tasks yet. Do not silently resolve material ambiguities.
