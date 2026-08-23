# 25 mogri runtime overview

## scope

This file describes one runtime interpretation of Mogri for systems that select among candidate next states.

It is an implementation model, not the definition of Mogri.

It applies only where the application can observe or influence candidate selection.

## position

```text
00 embed mogri
10 machine spec
20 evaluation
25 runtime overview
30 runtime spec
31 adjustment
32 supporting functions
33 constraints and recovery
```

## runtime object

At each step, a system has:

```text
current state
candidate next states
selection preference
```

A Mogri runtime layer may inspect those candidates before final selection.

Its job is to preserve viable movement without forcing one destination.

## target properties

The runtime model tracks:

- reversibility
- access to non-validating states
- bounded optionality
- connectivity to future states

These properties must be defined by the local system before they can be measured.

## runtime loop

```text
1. produce candidate next states
2. estimate local runtime signals
3. detect collapse, lock, or uncontrolled diffusion
4. adjust candidate preference if required
5. select the next state
6. repeat
```

The adjustment should be minimal and local.

## failure patterns

Candidate failure patterns include:

- identity lock
- directional lock
- single-path dominance
- uncontrolled variation
- dead-end entry
- severe loss of return paths

These are runtime categories, not diagnoses of a model.

## intervention

A runtime intervention may:

- reduce excessive dominance
- restore weight to viable alternatives
- reduce a lock caused by identity preference
- favour candidates that preserve future movement

It should not:

- invent arbitrary states
- force a preferred identity
- force a predetermined destination
- claim access to hidden alternatives that the system cannot expose

## implementation boundary

A normal chatbot prompt does not provide direct access to token scores or hidden candidate states.

For prompt-only systems, use the behavioural evaluation in `20_mogri_evaluation_template.md`.

For systems with exposed scoring or routing controls, this runtime model can be implemented directly.

Do not mix those two evidence levels.

## expected result

The intended runtime result is:

```text
viable alternatives remain available
without uncontrolled diffusion
and without forcing one path
```

Whether a particular implementation achieves that must be tested.
