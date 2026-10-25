# 08. Metrics Framework

Most Copilot reporting stops at usage. This framework uses **three separate layers**, plus a set of guardrail metrics, and never reports one layer as if it were another.

```
Layer 1: ADOPTION          →  Layer 2: PRODUCTIVITY       →  Layer 3: BUSINESS OUTCOMES
Are people using it,          Is the work getting faster      Is the business measurably
and using it well?            or easier at the task level?     better?

Leading indicator             Intermediate indicator           The result
Owned by: AI and Automation   Owned by: AI and Automation      Owned by: Business owner
                              with the business owner
```

**Guardrails** (quality, risk, sentiment) run across all three layers. A gain in any layer does not count if a guardrail fails.

Template: [templates/value-scorecard.csv](templates/value-scorecard.csv)

---

## Why three layers

| Common claim | Which layer it is | What it does not prove |
|---|---|---|
| "80% of licensed users are active." | Adoption | That anything got faster or better |
| "Users report saving 2 hours a week." | Productivity (self-reported) | That the time went anywhere useful |
| "Copilot Dashboard shows 1,200 assisted hours." | Productivity (tool-estimated) | That handle time, cycle time, or cost changed |
| "Average handle time fell 6% against the comparison group." | Business outcome | — this is the result |

Microsoft's Copilot Dashboard reports readiness, adoption, impact, and sentiment, and estimates Copilot-assisted hours and their dollar value ([Microsoft](https://learn.microsoft.com/en-us/viva/insights/copilot-analytics-introduction)). Those figures belong mainly in Layers 1 and 2. Microsoft's business impact report lets an organization upload its own outcome data to compare with Copilot usage ([Microsoft](https://learn.microsoft.com/en-us/viva/insights/copilot-analytics-introduction)). That is one way to support Layer 3, but the outcome data and its owner still have to come from the business.

---

## Layer 1: Adoption metrics

Is Copilot being used, and used well?

| Metric | Definition | Source | Example target |
|---|---|---|---|
| Licensed users | Users assigned a Microsoft 365 Copilot license | Microsoft 365 admin center | Per wave plan |
| Active users | Licensed users who used Copilot at least once in the last 28 days | Copilot Dashboard | 80% of licensed |
| Frequency | Share of active users using Copilot on 3 or more days a week | Copilot Dashboard / Viva Insights | 50% |
| Retention | Share of users active in month 1 who are still active in month 3 | Copilot Analytics | 85% |
| Training completion | Share of licensed users who completed required modules before access | Learning system | 100% |
| AI proficiency | Share of users who pass the role-lab proficiency check ([07](07-adoption-plan.md)) | Proficiency check | 75% |
| License utilization | Licenses with no activity in 60 days (reassignment candidates) | Admin center | Under 10% |

## Layer 2: Productivity metrics

Is the task faster or easier for the person doing it? Measure the tasks that were named at intake.

| Metric | Definition | Measurement method |
|---|---|---|
| Drafting time | Minutes to produce a first draft of a defined document type (email, letter, procedure, report section) | Timed sample before and after; pulse survey |
| Meeting-summary time | Minutes spent writing notes and action items after a meeting | Timed sample; Copilot Dashboard meeting recap metrics |
| Search and research time | Minutes to find an answer in policies, procedures, or prior documents | Timed lookups; contact-center hold or lookup time where captured |
| After-call documentation time | Minutes of wrap-up per contact | Contact-center platform after-call work time |
| Self-reported time saved | Minutes saved per week | Pulse survey |
| Tool-estimated assisted hours | Microsoft's estimate of hours assisted | Copilot Dashboard |

**Rules for Layer 2**

- Prefer system-measured task time over survey estimates. Use surveys to explain results, not as the main evidence.
- Report self-reported and tool-estimated hours as "estimated," never as realized savings.
- Measure the same task, the same way, before and after.

## Layer 3: Business outcomes

Did the business get measurably better? The business owner owns these numbers and their source.

| Outcome | Example metric | Typical source |
|---|---|---|
| Process cycle time | Average handle time; loan turnaround days; dispute resolution days; month-end close days | Contact-center platform, loan origination system, case system |
| Throughput | Contacts, files, or cases handled per FTE per day | Operational systems |
| Error and rework | QA failure rate; documents returned for correction; repeat contacts | QA program, case system |
| Capacity released | Hours redirected to defined higher-value work (callbacks, outreach, backlog) | Workforce management, with a documented redirection plan |
| Cost avoided | Backfill or overtime not needed; contractor hours avoided | Finance, HR |
| Member satisfaction | Member satisfaction score, Net Promoter Score, first-contact resolution | Survey platform, contact-center platform |
| Risk reduction | Documentation exceptions; complaint-handling timeliness; audit findings | QA, compliance testing, audit |
| Revenue or retention | Member retention; product adoption after service contact; cross-sell referrals | Core system, CRM |

**Rules for Layer 3**

- **Capacity is not cash.** Hours released count as value only when the organization records where they went, or avoids a cost.
- **Use a comparison.** Compare against baseline and, where possible, a similar group without Copilot over the same period. Note seasonality and other changes, such as new staff or a product launch.
- **One owner per outcome.** The business owner confirms the result before it is reported.
- **Report honestly.** If adoption is high and the outcome has not moved, say so and explain the next step.

## Guardrail metrics

| Guardrail | Metric | Source | Threshold |
|---|---|---|---|
| Quality | QA score on Copilot-assisted work against baseline | QA program | No decline |
| Quality | Output errors caught in review; errors that reached a member or decision | Pulse survey, incident log | Escaped errors: 0 at Sev 1 or 2 |
| Data risk | DLP policy matches on Copilot prompts and content | Purview | Trend down after training |
| Data risk | Oversharing signals reported | Incident log | All resolved within 5 days |
| Shadow AI | Detected use of unapproved AI services | Web filter or CASB | Trend down |
| Governance | Intake turnaround by tier | Intake log | Within service levels |
| Sentiment | "Copilot helps me do my job better" (1 to 5) | Pulse survey | 4.0 or higher |
| Sentiment | "I know what I can and cannot do with Copilot" (1 to 5) | Pulse survey | 4.0 or higher |

## From layer to layer: a worked chain

| Layer | Member Care example (fictional) |
|---|---|
| Adoption | 82% of 40 pilot agents active weekly; 90% passed the proficiency check |
| Productivity | After-call documentation from 4.5 to 2.8 minutes; knowledge lookup from 2.8 to 1.9 minutes |
| Business outcome | Average handle time down 6% against the comparison group; QA completeness failures from 12% to 7% |
| Value statement | About 285 agent-hours a month released at full rollout, based on the handle-time gain against the comparison group, redirected to outbound member callbacks. The larger task-level saving (about 1,300 hours) is shown as potential, not value (see [10](10-member-care-scenario.md)) |

## Reporting cadence

| Audience | Frequency | Content |
|---|---|---|
| AI Review Group | Monthly | Full scorecard, all layers and guardrails, intake queue, incidents |
| CTO and executive team | Monthly, one page | Layer 3 first, then Layers 2 and 1; risks; decisions needed |
| Board risk committee | Quarterly | Business outcomes, risk and guardrail summary, Tier 3 inventory, policy changes |

Put Layer 3 at the top of executive reports. Adoption is the reason a result can happen. It is not the result.

## Pulse survey (under one minute)

1. In the last two weeks, about how much time did Copilot save you per week? (None / under 30 min / 30 to 60 min / 1 to 2 hours / more than 2 hours)
2. What did you use that time for? (More member time / clearing backlog / other projects / not sure)
3. Did you catch an error in Copilot output? (Yes / No)
4. One task you wish Copilot could help with:
