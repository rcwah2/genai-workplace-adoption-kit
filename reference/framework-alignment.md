# Reference: Framework Alignment

How this framework's artifacts support the NIST AI Risk Management Framework, the NIST Generative AI Profile, ISO/IEC 42001, and NCUA supervisory expectations. Use it as an evidence map for exams and audits. Confirm subcategory and clause references against the source documents and the [AI Governance Crosswalk](https://github.com/rcwah2/ai-governance-crosswalk) before relying on them.

---

## 1. NIST AI RMF 1.0

| Function | What it asks | Framework artifact and evidence |
|---|---|---|
| **GOVERN** | Policies, roles, accountability, training, third-party risk | Acceptable-use standard ([reference](acceptable-use-standard.md)); decision rights and RACI ([05](../05-governance-model.md) §1–2); training records ([07](../07-adoption-plan.md)); inventory (GOVERN 1.6); training (GOVERN 2.2); third-party policies (GOVERN 6.1) |
| **MAP** | Context, intended use, impacts, human oversight | Phase 0 intake ([02](../02-phase-0-opportunity-intake.md)); risk tiers ([05](../05-governance-model.md) §5); data classes ([acceptable use](acceptable-use-standard.md) §3); intended purpose and context (MAP 1.1) |
| **MEASURE** | Testing, metrics, and tracking of trustworthiness | Tier obligations and test plans ([05](../05-governance-model.md) §5); baselines and guardrail metrics ([08](../08-metrics-framework.md)) |
| **MANAGE** | Prioritize, respond to, and monitor risk | Prioritization gates ([04](../04-prioritization-model.md)); scale-or-stop decision ([06](../06-pilot-model.md)); incident escalation ([05](../05-governance-model.md) §8); post-deployment monitoring (MANAGE 4.1); vendor monitoring (MANAGE 3.1) |

## 2. NIST AI 600-1 Generative AI Profile

NIST lists 12 risks that generative AI creates or makes worse ([NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)). The ones most relevant to workplace assistants in a credit union:

| GAI risk | How it shows up | Framework control |
|---|---|---|
| Confabulation | Wrong rates, policy statements, or regulatory citations | Required human review; verification against official sources ([acceptable use](acceptable-use-standard.md) §4) |
| Data Privacy | Member information entered into the wrong tool or surfaced to the wrong user | Data-class matrix; DLP for Copilot; permission cleanup ([acceptable use](acceptable-use-standard.md) §3; [03 readiness](../03-readiness-assessment.md) domains 3–5) |
| Information Security | Prompt injection; AI-enabled phishing and vishing | Security awareness ([acceptable use](acceptable-use-standard.md) §6); connector and agent approval |
| Human-AI Configuration | Over-reliance; automation bias | Human-review rules; prohibited sole-basis decisions; training |
| Harmful Bias and Homogenization | Unfair treatment in lending, collections, or HR uses | Tier 3 classification and fair-lending review |
| Information Integrity | Deepfakes and synthetic impersonation | Prohibited uses; verification of unusual requests |
| Intellectual Property | Copying licensed or third-party content | Acceptable use guidance; marketing review |
| Value Chain and Component Integration | Unreviewed plug-ins, GPTs, and vendor AI features | Approval required for connectors and vendor AI; vendor due diligence |

## 3. ISO/IEC 42001 (AI management system)

| ISO/IEC 42001 area | Framework artifact |
|---|---|
| Clause 5.2 AI policy | [Acceptable-use standard](acceptable-use-standard.md); [05 Governance](../05-governance-model.md) §3 |
| Clause 5.3 Roles, responsibilities, and authorities | [05 Governance](../05-governance-model.md) §1–2: decision rights and RACI |
| Clause 6.1 Actions to address risks (AI risk and impact assessment) | [02 Intake](../02-phase-0-opportunity-intake.md); [03 Readiness](../03-readiness-assessment.md); risk tiers and Tier 3 impact assessment |
| Clause 6.2 AI objectives | Expected business outcome at intake; pilot success criteria ([06](../06-pilot-model.md)) |
| Clause 7.2 to 7.4 Competence, awareness, communication | [07 Adoption plan](../07-adoption-plan.md): training, proficiency check, champions, communications |
| Clause 8 Operation | [06 Pilot model](../06-pilot-model.md); [09 Roadmap](../09-30-60-90-roadmap.md) |
| Clause 9.1 Monitoring and measurement | [08 Metrics framework](../08-metrics-framework.md) |
| Clause 9.3 Management review | Monthly executive scorecard; quarterly board risk committee report |
| Clause 10 Improvement | Feedback loops; exception reviews; incident lessons learned; semi-annual standard review |
| Annex A (policies, resources, impact assessment, data, use of AI systems, third-party relationships) | Acceptable-use standard, data classes, readiness domains, intake, vendor governance ([05](../05-governance-model.md) §7) |

## 4. NCUA supervisory expectations

NCUA has not issued AI-specific rules; existing, technology-neutral requirements apply. Examiners look at safety and soundness, compliance, internal controls around the AI tool, ongoing monitoring, and third-party due diligence ([NCUA](https://ncua.gov/regulation-supervision/regulatory-compliance-resources/artificial-intelligence-ai)).

| Expectation | Source | Framework evidence |
|---|---|---|
| Information security program and safeguarding member information | 12 CFR Part 748 and Appendix A | Data classes; readiness domains 2–5 ([03](../03-readiness-assessment.md)) |
| Cyber incident notification within 72 hours of a reportable incident | 12 CFR 748.1(c) | Incident escalation, Sev 1 ([05](../05-governance-model.md) §8) |
| Third-party due diligence and oversight | NCUA Letters 07-CU-13 and 01-CU-20 | Vendor governance ([05](../05-governance-model.md) §7); vendor due-diligence template |
| Identify, monitor, and control AI-specific risks | NCUA AI resource page | Risk tiers, monitoring obligations, guardrail metrics |
| Board and management oversight | NCUA AI resource page | Quarterly board risk committee reporting |
| Fair lending and consumer protection | ECOA/Reg B; UDAAP | Tier 3 for credit-influencing or member-facing uses; fair-lending trigger at intake |
