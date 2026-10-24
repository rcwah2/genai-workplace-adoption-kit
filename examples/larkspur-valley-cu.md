# Worked Example: Larkspur Valley Credit Union (fictional)

> **Fictional organization.** Larkspur Valley Credit Union and all figures below are invented to show how the kit is used. They are not benchmarks.

**Profile:** $3.1 billion in assets, 160,000 members, 420 team members, 20 branches, recently completed two mergers. Microsoft 365 E5 tenant; ChatGPT Enterprise workspace for 60 users.

---

## Situation

Team members had been using personal AI accounts for drafting and summarizing. Licenses for Microsoft 365 Copilot were purchased for 150 users, but there was no usage policy, no intake process, and no way to show value. A permission review found several SharePoint sites from the merged credit unions shared with "everyone."

## Phase 0 decisions (weeks 0 to 4)

- Acceptable Use Standard approved by the CTO, CRO, ISO, and Compliance.
- 14 overshared SharePoint sites remediated; Restricted SharePoint Search used for HR and Finance sites until cleanup was done.
- DLP for Copilot set to block Restricted-labeled content, run in simulation for two weeks first.
- Baselines collected for six pilot use cases.

## Sample Tier 2 intake decision

| Field | Entry |
|---|---|
| Intake ID | GAI-2026-007 |
| Use case | Member Care procedures agent: answers staff questions using the approved procedures library |
| Business owner | VP, Member Care |
| Tool | Copilot agent grounded in one SharePoint library |
| Highest data class | Internal |
| Reaches members | No; staff use answers in their own words |
| Human review | Agent cites the source procedure for every answer; staff confirm |
| Tier | 2 |
| Decision | Approve with conditions: one curated library only; monthly sample of 30 answers; procedure owners notified when an answer is flagged as wrong |
| Success measure | Escalations to the supervisor help line, down from a baseline of 410 per month |

## Day-90 scorecard snapshot (illustrative)

| Metric | Result |
|---|---|
| Enabled / active users (28 days) | 150 / 112 (75%) |
| Habitual use (3+ days per week) | 38% |
| Self-reported time saved | Median 1 to 2 hours per user per week |
| Verified use cases | 7 |
| Member Care help-line escalations | 410 to 300 per month (down 27%) |
| Data incidents | 1 (member account number pasted into Copilot Chat; contained, no external exposure; retraining completed) |
| Usefulness / confidence | 4.1 / 3.8 |

## Lessons

- Fixing permissions took longer than licensing. Start it first.
- Champions mattered more than training videos; the most-used prompts came from frontline staff.
- Reporting where saved time went (member callbacks, backlog cleared) made the value story credible to the board.
