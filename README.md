# Generative AI Workplace Adoption Kit

A governance-first kit for rolling out enterprise generative AI assistants, such as **Microsoft 365 Copilot**, **Copilot Chat**, and **ChatGPT Enterprise**, in a regulated financial institution. It is written for a credit union of roughly 300 to 1,000 team members, but it adapts to banks, insurers, healthcare, and public-sector organizations.

The kit answers four questions leaders ask before and after licensing an AI assistant:

1. **What are people allowed to do with it?** An acceptable-use standard with data-handling rules.
2. **How do new uses get approved?** A risk-tiered intake process.
3. **Where should we start?** A use-case library by department.
4. **Is it working?** A rollout plan and a value scorecard that measure outcomes, not just logins.

> **Status:** Template. Adapt it to your institution's policies, regulator expectations, and legal advice. This kit is not legal advice.

---

## Contents

| File | Purpose |
|---|---|
| [01-acceptable-use-standard.md](01-acceptable-use-standard.md) | Rules for team members: approved tools, data classes, required human review, prohibited uses |
| [02-intake-and-risk-tiers.md](02-intake-and-risk-tiers.md) | How new AI uses are classified (Tier 1 to Tier 3), reviewed, and approved |
| [03-use-case-library.md](03-use-case-library.md) | 30 starter use cases by department, each with tier, data class, and value measure |
| [04-rollout-and-enablement-plan.md](04-rollout-and-enablement-plan.md) | Phased rollout: readiness, pilot, scale, operate; roles, training, champions, exit criteria |
| [05-value-scorecard.md](05-value-scorecard.md) | Adoption, value, risk, and sentiment metrics with definitions and reporting cadence |
| [06-framework-alignment.md](06-framework-alignment.md) | Mapping to NIST AI RMF, the NIST Generative AI Profile (AI 600-1), ISO/IEC 42001, and NCUA expectations |
| [templates/use-case-intake.yaml](templates/use-case-intake.yaml) | Intake record template |
| [templates/value-scorecard.csv](templates/value-scorecard.csv) | Monthly scorecard template |
| [examples/larkspur-valley-cu.md](examples/larkspur-valley-cu.md) | Worked example for a **fictional** credit union |

---

## Design principles

- **Augment, don't replace.** AI drafts and summarizes; accountable people decide and send.
- **Fix permissions before you switch it on.** Copilot surfaces whatever a user can already access, so oversharing has to be fixed first.
- **Tier by impact, not by tool.** The same tool can be low risk for drafting an internal email and high risk for writing a member adverse-action letter.
- **One inventory.** Every approved use is recorded in the AI system inventory, including AI built into vendor platforms.
- **Measure value, not activity.** Active users are a leading indicator; hours returned, cycle time, and quality are the outcomes.

## How this kit relates to other portfolio artifacts

- [AI System Inventory Template](https://github.com/rcwah2/ai-system-inventory-template): Tier 2 and Tier 3 uses become inventory records.
- [AI Vendor Due Diligence Template](https://github.com/rcwah2/ai-vendor-due-diligence-template): vendor review for any new AI tool or plug-in.
- [AI Governance Crosswalk](https://github.com/rcwah2/ai-governance-crosswalk): how NIST AI RMF and ISO/IEC 42001 work together.
- [AI Implementation Reference Model](https://github.com/rcwah2/ai-implementation-reference-model): the broader implementation sequence and decision gates.

## Key references

- Microsoft, [Enterprise data protection in Microsoft 365 Copilot and Copilot Chat](https://learn.microsoft.com/en-us/microsoft-365/copilot/enterprise-data-protection)
- Microsoft, [Configure a secure and governed foundation for Microsoft Copilot](https://learn.microsoft.com/en-us/copilot/microsoft-365/configure-data-security-copilot)
- Microsoft, [Copilot Analytics introduction](https://learn.microsoft.com/en-us/viva/insights/copilot-analytics-introduction)
- OpenAI, [Enterprise privacy](https://openai.com/enterprise-privacy) and [Business data privacy, security, and compliance](https://openai.com/business-data/)
- NIST, [AI 600-1: Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)
- NCUA, [Artificial Intelligence resources for credit unions](https://ncua.gov/regulation-supervision/regulatory-compliance-resources/artificial-intelligence-ai)

## License

CC BY 4.0. Author: Raymond Wah, Lissome Technology Consulting.
