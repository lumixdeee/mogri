# On Renaming Mogri

Mogri is not tied to the spelling `Mogri`.

The functional job can survive a rename if the replacement label does not collide with another active job.

## Naming requirement

Prefer an identifier that is:

- unused in the local prompt
- short
- stable
- easy to trace
- unlikely to be reinterpreted as a role, entity, variable, or task instruction

Avoid labels that already carry another active job.

Examples of risky choices:

- a human name, if people or agents are active in the task
- a company name, if business context is active
- a programming term already used by the system
- a descriptive phrase that can be read as a new instruction

The goal is low collision.

## Identifier versus definition

This is an identifier:

```text
Mogri
```

This is a definition:

```text
minimal pre-container preserving important unresolved potential
```

Do not confuse the two jobs.

A descriptive phrase can work as a definition while being a poor identifier.

Long descriptive identifiers also add token load and invite local reinterpretation.

## Matching the framework name

Renaming Mogri to match the surrounding framework increases coupling.

Example:

```text
[Meridian] = ...
```

Possible benefit:

- stronger local association

Possible cost:

- the identifier now carries task-specific meaning
- the container can be mistaken for its content
- later domain changes can alter how the label is read

Mogri is intended to remain separable from the content it holds.

## A reversible rename

`Irgom` is a simple reversible alternative:

```text
Mogri -> Irgom
```

It preserves traceability to the original term while reducing direct lexical carry-over.

It is only an example, not a required replacement.

## Recoverability

The useful requirement is not historical etymology.

The useful requirement is recoverability:

- can the identifier be traced back to the same primitive?
- can renamed instances be compared?
- can the definition remain stable when the label changes?

A rename succeeds when the job remains the same and collisions do not increase.

## Test

Do not assume two labels are equivalent because their definitions look equivalent.

Run matched tasks.

Compare:

- intent retention
- unresolved-object retention
- drift
- leakage of the identifier into output
- accidental binding to roles or entities
- user correction required

If the renamed condition behaves materially differently, the rename changed more than the label.

## Summary

```text
name is replaceable
job is not

prefer low-collision identifiers
keep identifier separate from definition
keep container separate from content
test equivalence behaviourally
```
