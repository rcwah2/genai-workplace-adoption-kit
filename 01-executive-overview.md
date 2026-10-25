# 01. Executive Overview

## The problem

Most organizations buy Microsoft 365 Copilot licenses before they decide what Copilot is for. The usual result:

- **Licenses without a business case.** Seats go to enthusiasts or senior staff, not to the work with the most value.
- **Risk found after launch.** Copilot respects existing permissions, so years of overshared SharePoint sites and Teams suddenly become easy to search.
- **Activity reported as value.** Leaders get counts of active users and prompts, but no answer to "what changed in the business?"
- **No decision point.** Pilots drift into production, or quietly fade, without anyone deciding to scale, change, or stop.

Microsoft publishes detailed deployment guidance, including its oversharing blueprint and readiness checklists ([Microsoft](https://learn.microsoft.com/en-us/copilot/microsoft-365/configure-data-security-copilot)). That guidance covers how to configure the product. It does not cover which business problems to fund, who approves them, or how to show a board that the investment paid off.

## What this framework adds

| Microsoft's deployment guidance covers | This framework covers |
|---|---|
| Licensing, update channels, tenant settings | Which business problems justify a license, and who owns each one |
| Oversharing tools (SharePoint Advanced Management, Purview) | Readiness gates leadership signs off before go-live |
| Copilot Analytics usage and assisted-hours reports | A three-layer measurement model: adoption, productivity, business outcomes |
| Adoption resources and training content | Decision rights, risk tiers, exceptions, incident escalation, and scale-or-stop gates |

## How it maps to Microsoft's guidance

This framework builds on Microsoft's guidance; it does not replace it. Microsoft's oversharing blueprint runs in three phases, Pilot, Deploy, and Operate ([Microsoft Tech Community](https://techcommunity.microsoft.com/blog/microsoft-copilot-blog/mitigate-oversharing-to-govern-microsoft-365-copilot-and-agents/4448744)), and its data-security foundation is to fix oversharing first and then set guardrails ([Microsoft](https://learn.microsoft.com/en-us/copilot/microsoft-365/configure-data-security-copilot)). Use Microsoft's documentation for configuration steps and this framework for the leadership decisions around them.

| Framework stage | Related Microsoft guidance | What this framework adds |
|---|---|---|
| Intake ([02](02-phase-0-opportunity-intake.md)) | Not covered directly | Business problem, accountable owner, baseline, data declared, process maturity, expected outcome |
| Assessment ([03](03-readiness-assessment.md)) | Readiness and oversharing remediation with SharePoint Advanced Management and Purview ([Microsoft](https://learn.microsoft.com/microsoft-365/copilot/get-ready-copilot-sharepoint-advanced-management)) | Red/amber/green ratings across nine domains, including organizational and change readiness, with a signed go/no-go gate |
| Approve ([04](04-prioritization-model.md), [05](05-governance-model.md)) | Admin controls and Copilot settings | Weighted prioritization, gate rules, decision rights, risk tiers, exceptions |
| Baseline ([08](08-metrics-framework.md)) | Not covered directly | Current-state measures locked before licenses are assigned; comparison group |
| Pilot ([06](06-pilot-model.md)) | Pilot phase: a subset of users with access to low-risk sites | Cohort design, success criteria, and stop criteria agreed in advance |
| Measure ([08](08-metrics-framework.md)) | Copilot Analytics: readiness, adoption, impact, sentiment ([Microsoft](https://learn.microsoft.com/en-us/viva/insights/copilot-analytics-introduction)) | Three separate layers (adoption, productivity, business outcomes) with guardrails; business owner confirms outcomes |
| Decide ([06](06-pilot-model.md)) | Not covered directly | Scale, extend, redesign, or stop, recorded as governance evidence |
| Scale ([07](07-adoption-plan.md), [09](09-30-60-90-roadmap.md)) | Deploy and Operate phases: broad rollout with guardrails, ongoing governance | Wave plan, persona-based adoption, tier-based monitoring, board reporting |

Microsoft updates its guidance often. Check the linked pages before relying on a specific feature or step.

## Who it is for

- **Primary:** credit unions and community banks with 300 to 1,000 employees, on Microsoft 365 E3 or E5, supervised by NCUA, a state regulator, or a federal banking agency.
- **Also fits:** insurers, healthcare providers, and public-sector organizations with similar data-protection and audit obligations.
- **Audience:** CTO or CIO, AVP or Director of AI and Automation, CISO, Chief Risk Officer, Compliance, department heads.

## Operating model at a glance

```
Intake → Assessment → Approve → Baseline → Pilot → Measure → Decide → Scale
```

1. **Intake ([02](02-phase-0-opportunity-intake.md))**: every candidate starts as a business problem with an owner, baseline metrics, and an expected outcome.
2. **Assessment ([03](03-readiness-assessment.md))**: tenant, data, security, compliance, and people readiness are checked against go/no-go thresholds.
3. **Approve ([04](04-prioritization-model.md), [05](05-governance-model.md))**: candidates are scored, risk-tiered, and approved by the right decision owner.
4. **Baseline ([08](08-metrics-framework.md))**: current-state measurements are locked before anyone gets a license.
5. **Pilot ([06](06-pilot-model.md))**: a time-boxed pilot with a defined cohort, use cases, and success criteria.
6. **Measure ([08](08-metrics-framework.md))**: adoption, productivity, and business-outcome results are reported separately.
7. **Decide ([06](06-pilot-model.md))**: scale, extend, redesign, or stop, against criteria agreed in advance.
8. **Scale ([07](07-adoption-plan.md), [09](09-30-60-90-roadmap.md))**: department-by-department rollout with champions, role-based training, and ongoing governance.

## Principles

1. **Start from the business problem, not the license.**
2. **Fix permissions before switching it on.**
3. **Tier by impact, not by tool.**
4. **People stay accountable for every output that reaches a member or a decision.**
5. **Adoption is not value.** Report the three measurement layers separately.
6. **Earn the right to scale.** Every pilot ends in an explicit decision.
7. **One inventory.** Every approved use, agent, and connector is recorded and has an owner.

## What leadership gets

- A short, ranked list of Copilot opportunities, each tied to a measurable outcome.
- A signed-off readiness position covering permissions, labeling, DLP, retention, and audit.
- Clear decision rights, so routine use moves quickly and high-impact use gets full review.
- A monthly one-page scorecard that shows the business result, not only usage.
- A documented scale-or-stop decision after each pilot, which also serves as exam and audit evidence.

## Applying it to other assistants

The governance, intake, prioritization, and metrics model is tool-neutral. The same approach applies to ChatGPT Enterprise, Copilot Studio agents, or AI features built into vendor platforms. Only the readiness checks in [03](03-readiness-assessment.md) are specific to Microsoft 365.
