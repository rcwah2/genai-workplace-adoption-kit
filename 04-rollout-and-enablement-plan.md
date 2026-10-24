# 04. Rollout and Enablement Plan

A phased plan that fixes data permissions before broad access, proves value with a pilot, and then scales with training, champions, and measurement. The phases follow Microsoft's recommended Pilot, Deploy, Operate pattern for addressing oversharing ([Microsoft](https://techcommunity.microsoft.com/blog/microsoft-copilot-blog/mitigate-oversharing-to-govern-microsoft-365-copilot-and-agents/4448744)), with a readiness phase added in front.

---

## Phase overview

| Phase | Timing | Goal | Exit criteria |
|---|---|---|---|
| **0. Readiness** | Weeks 0 to 4 | Policy, data protection, and baseline in place | Acceptable Use Standard approved; oversharing review done for top sites; sensitivity labels and DLP (data loss prevention) policies in place, at least in simulation; training ready; baselines collected for pilot use cases |
| **1. Pilot** | Weeks 5 to 12 | Prove value and find problems with 50 to 100 users | At least 60% of pilot users active weekly; at least 5 use cases with measured time savings; no unresolved high-severity data incidents; feedback themes addressed |
| **2. Scale** | Months 4 to 6 | Expand by department, with champions and role-based training | Department rollouts complete; champions in every department; scorecard reported monthly |
| **3. Operate** | Month 7 onward | Continuous improvement and new Tier 2 and Tier 3 uses | Quarterly value report; semi-annual standard review; intake running within turnaround targets |

## Phase 0: Readiness

**Policy and governance**
- Approve the [Acceptable Use Standard](01-acceptable-use-standard.md) and the [intake and risk tiers](02-intake-and-risk-tiers.md).
- Stand up the AI Review Group (business owner, AI and Automation, Information Security, Compliance, Legal as needed, Data and Analytics).
- Add generative AI to the AI system inventory and the vendor management program.

**Data protection** (Microsoft 365)
Microsoft's guidance is to fix oversharing first and then set guardrails ([Microsoft](https://learn.microsoft.com/en-us/copilot/microsoft-365/configure-data-security-copilot)):
- Review the most-used SharePoint sites and Teams for overly broad access; remove "everyone" style sharing where it is not needed.
- Use Restricted SharePoint Search or Restricted Content Discovery as an interim control for sensitive sites.
- Publish sensitivity labels (Public, Internal, Confidential, Restricted) and apply default labels.
- Configure Purview DLP policies for Copilot to block processing of Restricted-labeled content and prompts containing sensitive data types, running in simulation first.
- Turn on audit logging and confirm retention and eDiscovery settings for Copilot interactions.

**ChatGPT Enterprise**
- Single sign-on and automated provisioning (SCIM), so access ends when employment ends.
- Set the workspace retention period, decide on connector and GPT-sharing permissions, and enable Compliance API logging ([OpenAI](https://openai.com/business-data/)).

**Baseline**
- Survey pilot users on time spent on target tasks.
- Record process baselines (handle time, turnaround time, hours per report).

## Phase 1: Pilot

- **Who:** 50 to 100 users across Member Care, Lending, Operations, Finance, Compliance, Marketing, HR, and IT, mixing enthusiasts with skeptics.
- **What:** 10 to 15 starter use cases from the [library](03-use-case-library.md), mostly Tier 1 plus two or three Tier 2.
- **Support:** weekly 30-minute office hours, a Teams channel, and a shared prompt library.
- **Measure:** weekly active use, a biweekly two-question pulse survey (time saved, quality), and incidents.
- **Close-out:** a pilot report to the CTO and executive team with value, issues, and the scaling recommendation.

## Phase 2: Scale

- Roll out department by department, led by each department's champion.
- Role-based training labs (60 minutes) using that department's real tasks.
- Expand the prompt library and promote proven Tier 2 agents.
- Begin monthly scorecard reporting ([05](05-value-scorecard.md)).

## Phase 3: Operate

- Quarterly value report to executives and the board risk committee.
- Review the Acceptable Use Standard every six months.
- License optimization: reassign unused licenses based on activity.
- Use intake to bring in Tier 2 and Tier 3 opportunities, such as process automation and member-facing uses.

---

## Roles and responsibilities

| Activity | AI & Automation | IT / M365 Admin | Info Security | Compliance / Risk | Training (C&TD) | Dept. leaders | Champions |
|---|---|---|---|---|---|---|---|
| Acceptable Use Standard | **A/R** | C | C | C | I | I | I |
| Data protection setup | C | **R** | **A** | C | — | — | — |
| Intake and tiering | **A/R** | C | C | C | — | R (submit) | C |
| Training content | **A** | C | C | C | **R** | C | C |
| Department rollout | A | C | — | — | C | **R** | **R** |
| Scorecard | **A/R** | C (data) | C | I | I | I | C |
| Incident handling | R | R | **A** | C | — | I | I |

A = accountable, R = responsible, C = consulted, I = informed.

## Training curriculum

| Module | Audience | Length | Required? |
|---|---|---|---|
| Safe Use of Generative AI (standard, data classes, review, fraud awareness) | All users | 30 min e-learning | Yes, before access |
| Prompting basics: role, task, context, format; checking output | All users | 45 min live or recorded | Yes |
| Role-based labs (Member Care, Lending, Operations, Finance, and so on) | By department | 60 min | Recommended |
| Champion training: advanced prompting, building agents, coaching others | Champions | 2 x 90 min | For champions |
| Leader briefing: value, risk, and what to ask your teams | Managers and executives | 30 min | Yes, for managers |

## Champions network

- One champion per 25 to 40 users, with at least one per department.
- About 2 hours per month: share wins, collect feedback, and run short team demos.
- Recognition: shout-outs in internal communications, plus a champion badge in Teams.

## Communications plan

| When | Message | Channel |
|---|---|---|
| Week 0 | Why we are doing this: more time for Members, not fewer people | Executive message |
| Week 4 | Pilot launch and how to get help | Email, Teams |
| Weekly during pilot | Tip of the week; a featured use case | Teams channel |
| End of pilot | Results and what's next | Town hall |
| Monthly after | Scorecard highlights, success stories | Newsletter |

## Common pitfalls

- **Switching it on before fixing permissions:** users see files they shouldn't.
- **Training once and stopping:** adoption drops after week three without coaching.
- **Counting logins as success:** report time returned and process results instead.
- **Ignoring shadow AI:** personal tool use continues unless the approved tools are easier and better.
