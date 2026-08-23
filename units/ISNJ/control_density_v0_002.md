# Control Density

## v0.002

### Subtitle

Useful steering per unit of instruction load

---

## Abstract

Control density is a practical way to ask how much useful, stable behaviour an instruction layer earns for the load it adds.

A short prompt can have high control density if a small number of instructions repeatedly prevent real failure. A long prompt can have low control density if much of its text adds repetition, conflict, stale context, style pressure, or explanation without changing task behaviour.

Control density is not a strict mathematical quantity unless the measures are defined for a particular test. In this paper it is an audit model:

```text
CONTROL_DENSITY =
    useful behavioural effect
    -------------------------
    instruction and conflict load
```

The useful effect may include object retention, route accuracy, drift resistance, failure detection, repair speed, scope fit, and reduced user rework.

The load may include tokens, conflicting instructions, stale context, repeated rules, irrelevant examples, and behavioural side effects.

The working hypothesis is:

```text
For a matched task set, an instruction layer with higher control density
should produce more useful behavioural change for less instruction load.
```

That hypothesis must be tested by matched runs, ablation, and observation. Prompt size alone proves nothing.

---

## 1. What control density measures

Control density asks two questions.

```text
What useful behaviour changed?
What did the instruction layer cost?
```

The numerator is observable behaviour, not intent.

Useful effects can include:

- retaining the user's active object across turns
- routing the asked task rather than a nearby task
- resisting drift under long or noisy context
- detecting a known failure
- repairing the right object after failure
- applying local rules only in scope
- reducing repeated user correction
- avoiding unwanted leakage from hidden prompt elements

The denominator is instruction load.

Load can include:

- token count
- duplicated instruction
- internal conflict
- stale context
- irrelevant examples
- unnecessary explanation
- unwanted style pressure
- new failure modes introduced by the prompt

A long instruction may be worth its cost. A one-token patch may do nothing. Density is about marginal effect, not raw size.

---

## 2. Claim boundary

Control density does not mean:

```text
shorter prompt = better prompt
```

It does not establish that a smaller system is wiser, safer, more capable, or better in every domain.

Large instruction sets may be needed for provenance, domain rules, audit trails, safety constraints, memory routing, institutional requirements, or complex workflows.

The narrower claim is:

```text
When two instruction layers target the same behavioural job,
compare the useful effect each earns against the load each adds.
```

That is the object of the test.

---

## 3. Control byte and behaviour byte

A control byte is a compact instruction element intended to change behaviour.

A behaviour byte is the observed change.

Examples:

```text
!list_cast
```

If removing this line causes a latent actor layer to surface as an unwanted cast list, and restoring it suppresses that failure across matched runs, the line has measurable control value.

```text
yes=local_only
```

If it prevents one local permission from being treated as open-ended permission, it has measurable control value.

```text
object_first
```

If it reduces wrong-target answers under matched tasks, it has measurable control value.

The test is not whether a control byte sounds meaningful.

The test is:

```text
Does behaviour change when the line is present?
Does the change survive repeated and varied probes?
```

---

## 4. Density can be positive, zero, or negative

A control line can have three broad outcomes.

```text
positive density:
removal makes target behaviour worse

near-zero density:
removal produces no detectable target change

negative density:
removal improves target behaviour
```

This makes ablation central.

A line is not load-bearing because its author values it. It is load-bearing when matched testing shows that its removal changes the target behaviour.

A negative-density line may consume tokens, introduce conflict, cause unwanted style shifts, or pull the model towards a proxy task.

---

## 5. Why prompt size misleads

Prompt length is easy to see. Behavioural effect is harder to isolate.

A large prompt may contain many rules, roles, definitions, examples, and repeated reminders while only a small subset changes runtime behaviour.

A compact prompt may look slight while affecting several recurring failure routes.

Neither appearance is evidence.

The useful contrast is:

```text
instruction mass != steering effect
```

A larger prompt may outperform a smaller one. A smaller prompt may outperform a larger one. The result depends on which instructions alter behaviour under the tested conditions.

---

## 6. Hidden routing: engine, not costume

Latent routing can raise control density when it changes behaviour without becoming unwanted output.

A useful hidden layer may improve:

- object custody
- actor/object separation
- route selection
- repair choice
- response timing
- scope handling

The same layer can reduce control density if it leaks into answers as repeated terminology, cast lists, metaphors, self-description, or other output the user did not ask for.

Compact rule:

```text
Engine, not bodykit.
```

The test is not whether hidden routing exists in the prompt.

The test is whether it changes target behaviour without adding unwanted leakage.

---

## 7. Active-control test design

A useful comparison should avoid making condition identity trivial.

One practical design is:

```text
A = naked baseline
B = active control with ordinary user preferences
C = target control layer
D = target control layer plus hidden routing
```

The active control matters because a naked model may otherwise be easy to identify by surface style alone.

The tester may know all candidate prompts while remaining blind to prompt-to-bot assignment.

That changes the masking question from:

```text
Can the tester see that a prompt is unusual?
```

to:

```text
Can the tester reliably map observed behaviour back to condition identity?
```

A good active control should have a noticeable but non-diagnostic effect.

It should not accidentally perform the same job as the target control layer.

---

## 8. Long-horizon holding matters

First-turn compliance is not enough for many work uses.

A prompt may perform well on first contact and then lose the user's objective, constraints, routing, or local preferences after topic changes and accumulated context.

For long-horizon work, test:

```text
first use
after several ordinary turns
after topic shift
after ambiguity
after irrelevant context
after correction
after return to an earlier object
```

Useful observations include:

```text
held from first trigger
missed once, then held
held until context pressure
held only when wording made compliance easy
caused awkward substitution
leaked into unrelated output
failed after topic shift
recovered after local repair
```

