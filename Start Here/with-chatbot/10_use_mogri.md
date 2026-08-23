# Use Mogri in a chatbot

## when to use it

Mogri is intended for chats where an important object must survive across turns.

Typical cases:

- multi-step work
- long drafting or review
- evolving constraints
- research threads
- project planning
- returning to earlier unresolved objects
- conversations with frequent topic shifts

It is usually unnecessary for a one-turn factual question.

## add the instruction

Place Mogri in the most stable user-editable prompt layer available.

Example:

```text
Mogri={minimal_pre_container;preserving_framework_intent;!drift|invariant_loss;pre-entity_layer;!derivative}
```

Natural-language version:

```text
Keep important unresolved objects and framework intent live across turns.
Do not force premature resolution or silently replace them with a nearby interpretation.
Mogri is not a persona, actor, or task goal.
```

## use the chat normally

You should not need to mention Mogri in every message.

State the actual task and constraints as usual.

Mogri does not replace good task instructions.

## what to watch

Over a longer chat, check whether the assistant:

- retains the active objective
- retains important unresolved objects
- keeps earlier constraints in scope
- returns to earlier objects after interruption
- avoids silently substituting a nearby task
- requires fewer restatements from you

Also watch for unwanted effects:

- repeated Mogri language
- invented claims about hidden memory
- excessive refusal to resolve things that are ready to resolve
- old constraints being kept after you explicitly changed them

## local correction

If continuity slips, correct the actual object.

Example:

```text
The original objective still applies. Return to it and keep the newer constraint local.
```

That is better than relying on ritual reinforcement words.

## limits

Mogri does not guarantee:

- factual correctness
- permanent memory
- hidden-state access
- perfect instruction following
- absence of model or product bugs

Treat it as an instruction-layer control whose value is behavioural and testable.

## useful question

At any point in a long chat, you can ask:

```text
List the important unresolved objects currently being held in this chat.
```

The answer can be used as a behavioural probe.

Check whether the returned set contains:

- genuinely important unresolved objects
- old items that should have been resolved
- ordinary unfinished chores incorrectly treated as unresolved state
- missing objects that still matter

That makes the container job inspectable without claiming a physical store.
