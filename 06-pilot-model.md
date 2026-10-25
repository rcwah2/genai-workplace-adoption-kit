# 06. Pilot Model

```
Intake → Assessment → Approve → Baseline → Pilot → Measure → Decide → Scale
```

Each stage has an entry condition, a defined output, and an owner. A candidate cannot skip a stage. The pilot ends in an explicit decision against criteria agreed before it started.

---

## Stage by stage

| # | Stage | Entry condition | Key activities | Output | Gate owner |
|---|---|---|---|---|---|
| 1 | **Intake** | A business problem exists | Complete the [Phase 0 intake](02-phase-0-opportunity-intake.md): problem, owner, data, maturity, expected outcome | Signed intake record | AVP AI and Automation |
| 2 | **Assessment** | Intake accepted | Run the relevant [readiness checks](03-readiness-assessment.md) for this use case's data and users; score with the [prioritization model](04-prioritization-model.md); propose a tier | Readiness ratings, score, proposed tier | AI Review Group |
| 3 | **Approve** | No blocking red ratings; score and wave assigned | Tier decision and conditions per [governance](05-governance-model.md); success criteria and stop criteria written and signed | Approval record with conditions | Per tier decision rights |
| 4 | **Baseline** | Approved | Measure current state for 4 to 8 weeks; select a comparison group where possible | Locked baseline report | Business owner |
| 5 | **Pilot** | Baseline locked; training complete | 6 to 10 weeks with a defined cohort; weekly office hours; champion support; feedback channel | Usage, feedback, and incident log | Day-to-day lead |
| 6 | **Measure** | Pilot period complete | Report adoption, productivity, and business-outcome results separately ([08](08-metrics-framework.md)); compare with baseline and comparison group | Pilot results report | AVP AI and Automation |
| 7 | **Decide** | Results report issued | Decision meeting against the pre-agreed criteria | Scale / extend / redesign / stop decision | Business owner and AVP AI and Automation |
| 8 | **Scale** | Scale decision | Rollout plan by department; license allocation; [adoption plan](07-adoption-plan.md); ongoing monitoring by tier | Rollout plan and updated inventory | CTO |

## Pilot design standards

| Element | Standard |
|---|---|
| Cohort size | 25 to 100 users per use case; enough for a meaningful comparison, small enough to support closely |
| Cohort mix | Include skeptics and average performers, not only enthusiasts |
| Comparison group | A similar team or shift without Copilot for the same period, where practical |
| Duration | 6 to 10 weeks after training; a 2-week ramp is excluded from results |
| Use cases | 2 to 4 per cohort, each with its own metric |
| Content scope | Copilot grounded only on remediated, owned sites; Restricted Content Discovery on the rest |
| Support | Weekly office hours, a Teams channel, champion check-ins, help-desk script |
| Data collection | System metrics where possible; a pulse survey every 2 weeks; QA sampling for Tier 2 |

## Success criteria and stop criteria

Write both before the pilot starts. Example:

| Type | Criterion |
|---|---|
| **Adoption** | 70% or more of the cohort active weekly by week 6 |
| **Productivity** | Target task time down 25% or more against baseline |
| **Business outcome** | At least one outcome metric (handle time, cycle time, error rate) improves against both baseline and comparison group |
| **Quality** | No drop in QA scores |
| **Risk** | No unresolved Sev 1 or Sev 2 incident |
| **Stop** | Any Sev 1 incident; QA scores fall more than 5 points; weekly active use under 40% at week 6 despite coaching |

## The decision

| Decision | When | What happens next |
|---|---|---|
| **Scale** | Success criteria met; risk within appetite | Roll out to the wider population in waves; move to ongoing monitoring |
| **Extend** | Promising but inconclusive; for example, adoption met but the outcome metric is not yet clear | Up to 6 more weeks with a specific fix; one extension only |
| **Redesign** | Value exists but the use case, content, or process needs changing | Return to Approve with a revised design |
| **Stop** | Stop criteria hit, or no measurable value after extension | Reclaim licenses; record lessons; close in the inventory |

A stop decision is a valid result. It saves license cost, protects credibility, and is recorded as evidence that governance works.

## Pilot results report (one page)

1. Use case, owner, cohort, dates
2. Adoption results against target
3. Productivity results against baseline
4. Business-outcome results against baseline and comparison group
5. Quality and risk results, incidents
6. What users said (top three themes)
7. Cost: licenses, effort, remediation
8. Recommendation and decision requested
