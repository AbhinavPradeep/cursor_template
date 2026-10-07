# Architecture

Keep this short enough that the relevant contributors can explain it from memory.

## Scope and approach

- Responsible for:
- Deliberately not responsible for:

## Major dataflow

```text
INPUT
  |
  v
...
```

## State ownership

| State | Owner | Who may mutate it? | Important invariant(s) |
|---|---|---|---|
|  |  |  |  |

## Components / modules

### Component: ...

Responsibilities:
- 

Owns:
- 

Consumes:
- 

Produces:
- 

May depend on:
- 

Must not depend on:
- 

## Mutation policy

- boundary messages: immutable;
- shared contracts: typed;
- internal state: may mutate only inside its owner;
- no cross-owner direct mutation.

## Failure semantics

Expected domain outcomes represented as data:
- 

Exceptions reserved for:
- 

Partial-state policy:
- 

## Idempotency / duplicate semantics

| Input / event | Can repeat? | Identity / key | Duplicate behaviour |
|---|---|---|---|
|  |  |  |  |

## Ordering semantics

| Operations / stream | Required ordering scope | Why / invariant protected |
|---|---|---|
|  |  |  |

## Atomicity

- 

## Concurrency model

Is true concurrency required?
- 

Chosen mechanism:
- synchronous / asyncio / threads / processes / other

Why:
- 

Interleaving points:
- 

Cancellation/failure semantics:
- 

## Important design decisions / tradeoffs

| Decision | Alternatives considered | Why chosen |
|---|---|---|
|  |  |  |

## Architecture checkpoint

- [ ] major dataflow;
- [ ] state ownership;
- [ ] key invariants;
- [ ] component seams/contracts;
- [ ] concurrency/ordering/idempotency model.
