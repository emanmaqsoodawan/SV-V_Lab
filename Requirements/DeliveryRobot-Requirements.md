### Task 1 — Extracted Requirements

| Req. ID | Description | Priority |
| --- | --- | --- |
| **R1** | The system shall initialize into an idle state upon power-on and wait for an incoming delivery request. | High |
| **R2** | The robot shall initiate autonomous navigation toward the destination only after a valid delivery request is received. | High |
| **R3** | While navigating, the robot shall continuously poll onboard proximity sensors to detect obstacles along its path. | High |
| **R4** | Upon detecting an obstacle during transit, the robot shall halt primary navigation and enter obstacle-avoidance mode within the defined safety reaction window. | Critical |
| **R5** | The robot shall exit obstacle-avoidance mode and resume its standard navigation path toward the target coordinates once the obstacle is cleared. | High |
| **R6** | The robot shall initiate the package delivery/handover process only after confirming physical arrival at the target destination. | High |
| **R7** | Upon successful completion of package delivery, the robot shall autonomously plot and begin travel back to the warehouse depot. | Medium |
| **R8** | If the battery level drops below a predefined critical threshold at any point during navigation, the robot shall immediately abort the delivery and initiate a return to the warehouse. | Critical |
| **R9** | The robot shall transition to the idle standby state immediately upon arriving back at the warehouse. | Medium |
| **R10** | The system shall strictly prohibit starting the package delivery process directly from an idle state or while in obstacle-avoidance mode. | Critical |
