---
name: define-contract
description: Define an explicit behavioural and typed contract at a boundary between independently implemented components/workstreams.
---

# Define contract

For each important seam, record in `docs/CONTRACTS.md`:

1. purpose and participants;
2. authoritative state owner;
3. input type/message;
4. output/result/event type;
5. preconditions;
6. postconditions;
7. invariants protected;
8. state changes;
9. expected domain failure outcomes;
10. exceptional failures;
11. idempotency key/duplicate behaviour when relevant;
12. ordering guarantee and scope;
13. atomicity boundary;
14. retry/cancellation semantics where relevant;
15. contract tests/fakes needed by each side.

Prefer explicit Python dataclasses/enums/unions/Protocols once the seam is stable.
