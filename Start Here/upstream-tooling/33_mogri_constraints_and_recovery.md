# 33 mogri constraints and recovery

This section defines how failure is detected and how intervention is applied.

It operates during runtime.

---

## role

The runtime layer adjusts preferences continuously.

This section handles cases where adjustment is not sufficient.

It detects loss of mogri and applies correction.

---

## failure conditions

Failure occurs when movement is no longer viable.

Typical conditions include:

* identity lock
* directional lock
* collapse to a single dominant path
* diffusion into unstructured variation
* entry into dead end states

These conditions reduce or remove usable transitions.

---

## detection

Failure is detected from current signals.

Examples:

* one option dominates most of the preference
* distribution becomes extremely narrow
* distribution becomes near uniform without structure
* identity influence exceeds base transition cost
* continuation signals drop sharply

Detection is local and continuous.

---

## response

When failure is detected, intervention is applied.

Intervention does not force a specific outcome.

It reshapes the available options.

---

## recovery actions

Typical actions include:

* reducing dominance of the leading option
* increasing weight of suppressed alternatives
* flattening overly sharp distributions
* rebalancing overly diffuse distributions
* favouring options that restore connectivity

These actions restore the ability to move.

---

## constraints

Intervention is limited.

It must:

* preserve valid options
* avoid introducing arbitrary states
* avoid forcing identity
* maintain consistency with local structure

The goal is restoration of movement, not control of direction.

---

## persistence

Recovery is temporary.

Normal adjustment resumes once conditions return to range.

Repeated failure indicates upstream constraints.

---

## implementation note

In probabilistic systems, recovery modifies the current preference distribution.

This can be done by:

* rescaling values
* subtracting mean or peak bias
* boosting low preference options

In language models, this corresponds to modifying token scores before selection.

---

## limits

Recovery cannot create new structure.

If all available options are constrained or disconnected, recovery has limited effect.

Long term stability depends on the underlying system.

---

## relation

30 defines runtime context.
31 adjusts selection.
32 defines supporting functions.
33 detects failure and restores movement.

---
