###Test Cases

| ID | Feature | Objective | Steps (summary) | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|-----------------|-----------------|---------------|--------|-----------|
| TC-01 | Leaderboard | Verify top-3 sorting logic | Submit scores 70,80,180 → open leaderboard | Scores shown 180,80,70| 180,80,70 | Pass | R-01 |
| TC-02 | Reset Game | Verify Reset clears score & progress | Play to score >0 → Click Reset | Score=0, puzzle index resets | Score & index reset | Pass | R-02 |
| TC-03 | Bonus Round | Verify every 3rd puzzle applies x2 multiplier | Complete puzzles 1–3 and note points | Puzzle 3 points = base ×2 | Multiplier applied correctly | Pass | R-03 |
| TC-04 | Input Validation (Negative) | Ensure invalid inputs don't crash app | Submit "<script>" as answer | App sanitizes/blocks input; no crash | App threw an error | Fail | R-05 |
| TC-05 | Leaderboard (Boundary) | Verify only top 3 scores persist | Submit >3 scores with varying values | Only top-3 are stored | Top-3 retained | Pass | R-01 |
| TC-06 | Usability | New user can complete tutorial puzzle | Observe new user attempting tutorial | User completes with minor confusion (notes) | not Completed; no notes recorded | fail | R-04 |
| TC-07 | Reset + Persistence (Negative) | Reset does not clear leaderboard | Save score → Reset → check leaderboard | Leaderboard remains intact | Leaderboard intact | Pass | R-02, R-06 |
| TC-08 | Performance | App responsiveness under diffrent screen sizes | adapt to diffrent screen sizes | UI responds properly, no glitch| Responsive; acceptable | Pass | R-04 |

Total executed: 8 | Passed: 6 | Failed: 2

## Defects (GitHub Issues)

| ID | Issue Title       | Severity | Risk ID | Status |
|----|-------------------|----------|---------|--------|
| D-01 | Game never ends | Medium   | R-01    | Open |
| D-02 | no filtering and verification of input | High | R-05 | open |


## Metrics

- Test Case Pass Percent: (6 / 8) × 100 = 75%
- Defect Density: Defects / Test Cases = 2 / 8 = 0.25
- Risk Coverage Percent: 100% (6 / 6)
- Regression success rate:0 retest executed

### Defect Distribution
```
Critical: 0   
High:    1 
Medium:  1   
Low:     0 

### Defect Summary

- Total Defects Logged: 2
- Critical / High: 1
- Fix Rate: 0

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| Planning | Test plan & risk list | Completed | 2hrs| Test Manager |
| Design | Test cases documented | Completed | 2hrs | Risk Analyst |
| Execution | Test execution & evidence | Completed (see table) | 6hrs | Test Executor |
| Triage | Defect triage & retest | pending | - | all |
| Closure | Final report & sign-off | Pending | - | Test Manager |

**Progress Tracking Method:** GitHub Issues for defects, markdown files, risk analysis ,test cases and this report for metrics.

**Change Control Notes:** Any scope deviation or blocked tests were recorded as issues and communicated via the project board.


## ✅ Sign-Off
| Name | Role | Initials | Date |
|------|------|-----------|------|
| Whitney Wairimu | Test Executor | WW | 2025-10-28 |

