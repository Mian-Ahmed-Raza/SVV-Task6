# Task 3 — Identify Constraint Violations

For each formalized constraint, one realistic violation scenario (values that break the rule) and an explanation.

---

## F1: P → ¬BO
**Violation scenario:** P = TRUE, BO = TRUE  
**What went wrong / how we know:**  
- A train is detected as present in the crossing, but the barrier is open.  
- This directly contradicts ¬BO required when P is TRUE.

---

## F2: A → (WL ∧ AL)
**Violation scenario:** A = TRUE, WL = FALSE, AL = TRUE  
**What went wrong / how we know:**  
- A train is approaching, but warning lights are not on.  
- Since WL ∧ AL is FALSE (WL is FALSE), the implication is violated.

---

## F3: (CL ∨ BC) → (WL ∧ AL)
**Violation scenario:** CL = TRUE, WL = TRUE, AL = FALSE  
**What went wrong / how we know:**  
- The barrier is actively closing, but the audible alarm is off.  
- WL ∧ AL is FALSE, so the required warnings are not fully active.

---

## F4: BO → (TC ∧ ¬A ∧ ¬P)
**Violation scenario:** BO = TRUE, TC = FALSE, A = FALSE, P = FALSE  
**What went wrong / how we know:**  
- The barrier is open even though the system has not confirmed the train cleared (TC is FALSE).  
- BO implies TC must be TRUE; it is not.

(Alternative violation example: BO=TRUE while A=TRUE, meaning barrier open while a train is approaching.)

---

## F5: (A ∨ P) → RR
**Violation scenario:** P = TRUE, RR = FALSE  
**What went wrong / how we know:**  
- Train is present, but road signal is not red (could be green/amber).  
- The road is being allowed/encouraged to move despite danger.

---

## F6: TP → BC
**Violation scenario:** TP = TRUE, BC = FALSE  
**What went wrong / how we know:**  
- System permits the train to pass even though the barrier is not confirmed closed.  
- This violates the safe requirement for road protection before train entry.

---

## F7: (SF ∨ CF) → (BC ∧ WL ∧ AL ∧ AS)
**Violation scenario:** SF = TRUE, BC = FALSE, WL = TRUE, AL = TRUE, AS = FALSE  
**What went wrong / how we know:**  
- A sensor failure is detected, but the system neither forces/keeps barrier closed nor sends an alert.  
- Consequent requires BC and AS to be TRUE; both are FALSE here.

---

## F8: BF → (WL ∧ AL ∧ AS)
**Violation scenario:** BF = TRUE, WL = FALSE, AL = TRUE, AS = TRUE  
**What went wrong / how we know:**  
- Barrier failure occurs, but warning lights are not active.  
- WL ∧ AL ∧ AS is FALSE because WL is FALSE.
