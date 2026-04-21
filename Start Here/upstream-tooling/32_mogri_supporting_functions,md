# 32 mogri supporting functions

This section defines the functions used to apply mogri during operation.

These functions measure and adjust how a system moves between states.

---

## role

The runtime layer requires signals about:

* how reversible movement is
* how strongly identity is enforced
* how balanced the available options are
* how well states remain connected

These functions provide those signals.

---

## inputs

The functions operate on:

* candidate next states
* transition preferences or costs
* representations of current and candidate states
* identity signals derived from the current state

---

## core measures

Four measures are used.

---

### reversibility

Measures how similar forward and return transitions are.

If moving from A to B is easy but returning is difficult, reversibility is low.

High reversibility means movement does not trap the system.

---

### identity influence

Measures how much identity affects transitions.

If identity strongly increases or blocks access to certain states, influence is high.

Low influence allows entry into non validating states.

---

### option balance

Measures how evenly preference is distributed across candidates.

If one option dominates, balance is low.
If all options are equally weak or random, balance is also low.

Balance is highest in a middle range.

---

### connectivity

Measures whether states remain connected to the wider system.

If entering a state reduces future options or leads to dead ends, connectivity is low.

High connectivity preserves the ability to continue moving.

---

## combination

These measures are combined.

No single measure defines mogri.

A system has usable mogri when all measures remain within acceptable range.

---

## adjustment terms

From these measures, adjustment terms are produced.

Each term shifts candidate preferences:

* identity term reduces identity lock
* balance term maintains usable spread
* asymmetry term reduces dominance
* connectivity term preserves future paths

These terms are applied together.

---

## implementation note

In many systems, candidate preferences are numeric values.

These values can be adjusted directly.

In language models, this corresponds to modifying token scores before selection.

Reversibility and identity influence are approximated from local signals.

Option balance is derived from the current distribution.

Connectivity can be estimated from continuation signals or heuristics.

---

## limits

These functions are local.

They operate on the current step and nearby structure.

They do not compute full global properties of the system.

They provide practical approximations sufficient for runtime use.

---

## relation

30 defines runtime context.
31 applies adjustment at selection.
32 defines the functions used.
33 defines constraint detection and recovery.

---
