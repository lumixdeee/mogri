# Contributing: Scope, Boundaries, and How to Help

Thanks for your interest in contributing. This project welcomes builders, thinkers, testers, writers, artists, and code-warriors. It also has very explicit scope boundaries. Please read this before proposing features or integrations.

## What This Project Is

This kit is a meaning-first story and sense-making framework.

It is designed to work in domains where:
- experience precedes interpretation
- ambiguity is informative, not an error
- multiple readings can coexist
- structure matters more than final outcome
- human sense-making is part of the system

It acts as a compression and description layer, not a truth engine and not infrastructure.

---

## Where This Project Does Not Go

This framework intentionally does not operate directly inside domains that are:

- purely mechanical  
  (e.g. arithmetic, checksums, cryptographic primitives)

- fully constrained and deterministic  
  (e.g. protocols, encodings, clocked systems, state machines)

- optimised for precision over meaning  
  (e.g. formal verification, calibration, timing, proofs)

This is a design choice, not a missing feature.

Those domains already require guarantees (correctness, completeness, auditability) that this kit is not built to provide. Forcing a meaning-first framework into those spaces would:

- sterilise exploratory output
- collapse ambiguity prematurely
- convert play into liability
- create long-term maintenance and correctness obligations
- blur responsibility boundaries

In short: we do not claim authority where correctness must be absolute.

---

## Meaning vs Mechanism (ASCII Map)

```
                 ↑  Meaning / Interpretation
                 |
                 |   myth
                 |      theatre
                 |         waking-dreams
                 |            ritual
                 |               narrative systems
                 |                  ↑
                 |                  |  THIS KIT LIVES HERE
                 |                  |
-----------------+------------------------------------→ Mechanism / Determinism
                 |                  |
                 |                  |
                 |          protocols
                 |       encodings
                 |    checksums
                 | arithmetic
                 |
                 ↓
```

The kit lives above the line, where interpretation, experience, and structure matter.

Below the line, existing tools already do the job better and more safely.

---

## What You Can Contribute

Contributions are welcome in areas such as:

- framework primitives and extensions
- story domains and taxonomy (documentation-level)
- wake-dream and non-ordinary experience modeling
- narrative, theatrical, symbolic, or embodied mappings
- examples, case studies, and records
- documentation, diagrams, explanations
- tests of conceptual coherence (not correctness)
- critique and boundary stress-testing

If it helps humans describe experience more clearly without forcing conclusions, it probably fits.

---

## What Code-Warriors Are Invited To Build

Code-warriors are explicitly welcome to build downstream or adjacent tooling, including:

- visualisation layers
- dashboards and exploratory UIs
- educational or explanatory tools
- narrative wrappers around deterministic outputs
- playful or experimental compatibility layers
- simulations or sandboxes
- documentation generators

These should be:
- opt-in
- clearly non-authoritative
- framed as interfaces or lenses, not engines of truth

Bridges are encouraged.  
Collapse is not.

---

## What We Will Not Accept

We will not merge contributions that:

- claim correctness in mechanical domains
- replace or bypass formal verification
- present the framework as authoritative infrastructure
- imply automation supremacy over human judgement
- erase ambiguity in order to appear "rigorous"

This is not a refusal of rigor.  
It is rigor about scope.

---

## Why This Boundary Exists

Blurring meaning-driven systems with fully deterministic ones leads to predictable failure modes:

1. exploratory tools become brittle  
2. maintenance and audit costs explode  
3. humans get quietly displaced by their own abstractions  

This project exists to avoid all three.

---

## Related Documents

- Complete list of story domains and types  
- Wake-dream vs sleep-dream scope  
- Mogri as structural descriptor (not mechanism)  
- Framework kit components (primitives, faces, dragon kit, etc.)

These documents reference each other but remain modular.

---

If you’re unsure whether a contribution fits, open an issue and describe what domain it lives in and what kind of guarantees it expects. That’s usually enough to answer the question quickly and without drama.

Welcome, and thanks for building carefully.
