# 04. Prioritization Model

Intake produces more candidates than any team can pilot well. This model ranks them on seven weighted criteria, then applies gate rules so a high score cannot hide a data or risk problem.

Template: [templates/prioritization-scoring.csv](templates/prioritization-scoring.csv). Candidate ideas: [reference/use-case-library.md](reference/use-case-library.md).

---

## Criteria and weights

Each criterion is scored from 1 to 5. Risk and effort are scored in reverse, so **5 always means "more favorable."**

| Criterion | Weight | 1 (unfavorable) | 5 (favorable) |
|---|---|---|---|
| **Business value** | 25% | Minor convenience for a few people | Large volume, high cost, or direct member impact |
| **Measurable outcome** | 15% | No baseline; benefit only self-reported | Baseline exists in a system; outcome metric is clear |
| **Feasibility** | 15% | Needs custom development or features not yet available | Works with standard Copilot features in existing apps |
| **Data readiness** | 15% | Source content overshared, stale, or unlabeled | Content current, owned, labeled, permissions reviewed |
| **Organizational readiness** | 10% | No sponsor; team resistant or overloaded | Engaged owner, a champion, capacity to pilot |
| **Risk** (reversed) | 10% | Restricted data, member-facing, or influences decisions | Internal data, human-reviewed, no decisions |
| **Implementation effort** (reversed) | 10% | Months of remediation or integration | Days to configure and train |

**Weighted score (0 to 100)** = sum of (score × weight) ÷ 5

Business value carries the most weight, and measurable outcome is weighted on its own. That is deliberate: a candidate that cannot be measured cannot be proven, however attractive it looks.

## Gate rules

Scores rank candidates. Gates decide whether a candidate can be piloted at all.

| Condition | Effect |
|---|---|
| Data readiness of 2 or lower | Not piloted until the content and permissions are fixed |
| Risk of 2 or lower | Full tier review and documented conditions before a pilot ([05](05-governance-model.md)) |
| Measurable outcome of 1 | Returned to intake to define a baseline |
| Process maturity below level 2 at intake | Returned to the owner to standardize the process |
| Prohibited data involved | Declined for general Copilot use |

## Waves

| Wave | Rule | Purpose |
|---|---|---|
| **Wave 1** | Score 80 or higher, no gate flags | First pilot: prove value quickly with low risk |
| **Wave 2** | Score 60 to 79, or flags with a remediation plan | Second pilot or scale phase |
| **Backlog** | Score under 60 | Revisit quarterly |

Aim for at least one Wave 1 candidate with a hard business metric (handle time, cycle time, error rate), not only time-saved surveys.

## Worked example (fictional)

| Candidate | Value | Outcome | Feasibility | Data | Org | Risk | Effort | Score | Wave |
|---|---|---|---|---|---|---|---|---|---|
| Draft after-call notes (Member Care) | 5 | 5 | 4 | 4 | 4 | 4 | 4 | **88** | 1 |
| Teams meeting recap for project and committee meetings | 3 | 3 | 5 | 5 | 4 | 5 | 5 | **82** | 1 |
| Policy and procedure knowledge search (Member Care) | 5 | 4 | 4 | 3 | 4 | 4 | 3 | **80** | 1 |
| Board-package variance commentary (Finance) | 4 | 4 | 4 | 4 | 3 | 3 | 4 | **76** | 2 |
| Marketing campaign variants | 2 | 3 | 5 | 5 | 4 | 4 | 5 | **75** | 2 |
| Loan condition letter drafting (Lending) | 4 | 4 | 3 | 3 | 3 | 2 | 3 | **66** | 2 (risk flag) |
| Member complaint summary for supervisors | 3 | 3 | 4 | 2 | 3 | 2 | 3 | **58** | Backlog (data and risk flags) |

**Reading the result:** Member Care leads because volume is high and the contact-center platform already measures handle time and first-contact resolution. Meeting recap scores well on ease and low risk but has softer value, so it is included as a quick win, not as the headline business case. Complaint summaries are valuable but wait until the complaint-tracking content is cleaned up and the Restricted-data controls are confirmed.

## Calibration

- Score in a 30-minute session with the business owner, AI and Automation, and Information Security. Do not score alone.
- Re-score after readiness remediation. Data readiness and effort often improve.
- Revisit weights once a year. An organization focused on cost may raise implementation effort; one focused on member growth may add a member-impact criterion.
