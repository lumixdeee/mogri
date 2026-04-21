# -09 minimal loop

This defines the smallest loop where mogri can be applied.

No tooling is required.   
Only the structure of selection.

---

## loop

Repeat:

* produce candidate next states
* assign a preference to each candidate
* adjust preferences
* select one candidate
* update current state

---

## key point

Adjustment occurs before selection.

If selection happens first, mogri cannot act.

---

## inputs

At each step:

* current state
* candidate next states
* preference values

Optional:

* identity signal
* continuation signals

---

## adjustment

Preferences are modified using runtime components.

This includes:

* reducing identity lock
* maintaining balanced options
* limiting dominance
* preserving connectivity

---

## selection

One candidate is chosen from the adjusted set.

This becomes the next state.

---

## observation

At each step it is possible to observe:

* how concentrated the preferences are
* whether alternatives remain viable
* whether movement remains reversible

---

## minimal condition

Mogri is possible if:

* at least one candidate does not reinforce identity
* that candidate is not a dead end

If not, the loop collapses.

---

## scope

This loop applies to any system that:

* proposes alternatives
* selects one outcome at a time

It is independent of implementation.

---

## relation

-09 defines the minimal structure.   
-10 defines a local system.   
30 to 33 define runtime behaviour.   

---
