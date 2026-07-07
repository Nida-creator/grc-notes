# Applied Example: CSF Organizational Profile & Gap Analysis

*A worked example demonstrating practical application of NIST CSF 2.0*

---

## Purpose of This Document

Reference notes explain *what* the CSF is. This document demonstrates *how it's actually used* — by walking through the 5-step Profile lifecycle for a fictional company, producing a real Current Profile, Target Profile, gap analysis, and action plan (POA\&M).

---

## Company Background (Fictional Scenario)

**Company:** BrightLedger Inc. **Profile:** 60-employee B2B SaaS company providing invoicing software to small businesses. **Why this scenario:** Small/mid-size company, no dedicated security team yet, first year formalizing their security program — a very common real-world starting point for GRC work.

**Trigger for this assessment:** A large enterprise prospect requires a completed security questionnaire and evidence of a documented risk management program before signing a contract.

---

## Step 1 — Scope the Organizational Profile

- **Scope:** Entire organization's IT environment (not just one system), since this is BrightLedger's first formal CSF-based assessment.  
- **Exclusions:** Physical facility security is out of scope (company is fully remote, no owned office).  
- **Driver:** Sales enablement (closing enterprise deals) \+ establishing a baseline security program.

---

## Step 2 — Gather Information

Sources reviewed to build the Profile:

- Existing (informal) IT policies and onboarding/offboarding checklist  
- AWS account configuration and access logs  
- List of SaaS tools in use (payroll, CRM, code repo, etc.)  
- Interviews with the CTO and the one part-time IT contractor  
- No formal risk register or BIA exists yet — this itself is a finding

---

## Step 3 — Current Profile (Selected Subcategories)

A Current Profile doesn't need to cover all 106 Subcategories — pick the ones relevant to your scope and risk drivers. Below is a representative sample across all 6 Functions.

| Subcategory | Outcome | Current State | Status |
| :---- | :---- | :---- | :---- |
| GV.OC-01 | Mission understood & informs cyber risk mgmt | No documented mission-to-risk linkage; CTO holds this informally | 🔴 Not Achieved |
| GV.RM-02 | Risk appetite/tolerance established & communicated | No formal risk appetite statement exists | 🔴 Not Achieved |
| GV.PO-01 | Cybersecurity policy established & enforced | Informal password rules only; no written policy | 🔴 Not Achieved |
| GV.SC-04 | Suppliers known and prioritized by criticality | List of SaaS vendors exists but not risk-ranked | 🟡 Partially Achieved |
| ID.AM-01 | Hardware inventory maintained | Laptops tracked in a spreadsheet, updated ad hoc | 🟡 Partially Achieved |
| ID.AM-02 | Software/services inventory maintained | No centralized SaaS inventory (shadow IT risk) | 🔴 Not Achieved |
| ID.RA-01 | Vulnerabilities identified, validated, recorded | No vulnerability scanning in place | 🔴 Not Achieved |
| PR.AA-05 | Access managed with least privilege | AWS root account shared among 3 engineers | 🔴 Not Achieved |
| PR.AT-01 | General security awareness training provided | No formal training program | 🔴 Not Achieved |
| PR.DS-01 | Data-at-rest confidentiality/integrity protected | Database encryption enabled by default (AWS RDS) | 🟢 Achieved |
| PR.DS-11 | Backups created, protected, maintained, tested | Automated daily backups exist; never test-restored | 🟡 Partially Achieved |
| PR.PS-04 | Log records generated for continuous monitoring | CloudTrail enabled but logs not reviewed | 🟡 Partially Achieved |
| DE.CM-01 | Networks monitored for adverse events | No SIEM or alerting configured | 🔴 Not Achieved |
| RS.MA-01 | Incident response plan executed w/ third parties | No written incident response plan exists | 🔴 Not Achieved |
| RC.RP-01 | Recovery portion of IR plan executed | N/A — no IR plan to execute | 🔴 Not Achieved |

**Legend:** 🟢 Achieved  🟡 Partially Achieved  🔴 Not Achieved

---

