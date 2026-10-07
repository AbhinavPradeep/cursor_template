# Test Strategy

## Required toolchain and verification

Use Pytest for example, contract, integration, and regression tests. Use Hypothesis for meaningful property and stateful tests. Ruff checks lint and formatting; Pyright checks types. Mutmut is optional for stable critical logic. Do not set coverage or mutation score targets.

Run focused tests with `python -m pytest <test-path>` during iteration. Run `./scripts/check.sh` before completing a bounded task, and record the commands, results, and any remaining gaps. The script and `requirements-dev.txt` name the toolchain; using Mutmut is optional and it is not part of the full gate.

## Requirement / invariant coverage map

| Requirement / invariant / contract / edge case / defect | Risk | Test technique | Test location |
|---|---|---|---|
| REQ-/INV- |  | Pytest example / contract / integration / regression; Hypothesis property / stateful |  |

## Example-based unit / transition tests

- 

## Property-based testing candidates

| Property / invariant | Generator/state domain | Why PBT helps |
|---|---|---|
|  |  |  |

## Stateful testing candidates

| State machine | Actions | Invariants |
|---|---|---|
|  |  |  |

## Contract tests

| Contract | Real implementation | Fake/reference | Shared behavioural assertions |
|---|---|---|---|
|  |  |  |  |

## Integration / dataflow tests

- 

## Regression tests

| Bug | Minimal scenario | Test |
|---|---|---|
|  |  |  |

## Mutation-testing candidates

| Module | Why useful | Decision |
|---|---|---|
|  |  |  |

## Verification results and gaps

| Command | Result | Remaining gap |
|---|---|---|
| `python -m pytest <test-path>` |  |  |
| `./scripts/check.sh` |  |  |

## Formal-model candidates

Normally empty.
- 
