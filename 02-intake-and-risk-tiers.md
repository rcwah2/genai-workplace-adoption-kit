# 02. Use-Case Intake and Risk Tiers

Not every AI use needs a committee. This tiering lets low-risk personal productivity move fast and focuses review effort where member, regulatory, or operational impact is real.

---

## 1. Risk tiers

| Tier | Description | Examples | Approval path | Target turnaround |
|---|---|---|---|---|
| **Tier 1: Personal productivity** | An individual uses an approved tool for their own work; a person reviews all output; data stays within the acceptable-use rules | Drafting internal emails, summarizing meetings, rewriting a procedure, building a spreadsheet formula | Self-service under the [Acceptable Use Standard](01-acceptable-use-standard.md). No intake needed. | Immediate |
| **Tier 2: Team or process use** | Shared or repeatable use: shared prompts, custom GPTs, Copilot agents, use of Confidential or limited Restricted data, output used by others | A shared Member Care knowledge agent, a lending stip-checklist assistant, a policy Q&A agent grounded in SharePoint | Intake form plus light review by the AI Review Group (business owner, AI and Automation, Information Security, Compliance) | 10 business days |
| **Tier 3: Member-impacting or regulated** | Output reaches members without line-by-line review, influences credit, account, fraud, BSA/AML, collections, or employment decisions, or the AI takes actions in systems | A member-facing chatbot answering account questions, AI-assisted underwriting, SAR narrative drafting, an agent that updates core records | Full review: impact assessment, vendor due diligence, testing, monitoring plan, sign-off by business executive and Chief Risk Officer, reported to the board risk committee | 30 to 60 days |
| **Prohibited** | Uses listed in Section 5 of the Acceptable Use Standard | AI as sole credit decision maker, synthetic impersonation | Not approved | — |

### Tier-raising factors

Raise the tier by one level if any of the following apply:
- Uses Restricted member data
- Output is sent outside the credit union
- Runs automatically on a schedule or trigger
- Connects to another system through a connector, plug-in, or API
- Affects a protected class, or could raise fair-lending or consumer-protection (UDAAP) questions
- Is provided by a new vendor not yet reviewed

## 2. Intake workflow

```
Submit intake  →  Triage (2 days)  →  Tier assigned
   Tier 1: no intake required
   Tier 2: AI Review Group review → approve / approve with conditions / decline → add to inventory
   Tier 3: impact assessment + vendor due diligence + test plan → executive and CRO sign-off → pilot → production approval → monitor
```

## 3. Intake questions (summary)

Full template: [templates/use-case-intake.yaml](templates/use-case-intake.yaml)

1. What problem does this solve, and for whom? What is the current process and its volume?
2. Which tool or vendor, and which features (chat, agent, connector, automation)?
3. What data goes in, and what is the highest data class?
4. Who sees the output? Does it reach members, regulators, or decisions?
5. Is a person reviewing every output before it is used? Who?
6. Does the AI take any action in a system (send, update, post, move money)?
7. What could go wrong (wrong answer, data exposure, bias, member harm), and how would we notice?
8. How will we measure value? What is the baseline today?
9. Who is the accountable business owner?

## 4. Decision outcomes

- **Approve:** add to the inventory with an owner, tier, and review date.
- **Approve with conditions:** for example, "internal use only," "human review of every output," "no Restricted data," "pilot of 25 users for 60 days."
- **Defer:** depends on another item first, such as data cleanup, vendor review, or the permission fix.
- **Decline:** with reasons and alternatives.

## 5. Ongoing obligations by tier

| Obligation | Tier 1 | Tier 2 | Tier 3 |
|---|---|---|---|
| Recorded in the AI inventory | Tool-level only | Yes | Yes, with full record |
| Named business owner | — | Yes | Yes (executive) |
| Pre-launch testing | — | Sample review of 20 to 50 outputs | Documented test plan, including accuracy, bias, and security tests |
| Monitoring | DLP and audit logs | Monthly output sampling | Defined metrics, thresholds, and escalation |
| Re-review | Annual standard update | Annually or on change | Every 6 months or on change |
| Reporting | Scorecard totals | Scorecard | Scorecard plus risk committee |

---

**Related:** [AI System Inventory Template](https://github.com/rcwah2/ai-system-inventory-template) · [AI Vendor Due Diligence Template](https://github.com/rcwah2/ai-vendor-due-diligence-template)
