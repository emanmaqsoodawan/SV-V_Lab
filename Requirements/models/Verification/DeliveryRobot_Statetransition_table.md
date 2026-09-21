### Task 3 — Identify Events and Transitions

| Transition ID | From State | Event / Trigger | To State | Req. ID |
| --- | --- | --- | --- | --- |
| **T1** | `IDLE` | Delivery Request Received | `NAVIGATING` | R2 |
| **T2** | `NAVIGATING` | Obstacle Detected | `AVOIDING_OBSTACLE` | R3, R4 |
| **T3** | `AVOIDING_OBSTACLE` | Obstacle Avoided | `NAVIGATING` | R5 |
| **T4** | `NAVIGATING` | Destination Reached | `DELIVERING` | R6 |
| **T5** | `NAVIGATING` | Critical Battery | `RETURNING` | R8 |
| **T6** | `AVOIDING_OBSTACLE` | Critical Battery | `RETURNING` | R8 |
| **T7** | `DELIVERING` | Delivery Successful | `RETURNING` | R7 |
| **T8** | `RETURNING` | Obstacle Detected | `AVOIDING_OBSTACLE` | R3, R4 |
| **T9** | `RETURNING` | Warehouse Reached | `IDLE` | R9 |
