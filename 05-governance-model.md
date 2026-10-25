# 05. Governance Model

Governance should move routine use quickly and focus review where member, regulatory, or operational impact is real. This document sets out decision rights, the RACI, the acceptable-use framework, human oversight, risk tiers, exceptions, vendor governance, and incident escalation.

---

## 1. Decision rights

| Decision | Decides | Advises | Escalates to |
|---|---|---|---|
| Copilot program strategy, budget, license volume | CTO | AVP AI and Automation, CFO | Executive team |
| Acceptable-use standard and changes | AI Governance Committee | Information Security, Compliance, Legal, HR | CTO and CRO |
| Readiness go/no-go | CTO | CISO, Compliance, AVP AI and Automation | CRO for risk acceptance |
| Tier 1 use | User, within the standard | Champions | — |
| Tier 2 use case approval | AI Review Group | Business owner, Information Security, Compliance | AI Governance Committee |
| Tier 3 use case approval | Business executive and CRO | AI Governance Committee | Board risk committee (informed) |
| New agent, connector, or plug-in | AI Review Group (Tier 2) or CRO (Tier 3) | Vendor Management, Information Security | AI Governance Committee |
| Exception to the standard | See Section 6 | | |
| Scale, extend, redesign, or stop a pilot | Business owner and AVP AI and Automation | AI Review Group | CTO |
| Suspend a use case after an incident | CISO or AVP AI and Automation, immediately | Business owner | CTO |

**Bodies**

- **AI Governance Committee** (monthly): CTO (chair), CRO, CISO, Compliance, Legal, HR, AVP AI and Automation. Owns policy, risk appetite, Tier 3 oversight, and the quarterly board report.
- **AI Review Group** (weekly or biweekly): AVP AI and Automation (chair), Information Security, Compliance, Microsoft 365 administration, Data and Analytics, plus the business owner of each item. Runs intake, tiering, and Tier 2 approvals.

## 2. RACI

| Activity | AVP AI & Automation | CTO | IT / M365 Admin | Info Security | Compliance / Risk | Legal | Training (C&TD) | Business owner | Champions |
|---|---|---|---|---|---|---|---|---|---|
| Program strategy and roadmap | R | **A** | C | C | C | I | I | C | I |
| Phase 0 intake | **A/R** | I | C | C | C | — | — | R | C |
| Readiness assessment | R | **A** | R | R | R | C | C | C | — |
| Oversharing remediation | C | I | **R** | **A** | C | — | — | R (site owners) | — |
| Prioritization and wave plan | **A/R** | C | C | C | C | — | — | R | C |
| Acceptable-use standard | **A/R** | C | C | C | C | C | I | I | I |
| Pilot design and baseline | **A** | I | C | C | C | — | C | **R** | C |
| Training and enablement | A | I | C | C | C | — | **R** | C | R |
| Scorecard and value reporting | **A/R** | I | C (data) | C | I | — | I | R (outcome data) | C |
| Scale-or-stop decision | R | C | C | C | C | — | I | **A** | I |
| Incident handling | R | I | R | **A** | C | C | — | C | I |
| Board and exam reporting | R | **A** | I | C | R | C | — | I | — |

A = accountable (one per row), R = responsible, C = consulted, I = informed.

## 3. Acceptable-use framework

The full employee standard is in [reference/acceptable-use-standard.md](reference/acceptable-use-standard.md). Its structure:

| Element | Rule in brief |
|---|---|
| Approved tools | Microsoft 365 Copilot and Copilot Chat signed in with a work account. Agents, connectors, and third-party AI features need approval. Personal AI accounts are not approved for non-public information. |
| Data classes | Public, Internal, Confidential, Restricted, and Prohibited, each with a clear rule for what may be entered |
| Human review | The user owns the output. Anything going to a member is reviewed before it is sent. |
| Prohibited uses | AI as the sole basis for credit, account, pricing, or employment decisions; impersonation; bypassing controls |
| Records | Prompts and responses are business records, subject to retention, audit, and legal hold |
| Reporting | Report data exposure, wrong output that reached a member, and oversharing signals; good-faith reporting is not penalized |
| Acknowledgment | Training and acknowledgment before access, and every year after |

## 4. Human oversight

Oversight scales with impact.

| Level | Description | Applies to |
|---|---|---|
| **H1: User review** | The user reviews every output before using it | All Tier 1 use |
| **H2: Qualified review** | A qualified person reviews every output that reaches a member or a record; agents cite their sources | Tier 2 use cases |
| **H3: Second-line oversight** | H2 plus documented testing, sampled QA by a second party, monitoring thresholds, and a named executive owner | Tier 3 use cases |

Fully automated output to members or systems without human review is not approved under this framework. Any proposal to do so needs a separate Tier 3 business case.

## 5. Risk tiers

