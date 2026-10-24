# 03. Starter Use-Case Library

Thirty starter use cases for a credit union, grouped by department. Start with Tier 1 uses to build skills and trust; move to Tier 2 once permission fixes and training are in place.

**Key:** Tier = risk tier from [02](02-intake-and-risk-tiers.md). Data = highest data class used. Tool: M365 = Microsoft 365 Copilot; Chat = Copilot Chat or ChatGPT Enterprise; Agent = Copilot agent or custom GPT.

---

## Member Care Center and branches

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 1 | Search procedures and product rules in plain language ("What are the hold rules for a mobile deposit over $5,000?") | 2 | Internal | Agent | Time to find an answer; calls transferred for help |
| 2 | Draft a follow-up email after a member conversation, using approved templates | 1 | Internal (no member identifiers) | M365 | Minutes per email |
| 3 | Summarize a long member complaint thread for a supervisor | 2 | Restricted | M365 | Time to prepare an escalation |
| 4 | Create role-play scripts for new-hire training (fee reversals, fraud claims) | 1 | Internal | Chat | Time for new hires to reach proficiency |
| 5 | Translate approved member materials into Spanish for review by a bilingual team member | 1 | Public / Internal | Chat | Turnaround time |

## Lending

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 6 | Answer questions about underwriting guidelines and stip requirements | 2 | Internal | Agent | Questions to the underwriting desk |
| 7 | Draft condition letters and requests for missing documents from a checklist | 2 | Restricted | M365 | Minutes per file |
| 8 | Summarize a commercial or business loan narrative for credit committee | 2 | Confidential | M365 | Analyst prep hours |
| 9 | Compare loan policy revisions and highlight changes | 1 | Internal | M365 | Review time |
| 10 | Draft dealer communication and indirect lending program updates | 1 | Internal | Chat | Minutes per communication |

> Credit decisions stay with people. Any use that influences a credit decision is Tier 3 and needs fair-lending review.

## Operations and deposit services

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 11 | Turn procedure updates into step-by-step job aids | 1 | Internal | M365 | Hours per job aid |
| 12 | Summarize Reg E dispute case notes into a standard format for review | 2 | Restricted | M365 | Minutes per case; timeliness |
| 13 | Reconcile procedure differences between legacy and acquired credit unions after a merger | 2 | Internal | M365 | Hours to produce a unified procedure |
| 14 | Draft exception reports and highlight trends from exported spreadsheets | 1 | Confidential | M365 (Excel) | Report prep time |

## Fraud, BSA/AML, and risk

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 15 | Summarize fraud typology bulletins and regulatory alerts for staff | 1 | Public | Chat | Hours per briefing |
| 16 | Draft risk assessment narratives from completed control templates | 2 | Confidential | M365 | Hours per assessment |
| 17 | Draft vendor due-diligence summaries from SOC reports and questionnaires | 2 | Confidential | M365 | Hours per vendor review |
| 18 | Draft SAR narratives | 3 | Prohibited in general tools | Dedicated, approved BSA platform only | — (not a general-assistant use) |

## Finance and accounting

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 19 | Draft variance commentary for the monthly board package | 2 | Confidential | M365 (Excel, Word) | Close-cycle hours |
| 20 | Explain complex formulas and build new ones in budget models | 1 | Confidential | M365 (Excel) | Analyst hours |
| 21 | Summarize vendor contracts for renewal dates, pricing terms, and termination clauses | 2 | Confidential | M365 | Hours per contract |

## Compliance, audit, and legal

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 22 | Summarize new regulations and compare them with current policy | 1 | Public / Internal | Chat / M365 | Hours per regulatory review |
| 23 | Draft audit workpaper narratives from testing results | 2 | Confidential | M365 | Hours per workpaper |
| 24 | First-pass review of marketing material against disclosure checklists | 2 | Internal | Agent | Review turnaround time |

## Marketing and communications

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 25 | Draft campaign copy, newsletter articles, and social posts within brand standards | 1 | Public / Internal | Chat | Drafts per week |
| 26 | Summarize member survey comments into themes | 2 | Confidential (de-identified) | M365 | Analysis hours |

## HR and training (C&TD)

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 27 | Draft job descriptions and interview guides | 1 | Internal | Chat | Hours per requisition |
| 28 | Build training modules and quizzes from procedures | 1 | Internal | M365 | Hours per module |

> Using AI to screen, rank, or evaluate candidates or employees is Tier 3.

## IT and project management

| # | Use case | Tier | Data | Tool | Value measure |
|---|---|---|---|---|---|
| 29 | Draft project status reports, risk logs, and meeting minutes from Teams meetings | 1 | Internal | M365 (Teams) | PM hours per week |
| 30 | Explain scripts and draft documentation for internal tools (no credentials or security configuration) | 1 | Internal | Chat | Documentation hours |

---

## How to pick the first ten

Score each candidate from 1 to 5 on:
- **Volume:** how often the task happens
- **Time per task:** minutes saved each time
- **Data risk:** lower is better (Public or Internal first)
- **Measurability:** a baseline exists or is easy to collect
- **Sponsor:** a leader wants it and will champion it

Start with the highest totals. Aim for at least one use case in Member Care, Lending, Operations, and Finance so every major area sees value early.
