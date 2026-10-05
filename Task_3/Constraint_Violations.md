# Task 3 — Identify Constraint Violations

## Violation 1 — C1

### Constraint

Train_Present → ¬Barrier_Open

### Violation

Train_Present = TRUE
Barrier_Open = TRUE

### Explanation

A train is present at the crossing, but the barrier is open. This violates C1 because the barrier must not open while a train is present.

## Violation 2 — C2

### Constraint

Train_Approaching → Barrier_Closed

### Violation

Train_Approaching = TRUE
Barrier_Closed = FALSE

### Explanation

A train is approaching, but the barrier is not closed. This violates C2 because the barrier must close when a train is approaching.

---

## Violation 3 — C3

### Constraint

(Train_Approaching ∨ Train_Present) → Warning_Light

### Violation

Train_Approaching = TRUE
Warning_Light = FALSE

### Explanation

A train is approaching, but the warning lights are OFF. This violates C3 because the warning lights must be ON whenever a train is approaching or present.

## Violation 4 — C4

### Constraint

(Train_Approaching ∨ Train_Present) → Alarm

### Violation

Train_Present = TRUE
Alarm = FALSE
### Explanation

A train is present at the crossing, but the audible alarm is OFF. This violates C4 because the alarm must be active while the crossing is unsafe.

## Violation 5 — C5

### Constraint

Barrier_Open → Clearance_Confirmed

### Violation

Barrier_Open = TRUE
Clearance_Confirmed = FALSE

### Explanation

The barrier has opened even though the system has not confirmed that the train has completely cleared the crossing. This violates C5 because the barrier can only open after clearance has been confirmed.

## Violation 6 — C6

### Constraint

¬Clearance_Confirmed → ¬Barrier_Open

### Violation

Clearance_Confirmed = FALSE
Barrier_Open = TRUE

### Explanation

Train clearance has not been confirmed, but the barrier is open. This violates C6 because the barrier must remain closed until clearance is confirmed.

## Violation 7 — C7

### Constraint

Sensor_Failure → ¬Barrier_Open

### Violation

Sensor_Failure = TRUE
Barrier_Open = TRUE

### Explanation

A safety sensor has failed, but the system has opened the barrier. This violates C7 because the barrier must not open when a safety sensor has failed.

## Violation 8 — C8

### Constraint

Barrier_Failure → (Warning_Light ∧ Alarm)

### Violation

Barrier_Failure = TRUE
Warning_Light = FALSE
Alarm = FALSE

### Explanation

The barrier has failed, but the warning light and audible alarm are both OFF. This violates C8 because emergency warnings must be activated when the barrier fails.
