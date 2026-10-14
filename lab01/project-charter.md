# Project charter: Realtime Quiz platform

| Field    | Value                              |
|----------|------------------------------------|
| Version  | 1.0 (draft for sponsor approval)   |
| Date     | 2026-09-29                         |
| Sponsor  | Head of the IT department          |
| PM       | Chiv Inthera, supervising lecturer    |

## 1. Purpose and justification
Lecturers currently spend excessive time manually marking quizzes and lack a tool for immediate student feedback during classes. The Realtime Quiz platform provides a live, WebSocket-driven application where students answer timed multiple-choice questions with instant scoring. This reduces marking load, increases classroom engagement, and keeps data ownership on campus. See business-case.md for the financial justification.

## 2. Objectives and success criteria
| #  | Objective (what will be true)      | Success criterion (number + week) |
|----|------------------------------------|-----------------------------------|
| O1 | MVP deployment completed           | All Must features live, 0 blocking defects, week 7 |
| O2 | Pilot with 50 students in one live session | 50 participants, 0 blocking defects, week 14 |
| O3 | Broadcast latency during the pilot | <= 500 ms at the 95th percentile, measured week 14 |
| O4 | Server capacity handles concurrent load | 20 sessions of 100 participants stable, week 13 |
| O5 | Codebase meets quality and testing standards | Line coverage >= 80% with CI green, week 14 |

## 3. High-level scope
In scope:
- Multiple-choice quiz authoring interface
- Real-time live sessions with a 6-character join code
- Instant scoring and live leaderboards
- Analytics and CSV/PDF result exports
- Role-based authentication (Instructor, Student, Guest)

Out of scope:
- Native mobile applications
- Question types other than multiple choice (no free text)
- Video conferencing integration
- Learning Management System (LMS) integration

## 4. Milestones
| Week | Milestone                          | Ends process group |
|------|------------------------------------|--------------------|
| 1    | Charter approved, team formed      | Initiating         |
| 3    | PM plan and UI mockups approved    | Planning           |
| 7    | MVP demo                           | Executing          |
| 9    | Analytics and export modules done  | Executing          |
| 11   | Chat and stretch features done     | Executing          |
| 13   | Load test (100 simulated users)    | Executing          |
| 14   | Pilot with 50 students, closure    | Closing            |

## 5. Budget summary
Effort: students 4 x 14 x 8 h = 448 h; PM 14 x 3 h = 42 h; total 490 h
Cash: hosting 4 x 25 USD = 100 USD; domain 15 USD; tools 60 USD; reserve 25 USD (14.2 %) total 200 USD

## 6. Assumptions
- The team of 4 students will consistently contribute 8 hours per week each.
- The campus network proxy will not block SockJS/WebSocket traffic.
- 2 vCPU and 2 GB RAM on Linode will be sufficient to host the load.

## 7. Constraints
- The project must be completed within the fixed 14-week semester timeline.
- Cash expenditures must not exceed the strict 200 USD cap.
- The PDF export library must successfully render Khmer fonts.

## 8. High-level risks
- The campus proxy may block WebSocket, requiring a fallback to SockJS which increases latency.
- Client clock drift from the server may cause race conditions on late answers.
- Feature creep from "Could" features might delay the critical week 7 MVP delivery.

## 9. Project manager authority
The PM re-plans within the 490 h and 200 USD limits without approval; adding scope, moving the pilot, or spending beyond the 25 USD reserve needs the sponsor's written approval within 5 working days.

## 10. Approval
Sponsor: ____________________  Date: ________
PM:      ____________________  Date: ________