# Reference: Generative AI Acceptable Use Standard

**Applies to:** all team members, contractors, and temporary staff using generative AI for credit union work.
**Owner:** AVP, Enterprise AI and Automation. **Approvers:** CTO, Chief Risk Officer, Information Security Officer, Compliance. **Review cycle:** every 6 months, or when tools or regulations change.

---

## 1. Purpose

Generative AI can save time on writing, summarizing, analysis, and research. It can also expose member information, produce confident but wrong answers, and create compliance risk. This standard sets out how to use approved tools safely so team members can use them with confidence.

## 2. Approved tools

| Tool | Status | Notes |
|---|---|---|
| Microsoft 365 Copilot (licensed) | Approved | Works inside Word, Excel, Outlook, Teams, and PowerPoint and uses content you already have permission to see. Prompts and responses are not used to train foundation models and are logged for audit and eDiscovery ([Microsoft](https://learn.microsoft.com/en-us/microsoft-365/copilot/enterprise-data-protection)). |
| Microsoft Copilot Chat, signed in with your work account | Approved | Covered by enterprise data protection only when you sign in with your work account ([Microsoft](https://support.microsoft.com/en-us/topic/data-protection-when-using-microsoft-365-copilot-chat-for-work-or-school-1e7de2a4-5ca8-4e93-a6e6-1965def6a0fe)). |
| ChatGPT Enterprise (credit union workspace) | Approved | Business data is not used for training by default; admins control retention and can access audit logs ([OpenAI](https://openai.com/enterprise-privacy)). |
| Copilot agents, custom GPTs, connectors, and plug-ins | Approval required | Must go through intake (see [05 Governance model](../05-governance-model.md)) before being shared beyond the person who built them. |
| AI meeting note-takers, browser extensions, and AI features inside other vendor products | Approval required | Treated as a third-party AI vendor. |
| Personal or consumer AI accounts (free or paid) | **Not approved** for any non-public credit union information. | |

If a tool is not on this list, assume it is not approved and ask the AI and Automation team.

## 3. Data classes and what you may enter

| Data class | Examples | Copilot (M365 / work Chat) | ChatGPT Enterprise | Personal AI accounts |
|---|---|---|---|---|
| **Public** | Published rates, website content, press releases | Yes | Yes | Yes |
| **Internal** | Procedures, training material, internal emails, meeting notes without member data | Yes | Yes | No |
| **Confidential** | Financial results before release, vendor contracts, strategy, HR policies, aggregated member statistics | Yes, within your existing access | Only for uses approved through intake | No |
| **Restricted: member information** | Names with account details, Social Security numbers, account and card numbers, loan files, income documents | Only within an approved Tier 2 or Tier 3 use case | Only within an approved Tier 3 use case | **Never** |
| **Prohibited in all general-purpose AI tools** | Suspicious Activity Report (SAR) information, passwords and authentication codes, full card data (PAN, CVV), security architecture details | **Never** | **Never** | **Never** |

When in doubt, remove or mask identifiers, for example "Member A" or "account ending 1234."

## 4. Required human review

1. **You own the output.** Check every AI-generated draft for accuracy, tone, and completeness before you use it. AI can produce confident but false content, which NIST calls "confabulation" ([NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)).
2. **Anything going to a member** (letters, emails, chat responses, disclosures) must be reviewed by a qualified team member before it is sent, and must follow approved templates and brand standards.
3. **Facts, rates, policy statements, and regulatory citations** must be verified against the official source.
4. **Do not paste AI output into the core system** or a loan file without checking it.

## 5. Prohibited uses

- Using AI as the **sole basis** for approving or denying credit, opening or closing accounts, setting pricing, or making employment decisions.
- Generating content that impersonates a member, team member, or regulator, or creating synthetic voices or images of real people.
- Uploading member data to tools not listed in Section 2.
- Using AI to bypass security controls, access rules, or approval steps.
- Representing AI-generated content as a person's own work where disclosure is required.
- Building or sharing agents, GPTs, or automations that act on systems (send, post, update, transfer) without Tier 3 approval.

## 6. Security and fraud awareness

- AI makes phishing, voice impersonation ("vishing"), and deepfakes more convincing. Verify unusual requests through a known channel, especially requests to change payment details, reset credentials, or move money.
- Report suspected prompt injection (for example, a document or email that tells the AI to ignore instructions or share data) to Information Security.

## 7. Records, privacy, and monitoring

- Prompts and responses in approved tools are business records. They may be logged, retained, reviewed, and produced for audits, exams, or legal holds.
- Do not delete AI interactions that are subject to a legal hold.
- Monitoring and data loss prevention controls apply to AI tools in the same way they apply to email and file sharing.

## 8. Reporting issues

Report the following to the AI and Automation team or Information Security as soon as you notice them:
- Restricted or prohibited data entered into an AI tool
- AI output that was wrong and reached a member or a decision
- An AI response that exposed information you should not see (an oversharing signal)

Reporting promptly is expected and will not be penalized when done in good faith.

## 9. Acknowledgment

All users complete "Safe Use of Generative AI" training and acknowledge this standard before access is granted, and again each year.

---

**Related:** [05 Governance model](../05-governance-model.md) · [07 Adoption plan](../07-adoption-plan.md)
