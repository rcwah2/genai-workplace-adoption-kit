# Reference: Framework Alignment

How this framework's artifacts support the NIST AI Risk Management Framework, the NIST Generative AI Profile, ISO/IEC 42001, and NCUA supervisory expectations. Use it as an evidence map for exams and audits. See also the [AI Governance Crosswalk](https://github.com/rcwah2/ai-governance-crosswalk).

> **Verification status:** references checked against primary sources on October 25, 2026: [NIST AI 100-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf), the ISO/IEC 42001:2023 table of contents, [12 CFR Part 748](https://www.ecfr.gov/current/title-12/chapter-VII/subchapter-A/part-748), and [NCUA's AI resource page](https://ncua.gov/regulation-supervision/regulatory-compliance-resources/artificial-intelligence-ai). Recheck before an exam or audit; several of these sources are under revision.

---

## 1. NIST AI RMF 1.0

AI RMF 1.0 (NIST AI 100-1, January 2023) is still the current version. NIST says it is being revised as part of the White House AI Action Plan ([NIST](https://www.nist.gov/itl/ai-risk-management-framework)), so subcategory numbers may change in the next version.

| Function | What it asks | Framework artifact and evidence |
|---|---|---|
| **GOVERN** | Policies, roles, accountability, training, third-party risk | Acceptable-use standard ([reference](acceptable-use-standard.md)); decision rights and RACI ([05](../05-governance-model.md) §1–2); training records ([07](../07-adoption-plan.md)); inventory (GOVERN 1.6); training (GOVERN 2.2); third-party policies (GOVERN 6.1); contingency for third-party AI failures (GOVERN 6.2) |
| **MAP** | Context, intended use, impacts, human oversight | Phase 0 intake ([02](../02-phase-0-opportunity-intake.md)); risk tiers ([05](../05-governance-model.md) §5); data classes ([acceptable use](acceptable-use-standard.md) §3); intended purpose and context (MAP 1.1); human oversight levels H1 to H3 ([05](../05-governance-model.md) §4, MAP 3.5) |
| **MEASURE** | Testing, metrics, and tracking of trustworthiness | Tier obligations and test plans ([05](../05-governance-model.md) §5); baselines and guardrail metrics ([08](../08-metrics-framework.md)); security checks ([03](../03-readiness-assessment.md) domain 5, MEASURE 2.7); user feedback loops ([07](../07-adoption-plan.md) §6, MEASURE 3.3) |
| **MANAGE** | Prioritize, respond to, and monitor risk | Prioritization gates ([04](../04-prioritization-model.md)); scale-or-stop decision ([06](../06-pilot-model.md)); incident escalation ([05](../05-governance-model.md) §8); authority to suspend a use case (MANAGE 2.4); vendor monitoring (MANAGE 3.1); post-deployment monitoring (MANAGE 4.1); incident tracking and communication (MANAGE 4.3) |

## 2. NIST AI 600-1 Generative AI Profile

NIST AI 600-1 (July 2024) lists 12 risks that generative AI creates or makes worse ([NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)). Risk names below use NIST's wording. The ones most relevant to workplace assistants in a credit union:

| GAI risk | How it shows up | Framework control |
|---|---|---|
| Confabulation | Wrong rates, policy statements, or regulatory citations | Required human review; verification against official sources ([acceptable use](acceptable-use-standard.md) §4) |
| Data Privacy | Member information entered into the wrong tool or surfaced to the wrong user | Data-class matrix; DLP for Copilot; permission cleanup ([acceptable use](acceptable-use-standard.md) §3; [03 readiness](../03-readiness-assessment.md) domains 3–5) |
| Information Security | Prompt injection; AI-enabled phishing and vishing | Security awareness ([acceptable use](acceptable-use-standard.md) §6); connector and agent approval |
| Human-AI Configuration | Over-reliance; automation bias | Human-review rules; prohibited sole-basis decisions; training |
| Harmful Bias or Homogenization | Unfair treatment in lending, collections, or HR uses | Tier 3 classification and fair-lending review |
| Information Integrity | Deepfakes and synthetic impersonation | Prohibited uses; verification of unusual requests |
| Intellectual Property | Copying licensed or third-party content | Acceptable use guidance; marketing review |
| Value Chain and Component Integration | Unreviewed plug-ins, GPTs, and vendor AI features | Approval required for connectors and vendor AI; vendor due diligence |

## 3. ISO/IEC 42001 (AI management system)

| ISO/IEC 42001 area | Framework artifact |
|---|---|
| Clause 5.2 AI policy | [Acceptable-use standard](acceptable-use-standard.md); [05 Governance](../05-governance-model.md) §3 |
| Clause 5.3 Roles, responsibilities, and authorities | [05 Governance](../05-governance-model.md) §1–2: decision rights and RACI |
| Clause 6.1 Actions to address risks and opportunities: 6.1.2 AI risk assessment, 6.1.3 AI risk treatment, 6.1.4 AI system impact assessment (performed in operation under 8.2 to 8.4) | [02 Intake](../02-phase-0-opportunity-intake.md); [03 Readiness](../03-readiness-assessment.md); risk tiers and Tier 3 impact assessment |
| Clause 6.2 AI objectives and planning to achieve them | Expected business outcome at intake; pilot success criteria ([06](../06-pilot-model.md)) |
| Clause 7.2 to 7.4 Competence, awareness, communication | [07 Adoption plan](../07-adoption-plan.md): training, proficiency check, champions, communications |
| Clause 8 Operation | [06 Pilot model](../06-pilot-model.md); [09 Roadmap](../09-30-60-90-roadmap.md) |
| Clause 9.1 Monitoring and measurement | [08 Metrics framework](../08-metrics-framework.md) |
| Clause 9.3 Management review | Monthly executive scorecard; quarterly board risk committee report |
| Clause 10 Improvement | Feedback loops; exception reviews; incident lessons learned; semi-annual standard review |
| Annex A control objectives A.2 to A.10 (policies, internal organization, resources, impact assessment, life cycle, data, information for interested parties, use of AI systems, third-party and customer relationships) | Acceptable-use standard, data classes, readiness domains, intake, vendor governance ([05](../05-governance-model.md) §7) |

## 4. NCUA supervisory expectations

NCUA has not issued AI-specific rules; existing, technology-neutral requirements apply. Examiners look at safety and soundness, compliance, internal controls around the AI tool, ongoing monitoring, and third-party due diligence ([NCUA](https://ncua.gov/regulation-supervision/regulatory-compliance-resources/artificial-intelligence-ai)).

| Expectation | Source | Framework evidence |
|---|---|---|
| Information security program and safeguarding member information | 12 CFR 748.0 and Appendix A to Part 748 (Guidelines for Safeguarding Member Information) | Data classes; readiness domains 2–5 ([03](../03-readiness-assessment.md)) |
| Notify NCUA as soon as possible and no later than 72 hours after reasonably believing a reportable cyber incident occurred | 12 CFR 748.1(c) | Incident escalation, Sev 1 ([05](../05-governance-model.md) §8) |
| Response program and member notice for unauthorized access to member information | Appendix B to Part 748 | Incident escalation, Sev 1 and Sev 2 ([05](../05-governance-model.md) §8); Legal and Compliance assess member notice |
| Third-party due diligence and oversight | NCUA Letters 07-CU-13 and 01-CU-20 | Vendor governance ([05](../05-governance-model.md) §7); vendor due-diligence template |
| Identify, monitor, and control AI-specific risks | NCUA AI resource page | Risk tiers, monitoring obligations, guardrail metrics |
| Board and management oversight | NCUA AI resource page | Quarterly board risk committee reporting |
| Fair lending: specific reasons for adverse action, regardless of the technology used | ECOA and Regulation B (12 CFR 1002.9) | Tier 3 for credit-influencing uses; AI is never the sole basis of a credit decision; fair-lending trigger at intake |
| Unfair, deceptive, or abusive acts or practices | Dodd-Frank Act UDAAP (12 U.S.C. 5531, 5536); FTC Act Section 5 UDAP | Tier 3 for member-facing output; human review of member communications |

NCUA examines credit unions with $10 billion or less in assets for consumer financial protection and fair lending compliance; the CFPB supervises larger credit unions ([NCUA](https://ncua.gov/regulation-supervision/examination-program)).

> **Note on withdrawn guidance:** the CFPB withdrew Circular 2022-03 (adverse action notices for credit decisions based on complex algorithms) and Circular 2023-03 on May 12, 2025, and said the withdrawal is not necessarily final ([CFPB](https://www.consumerfinance.gov/compliance/guidance/withdrawn-guidance/)). The underlying ECOA and Regulation B requirement to give specific reasons for adverse action still applies, which is why this framework keeps credit-influencing uses in Tier 3.
