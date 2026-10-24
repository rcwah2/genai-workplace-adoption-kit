# 05. Value Scorecard

A one-page monthly scorecard that tracks adoption (leading indicators), value (outcomes), risk, and sentiment. Template: [templates/value-scorecard.csv](templates/value-scorecard.csv).

---

## Metrics

### Adoption

| Metric | Definition | Source | Target (illustrative) |
|---|---|---|---|
| Enabled users | Users with a license or access | Admin console | Per rollout plan |
| Active users (28 days) | Users who used the tool at least once in the last 28 days | Microsoft Copilot Dashboard; ChatGPT admin analytics | — |
| Adoption rate | Active users divided by enabled users | Calculated | 70% or more by month 6 |
| Habitual use | Share of active users using the tool 3 or more days per week | Copilot Dashboard; admin analytics | 40% or more by month 6 |
| Departments with a verified use case | Departments with at least one measured use case | Use-case register | All by month 6 |

Microsoft's Copilot Dashboard reports readiness, adoption, impact, and sentiment, and estimates Copilot-assisted hours and value ([Microsoft](https://learn.microsoft.com/en-us/viva/insights/copilot-analytics-introduction); [Microsoft Adoption](https://adoption.microsoft.com/en-us/copilot/measure-business-impact/)).

### Value

| Metric | Definition | Source |
|---|---|---|
| Self-reported hours saved | Survey: minutes saved per week times active users | Pulse survey |
| Estimated assisted hours | Tool-estimated hours (for example, Copilot-assisted hours) | Copilot Dashboard |
| Process outcomes | Change in handle time, turnaround time, hours per report, against baseline | Department systems |
| Capacity value | Hours saved times loaded hourly cost | Calculated |
| Verified use cases | Use cases with a before-and-after measurement | Use-case register |

> **Capacity is not cash.** Hours saved become value only when they are redirected to member service, growth work, or avoided hiring. Report where the time went.

### Risk and quality

| Metric | Definition | Source |
|---|---|---|
| DLP events | Policy matches for AI prompts or content | Purview / DLP |
| Data incidents | Confirmed cases of Restricted or prohibited data in AI tools | Incident log |
| Output errors caught | Errors found in review before use | Pulse survey, QA sampling |
| Output errors escaped | Errors that reached a member or a decision | Incident log |
| Shadow AI signals | Detected use of unapproved AI services | Web filtering, CASB |
| Intake turnaround | Average days from submission to decision, by tier | Intake log |

### Sentiment

| Metric | Definition | Source |
|---|---|---|
| Usefulness | "AI tools help me do my job better" (1 to 5) | Pulse survey |
| Confidence | "I know what I can and cannot do with AI tools" (1 to 5) | Pulse survey |
| Champion feedback themes | Top three themes each month | Champions |

## Reporting cadence

| Audience | Frequency | Content |
|---|---|---|
| AI Review Group | Monthly | Full scorecard, incidents, intake queue |
| CTO and executive team | Monthly (one page) | Adoption, top value stories, risks, decisions needed |
| Board risk committee | Quarterly | Value summary, risk metrics, Tier 3 inventory, policy changes |

## Survey questions (biweekly, under one minute)

1. In the last two weeks, about how much time did AI tools save you per week? (None / under 30 min / 30 to 60 min / 1 to 2 hours / more than 2 hours)
2. What did you use the time for? (More member time / clearing backlog / other projects / not sure)
3. Did you catch any errors in AI output? (Yes / No)
4. One task you wish AI could help with:
