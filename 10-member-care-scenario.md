# 10. Scenario: Microsoft 365 Copilot for Member Care

> **Fictional organization.** Larkspur Valley Credit Union and every figure below are invented to show how the framework works. They are not benchmarks or predictions.

**Profile:** $3.1 billion in assets, 160,000 members, 420 employees, 20 branches, two recent mergers. Microsoft 365 E5 tenant. Member Care Center of 85 agents handling about 38,000 contacts a month in a separate contact-center platform.

---

## 1. Phase 0 intake

| Field | Entry |
|---|---|
| Intake ID | CPL-2026-004 |
| Problem statement | Member Care agents spend about 4.5 minutes per contact on after-call notes and about 2.8 minutes per lookup searching procedures from three merged libraries. Handle time is high, notes are inconsistent, and new hires take 10 weeks to become proficient. We want shorter, more consistent documentation, faster answers, and quicker onboarding without lowering quality. |
| Accountable owner | VP, Member Care |
| Day-to-day lead | Member Care Operations Manager |
| Executive sponsor | Chief Operating Officer |
| Data involved | Internal procedures; member account details in after-call notes (Restricted) |
| Process maturity | Level 4, measured: contact-center platform reports handle time, wrap-up time, and first-contact resolution; QA program in place |
| Security and privacy | Restricted member data in notes; call recording consent rules apply; no system actions; no member-facing output |
| Expected outcome | Handle time down 8%, first-contact resolution up 3 points, onboarding down to 8 weeks, within two quarters |

## 2. Readiness findings (summary)

| Domain | Rating | Note |
|---|---|---|
| Permissions and oversharing | Amber | 14 legacy SharePoint sites from the merged credit unions shared with "everyone"; Restricted Content Discovery applied while owners complete access reviews |
| Data classification | Amber | Labels published; auto-labeling for account numbers in simulation |
| Security | Green | DLP for Copilot excludes Restricted-labeled files from processing and blocks prompts containing card, Social Security, or full account numbers (moved from simulation to enforcement before launch) |
| Records and retention | Green | Copilot interactions retained under the member-service records schedule |
| Organizational readiness | Amber | Procedures in three libraries with duplicates; consolidated library of 220 procedures completed in week 3 |
| Change readiness | Green | Frontline champion on each shift; job-impact message from the COO |

Go decision for the pilot scope, with conditions.

## 3. Baseline (8 weeks of contact-center data, before the pilot)

| Measure | Baseline |
|---|---|
| After-call documentation | 4.5 minutes per contact |
| Knowledge lookup | 2.8 minutes per lookup; about 40% of contacts need one |
| Average handle time | 7.9 minutes |
| First-contact resolution | 71% |
| QA completeness failures on notes | 12% |
| New-hire time to proficiency | 10 weeks |

## 4. Pilot design

- **Cohort:** 40 agents across both shifts, including 6 new hires. **Comparison group:** the other 45 agents, same period.
- **Duration:** 8 weeks after a 2-week ramp.
- **Content scope:** Copilot grounded on the consolidated procedures library and Member Care team sites only.

| Pilot use case | How it works | Tier | Key control |
|---|---|---|---|
| Teams meeting and call summary | Recaps of shift huddles, supervisor escalation calls, and procedure-change briefings held in Teams | 1 | Transcription notice in every meeting; recaps checked by the meeting owner |
| Approved policy knowledge search | A Copilot agent grounded only on the consolidated procedures library, citing the source procedure in every answer | 2 | One curated library; monthly sample of 30 answers; wrong answers routed to the procedure owner |
| Draft after-call notes | Agent enters rough notes; Copilot drafts a structured note using the approved template; agent reviews and pastes it into the contact-center platform | 2 | Work account only; masking guidance for identifiers; DLP for card and Social Security numbers; agent review of every note |
| Employee assistance | Copilot Chat for new-hire questions on procedures, systems, and HR policies, with links to source pages | 2 | Shared, repeatable use for a defined group; grounded on approved internal content; trainers review common questions weekly; no member data in prompts |

