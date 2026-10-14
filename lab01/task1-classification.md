# Task 1: project, operation or programme?

| #  | Initiative | Temporary? | Unique? | Coordinated? | Class | Justification |
|----|------------|------------|---------|--------------|-------|---------------|
| 1  | Build the Realtime Quiz platform and pilot it with 50 students in week 14 | yes | yes | no | Project | Has a clear deadline (week 14) and produces a unique result (the platform). |
| 2  | Run the nightly backup of the gicitc.com PostgreSQL database | no | no | no | Operation | Repeats every night with the same output and no end date; it is part of keeping the service running. |
| 3  | Move the department's three web servers to a new Linode region before 15 December | yes | yes | no | Project | Has a specific end date (15 December) and results in a unique state change. |
| 4  | Answer helpdesk tickets within the 4-hour service level | no | no | no | Operation | Continuous, repetitive daily task to maintain existing services. |
| 5  | "Digital classroom": Realtime Quiz, LMS upgrade and lecture capture sharing one login and one grade export | yes | yes | yes | Programme | Three related projects; the shared login and grade export are a benefit that none of them delivers alone, so they are coordinated. |
| 6  | Apply the monthly security patches to the VPS | no | no | no | Operation | Repetitive maintenance task with no final end date. |
| 7  | Add multi-node scaling (RabbitMQ relay, Redis registry) to Realtime Quiz next semester | yes | yes | no | Project | Has a specific delivery timeframe and adds unique new capabilities. |
| 8  | Operate the Realtime Quiz platform after go-live: password resets, restarts, monitoring | no | no | no | Operation | Continuous support activities required to sustain the product lifecycle. |
| 9  | Write and publish the department's annual IT report for the dean by 31 January | yes | yes | no | Project | Annual and repetitive, yet each report is unique with a strict deadline. |
| 10 | Replace 40 wireless access points in two buildings during the summer break | yes | yes | no | Project | Has a specific timeframe (summer break) and a defined physical completion state. |

## Grey zones
Initiative 7 (multi-node scaling) could be an operation if funded as routine maintenance, or a project if the sponsor funds it as a separate endeavour with its own end. 
Initiative 9 (annual report) repeats yearly like an operation, but most departments treat it as a small yearly project because each report requires unique data gathering and has a strict deadline.

## What our project hands over
At week 14, the Realtime Quiz project hands over the platform to IT operations (the gicitc.com VPS admins). They will run the live system, handle backups, and manage monitoring. To do this successfully, they need a deployment checklist, a runbook, and the docker-compose.prod.yml file from the project team.