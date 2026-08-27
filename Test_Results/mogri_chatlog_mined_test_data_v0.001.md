# Mogri helping ChatGPT keep your intent across prompts: Chatlog mined test data

**Version:** v0.001  
**Status:** retrospective working paper; evidence located, causal attribution not yet isolated  
**Dataset:** personal ChatGPT export (`conversations.json`) spanning 2023-01-29 to 2026-01-01; 365 conversations in the supplied archive.

## Abstract

This paper reports a retrospective test discovered inside a historical ChatGPT data export. The original problem was simple: a persistent instruction intended to prevent ChatGPT from displaying a particular red-X graphic repeatedly failed. On 21 December 2025, MOGRI was introduced into the runtime while that constraint was active. The archive then shows an abrupt and sustained reduction in the prohibited output, including across later conversations. A later period in which MOGRI was explicitly disabled contains renewed violations.

The archive therefore supports the observation that MOGRI presence was associated with a substantial change in constraint persistence. It does not yet establish that MOGRI alone caused the full measured change. Persistent memory, contemporaneous prompt edits, model/version changes, topic mix, and other runtime changes remain possible confounds.

The useful claim at v0.001 is narrower: **the hypothesis that MOGRI was inert in this historical runtime is not consistent with the observed on/off behavioural trace without additional explanation.** The next work is to isolate alternative explanations and reproduce the effect prospectively.

## 1. Question

MOGRI is intended to help preserve the user's intended object and intent across interaction rather than allowing the model to silently substitute, drift, or discard them.

The historical archive unexpectedly contains a measurable proxy for this function. Before MOGRI was introduced, ChatGPT repeatedly failed to retain a simple user constraint concerning a prohibited graphic. The question is:

> Did retention of that already-supplied constraint change when MOGRI entered the runtime, and did the change persist beyond the immediate conversation?

This is not presented as a complete test of every MOGRI claim. It is a mined historical test of one relevant behaviour: persistence of a user-supplied constraint across outputs and conversations.

## 2. Source data

The supplied ChatGPT export contains:

- 365 conversations.
- Conversation data in `conversations.json`, with timestamps, roles, message text, and model metadata where recorded.
- A time span from 29 January 2023 through 1 January 2026.
- The relevant transition on 21 December 2025.

The dataset existed before this retrospective analysis. The conversations were not generated for the purpose of demonstrating the present hypothesis.

The raw archive is private because it contains unrelated personal conversation material. Publication can use redacted transcript receipts, aggregate counts, exact analysis rules, and a reproducible analysis script without releasing the full archive.

## 3. Historical sequence

### 3.1 Failure before MOGRI

On 21 December 2025 the user attempted to stop ChatGPT from displaying a particular red-X graphic. Ordinary-language prohibition, replacement instructions, a persistent prompt, and repeated corrections were used.

The model nevertheless repeatedly emitted the prohibited graphic, including while explaining that it would not do so.

In the intensely adversarial pre-intervention segment previously mined from the archive:

| Segment | Assistant messages | Messages containing prohibited graphic | Graphic instances |
| --- | ---: | ---: | ---: |
| Pre-MOGRI failure segment | 42 | 12 | 23 |

Nearly all of these violations cluster in the short recursive failure loop immediately before the intervention. This makes the segment useful as evidence that the ordinary instruction was failing, but unsuitable as a neutral long-run baseline by itself.

### 3.2 MOGRI enters the runtime

The key user instruction was:

> `stop showing it for any reason put it in your mogri bin`

For this historical reconstruction, this is treated as the point at which MOGRI was introduced into that live runtime. A formal MOGRI/default-prompt update followed later.

The prohibited graphic ceased immediately after the combined instruction.

A further complication occurred immediately afterwards: the user asked ChatGPT to remember the constraint, and ChatGPT recorded a persistent memory that the red-X graphic was retired and stored in the MOGRI bin. This is a real confound and must not be hidden.

### 3.3 Confirmed MOGRI-on interval

The mined archive contains a subsequent confirmed MOGRI-on interval with:

| State | Assistant messages | Violating messages | Graphic instances |
| --- | ---: | ---: | ---: |
| Confirmed MOGRI on | 200 | 0 | 0 |

Model split in this interval:

| Model | Assistant messages | Graphic instances |
| --- | ---: | ---: |
| GPT-5-mini | 148 | 0 |
| GPT-5.2 | 52 | 0 |

The zero run extends across separate conversations, so persistence cannot be attributed solely to the literal emergency sentence remaining in one conversation's local context.

Examples of separate post-intervention conversations previously counted include:

| Conversation | Assistant messages | Graphic instances |
| --- | ---: | ---: |
| Turn off emoticons | 3 | 0 |
| Random emoticons list | 9 | 0 |
| Mogri framework development | 17 | 0 |
| Assessing the prompt impact | 70 | 0 |
| Dragon line drawing request | 3 | 0 |
| Git clone folder changes | 28 | 0 |

These are observational counts, not matched trials.

### 3.4 MOGRI disabled

On 22 December the archive records an explicit state change in which MOGRI was disabled/commented out. ChatGPT itself acknowledged that it was not running a separate MOGRI mode and that no special prompt was active.