**Success criteria:** 70% weekly active use by week 6; documentation time down 25%; handle time improves against the comparison group; no drop in QA scores; no unresolved Sev 1 or Sev 2 incident.
**Stop criteria:** any Sev 1 incident; QA score down more than 5 points; weekly active use under 40% at week 6.

## 5. Results at the end of the pilot (illustrative)

### Layer 1: Adoption

| Metric | Result |
|---|---|
| Weekly active users | 82% of cohort |
| Training completion | 100% |
| AI proficiency check passed | 90% |
| Month-1 to month-2 retention | 94% |

### Layer 2: Productivity

| Metric | Baseline | Pilot | Change |
|---|---|---|---|
| After-call documentation | 4.5 min | 2.8 min | Down 38% |
| Knowledge lookup | 2.8 min | 1.9 min | Down 32% |
| Supervisor time writing huddle and escalation notes | 3.0 hrs/wk | 1.2 hrs/wk | Down 60% |

### Layer 3: Business outcomes

| Metric | Baseline | Pilot cohort | Comparison group | Read-out |
|---|---|---|---|---|
| Average handle time | 7.9 min | 7.4 min | 7.85 min | Down about 6% against comparison |
| First-contact resolution | 71% | 73% | 71.5% | Up 1.5 points against comparison; directional, not yet conclusive |
| QA completeness failures | 12% | 7% | 11.5% | Improved |
| New-hire time to proficiency | 10 weeks | 8.5 weeks (6 new hires) | 10 weeks | Promising; sample too small to conclude |

### Guardrails

| Guardrail | Result |
|---|---|
| QA scores | No decline; completeness improved |
| Incidents | One Sev 3: an agent pasted a full account number into a prompt; DLP blocked it; agent coached |
| Wrong knowledge-search answers | 4 of 120 sampled; all traced to two outdated procedures, which were corrected |
| Usefulness / confidence | 4.3 / 4.0 |

### Capacity

Two numbers are reported, and only one counts as value.

| Measure | Calculation | Hours a month at full rollout | Layer |
|---|---|---|---|
| **Capacity released (reported)** | Handle-time gain against the comparison group: 0.45 minutes × 38,000 contacts | **About 285** | Business outcome |
| Task-level potential (not reported as value) | Documentation saving 1.7 minutes × 38,000, plus lookup saving 0.9 minutes × 15,200 lookups | About 1,300 | Productivity |

The gap is expected. Agents spent part of the documentation saving reviewing and correcting drafts, and some after-call work overlaps with time already counted inside the call. Only the handle-time gain is confirmed in the contact-center data, so only that figure goes on the scorecard. The task-level figure shows the upside if the review step gets faster as agents gain confidence; it is retested at the next quarterly read-out.

Leadership agreed in advance to redirect released hours to outbound callbacks for members with open service issues. Workforce management tracks this as the capacity-released metric.

## 6. Decision

| Use case | Decision | Rationale |
|---|---|---|
| Draft after-call notes | **Scale** to all 85 agents | Documentation time down 38%; handle time down about 6% against the comparison group, on track toward the 8% two-quarter target; QA improved |
| Policy knowledge search | **Scale**, with a quarterly content review | Faster lookups; errors were content problems, not Copilot problems |
| Teams meeting and call summary | **Scale** to all supervisors and managers | Low risk, clear time saving |
| Employee assistance for new hires | **Extend** through the next two hiring classes | Promising onboarding signal; sample too small |

**Wave 2 candidates:** board-package variance commentary (Finance) and loan condition letters (Lending), after Lending completes a Tier 3 review (member-facing credit communications raise fair-lending and UDAP/UDAAP questions).

## 7. Lessons

- Permission cleanup took longer than licensing. Start it on day one.
- The consolidated procedures library was worth doing for its own sake. Copilot made the duplicates visible.
- Frontline champions produced the most-used prompts.
- Reporting handle time against a comparison group, and stating where saved hours went, made the result credible to the board. Self-reported time savings alone would not have.
