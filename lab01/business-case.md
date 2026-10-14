# Business case: live quizzes for the IT department

## 1. Problem
Lecturers currently spend significant unpaid time manually marking paper quizzes, delaying feedback to students and reducing classroom interactivity. 
Assumptions:
- lecturers running quizzes: 10
- marking time per lecturer per week: 1 h
- teaching weeks per year: 30
- notional value of one hour: 10 USD (students are unpaid; used to compare)

## 2. Options
| Option | Description | One-off cost | Annual cost | Annual benefit |
|--------|-------------|--------------|-------------|----------------|
| A      | Do nothing  | 0            | 0           | 0              |
| B      | Buy SaaS    | 0            | 1,800       | 3,000          |
| C      | Build       | 4,900        | 300         | 4,800          |

*Note: Option B assumes an educational SaaS tier at 15 USD per lecturer per month.*

## 3. Comparison
| Option | Net annual benefit | Payback (years) | Sensitivity (6 lecturers) |
|--------|--------------------|-----------------|----------------------------|
| B      | 3,000 - 1,800 = 1,200 | 0 (no one-off) | 1,800 - 1,080 = 720   |
| C      | 3,000 + 1,800 - 300 = 4,500 | 4,900 / 4,500 = 1.09 | 2,880 net benefit: 1.7 payback |

## 4. Benefits not priced
- Educational learning outcome for the student development team.
- Complete campus ownership of student data.
- No artificial per-seat participant limits during large lectures.

## 5. Risks per option
**Option B (Buy SaaS):**
- Vendor lock-in and potential sudden educational pricing increases.
- Data privacy concerns hosting student names on third-party offshore servers.

**Option C (Build):**
- The campus proxy may block WebSocket, degrading performance.
- The student team might fail to deliver the MVP by week 7 due to learning curves with Spring Boot.

## 6. Recommendation and review gate
Recommendation: Option C. The payback period is just over one academic year (1.09 years), and it remains viable (1.7 years) even if only 6 lecturers adopt it. The department retains its data and students gain capstone experience. 

Review gate: If the week-7 MVP demo fails to pass all Must features live, the sponsor will switch to Option B for the next semester and treat the platform build as an extended two-semester project.