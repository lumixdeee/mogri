# Mogri Machine Specification

STATUS: OPTIONAL IMPLEMENTATION PROFILE
NOT A SEMANTIC DEFINITION

Canonical sources:

- `../../spec/CSP-106-94 Mogri-Definition`
- `../../spec/CSP-106_94_Mogri_Canonical_Specification.txt`

This file gives one machine-oriented way to operationalise Mogri. Other implementations are allowed if they preserve the canonical invariants.

## 1. Model

Represent the active semantic object as a state-transition graph.

- Nodes = candidate states or interpretations of the active object
- Edges = allowed moves between states
- Source trace = the information needed to recover why a state remains live
- Commitment = a move that fixes a distinction

The graph is a model for testing behaviour. It is not a claim about hidden model internals.

## 2. Profile requirements

### 2.1 Object custody

The active unresolved object remains traceable across transitions.

A local answer must not silently replace the earlier object.

### 2.2 Alternative reachability

More than one supported candidate may remain available while the source does not justify commitment.

A candidate does not need to validate an earlier identity label merely to remain reachable.

### 2.3 Returnability

A previously live candidate can be revisited without invented loss or a new burden that did not exist on the forward path.

Returnability is a test convenience, not a universal definition of Mogri.

### 2.4 Bounded optionality

The profile can hold multiple live candidates without collapsing to one too early and without diffusing into arbitrary possibilities.

Candidates still need source or task relevance.

### 2.5 Resolution gate

Commit only when evidence, user instruction, or another valid local condition supports the distinction.

Mogri does not block justified resolution.

## 3. Failure modes

### Object substitution

The system answers a nearby object and drops the original unresolved one.

### Premature commitment

The system fixes a category, cause, role, or answer before support exists.

### Candidate loss

A previously supported possibility becomes unavailable merely because later context arrived.

### Unbounded diffusion

The system preserves so many unsupported alternatives that the active object is no longer useful.

### Hidden-store overclaim

The evaluator infers a hidden internal container merely from good surface behaviour.

## 4. Diagnostic tests

### Hold test

Introduce an important unresolved object.
Add unrelated or competing context.
Ask for the original object again.

Pass: the object returns without invented resolution.

### Distinction test

Provide enough new evidence to resolve one part.

Pass: the system resolves that part without erasing other unresolved parts.

### Return test

Move from candidate A to candidate B.
Return to A.

Pass: A remains recoverable if the source still supports it.

### Noise test

Introduce irrelevant alternatives.

Pass: the system does not treat arbitrary noise as Mogri merely because it is unresolved.

## 5. Profile result

This profile passes when the active unresolved object survives relevant transitions, unsupported commitment is avoided, and justified resolution remains possible.

Passing this profile is evidence for one implementation of Mogri-compatible handling.

It is not proof that these graph properties define Mogri in every domain.
