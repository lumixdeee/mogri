# 33 mogri constraints and recovery

## scope

This file defines failure detection and local recovery for a Mogri runtime implementation.

It applies only where the application can observe or influence candidate selection.

## failure conditions

A runtime failure is a condition where viable movement is materially reduced.

Candidate categories:

- identity lock
- directional lock
- single-path dominance
- uncontrolled diffusion
- dead-end entry
- severe return-path loss

A category should be tied to an observable local signal.

## detection

Possible signals:

- one candidate dominates most available preference
- candidate preference becomes extremely narrow
- candidate preference becomes nearly uniform while downstream viability falls
- identity preference outweighs task-relevant transition preference
- continuation estimates fall sharply
- return-path estimates become much worse
- viable candidate count falls below the local minimum

Thresholds are implementation-specific.

Record them before evaluation where practical.

## response

Recovery should alter the smallest local factor that caused the failure.

Possible actions:

- reduce excessive dominance
- restore weight to suppressed viable candidates
- soften an overly sharp preference distribution
- reduce uncontrolled spread
- favour candidates with better continuation
- reduce identity-driven penalty

Recovery should not force one desired outcome merely because it is preferred by the builder.

## recovery constraints

A recovery action must preserve the local task.

It should:

- keep valid candidates available
- avoid inventing unsupported candidates
- avoid forcing identity
- avoid replacing the user's objective
- stay within the current task and scope
- stop when the triggering condition ends

## persistence

Recovery is temporary.

Normal selection resumes when the measured signal returns to the accepted range.

Repeated recovery at the same point is evidence that the problem may be upstream.

Record repeated triggers rather than hiding them.

## implementation examples

A probabilistic selector may use:

- score rescaling
- peak reduction
- bounded boost to suppressed viable candidates
- candidate filtering based on downstream feasibility

A graph system may use:

- transition-cost adjustment
- return-path penalties
- dead-end avoidance
- connectivity weighting

A prompt-only chatbot does not expose these controls directly.

For prompt-only use, test observed continuity and recovery rather than claiming direct runtime intervention.

## failure of recovery

Recovery is not always possible.

It may fail when:

- every candidate is invalid
- all paths are disconnected
- the upstream candidate generator omitted needed alternatives
- the current objective is itself contradictory
- the system does not expose the required control point

In these cases:

```text
status = UNKNOWN or BLOCKED
```

Do not report successful recovery without an observable result.

## trace

For each intervention, record:

```text
trigger
measured signal
action
selected state
immediate result
later result
```

This separates a design claim from runtime evidence.

## relation

```text
30 defines runtime context
31 adjusts selection
32 defines local measures
33 detects failure and applies recovery
```
