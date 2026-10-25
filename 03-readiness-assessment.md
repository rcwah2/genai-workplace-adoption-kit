# 03. Readiness Assessment

Readiness is assessed in nine domains: seven technical and two organizational. Each domain gets a red, amber, or green rating, with evidence, before any pilot starts. Leadership signs off the result as a go/no-go gate.

Checklist template: [templates/readiness-checklist.csv](templates/readiness-checklist.csv)

---

## Rating scale

| Rating | Meaning | Gate effect |
|---|---|---|
| **Green** | Control in place and evidenced | Proceed |
| **Amber** | Partly in place; interim control or remediation date agreed | Proceed with conditions, limited pilot scope |
| **Red** | Not in place | No go for the affected scope |

**Go/no-go rule:** no red ratings in identity and access, permissions and oversharing, or security. No more than three amber ratings overall for a pilot. All green, or amber with dated remediation, before broad rollout.

---

## Technical readiness

### 1. Microsoft 365 environment

| Check | Evidence |
|---|---|
| Eligible Microsoft 365 or Office 365 base licenses for pilot users | License report |
| Microsoft 365 Apps on a supported update channel | Admin center channel report |
| Users have Exchange Online mailboxes and OneDrive | Admin center |
| Teams meeting transcription policy decided | Teams policy export |
| Copilot features and agent settings in the admin center reviewed and decided | Configuration record |
| Web grounding setting decided | Configuration record |

### 2. Identity and access

| Check | Evidence |
|---|---|
| Multifactor authentication enforced for all users | Conditional Access report |
| Conditional Access policies cover Copilot apps and unmanaged devices | Policy export |
| Joiner, mover, and leaver processes remove access promptly | Sample of last 20 leavers |
| Privileged admin roles reviewed, with just-in-time elevation where available | Role review |
| Guest and external access reviewed | Guest access report |

### 3. Data classification

| Check | Evidence |
|---|---|
| Sensitivity labels published (for example Public, Internal, Confidential, Restricted) | Label policy |
| Default labels applied to new documents and email | Policy setting |
| Auto-labeling for member personal information and card data | Auto-label policy, simulation results |
| Site-level labels required for new SharePoint sites and Teams | Provisioning policy |

### 4. Permissions and oversharing

This is usually the longest workstream. Microsoft recommends fixing oversharing first and then setting guardrails, using Purview and SharePoint Advanced Management, which is included with Microsoft 365 Copilot licenses ([Microsoft](https://learn.microsoft.com/en-us/copilot/microsoft-365/configure-data-security-copilot); [Microsoft Tech Community](https://techcommunity.microsoft.com/blog/microsoft-copilot-blog/mitigate-oversharing-to-govern-microsoft-365-copilot-and-agents/4448744)).

| Check | Evidence |
|---|---|
| Top 100 most-used SharePoint sites reviewed for broad access | Usage export, permission state report |
| "Everyone except external users" and organization-wide links removed where not needed | Data access governance report |
| Purview DSPM data risk assessment run and high-risk sites listed | Assessment output |
| Restricted Content Discovery applied to high-risk sites during remediation | Site settings |
| Site access reviews sent to owners of overshared sites | Review completion rate |
| Every remediated site has an owner | Site ownership policy |
| Inactive and ownerless sites archived or deleted | Lifecycle report |

### 5. Security

| Check | Evidence |
|---|---|
| Purview DLP for Copilot configured to exclude labeled content from processing, tested in simulation first | DLP policy, simulation report |
| DLP for Copilot prompts with sensitive information types, where licensed | Policy |
| Purview Audit on, with Copilot interactions captured | Audit search sample |
| Insider risk and communication compliance policies reviewed for AI use | Policy decision |
| Prompt-injection and AI-enabled phishing added to the security awareness program | Training content |
| Shadow AI monitoring (web filtering or a cloud access security broker) in place | Report |

### 6. Compliance

| Check | Evidence |
|---|---|
| Copilot listed in the AI system inventory, with the use cases it supports | Inventory entry |
| Microsoft confirmed in the third-party risk program for this use (terms, data protection addendum, SOC reports) | Vendor record |
| Recording and transcription consent rules reviewed by Legal | Legal memo |
| Fair-lending, UDAAP, and privacy review triggers built into intake | Intake form |
| Regulatory evidence map prepared ([framework alignment](reference/framework-alignment.md)) | Evidence map |

### 7. Records and retention

| Check | Evidence |
|---|---|
| Retention policies for Copilot prompts and responses decided and applied | Retention policy |
| Records schedule updated to cover AI interactions and agent outputs | Records schedule |
| Legal-hold and eDiscovery searches tested on Copilot interactions | Test record |
| Teams meeting recording and transcript retention aligned with the records schedule | Policy |

---

## Organizational readiness

### 8. Organizational readiness

| Check | Evidence |
|---|---|
| Executive sponsor named and steering cadence set | Charter |
| Acceptable-use standard approved | Signed standard |
| Business owners named for each pilot use case | Intake records |
| Baselines collected for pilot use cases | Baseline report |
| Source content for pilot use cases (procedures, policies) is current, owned, and in one place | Content inventory |
| A process exists to fix source content when Copilot gives a wrong answer | Feedback workflow |
| Help desk briefed and knowledge articles ready | Support runbook |

### 9. Change readiness

| Check | Evidence |
|---|---|
| Stakeholder map complete, including likely resisters | Map |
| Employee concerns about job impact addressed in leadership messaging | Message draft |
| Managers briefed on what to expect and how to coach | Briefing record |
| Champions recruited for each pilot team | Champion list |
| Training scheduled before access is granted | Training calendar |

---

## Sign-off

| Role | Signs off |
|---|---|
| CTO or CIO | Overall go/no-go |
| CISO or Information Security Officer | Domains 2, 4, 5 |
| Compliance and Records | Domains 6, 7 |
| Chief Risk Officer | Overall risk acceptance for amber items |
| IT / Microsoft 365 administration | Domains 1, 3 |
| AVP, AI and Automation | Domains 8, 9 and the assessment record |
