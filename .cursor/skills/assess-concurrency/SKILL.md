---
name: assess-concurrency
description: Decide whether and how concurrency is actually needed, including state ownership, ordering, idempotency, cancellation and formal-model escalation.
---

# Assess concurrency

Ask:
1. Is simultaneous execution actually required?
2. Could synchronous processing satisfy the spec/harness?
3. What state can be affected concurrently and who owns it?
4. Can mutations be serialized through that owner?
5. What are interleaving points and atomic operations?
6. Which operations commute?
7. What is the narrowest required ordering scope?
8. Can messages be retried/duplicated/reordered/dropped?
9. What identity enables idempotency?
10. What happens on cancellation/failure during a multi-step operation?

Choose the simplest mechanism: synchronous → asyncio → threads → processes.

Recommend a tiny formal model only if meaningful interleavings are genuinely difficult to enumerate and several risk signals are present. If recommended, identify only the small protocol, state variables, actions, safety invariants, and any essential liveness property.
