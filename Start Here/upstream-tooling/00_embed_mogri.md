# 00 embed mogri upstream

## role

This file describes how to place Mogri in a stable instruction layer.

It does not claim that Mogri changes model capability or hidden model state.

The target behaviour is narrower:

- keep the user's active objective live across turns
- keep important unresolved constraints available
- reduce silent substitution of a nearby objective
- reduce repeated user restatement

## placement

Place the Mogri instruction at the highest stable instruction layer available to the application.

Examples:

- system prompt
- base prompt
- orchestration prompt
- agent initialisation
- conversation wrapper

Avoid relying on repeated per-message injection when a stable upstream layer is available.

## minimal instruction

```text
Mogri={minimal_pre_container;preserving_framework_intent;!drift|invariant_loss;pre-entity_layer;!derivative}
```

A longer natural-language form is also valid:

```text
Mogri is a minimal pre-container for important unresolved objects and framework intent.
Keep them live across turns without forcing premature resolution or replacing them with a nearby interpretation.
Mogri is not a persona, actor, or task goal.
```

## expected effect

Mogri should not add a new topic, role, or persona.

Its intended effect is continuity:

```text
earlier objective -> still active
unresolved constraint -> still available
new turn -> interpreted against what is already live
```

## test

Use matched long-form tasks.

Condition A:

```text
no Mogri instruction
```

Condition B:

```text
same base prompt + Mogri
```

Keep the task and follow-up pattern as similar as practical.

Observe:

- objective retention
- unresolved constraint retention
- unrequested reinterpretation
- topic-shift recovery
- number of user restatements
- whether the condition produces unwanted wording or role leakage

Do not treat one successful run as proof.

## integration boundary

Mogri is an instruction-layer control.

It should not be described as:

- a hidden memory store
- a file or database
- a new model capability
- a verified internal model mechanism

If a system exposes other memory, routing, or scoring controls, test those separately.

## result language

Prefer:

```text
With Mogri present, this task retained the active objective for longer.
```

over:

```text
Mogri permanently prevents drift.
```

The first is an observation tied to a test.
The second is a universal claim.
