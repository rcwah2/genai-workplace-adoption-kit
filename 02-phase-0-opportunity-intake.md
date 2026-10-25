# 02. Phase 0: AI Opportunity Intake

Phase 0 happens before anyone gets a license. Every Copilot candidate enters as a **business problem with an owner and a baseline**, not as a feature request. That one discipline settles most later debates about value, because the "before" picture is agreed before the pilot starts.

Template: [templates/opportunity-intake.yaml](templates/opportunity-intake.yaml)

---

## Why Phase 0 comes first

| Without Phase 0 | With Phase 0 |
|---|---|
| "Marketing wants Copilot." | "Marketing spends 14 hours a week drafting campaign variants; the target is 7." |
| Value is estimated after the pilot, from surveys. | Value is measured against a baseline recorded before the pilot. |
| Data risk is found after go-live. | Data involved is declared at intake and drives the risk tier. |
| No one owns the outcome. | A named business owner signs the intake and the result. |

## The intake form

Eight sections. A Tier 1 personal-productivity request can be answered in 10 minutes. A Tier 2 or Tier 3 request needs the full form.

### 1. Business problem statement

One or two sentences in this form:

> **[Team]** spends **[time or cost]** on **[task]**, which causes **[business impact]**. We want to **[outcome]**.

Example: "Member Care agents spend about 4.5 minutes per call writing after-call notes, which lengthens handle time and leaves inconsistent records for the next agent. We want shorter, more consistent notes without lowering quality."

Reject or return requests that describe a tool ("we want an agent") instead of a problem.

### 2. Business owner

| Field | Guidance |
|---|---|
| Accountable owner | A director or above who owns the process and its results |
| Day-to-day lead | The person who runs the pilot inside the team |
| Executive sponsor | Required for Tier 3 |

The owner signs the intake, agrees the success criteria, and makes the scale recommendation.

### 3. Baseline metrics

Record the current state before the pilot. If a baseline does not exist, measuring it becomes the first pilot task, and the pilot clock does not start until it is collected.

| Field | Example |
|---|---|
| Volume | 38,000 calls per month |
| Time per task | 4.5 minutes of after-call documentation |
| Quality or error rate | 12% of notes fail the QA completeness check |
| Cycle time or service level | Average handle time 7.9 minutes |
| Data source and owner | Contact-center platform report, owned by the Workforce Management analyst |
| Measurement period | Eight weeks before pilot start |

See [08 Metrics framework](08-metrics-framework.md) for which layer each metric belongs to.

### 4. Data involved

| Question | Why it matters |
|---|---|
| What content will Copilot read (mailboxes, Teams, SharePoint sites, files)? | Defines the grounding scope that needs a permission review |
| What is the highest data class? Public, Internal, Confidential, Restricted | Drives the risk tier and DLP needs |
| Does it include member personal information? | Sets a floor of Tier 2; triggers privacy review |
| Is any prohibited data involved (SAR information, credentials, full card data)? | If yes, not a general Copilot use |
| Are the source documents current and owned? | Stale content produces wrong answers |

### 5. Process maturity

Copilot speeds up a defined process. It does not fix an undefined one.

| Level | Description | Implication |
|---|---|---|
| 1. Ad hoc | Done differently by each person; no written procedure | Not ready. Standardize the process first. |
| 2. Documented | A procedure exists but is not consistently followed | Pilot possible; expect variable results |
| 3. Standardized | Consistent procedure, templates, and QA | Good candidate |
| 4. Measured | Standardized, with routine metrics | Strong candidate; value is easy to prove |

### 6. Security and privacy considerations

- Will output leave the organization (members, vendors, regulators)?
- Will Copilot or an agent take an action (send, post, update a record)?
- Are connectors, plug-ins, or third-party agents involved?
- Are there recording or transcription consent requirements, such as for calls or meetings?
- Are there retention, legal-hold, or eDiscovery implications?
- Could the use affect credit, account, fraud, collections, or employment decisions?

Any "yes" raises the tier review in [05 Governance model](05-governance-model.md).

### 7. Expected business outcome

State the outcome in business terms with a target and a time frame:

| Outcome type | Example target |
|---|---|
| Cycle time | Average handle time down 8% within two quarters |
| Quality | QA completeness failures from 12% to under 6% |
| Capacity | 300 agent-hours a month, confirmed by handle-time data, redirected to callbacks and outreach |
| Member experience | First-contact resolution up 3 points |
| Risk | Fewer documentation exceptions found in QA review |

### 8. Initial classification (completed by the AI and Automation team)

- Proposed risk tier (1, 2, or 3)
- Readiness flags from [03](03-readiness-assessment.md)
- Prioritization score from [04](04-prioritization-model.md)
- Decision: proceed to assessment / return for more detail / decline

## Intake service levels

| Step | Target |
|---|---|
| Acknowledge and triage | 2 business days |
| Tier 1 decision | Self-service under the [acceptable-use standard](reference/acceptable-use-standard.md) |
| Tier 2 decision | 10 business days |
| Tier 3 decision | 30 to 60 days, including impact assessment and vendor review |

## Quality checks before an intake moves forward

- [ ] The problem is stated as a business problem, not a tool request
- [ ] A named owner at director level or above has signed
- [ ] A baseline exists, or a plan to collect it is agreed
- [ ] The highest data class is declared
- [ ] Process maturity is level 2 or higher
- [ ] The expected outcome has a number and a date
