# 30 mogri at runtime

This section describes how mogri is applied while a system is running.

It does not define mogri.
It applies mogri during operation.

---

## position

00 embed mogri   
10 machine spec   
20 evaluation   
   
30 runtime   
31 adjusting next step selection   
32 supporting functions   
33 constraints and recovery   

This is the point where mogri moves from description into use.

---

## runtime

A system produces outputs step by step.

At each step it considers several possible next states.

Runtime mogri acts at this point.

It adjusts how those options are treated before a choice is made.

---

## purpose

Systems tend to lose mogri during operation.

They:

* narrow into a single path
* reinforce identity at each step
* enter states that are hard to leave

This layer exists to prevent that.

---

## what is enforced

The runtime layer maintains:

* reversibility   
* non validating reachability   
* bounded optionality   
* connectivity   

These properties are defined earlier.

Here they are applied to step to step transitions.

---

## how it operates

At each step:

* the system proposes candidate next states
* each candidate has an associated preference
* preferences are adjusted
* a next state is selected from the adjusted set

This repeats continuously.

---

## scope

This applies to systems that:

* generate sequences
* choose between alternatives
* allow intervention at selection time

It does not require retraining.
It does not depend on a specific model type.

---

## relation to evaluation

Evaluation measures mogri after generation.

Runtime maintains mogri during generation.

Evaluation detects collapse.
Runtime reduces the chance of collapse.

---

## constraints and recovery

The runtime layer includes:

* detection of failure conditions
* simple interventions when they occur

If the system collapses or drifts:

* preferences are reshaped
* suppressed options are restored

No specific path is forced.
Only the ability to move is preserved.

---

## implementation note

In probabilistic systems, each step produces a distribution over next states.

Runtime mogri modifies this distribution before sampling.

In language models, this appears as modifying token scores before selection.

---

## limits

This layer preserves conditions for mogri.

It does not create mogri where none exists.

If all available options are already constrained, only limited recovery is possible.

---

## note

Mogri is independent of any system.

This is one way to maintain it where systems tend to lose it.

---