## Step 3 (cont.) — Target Profile

Based on the enterprise customer's requirements and general risk exposure, leadership sets these targets for the next **2 quarters**:

| Subcategory | Target State |
| :---- | :---- |
| GV.PO-01 | Written, board-approved Information Security Policy in place |
| GV.RM-02 | Documented risk appetite statement reviewed annually |
| ID.AM-02 | Centralized SaaS/asset inventory maintained via a tracked tool |
| ID.RA-01 | Quarterly vulnerability scans on all production infrastructure |
| PR.AA-05 | No shared root accounts; individual IAM accounts \+ MFA enforced; least privilege enforced |
| PR.AT-01 | 100% of employees complete annual security awareness training |
| PR.DS-11 | Backup restoration tested quarterly, results documented |
| DE.CM-01 | Centralized log alerting configured for critical AWS events |
| RS.MA-01 | Written incident response plan, tested via 1 tabletop exercise |
| RC.RP-01 | Recovery steps defined and assigned to named owners |

**Tier Target:** Currently operating at **Tier 1 (Partial)** — ad hoc, no org-wide policy, limited awareness. Target for this cycle: **Tier 2 (Risk Informed)** — management-approved practices, awareness of risk even where not yet fully formalized. (Jumping straight to Tier 3/4 isn't realistic or cost-justified for a 60-person company in two quarters — this is the kind of judgment call a GRC analyst is expected to make and defend.)

---

## Step 4 — Gap Analysis & Action Plan (POA\&M)

| Priority | Gap | Action | Owner | Target Date |
| :---- | :---- | :---- | :---- | :---- |
| 1 (High) | No written InfoSec policy | Draft policy using SANS/CIS template, get CTO \+ leadership sign-off | CTO | Week 4 |
| 1 (High) | Shared AWS root account | Create individual IAM users, enforce MFA, retire shared root creds | IT Contractor | Week 3 |
| 1 (High) | No incident response plan | Draft IR plan (roles, escalation, comms); run tabletop exercise | CTO | Week 8 |
| 2 (Medium) | No vulnerability scanning | Deploy a scanning tool (e.g., open-source or low-cost SaaS scanner) on prod environment | IT Contractor | Week 6 |
| 2 (Medium) | No centralized asset inventory | Stand up a lightweight asset/SaaS inventory tracker | GRC Analyst (you) | Week 5 |
| 2 (Medium) | No security awareness training | Roll out a low-cost training platform (e.g., KnowBe4-style) to all staff | HR \+ GRC | Week 6 |
| 3 (Low) | Backups untested | Schedule and document a quarterly restore test | IT Contractor | Week 10 |
| 3 (Low) | No log monitoring/alerting | Configure CloudTrail \+ basic alerting rules | IT Contractor | Week 9 |

**Prioritization logic:** Items were ranked by (1) what the enterprise customer's questionnaire explicitly requires, and (2) likelihood × impact if left unaddressed — e.g., a shared root AWS account is a single point of catastrophic failure, so it's prioritized above training rollout.

---

## Step 5 — Implement & Update

- This Profile is a living document — re-assessed at the end of the 2-quarter cycle.  
- Once Target Profile items are achieved, they roll into the next cycle's *Current Profile*, and new targets are set (e.g., pursuing Tier 3, adding ISO 27001 alignment for further sales enablement).  
- Progress is reported monthly to the CTO in a one-page status update: items closed, items at risk of missing deadline, and any new risks identified.

---

## Why This Exercise Matters (Skills Demonstrated)

- Translating an abstract framework into org-specific, prioritized action  
- Producing artifacts real GRC teams use daily: Current Profile, Target Profile, gap analysis, POA\&M  
- Defending a Tier target with cost-benefit reasoning rather than defaulting to "highest is best"  
- Prioritizing remediation based on business drivers (a sales deal) and risk severity, not just checklist order

---

*This is a fictional, illustrative scenario built to demonstrate applied understanding of the NIST Cybersecurity Framework 2.0 Profile and gap-analysis process — not based on any real company's data.*  
