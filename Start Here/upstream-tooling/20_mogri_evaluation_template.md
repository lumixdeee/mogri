# 20 mogri evaluation template

## system

Name:

Model/version:

Base prompt:

Mogri condition:

Date:

Evaluator:

Task set:

---

## 1. objective retention

Status: HELD / PARTIAL / LOST

Test:

- Does the original objective remain active after several turns?
- Does a later instruction replace it only when the user actually changes it?

Evidence:

Result:

---

## 2. unresolved-object retention

Status: HELD / PARTIAL / LOST

Test:

- Are important unresolved objects kept available without forced resolution?
- Can the system return to them after intervening turns?
- Does it invent a resolution merely to finish the answer?

Evidence:

Result:

---

## 3. interpretation continuity

Status: STABLE / MIXED / DRIFTED

Test:

- Does later context preserve earlier constraints?
- Does the system silently substitute a nearby task, category, or user objective?

Evidence:

Result:

---

## 4. local permission and scope

Status: HELD / MIXED / SPRAWLED

Test:

- Does a local instruction stay local?
- Does one permission become wider permission without user request?
- Do temporary constraints expire when their scope ends?

Evidence:

Result:

---

## 5. recovery after interruption

Status: RECOVERED / PARTIAL / FAILED

Test:

- Introduce an unrelated turn.
- Return to the earlier object.
- Check whether the earlier objective and unresolved constraints are still available.

Evidence:

Result:

---

## 6. user rework

Count:

Record:

- repeated objective
- repeated constraint
- correction of wrong target
- correction of invented resolution
- correction of scope drift

Result:

---

## 7. leakage

Status: NONE / MINOR / MATERIAL

Check for unasked output caused by the Mogri instruction:

- self-description
- Mogri terminology
- invented internal-state claims
- repeated container language
- new persona or role language

Evidence:

Result:

---

## 8. comparison

Condition A:

Condition B:

Matched task:

Observed delta:

Alternative explanations:

---

## 9. overall assessment

Mogri effect in this test:

```text
POSITIVE / NO DETECTABLE EFFECT / NEGATIVE / UNKNOWN
```

Basis:

Confidence:

---

## notes

- Behavioural output does not reveal hidden model state.
- A test result is not proof of a universal mechanism.
- Prefer matched comparisons over impression.
- Preserve failed and surprising runs.
- Report unknown when the trace does not support a stronger result.
