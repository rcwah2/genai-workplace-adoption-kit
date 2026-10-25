# 07. Adoption Plan

Licensing makes Copilot available. Adoption makes it useful. This plan covers personas, role-based training, champions, communications, the prompt and use-case library, feedback loops, and the support model.

---

## 1. Personas

Design training, communications, and support around how each group works, not around product features.

| Persona | Typical work | What they need from Copilot | Main concern | Adoption approach |
|---|---|---|---|---|
| **Member Care agent** | High-volume calls and chats; documentation; knowledge lookups | Faster notes, quicker answers to procedure questions | "Will this be used to monitor or replace me?" | Short task-based labs; supervisor coaching; show time returned to members |
| **Branch member service rep** | Walk-in service, account opening, referrals | Procedure answers, member follow-up drafts | Accuracy in front of a member | Job aids at the desk; verify-the-source habit |
| **Lender or underwriter** | Loan files, conditions, policy interpretation | Guideline search, condition letter drafts | Fair-lending and compliance exposure | Clear Tier 2 rules; human-review checkpoints |
| **Operations and back office** | Disputes, exceptions, reconciliations, procedures | Summaries, job aids, spreadsheet analysis | Data accuracy | Excel and Word labs; sample-review practice |
| **Manager** | Meetings, reporting, coaching, approvals | Meeting recaps, status drafts, team insights | Knowing how to coach and what good looks like | Leader briefing; scorecard for their team |
| **Executive** | Board materials, strategy, decisions | Briefing summaries, document review | Value and risk in one view | 30-minute briefing; monthly one-page scorecard |
| **Risk, compliance, and audit reviewer** | Testing, policy, exam preparation | Regulation summaries, workpaper drafts | Evidence and audit trail | Governance walkthrough; access to evidence map |
| **IT and Microsoft 365 admin** | Configuration, support, security | Admin controls, reporting, troubleshooting | Oversharing and support load | Technical readiness runbook; Microsoft admin guidance |

## 2. Role-based training

| Module | Audience | Length | Required |
|---|---|---|---|
| Safe use of Copilot: the standard, data classes, human review, AI-enabled fraud awareness | Everyone | 30 min e-learning | Before access |
| Copilot fundamentals: prompts that work (goal, context, source, format), checking output, citing sources | Everyone | 45 min live | First week |
| Role labs: three to five real tasks from the persona's own work | By persona | 60 min | First month |
| Manager briefing: what to expect, how to coach, reading the scorecard | Managers | 30 min | Before team access |
| Champion training: advanced prompting, agent basics, coaching, feedback collection | Champions | 2 × 90 min | Champions |
| Refresher and new features | Everyone | 15 min monthly tip session | Recommended |

**AI proficiency check.** After the role lab, each user completes three persona tasks and one "spot the error" exercise. The result feeds the proficiency metric in [08](08-metrics-framework.md).

## 3. Champions network

| Element | Standard |
|---|---|
| Ratio | One champion per 25 to 40 users; at least one per department and per Member Care shift |
| Selection | Respected peers, not only the most technical people; include a frontline champion in every pilot |
| Time | About 2 hours a month, agreed with their manager |
| Role | Run short team demos, collect prompts and feedback, flag problems, coach colleagues |
| Cadence | Monthly champion call with the AI and Automation team |
| Recognition | Internal shout-outs, early access to new features, input to the roadmap |

## 4. Communications

| When | Message | Audience | Channel |
|---|---|---|---|
| Before pilot | Why we are doing this: more time for members and less rework, not fewer people | All staff | Executive message |
| Before pilot | What managers should expect and how to coach | Managers | Briefing |
| Pilot launch | How to get access, training, and help | Pilot cohort | Email, Teams |
| Weekly in pilot | Tip of the week; a featured use case from a colleague | Pilot cohort | Teams channel |
| End of pilot | Results, including what did not work, and the decision | All staff | Town hall, intranet |
| Scale phase | Department launch, champion names, training dates | Department | Department meeting |
| Monthly | Scorecard highlights and stories with numbers | All staff and leaders | Newsletter |

Be specific about workforce intent. If saved time will be redirected to member callbacks, backlog, or growth, say so, and report it.

## 5. Prompt and use-case library

The library turns individual wins into shared practice.

| Element | Standard |
|---|---|
| Location | One SharePoint page or list, organized by persona and task |
| Entry contents | Task, persona, tier, example prompt, required source, review step, expected time saved, owner |
| Quality gate | Tested by a champion on real work; reviewed by AI and Automation for tier and data rules |
| Tier rule | Tier 2 entries list their approval ID; Tier 3 entries are not self-service |
| Maintenance | Owner reviews each entry every 6 months; entries with poor feedback are revised or removed |
| Starter content | [reference/use-case-library.md](reference/use-case-library.md) |

## 6. Feedback loops

| Loop | Mechanism | Cadence | Feeds |
|---|---|---|---|
| In the moment | Thumbs up or down in Copilot; a "report a wrong answer" form | Continuous | Content fixes, incident log |
| Pulse survey | Two to four questions on time saved, quality, confidence | Every 2 weeks in pilot, monthly after | Productivity and sentiment metrics |
| Champion round-up | Top three wins and top three problems per department | Monthly | Library, training, roadmap |
| Content correction | Wrong answers routed to the source document owner for a fix | Within 5 business days | Data and content quality |
| Governance review | Incidents, exceptions, and intake trends | Monthly | Standard and control updates |

Close the loop publicly: each month, publish what changed because of feedback.

## 7. Support model

| Tier | Who | Handles |
|---|---|---|
| **Self-help** | Prompt library, job aids, short videos | How-to questions |
| **Peer** | Champions | Coaching, prompt help, "is this allowed?" |
| **Service desk** | IT service desk with a Copilot script | Access, licensing, app problems |
| **Specialist** | AI and Automation team; Microsoft 365 admin | Agents, grounding problems, wrong answers, tier questions |
| **Security** | Information Security | Suspected data exposure, prompt injection, incidents |
| **Vendor** | Microsoft support | Product defects and service issues |

Service desk tickets are tagged "Copilot" so support volume and themes appear in the monthly scorecard.
