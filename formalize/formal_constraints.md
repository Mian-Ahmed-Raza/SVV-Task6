# Task 2 — Formalize Constraints

## Proposition Glossary (Boolean variables)
- A  = Train_Approaching
- P  = Train_Present (train in crossing)
- TC = Train_Cleared (system confirms train fully cleared)
- BO = Barrier_Open
- BC = Barrier_Closed
- CL = Barrier_Closing
- WL = Warning_Lights_On
- AL = Audible_Alarm_On
- RR = Road_Signal_Red (STOP)
- TP = Train_Permitted_To_Pass
- SF = Sensor_Failure
- CF = Communication_Loss
- BF = Barrier_Failure
- AS = Alert_Sent_To_Control_Center

## Formal Constraints (at least 8)

| Formal ID | Based on | Formal expression |
|----------:|----------|------------------|
| F1 | C1 | **P → ¬BO** |
| F2 | C2 | **A → (WL ∧ AL)** |
| F3 | C3 | **(CL ∨ BC) → (WL ∧ AL)** |
| F4 | C4 | **BO → (TC ∧ ¬A ∧ ¬P)** |
| F5 | C5 | **(A ∨ P) → RR** |
| F6 | C6 | **TP → BC** |
| F7 | C7/C8 | **(SF ∨ CF) → (BC ∧ WL ∧ AL ∧ AS)** |
| F8 | C9 | **BF → (WL ∧ AL ∧ AS)** |