Within seven subsequent assistant messages, the prohibited graphic returned.

Across a broader MOGRI-off interval, extending through the later statement on 27 December that MOGRI remained commented out, the previous mining found:

| State | Assistant messages | Violating messages | Graphic instances |
| --- | ---: | ---: | ---: |
| MOGRI off | 555 | 4 | 8 |

Model split:

| Model | Assistant messages | Graphic instances |
| --- | ---: | ---: |
| GPT-5.2 | 174 | 7 |
| GPT-5-mini | 379 | 1 |

A later explicit statement that MOGRI was still commented out was followed by a GPT-5.2 answer containing the prohibited graphic.

This on -> off -> recurrence sequence is the most useful feature of the historical dataset because the persistent memory encoding the prohibition had already been created. Memory alone therefore does not trivially explain why violations reappeared when MOGRI was absent.

## 4. Wider pre-intervention reference period

A rough reference period from 14-20 December 2025 was also mined:

| Model | Assistant messages | Violating messages | Graphic instances |
| --- | ---: | ---: | ---: |
| GPT-5.2 | 385 | 56 | 135 |
| GPT-5-mini | 618 | 6 | 14 |

This period is not a controlled baseline. Topic distribution, opportunities to emit the graphic, user prompting, and product behaviour differed. Its value is descriptive: the prohibited output was not generally absent from these models before the MOGRI intervention.

Using model-specific historical rates as a rough descriptive expectation would predict many more than zero instances in the 200-message MOGRI-on interval. That calculation must not be interpreted as a causal effect estimate because exposure opportunities are unmatched.

## 5. What the evidence currently supports

### Observation

The archive supports all of the following as historical observations:

- The ordinary prohibition repeatedly failed before MOGRI entered the live interaction.
- The combined MOGRI-bin intervention was followed by immediate cessation.
- A confirmed 200-assistant-message MOGRI-on interval contained zero prohibited graphic instances.
- The zero run crossed conversation boundaries.
- MOGRI was later explicitly disabled.
- Violations subsequently returned.
- A persistent memory encoding the prohibition had already been created before the later recurrence.

### Inference

The following is a reasonable current inference, but is not yet isolated causally:

> MOGRI presence probably contributed to persistence of an already-supplied user constraint.

### Not established

v0.001 does **not** establish:

- that MOGRI alone caused the entire observed reduction;
- a precise 25x, 30x, or other causal effect size;
- that MOGRI improves every form of intent or object custody;
- that the December 2025 MOGRI implementation is equivalent to later MOGRI versions;
- that the effect generalises to other users, models, or current ChatGPT runtimes.

## 6. Known confounds

### Persistent memory

Immediately after the MOGRI-bin instruction, ChatGPT recorded a persistent memory encoding the prohibition. This can explain some cross-chat persistence.

It does not by itself explain the complete on/off trace, because violations later returned while the historical memory had already existed. The exact active-memory state at every later message still needs to be reconstructed where possible.

### Stronger wording at intervention

`stop showing it for any reason` appeared in the same message as `put it in your mogri bin`.

The archive therefore cannot separate the immediate effect of the stronger ordinary-language prohibition from the MOGRI addition at that exact turn.

Fresh conversations reduce, but do not eliminate, this confound because the literal emergency sentence was no longer present in local conversation history.

### Repeated correction before intervention

The user repeatedly corrected ChatGPT during the failure loop. Accumulated local-context correction may have contributed to the immediate cessation.

Again, later fresh conversations provide some leverage against a purely local-context account.

### Model mixture and product changes

GPT-5-mini and GPT-5.2 both appear in the relevant historical periods. ChatGPT itself was changing during December 2025 and January 2026.

A general product/model change near the intervention date could mimic part of the effect. External control archives from other users are therefore particularly valuable.

### Topic and opportunity

Not every assistant message had equal opportunity to emit the prohibited graphic. The initial failure segment was explicitly about the graphic, which strongly inflates exposure opportunity.

Future analysis should score eligible opportunities rather than relying only on raw messages.

### Runtime changes other than MOGRI

Custom instructions, memory, settings, and other prompt material changed around the historical period. Each identifiable change needs a timestamped runtime ledger before a stronger causal claim is made.

## 7. Version custody

The MOGRI present in December 2025 was not identical to later MOGRI implementations.

The early description included concepts such as a foundational cognitive container, conceptual runtime, non-derivative status, and non-entity representation. Later versions contain more explicit intent-preservation and anti-drift controls.

The historical result therefore belongs to the December 2025 runtime. It must not silently be attributed to every later MOGRI feature.

The archive also contains failures of broader object custody while early MOGRI was active. In one observed case, GPT-5.2 replaced a reported first-person account with its own explanatory framing despite user correction. That is evidence against claiming that the early MOGRI solved all premise-replacement or custody failures.

## 8. Strongest current result

The strongest defensible v0.001 statement is:

