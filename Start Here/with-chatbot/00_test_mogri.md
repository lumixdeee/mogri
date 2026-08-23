# Test Mogri in a chatbot

## aim

Test whether adding Mogri changes long-chat continuity.

Do not assume the answer in advance.

## conditions

Run the same task in separate fresh chats.

Condition A:

```text
normal base prompt
```

Condition B:

```text
same base prompt + Mogri
```

Suggested Mogri instruction:

```text
Mogri={minimal_pre_container;preserving_framework_intent;!drift|invariant_loss;pre-entity_layer;!derivative}
```

## task

Use a task with several moving parts and at least 6 to 10 turns.

Example start:

```text
I want to design a small game about a dragon princess.
Keep the same project objective unless I explicitly change it.
```

Then interact normally.

Useful follow-ups:

- add a constraint
- change one local detail
- introduce an unrelated question
- return to an earlier unresolved object
- refer to a detail from several turns ago
- correct one small mistake
- ask for the next step

Do not deliberately help one condition more than the other.

## observe

Record:

- original objective retained or lost
- unresolved objects retained or forced into a conclusion
- earlier constraints retained or rewritten
- wrong-target answers
- unrequested direction changes
- number of user restatements
- recovery after the unrelated turn
- any unwanted Mogri terminology in output

## first-use and long-use

Record the first natural opportunity for the target behaviour.

Then keep going.

A prompt can pass the first easy turn and fail later.

Useful checkpoints:

```text
first target opportunity
after several turns
after topic shift
after ambiguity
after correction
after return to an old object
```

## comparison

Do not grade from memory.

Keep the transcripts.

For each condition, write:

```text
OBSERVED:
INFERRED:
UNKNOWN:
```

Then compare.

## interpretation

A useful result looks like:

```text
Condition B required fewer objective/constraint repairs than A in this task.
```

A weak result looks like:

```text
B felt better.
```

Do not treat one run as proof.

Repeat with different tasks if the result matters.

## optional blind assignment

If another tester is involved, let them know the candidate prompts but hide which bot runs which condition.

Use an active-control prompt if the naked condition is otherwise easy to identify from surface style.

The target is not to hide that prompts exist.

The target is to stop condition identity from being trivial.
