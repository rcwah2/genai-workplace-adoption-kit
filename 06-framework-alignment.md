# 06. Framework Alignment

How this kit's artifacts support the NIST AI Risk Management Framework, the NIST Generative AI Profile, ISO/IEC 42001, and NCUA supervisory expectations. Use it as an evidence map for exams and audits. Confirm subcategory and clause references against the source documents and the [AI Governance Crosswalk](https://github.com/rcwah2/ai-governance-crosswalk) before relying on them.

---

## 1. NIST AI RMF 1.0

| Function | What it asks | Kit artifact and evidence |
|---|---|---|
| **GOVERN** | Policies, roles, accountability, training, third-party risk | Acceptable Use Standard ([01](01-acceptable-use-standard.md)); AI Review Group and RACI ([04](04-rollout-and-enablement-plan.md)); training records; inventory (GOVERN 1.6); training (GOVERN 2.2); third-party policies (GOVERN 6.1) |
| **MAP** | Context, intended use, impacts, human oversight | Intake questions and tiering ([02](02-intake-and-risk-tiers.md)); data classes ([01](01-acceptable-use-standard.md) §3); intended purpose and context (MAP 1.1) |
| **MEASURE** | Testing, metrics, and tracking of trustworthiness | Tier 2 sample review and Tier 3 test plans ([02](02-intake-and-risk-tiers.md) §5); risk and quality metrics ([05](05-value-scorecard.md)) |
| **MANAGE** | Prioritize, respond to, and monitor risk | Decision outcomes and conditions ([02](02-intake-and-risk-tiers.md) §4); incident reporting ([01](01-acceptable-use-standard.md) §8); post-deployment monitoring (MANAGE 4.1); vendor monitoring (MANAGE 3.1) |

## 2. NIST AI 600-1 Generative AI Profile

NIST lists 12 risks that generative AI creates or makes worse ([NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)). The ones most relevant to workplace assistants in a credit union:

| GAI risk | How it shows up | Kit control |
|---|---|---|
| Confabulation | Wrong rates, policy statements, or regulatory citations | Required human review; verification against official sources ([01](01-acceptable-use-standard.md) §4) |
| Data Privacy | Member information entered into the wrong tool or surfaced to the wrong user | Data-class matrix; DLP for Copilot; permission cleanup ([01](01-acceptable-use-standard.md) §3, [04](04-rollout-and-enablement-plan.md) Phase 0) |
| Information Security | Prompt injection; AI-enabled phishing and vishing | Security awareness ([01](01-acceptable-use-standard.md) §6); connector and agent approval |
| Human-AI Configuration | Over-reliance; automation bias | Human-review rules; prohibited sole-basis decisions; training |
| Harmful Bias and Homogenization | Unfair treatment in lending, collections, or HR uses | Tier 3 classification and fair-lending review |
| Information Integrity | Deepfakes and synthetic impersonation | Prohibited uses; verification of unusual requests |
| Intellectual Property | Copying licensed or third-party content | Acceptable use guidance; marketing review |
| Value Chain and Component Integration | Unreviewed plug-ins, GPTs, and vendor AI features | Approval required for connectors and vendor AI; vendor due diligence |

## 3. ISO/IEC 42001 (AI management system)

| ISO/IEC 42001 area | Kit artifact |
|---|---|
| Clause 5.2 AI policy | Acceptable Use Standard |
| Clause 5.3 Roles, responsibilities, and authorities | AI Review Group; RACI |
| Clause 6.1 Actions to address risks (AI risk and impact assessment) | Intake, risk tiers, Tier 3 impact assessment |
| Clause 7.2 to 7.4 Competence, awareness, communication | Training curriculum; champions; communications plan |
| Clause 8 Operation | Intake workflow; rollout phases |
| Clause 9.1 Monitoring and measurement | Value scorecard |
| Clause 9.3 Management review | Monthly executive and quarterly board reporting |
| Clause 10 Improvement | Semi-annual standard review; incident lessons learned |
| Annex A (policies, resources, impact assessment, data, use of AI systems, third-party relationships) | Standard, data classes, intake, vendor approval requirements |

## 4. NCUA supervisory expectations

NCUA has not issued AI-specific rules; existing, technology-neutral requirements apply. Examiners look at safety and soundness, compliance, internal controls around the AI tool, ongoing monitoring, and third-party due diligence ([NCUA](https://ncua.gov/regulation-supervision/regulatory-compliance-resources/artificial-intelligence-ai)).

| Expectation | Source | Kit evidence |
|---|---|---|
| Information security program and safeguarding member information | 12 CFR Part 748 and Appendix A | Data classes; DLP; permission cleanup; access controls |
| Cyber incident notification within 72 hours of a reportable incident | 12 CFR 748.1(c) | Incident reporting route through Information Security |
| Third-party due diligence and oversight | NCUA Letters 07-CU-13 and 01-CU-20 | Vendor AI approval requirement; vendor due-diligence template |
| Identify, monitor, and control AI-specific risks | NCUA AI resource page | Tiering, monitoring obligations, scorecard risk metrics |
| Board and management oversight | NCUA AI resource page | Quarterly board risk committee reporting |
| Fair lending and consumer protection | ECOA/Reg B; UDAAP | Tier 3 for credit-influencing or member-facing uses |
