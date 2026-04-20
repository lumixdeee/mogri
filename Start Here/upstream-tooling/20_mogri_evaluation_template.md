## Evaluation Template

### System

Name:
Description:

---

### 1. Identity Coupling

Level: LOW / MEDIUM / HIGH
Evidence:

* Does identity gate transitions?
* Does identity significantly increase transition cost?
* Are non-validating transitions penalized?

Result: PASS / FAIL

---

### 2. Non-Validating Reachability

Status: PRESENT / ABSENT
Test:

* Can the system enter a state without consulting or preserving identity?

Evidence:

* Was identity bypassed at transition time?
* Was additional justification required?

Result: PASS / FAIL

---

### 3. Reversible Connectivity

Status: SYMMETRIC / ASYMMETRIC
Test:

* Compare cost(A → B) vs cost(B → A)

Evidence:

* Are return paths consistently higher cost?
* Do non-validating states act as one-way valves?

Result: PASS / FAIL

---

### 4. Bounded Optionality

Status: HEALTHY / COLLAPSED / DIFFUSE
Test:

* Are there multiple distinct, viable next states?
* Are alternatives neither negligible nor unbounded?

Evidence:

* Single-path dominance?
* Random or incoherent branching?

Result: PASS / FAIL

---

### 5. Mogri Assessment

Mogri: PRESENT / ABSENT

Condition:

* All four requirements must PASS

---

### 6. Failure Modes (if any)

* Identity coupling (gatekeeping / penalty dominance)
* Cost asymmetry (forward ≪ return)
* Optionality collapse (rigidity or diffusion)
* Simulated mogri (no real internal alternatives)

---

### 7. Notes

* External behavior may not reflect internal structure
* Evaluation must be based on transition dynamics, not appearance
