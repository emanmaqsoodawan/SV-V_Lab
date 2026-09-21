### Task 2 — Identify States

| State ID | State Name | Description | Entry Condition | Exit Condition |
| --- | --- | --- | --- | --- |
| **S1** | `IDLE` | The robot is stationary at the warehouse in a low-power standby mode, awaiting mission commands. | System power-on initialization completes, OR the robot successfully returns to and arrives at the warehouse depot. | A valid delivery request containing destination coordinates is received. |
| **S2** | `NAVIGATING` | The robot actively traverses planned route coordinates toward the target destination or en route back. | A delivery request is accepted, OR an obstacle has been successfully bypassed, resuming the active path. | The target destination is reached, an obstacle is detected in the path, or the battery drops to a critical level. |
| **S3** | `AVOIDING_OBSTACLE` | Normal trajectory is suspended while onboard sensors evaluate the hazard and compute/execute a safe detour. | An obstacle is detected along the robot's active path during navigation. | The path is confirmed clear of the hazard, OR the battery drops to a critical level requiring a route abort. |
| **S4** | `DELIVERING` | The drive motors are disengaged at the destination to allow package unlocking, unloading, and handover confirmation. | Arrival at the destination coordinates is physically verified while in normal navigation mode. | The package handover sequence completes successfully, or recipient confirmation is verified. |
| **S5** | `RETURNING` | The robot follows an autonomous return trajectory back to the central warehouse depot. | A delivery handover is marked successful, OR a critical low-battery threshold triggers an emergency mission abort. | The robot reaches the designated docking or staging area inside the warehouse. |
