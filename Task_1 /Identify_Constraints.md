# Automated Railway Level-Crossing Control System (ARLCCS)

## Task 1 Identify Constraints

| Constraint ID | Constraint in Simple English | Why the Constraint is Necessary |
|---|---|---|
| **C1** | The barrier must not open while a train is present at the crossing. | Prevents road traffic from entering the crossing while the train is passing. |
| **C2** | The barrier must close when an approaching train is detected. | Stops road traffic before the train reaches the crossing. |
| **C3** | Warning lights must be ON when a train is approaching or present. | Alerts drivers and pedestrians that a train is near. |
| **C4** | The audible alarm must be active while the crossing is unsafe. | Provides an additional warning to road users. |
| **C5** | The barrier must remain closed until the system confirms that the train has completely cleared the crossing. | Prevents the barrier from opening too early. |
| **C6** | The barrier must not open if train clearance has not been confirmed. | An unknown clearance status must be treated as unsafe. |
| **C7** | If a sensor fails, the system must prevent the barrier from opening. | A failed sensor may provide incorrect information about the train's position. |
| **C8** | If the barrier fails to close, the system must activate emergency warnings. | Alerts road users and the control center about the dangerous condition. |
| **C9** | If communication with the control center is lost, the crossing must continue operating in a safe state. | Communication failure must not create an unsafe crossing. |
| **C10** | The system must not allow road traffic to pass when a train is occupying the crossing. | Prevents collisions between road vehicles and trains. |
| **C11** | An emergency condition must cause the system to activate the required safety response. | Ensures dangerous situations are handled immediately. |
| **C12** | Conflicting or incorrect sensor readings must not cause the barrier to open. | Prevents unreliable sensor information from creating an unsafe condition. |
