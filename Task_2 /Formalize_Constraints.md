# Automated Railway Level-Crossing Control System (ARLCCS)

# Task 2 — Formalize Constraints

## C1 — Barrier Must Not Open When a Train Is Present
**Formal Expression:**
Train_Present → ¬Barrier_Open

**Meaning:**
If a train is present at the crossing, the barrier must not be open.

---

## C2 — Barrier Must Close When a Train Is Approaching

**Formal Expression:**

Train_Approaching → Barrier_Closed

**Meaning:**
If a train is approaching the crossing, the barrier must be closed.

---

## C3 — Warning Lights Must Be ON

**Formal Expression:**

(Train_Approaching ∨ Train_Present) → Warning_Light

**Meaning:**
If a train is approaching or already present, the warning lights must be ON.

---

## C4 — Audible Alarm Must Be ON

**Formal Expression:**

(Train_Approaching ∨ Train_Present) → Alarm

**Meaning:**
If a train is approaching or present, the audible alarm must be active.

---

## C5 — Barrier Can Open Only After Train Clearance Is Confirmed

**Formal Expression:**

```text
Barrier_Open → Clearance_Confirmed
```

**Meaning:**
The barrier can be open only when the system has confirmed that the train has completely cleared the crossing.

---

## C6 — Barrier Must Not Open Without Clearance Confirmation

**Formal Expression:**

¬Clearance_Confirmed → ¬Barrier_Open

**Meaning:**
If train clearance has not been confirmed, the barrier must not open.

---

## C7 — Sensor Failure Must Prevent the Barrier From Opening

**Formal Expression:**

Sensor_Failure → ¬Barrier_Open

**Meaning:**
If a safety sensor fails, the barrier must remain closed.

---

## C8 — Barrier Failure Must Activate Emergency Warnings

**Formal Expression:**

Barrier_Failure → (Warning_Light ∧ Alarm)

**Meaning:**
If the barrier fails, both the warning lights and audible alarm must be activated.

---

## C9 — Communication Loss Must Result in a Safe State

**Formal Expression:**

Communication_Lost → Barrier_Closed

**Meaning:**
If communication with the control center is lost, the barrier must remain closed.

---

## C10 — Road Traffic Must Not Pass When a Train Is Present

**Formal Expression:**

Train_Present → ¬Road_Traffic_Pass

**Meaning:**
If a train is present at the crossing, road traffic must not be allowed to pass.

---

## C11 — Emergency Must Activate the Safety Response

**Formal Expression:**

Emergency → (Alarm ∧ Warning_Light ∧ Barrier_Closed)

**Meaning:**
If an emergency occurs, the audible alarm and warning lights must be active and the barrier must be closed.

---

## C12 — Conflicting Sensor Readings Must Not Open the Barrier

**Formal Expression:**

Sensor_Conflict → ¬Barrier_Open

**Meaning:**
If sensors provide conflicting or unreliable readings, the barrier must not open.

---

# Logical Operators Used

| Symbol | Meaning           |
| ------ | ----------------- |
| `∧`    | AND               |
| `∨`    | OR                |
| `¬`    | NOT               |
| `→`    | IMPLIES / IF-THEN |

