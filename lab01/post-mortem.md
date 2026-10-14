# Post-mortem: CampusPay wallet (fictional case from Lab-01)

## 1. Timeline and sources
| # | When       | Event                                                              | Source                         |
|---|------------|--------------------------------------------------------------------|--------------------------------|
| 1 | January    | University asks IT to build CampusPay for canteen & library fines  | fictional case from Lab-01     |
| 2 | February   | Head of finance "sponsors" via email but attends no reviews        | fictional case from Lab-01     |
| 3 | March      | Scope expands to bus tickets and parking based on a survey         | fictional case from Lab-01     |
| 4 | September  | Launch day: no prior hardware testing done; 40% failure rate       | fictional case from Lab-01     |
| 5 | September  | App withdrawn after 3 days due to doubled canteen queues           | fictional case from Lab-01     |
| 6 | February+1 | App relaunches successfully for canteen only                       | fictional case from Lab-01     |

## 2. Classification and organisation
Project / programme: It was a project (temporary, unique software creation). 
Structure and PM authority: Projectized or strong matrix, but poorly defined. The PM was the lead developer, carrying too much technical bias and zero structural authority to push back on scope.
Sponsor, charter, PMO: No formal charter was signed. The sponsor (Head of Finance) was absent, effectively leaving the project orphaned. No PMO oversight existed to enforce testing standards.

## 3. Success criteria
Stated: "Launch in September".
Missing measurable criteria: Acceptable transaction failure rate (e.g., < 1%), maximum allowable transaction time, hardware compatibility targets.
Ignored dimensions: Operations (terminal integration was ignored until launch), Users (queues doubled, ruining the user experience), Benefits (the goal was cashless convenience, but it created delays).

## 4. Process groups and knowledge areas
| Process group              | What went wrong or was skipped |
|----------------------------|--------------------------------|
| Initiating                 | No charter; the head of finance never accepted the sponsor role, so nobody could refuse the bus-ticket scope creep. |
| Planning                   | Requirements were gathered via survey but never baselined against technical constraints or the timeline. |
| Executing                  | The lead developer built the software in isolation without integrating the actual hardware terminals. |
| Monitoring and controlling | Scope expanded unchecked; progress was likely tracked by software completion while ignoring the lack of end-to-end integration. |
| Closing                    | The project forced a launch without operational readiness, resulting in an immediate rollback. |

Knowledge areas most responsible: 
1. Project Scope Management (scope expanded uncontrollably from canteen to parking).
2. Project Quality Management (zero hardware integration testing prior to launch day).
3. Project Stakeholder Management (the sponsor was completely disengaged).

## 5. Ethics
Decision examined: Launching the app in September without having tested it on real card terminals. 
Responsibility / respect / fairness / honesty: This violated **responsibility** and **honesty**. The PM failed to fulfill the duty of ensuring the product was safe and functional (responsibility) and implicitly misled stakeholders about its operational readiness (honesty) by greenlighting the launch.

## 6. What our project will do differently
| # | Commitment (We will ...) | Measured by | By week | Charter line |
|---|--------------------------|-------------|---------|--------------|
| 1 | We will run a live session with 100 simulated students to test concurrent load. | load test report, 0 errors | 13 | milestone week 13, O4 capacity |
| 2 | We will hold a signed charter with a named sponsor who attends the week-7 and week-13 gates. | signature on charter, gate minutes | 1 | section 10 approval, authority clause |
| 3 | We will stick strictly to the MVP scope and reject "Could" features until core is stable. | feature list in release notes | 7 | section 3 High-level scope, constraint 1 |
| 4 | We will involve IT Operations early by delivering a runbook and docker-compose file. | runbook file committed | 12 | milestone week 14, constraint 1 |
| 5 | We will test the broadcast latency in real-world conditions rather than localhost. | ping latency logs <= 500ms | 14 | O3 latency objective |