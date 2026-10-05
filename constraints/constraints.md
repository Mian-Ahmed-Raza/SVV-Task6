# Task 1 — Identify Constraints (ARLCCS)

Below are system constraints (rules the system must always satisfy).

| ID  | Constraint (simple English) | Why necessary |
|-----|-----------------------------|---------------|
| C1  | The barrier must not open while a train is present in the crossing. | Prevents road vehicles from entering the crossing during passage. |
| C2  | If a train is approaching, warning lights and the audible alarm must be activated. | Alerts road users early to reduce collision risk. |
| C3  | If the barrier is closing or closed, warning lights and the audible alarm must remain active. | Ensures continuous warning while the road is blocked/unsafe. |
| C4  | The barrier must not open until the system has confirmed the train has completely cleared the crossing. | Prevents premature opening due to partial/inaccurate detection. |
| C5  | When a train is approaching or present, the road traffic signal must indicate STOP (red). | Prevents traffic from being directed onto the crossing. |
| C6  | A train must not be permitted to pass unless the barrier is confirmed closed (safe state for road). | Prevents train entering crossing while road is not secured. |
| C7  | If a train-detection sensor fails, the system must enter a fail-safe mode (keep barrier closed and warnings active) and notify the control center. | Sensor failures can hide an approaching train; safest default is to block road traffic. |
| C8  | If communication with the control center is lost, the system must enter/maintain a fail-safe state (barrier closed, warnings active). | System must remain safe even without supervision/remote coordination. |
| C9  | If the barrier mechanism fails (cannot close/open as commanded), the system must keep warnings active and notify the control center immediately. | Mechanical failure is hazardous and requires escalation. |
| C10 | Incorrect/inconsistent sensor readings must be treated as hazardous: the system must assume a train may be approaching/present until resolved. | Prevents unsafe actions based on unreliable data. |
| C11 | The system must not show “road clear/go” indications while the barrier is not fully open. | Avoids encouraging vehicles to move while barrier blocks/unsafe. |
| C12 | All detected abnormal conditions (sensor failure, barrier failure, comms loss, inconsistent readings, emergency) must be logged and reported to the control-center interface. | Supports incident response, auditing, and corrective action. |
