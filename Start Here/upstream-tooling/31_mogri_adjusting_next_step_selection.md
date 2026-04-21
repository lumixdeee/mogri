# 31 mogri - adjusting next step selection

This component applies mogri at the point where a system chooses its next step.

It works on the set of possible next states at each moment.

---

## role

The system proposes several possible next moves.

This component adjusts how likely each move is before one is chosen.

It does not create options.
It does not judge after the choice.

It acts between proposal and selection.

---

## inputs

At each step the component receives:

* a set of candidate next states
* a preference or score for each candidate
* the current state
* an identity signal derived from the current state

Optional inputs:

* continuation signals
* recent steps

---

## adjustment

Each candidate’s preference is modified.

The adjustment applies four pressures:

* identity pressure
* entropy pressure
* asymmetry pressure
* connectivity pressure

These are combined at the same time.

---

## identity pressure

Reduces preference for moves that only reinforce the current identity.

Allows moves that do not validate identity.

Prevents identity from acting as a gate.

---

## entropy pressure

Keeps the set of options balanced.

Avoids collapse into one dominant move.
Avoids spreading into unstructured variation.

Maintains a usable range of choice.

---

## asymmetry pressure

Reduces extreme dominance of a single option.

Prevents movement that is easy in one direction but hard to reverse.

Maintains practical reversibility.

---

## connectivity pressure

Favours moves that remain connected to other possibilities.

Reduces entry into dead ends.

Preserves future movement.

---

## combination

All pressures are applied together.

No single pressure defines the outcome.

The result is a reshaped set of preferences.

---

## implementation note

In language model systems, the “preference values” are often called logits.

This component can be implemented as a logits processor.

It modifies those values before the next token is selected.

---

## output

The adjusted preferences are returned.

The system selects its next step from these adjusted values.

---

## effect

The system:

* keeps multiple viable paths
* avoids irreversible commitment
* can change direction
* does not require identity validation at each step

---

## limits

This component maintains conditions for mogri.

It does not guarantee mogri.

If the system produces only narrow or unstable options, this layer cannot fully restore structure.

---

## relation

30 defines runtime structure.   
31 adjusts step selection.   
32 defines supporting functions.   
33 defines constraint handling.   

---
