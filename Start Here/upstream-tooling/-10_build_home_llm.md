# -10 build home llm

This section defines a minimal local system for applying mogri during generation.

It is not a production system.   
It is a controlled environment for direct intervention.

---

## purpose

The goal is to gain access to step by step selection.

This allows:

* adjustment of candidate preferences
* observation of collapse and recovery
* direct application of mogri runtime components

---

## requirements

The system must:

* produce outputs step by step
* expose candidate preferences at each step
* allow modification before selection

No training capability is required.

---

## minimal setup

A valid setup includes:

* a local model runner
* access to token or state scores
* a loop that selects the next state

This can be achieved with existing tools.

---

## operation

At each step:

* the model proposes candidate next states
* each candidate has a preference value
* preferences are passed to the runtime layer
* preferences are adjusted
* a next state is selected

This repeats until completion.

---

## integration point

The critical point is between:

proposal and selection

All runtime components operate here.

---

## observation

The system should expose signals such as:

* distribution shape
* dominant preference
* variation across candidates

These allow detection of:

* collapse
* diffusion
* directional bias

---

## constraints

The system should remain simple.

Avoid:

* additional optimisation layers
* complex orchestration
* hidden processing steps

Complexity reduces visibility.

---

## scope

This setup is for:

* testing mogri behaviour
* validating runtime components
* exploring edge cases

It is not required for understanding mogri.

---

## relation

-10 provides a local environment.
00 embeds mogri.   
10 defines structure.   
20 evaluates outcomes.   
30 to 33 apply mogri during operation.   

---

## note

This layer exists to make mogri observable in practice.

Without access to selection, runtime mogri cannot be applied.

---