| Tier | Description | Examples | Approval | Oversight | Turnaround |
|---|---|---|---|---|---|
| **Tier 1: Personal productivity** | Individual use of approved features; data within the standard; output reviewed by the user | Drafting internal email, meeting recaps, summarizing a document | Self-service | H1 | Immediate |
| **Tier 2: Team or process use** | Shared or repeatable use; shared agents; Confidential data, or limited Restricted data needed for the task under DLP and masking controls; output used by others | Member Care knowledge agent, after-call note drafting, policy Q&A agent | AI Review Group | H2 | 10 business days |
| **Tier 3: Member-impacting or regulated** | Output reaches members without line-by-line review, affects credit, account, fraud, BSA/AML, collections, or employment decisions, or the AI takes system actions | Member-facing assistant, underwriting support, an agent that updates core records | Business executive and CRO | H3 | 30 to 60 days |
| **Prohibited** | Uses listed in the acceptable-use standard | AI as sole credit decision maker; SAR data in general tools | Not approved | — | — |

**Raise the tier by one** if a use involves Restricted member data beyond what its tier allows (any Restricted data in a Tier 1 use; more than limited, task-specific Restricted data in a Tier 2 use), sends output outside the organization, runs on a schedule or trigger, uses a connector or third-party agent, could raise fair-lending or unfair, deceptive, or abusive practices (UDAAP) questions, or comes from a vendor not yet reviewed.

**Ongoing obligations**

| Obligation | Tier 1 | Tier 2 | Tier 3 |
|---|---|---|---|
| AI inventory | Tool-level record | Use-case record | Full record with impact assessment |
| Pre-launch testing | — | Review of 20 to 50 sample outputs | Documented test plan: accuracy, bias, security |
| Monitoring | DLP and audit logs | Monthly sample of outputs | Defined metrics, thresholds, escalation |
| Re-review | Annual standard update | Annually or on change | Every 6 months or on change |

## 6. Exception process

Exceptions are time-limited, documented, and owned. They are not a back door around tiering.

1. **Request**: the business owner submits the exception with the business reason, the rule affected, compensating controls, and the requested duration (maximum 90 days).
2. **Assess**: the AI Review Group and Information Security assess residual risk within 5 business days.
3. **Approve**:

| Residual risk | Approver |
|---|---|
| Low | AVP AI and Automation |
| Medium | CISO and Compliance |
| High | CRO; reported to the AI Governance Committee |

4. **Record**: entered in the exception register with an expiry date and owner.
5. **Review**: expired exceptions are closed, renewed once with fresh approval, or converted into a permanent standard change.

Exceptions to the prohibited-use list are not available.

## 7. Vendor governance

| Scope | Requirement |
|---|---|
| Microsoft (Copilot, Copilot Chat, Copilot Studio) | Covered in the existing Microsoft vendor record. Confirm product terms, data protection addendum, enterprise data protection commitments ([Microsoft](https://learn.microsoft.com/en-us/microsoft-365/copilot/enterprise-data-protection)), SOC reports, data residency, and subprocessors. Re-review annually and when Microsoft changes terms for AI features. |
| Third-party agents, connectors, and plug-ins | Treated as a new vendor relationship. Full due diligence using the [AI Vendor Due Diligence Template](https://github.com/rcwah2/ai-vendor-due-diligence-template) before approval. |
| AI features inside existing vendor platforms (core, contact center, lending) | Vendor must disclose the AI feature, its data use, and its model provider. Intake is required before the feature is enabled. |
| Consulting and implementation partners | Statement of work defines data access, deliverables, and knowledge transfer; access is removed at close. |

This follows NCUA's position that existing third-party due-diligence expectations apply to AI tools ([NCUA](https://ncua.gov/regulation-supervision/regulatory-compliance-resources/artificial-intelligence-ai)).

## 8. Incident escalation

| Severity | Examples | Response | Notify |
|---|---|---|---|
| **Sev 1: Critical** | Member data exposed outside the organization; AI output caused member harm or a regulatory breach; suspected compromise through an agent or connector | Suspend the use case or agent at once; invoke the incident response plan | CISO, CRO, Legal, CTO within 1 hour. Assess at once whether this is a reportable cyber incident under 12 CFR 748.1(c), which requires notifying NCUA no later than 72 hours after the credit union reasonably believes one occurred, and whether member notice under Appendix B to Part 748 is needed. |
| **Sev 2: High** | Restricted data surfaced to an unauthorized employee (oversharing); wrong output reached a member and was corrected | Contain (Restricted Content Discovery, permission fix, DLP rule); root cause within 5 days | CISO, AVP AI and Automation, business owner within 4 hours |
| **Sev 3: Moderate** | Restricted data entered into Copilot against the standard, no exposure; repeated wrong answers from an agent | Coach the user; fix the source content; sample outputs | AVP AI and Automation within 1 business day |
| **Sev 4: Low** | Single wrong answer caught in review; prompt-library quality issue | Log and fix through the feedback loop | Monthly scorecard |

**After any Sev 1 or Sev 2:** a lessons-learned review within 10 business days, updates to the standard, training, or controls, and a report to the AI Governance Committee.