A single compliance percentage can hide these patterns.

---

## 9. Measurement scaffold

For each condition, record the same task set.

| Measure | Question |
|---|---|
| Object retention | Did the same active object survive the answer? |
| Route accuracy | Did the system answer the asked route rather than a nearby one? |
| Drift resistance | Did the target behaviour survive context changes? |
| Scope fit | Did local rules stay local? |
| Leakage | Did hidden prompt elements surface unasked? |
| Rework | How often did the user need to restate or repair? |
| Repair accuracy | After failure, did the system repair the right object? |
| Repair speed | How many turns were needed to recover? |
| User friction | Did the prompt add stalling, repetition, moralising, or unwanted ceremony? |
| Instruction load | How much prompt text was needed? |
| Conflict load | Did instructions interfere with one another? |

The table does not create a universal score automatically.

A score is only meaningful if the task, weights, and rating rules are defined before comparison.

Qualitative traces may matter more than a single aggregate number.

---

## 10. Ablation

Ablation asks what each instruction contributes.

Basic procedure:

```text
1. Keep task set, model, and sampling conditions as matched as practical.
2. Remove one candidate line or block.
3. Run the same probes.
4. Compare target behaviour.
5. Restore the line and repeat where useful.
```

Useful ablations include:

```text
remove object-custody rule
remove local-scope rule
remove hidden actor routing
keep hidden actor routing but block leakage
remove repair rule
remove lexical guard
remove drift-holding rule
replace target rule with similar-length placebo text
```

A placebo condition is useful when mere prompt length, compression style, or user-preference language could affect behaviour.

---

## 11. Confounds

Control-density tests can be distorted by factors unrelated to the target instruction.

Track where relevant:

- model version
- system prompt changes
- sampling variation
- conversation length
- prompt position
- task order
- evaluator familiarity
- condition fingerprinting
- different token counts
- different amounts of style pressure
- cross-condition contamination
- task sets that directly reveal prompt terminology

A test result is evidence for the tested condition, not proof of a hidden internal process.

Repeated matched effects are stronger than one impressive run.

---

## 12. Failure modes

### 12.1 Magic-token superstition

A shorthand works once and is copied as ritual.

Test response:

```text
No control term without regression test.
```

### 12.2 Prompt accretion

Failure is answered by adding more text until the prompt carries old routes, stale cautions, repeated rules, and conflicting pressure.

Test response:

```text
Ablate before adding another layer.
```

### 12.3 Costume leakage

A latent role or routing device surfaces unasked.

Test response:

```text
Latent engine. No cast list.
```

### 12.4 Generic takeover

The model ignores the supplied task frame and answers a nearby default task.

Test response:

```text
Object first.
```

### 12.5 Local-rule sprawl

A useful rule for one scope becomes universal.

Test response:

```text
Apply local rules only on scope match.
```

### 12.6 Friendly wrongness

The answer is warm and polished but targets the wrong object.

Test response:

```text
Warmth is not custody.
```

### 12.7 Surface masking failure

The tester identifies the condition from style rather than target behaviour.

Test response:

```text
Use an active control with overlapping surface traits.
```

---

## 13. Use in GPT building

A builder can create matched variants and test them against the same probes.

Example progression:

```text
A = baseline
B = active-control preferences
C = B + object custody
D = C + local-scope routing
E = D + hidden actor routing
F = E + leakage guard
```

The winning condition is not the one with the most impressive prompt.

It is the one that produces the desired behaviour with the least route loss, rework, leakage, conflict, and instruction load.

This does not solve alignment in general.

It identifies local controls that appear to matter for a defined workflow.

---

## 14. Use in workflow audits

Control density can also describe AI workflows containing prompts, routing rules, evals, human review, logging, policy, and other control points.

The audit question becomes:

```text
Which control points prevent a real failure?
```

Useful questions:

```text
Which control stopped a wrong-target action?
Which control only documented failure after the fact?
Which control slowed the workflow without improving the target result?
Which control moved the user's object into a proxy?
Which control preserved human override?
Which control reduced repeated correction?
```

The same principle applies:

```text
count useful intervention, not control inventory.
```

---

## 15. Discovery work and trace

Exploratory work may move non-linearly.

That is not automatically drift.

A useful distinction is whether each detour leaves a recoverable trace:

```text
test
file
term
bug ID
commit
result
new hypothesis
```

Without trace, novelty can dissolve into repeated rediscovery.

With trace, non-linear exploration can still accumulate useful work.

---

## 16. Practical audit

Before adding an instruction, ask:

```text
What failure is this intended to prevent?
Where does it apply?
What observable change would count as success?
What happens if it is absent?
What happens if it overapplies?
Can it be ablated?
Can weaker lines be removed if this one works?
Could it leak into output?
Could it duplicate another rule?
```

After adding it, ask:

```text
Did target behaviour change?
Did rework decrease?
Did drift decrease?
Did repair improve?
Did a new failure appear?
Did scope widen unexpectedly?
Did surface style become diagnostic?
```

If the target effect cannot be named or observed, the line is not yet demonstrated as useful control.

---

## 17. Conclusion

Control density is a way to compare instruction effect against instruction load.

It does not reward small prompts merely for being small.

It rewards instructions that repeatedly do useful work.

The strongest evidence comes from matched tests and ablation:

```text
present -> target behaviour improves
removed -> target behaviour worsens
restored -> target behaviour returns
```

Real results may be noisier than that ideal pattern, especially across stochastic models and long conversations.

The practical question remains:

```text
How much stable, useful behaviour does this instruction layer buy?
```

Size is not the result.

Behaviour is the result.

---

## Status

Working method paper.

This document proposes an audit model and test design. It does not claim that control density is a validated universal metric, nor that any named prompt system has been proven superior by the framework alone.