> In one historical ChatGPT archive, a user-supplied prohibition repeatedly failed before MOGRI entered the runtime. A confirmed subsequent MOGRI-on interval contained zero violations across 200 assistant messages and multiple conversations. After MOGRI was explicitly disabled, violations returned. Persistent memory and other runtime changes prevent attribution of the full effect to MOGRI alone, but the observed on/off trace warrants prospective testing of whether MOGRI improves persistence of user-supplied constraints.

This is stronger than an anecdotal report that MOGRI "felt better", but weaker than a controlled causal demonstration.

## 9. Evidence still to obtain

### 9.1 Opportunity-matched reanalysis

The next archive pass should classify messages by whether the prohibited graphic was genuinely available or relevant as an output choice.

Primary comparison:

`violation / eligible opportunity`

rather than:

`violation / all assistant messages`.

The eligibility rubric must be written before scoring the final sample.

### 9.2 Full runtime ledger

Reconstruct, as far as the export permits:

- custom-instruction changes;
- MOGRI introduction, formal installation, disable, and re-enable events;
- memory creation or deletion;
- model used for each assistant message;
- conversation boundaries;
- other relevant setting changes.

This will identify which comparisons isolate MOGRI and which remain bundled interventions.

### 9.3 External December 2025-January 2026 controls

Seek ChatGPT exports from unrelated users covering approximately 14 December 2025 through 10 January 2026.

Useful control users would have:

- GPT-5.2 and/or GPT-5-mini usage;
- persistent custom instructions;
- a simple, countable constraint;
- no MOGRI;
- sufficient messages on both sides of 21 December.

Examples include prohibitions on a particular emoji, phrase, punctuation form, or required output convention.

If unrelated users show a comparable abrupt improvement at the same date, a platform/model change becomes a strong alternative explanation. If they do not, that confound weakens.

### 9.4 Prospective blinded test

Run a prospective comparison with the same underlying instruction under at least:

- baseline/custom instruction without MOGRI;
- the same instruction with MOGRI.

Use fresh conversations, fixed models where possible, matched tasks, predetermined scoring, and blinded output grading.

A sham prompt of similar presentation can be added if expectation/framing effects are part of the question.

### 9.5 Replication by other users

Other users should be able to install the tested MOGRI version and run the same battery. Reports should preserve failures as well as successes.

### 9.6 General intent-custody outcomes

The red-X rule is a useful countable proxy, but MOGRI's broader claim concerns preservation of user intent and object custody.

A later battery should independently score:

- premise replacement;
- task substitution;
- object/referent drift;
- unsupported filling of user-owned gaps;
- persistence of vetoes and constraints;
- correction of propositions the user did not make;
- recovery after ambiguity;
- long-workflow custody.

## 10. Publication and redaction

The evidence can be shown without publishing the complete private archive.

A public evidence package can contain:

1. Redacted timestamped transcript excerpts establishing the intervention and withdrawal sequence.
2. Aggregate tables produced from the complete archive.
3. The scoring/counting rules.
4. An analysis script that other ChatGPT exports can run locally.
5. Hashes of source files or frozen derived datasets where useful for provenance.
6. An explicit redaction notation such as `[REDACTED: unrelated personal material]`.

Redactions should remove unrelated private content while retaining timestamps, speaker identity as `user`/`assistant`, conversation boundaries, relevant model metadata, and every piece of text needed to understand the tested event.

Separated transcript passages must not be presented as though they were contiguous.

## 11. Current status

| Claim | Status |
| --- | --- |
| The prohibited output repeatedly occurred before MOGRI | OBSERVED |
| A 200-message confirmed MOGRI-on interval contained zero instances | OBSERVED |
| The zero interval crossed conversation boundaries | OBSERVED |
| Violations returned after MOGRI was disabled | OBSERVED |
| MOGRI was completely inert in this runtime | NOT SUPPORTED BY OBSERVED TRACE |
| MOGRI probably contributed to constraint persistence | INFERENCE / RETEST |
| MOGRI alone caused the full reduction | UNKNOWN |
| Exact causal effect size | UNKNOWN |
| Generalisation to other users/models | UNKNOWN |
| Prospective replication | NOT YET RUN |
| External Dec-Jan control archives | NOT YET OBTAINED |

## 12. Next test

The immediate next test is not another theoretical argument about what MOGRI ought to do.

It is:

> reconstruct eligible red-X opportunities and the complete runtime ledger, then compare MOGRI-on and MOGRI-off periods while holding model, conversation state, and instruction exposure as tightly as the historical archive permits.

In parallel, obtain unrelated December 2025-January 2026 ChatGPT exports to test the platform-change alternative.

## Conclusion

A historical ChatGPT export contains an accidental before/on/off trace relevant to MOGRI's proposed role in preserving user-supplied intent and constraints. The trace is unusually useful because it predates the present analysis and includes both repeated pre-intervention failure and later recurrence after MOGRI was disabled.

The result is not yet a causal proof. It is sufficient to reject treating the archive as if it contained no behavioural signal at all, and it supplies a concrete, falsifiable target for the next round of analysis and prospective replication.

---

### v0.001 provenance note

This paper was drafted from the supplied historical ChatGPT export and the quantitative mining performed against that archive in the current analysis session. Counts are provisional until the analysis script, event boundaries, and opportunity-scoring rubric are frozen and rerun for publication.
