# 32 mogri supporting functions

## scope

This file defines local measures for a Mogri runtime implementation.

These measures apply only when the system exposes candidate states, transition preferences, or equivalent routing signals.

They are not claims about inaccessible model internals.

## inputs

Possible inputs:

- current state
- candidate next states
- transition preference or cost
- return-path estimates
- identity-related preference signals
- continuation estimates

## 1. reversibility

Question:

```text
If the system moves from A to B, how costly is a return from B towards A or an equivalent prior region?
```

Low reversibility means movement tends to trap the system.

Possible local measure:

```text
reversibility(A,B) = compare(cost(A->B), estimated_return_cost(B->A))
```

The exact function depends on the application.

## 2. identity influence

Question:

```text
How much does identity preference alter access to otherwise viable candidates?
```

High identity influence may appear when candidates are penalised mainly because they do not preserve a current identity label.

Measure only signals that the application can observe.

## 3. option balance

Question:

```text
Is preference concentrated into one option, or dispersed so widely that selection becomes arbitrary?
```

Useful optionality sits between:

```text
single-path dominance
and
undirected diffusion
```

No universal numeric threshold is assumed.

## 4. connectivity

Question:

```text
Does this candidate preserve access to useful future states?
```

Low connectivity may appear as:

- dead ends
- severe loss of future options
- one-way transitions
- repeated inability to return to viable regions

Connectivity can be exact in a known graph or estimated in a local system.

## combining measures

No single measure is sufficient.

A runtime may combine them into an adjustment signal:

```text
adjustment =
    reversibility_term
  + identity_term
  + option_balance_term
  + connectivity_term
```

Weights and thresholds are local design choices.

They should be stated, tested, and ablated.

## adjustment terms

Possible jobs:

- identity term: reduce identity-driven lock
- option term: reduce single-option dominance or uncontrolled spread
- reversibility term: penalise severe one-way movement
- connectivity term: favour candidates with viable continuations

Each term should have a known target failure.

## implementation examples

In a graph system:

```text
candidate states and transition costs may be explicit
```

In a planner:

```text
candidate actions and downstream feasibility may be estimated
```

In a language-model application with exposed logits:

```text
candidate token or action scores may be adjusted before selection
```

In a normal chat interface:

```text
these signals are not directly available
```

Use behavioural tests instead of claiming hidden measurements.

## limits

Local estimates do not guarantee global behaviour.

A candidate can look viable locally and still fail later.

A runtime implementation should therefore preserve traces of:

- input state
- candidate set
- measured signals
- applied adjustment
- selected next state

That trace allows later comparison and ablation.

## relation

```text
30 defines runtime context
31 applies selection adjustment
32 defines local measures
33 detects failure and applies recovery
```
