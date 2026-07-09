# ISO/IEC 27001:2022 — Study Notes

Source: ISO/IEC 27001:2022(E), Third edition — "Information security, cybersecurity and privacy protection — Information security management systems — Requirements."

**How this document is organized**
- Section 1–2: what an ISMS is, what "certifiable" means, and how the standard is structured
- Section 3: Clauses 4–10 — the mandatory management-system requirements (what an auditor checks against)
- Section 4: Annex A — all 93 controls, organized by theme (reference for a Statement of Applicability or gap assessment)
- Section 5: cheat sheet — comparisons, glossary, and likely interview questions

Where NIST CSF describes *what outcomes* to aim for, ISO 27001 describes *how* the management system must be structured — and makes it provably certifiable. That distinction matters throughout.

---

## 1. What ISO 27001 Actually Is

ISO/IEC 27001 specifies requirements for building, running, and continually improving an **Information Security Management System (ISMS)** — the management structure (policies, roles, processes, risk handling) an organization uses to keep information secure.

- **It is a management system standard, not a control checklist.** Clauses 4–10 cover how security is run as a management discipline — leadership, planning, support, operation, evaluation, improvement — following the same "harmonized structure" as other ISO management standards (e.g. ISO 9001).
- **It is certifiable.** Unlike NIST CSF (voluntary guidance), an organization can be formally audited and awarded an ISO 27001 certificate by an accredited certification body. This is the single biggest practical difference from CSF.
- **Clauses 4–10 are mandatory.** The standard states explicitly that excluding any requirement in Clauses 4–10 is not acceptable when claiming conformity.
- **Annex A controls are not all mandatory.** Every control must be *considered*, but only the ones relevant to risk treatment need to be implemented — exclusions must be justified in the Statement of Applicability (SoA).

**Why this matters for GRC:**
- ISO 27001 is one of the most-requested credentials/skills in GRC job postings — client audits, vendor security questionnaires, and compliance roles reference it directly.
- The SoA and risk treatment plan are core GRC analyst deliverables — this standard is the day-to-day paperwork.
- Knowing the difference between "management system clauses" (4–10) and "Annex A controls" is what separates someone who's skimmed the standard from someone who's actually studied it.

### 1.1 ISO 27001 vs NIST CSF

| | NIST CSF 2.0 | ISO/IEC 27001:2022 |
|---|---|---|
| Nature | Voluntary guidance / taxonomy | Certifiable international standard |
| Tells you | WHAT outcomes to achieve | HOW to structure the management system + a control reference list |
| Core structure | 6 Functions → Categories → Subcategories | Clauses 4–10 (mandatory) + Annex A (93 controls, conditional) |
| Can you be "certified"? | No — you build a Profile, not a certificate | Yes — accredited third-party audit and certificate |
| Common pairing | Risk communication / maturity benchmarking | Contractual / compliance proof to clients and regulators |

In practice: many organizations use NIST CSF internally to talk about risk maturity, and ISO 27001 externally to prove to customers/regulators that their ISMS meets a recognized bar. Complementary, not competing.

---

## 2. The Big Picture — PDCA and the ISMS

ISO 27001 runs on the Plan-Do-Check-Act (PDCA) cycle, even though the 2022 text doesn't use those exact words. PDCA still shows up constantly in ISO training/certs, so know the mapping:

| PDCA Stage | ISO 27001 Clauses | What Happens |
|---|---|---|
| Plan | 4, 5, 6 | Understand context, secure leadership commitment, assess risk, plan objectives |
| Do | 7, 8 | Provide resources/training, operate the ISMS, treat risks |
| Check | 9 | Monitor, internally audit, management review |
| Act | 10 | Fix nonconformities, continually improve |

**Key concept — the ISMS:**
- ISMS = Information Security Management System. Not software — the whole system of policies, risk processes, roles, and controls an org runs to protect information.
- The ISMS preserves Confidentiality, Integrity, and Availability (CIA triad) by applying a risk management process.
- It must be scaled to the organization's needs — a 10-person startup's ISMS looks very different from a bank's, but both follow the same clause structure.

---

## 3. Clauses 4–10 — Requirements Summary (Mandatory)

Paraphrased for clarity, kept faithful to what a certification auditor checks.

### Clause 4: Context of the Organization
- **4.1** Determine external and internal issues relevant to the ISMS's intended outcomes (market conditions, regulatory landscape, internal culture, technology dependencies).
- **4.2** Identify interested parties (regulators, customers, employees, shareholders, suppliers), their relevant requirements (legal, regulatory, contractual), and which requirements the ISMS will address.
- **4.3** Define the ISMS boundaries/scope considering 4.1, 4.2, and interfaces with other organizations. The scope must be documented.
- **4.4** Establish, implement, maintain, and continually improve the ISMS, including all needed processes and their interactions.

### Clause 5: Leadership
- **5.1** Top management must demonstrably: align policy/objectives with strategic direction, integrate ISMS requirements into normal business processes, ensure resources are available, communicate the importance of info-sec, ensure the ISMS achieves its outcomes, support people's contribution, promote continual improvement, and support other managers' leadership in their areas.
- **5.2** Establish an information security policy that's appropriate to the org's purpose, includes objectives (or a framework for setting them), commits to satisfying requirements and continual improvement, and is documented/communicated/available to interested parties.
- **5.3** Assign and communicate info-sec roles/responsibilities/authorities — specifically, someone responsible for ISMS conformance and someone reporting performance to top management.

### Clause 6: Planning
- **6.1.1** Consider Clause 4 issues/requirements and determine risks/opportunities needed to achieve ISMS outcomes, prevent undesired effects, and enable continual improvement. Plan actions to address them.
- **6.1.2** Risk assessment: establish risk criteria (acceptance + assessment criteria), ensure repeatable/consistent results, identify risks (to CIA, with risk owners), analyze (consequences, likelihood, risk level), evaluate (compare against criteria, prioritize for treatment). Retain documented evidence.
- **6.1.3** Risk treatment: select treatment options, determine necessary controls, cross-check against Annex A to catch gaps, produce a **Statement of Applicability** (necessary controls, justification, implementation status, exclusion justification), formulate a treatment plan, get risk owner approval and residual-risk acceptance. Retain documented evidence.
- **6.2** Set info-sec objectives at relevant functions/levels — consistent with policy, measurable where practicable, tied to risk results, monitored/communicated/updated/documented. Define what will be done, resources needed, responsibility, deadline, and evaluation method.
- **6.3** Changes to the ISMS must be carried out in a planned manner.

### Clause 7: Support
- **7.1** Determine and provide resources needed for the ISMS.
- **7.2** Determine necessary competence, ensure it via education/training/experience, close gaps, retain evidence of competence.
- **7.3** Ensure personnel are aware of the policy, their contribution to ISMS effectiveness, and the implications of nonconformance.
- **7.4** Determine communication needs: what, when, with whom, how.
- **7.5** Documented information: what's required (7.5.1), how it's created/updated with proper identification/format/review (7.5.2), and how it's controlled — availability, protection, distribution, storage, version control, retention (7.5.3). Externally-originated documents deemed necessary must also be controlled.

### Clause 8: Operation
- **8.1** Plan/implement/control processes to meet requirements and Clause 6 actions; establish criteria; control planned and unintended changes; ensure externally-provided processes/products/services are controlled (the supplier/vendor risk hook).
- **8.2** Perform risk assessments at planned intervals or on significant change; retain documented results.
- **8.3** Implement the risk treatment plan; retain documented results.

### Clause 9: Performance Evaluation
- **9.1** Determine what to monitor/measure, methods that produce valid/comparable/reproducible results, when/who monitors and evaluates. Retain evidence; evaluate both info-sec performance and overall ISMS effectiveness.
- **9.2** Internal audit: conduct at planned intervals to check conformance to the org's own requirements and the standard, and effective implementation. Plan/establish/maintain an audit programme (frequency, methods, responsibilities, reporting) considering process importance and past results; define criteria/scope per audit; ensure auditor objectivity; report to management; retain evidence.
- **9.3** Management review: top management reviews the ISMS at planned intervals. Inputs must include status of previous actions, changes in issues/interested-party needs, performance feedback (nonconformities, monitoring results, audit results, objective fulfilment), interested-party feedback, risk assessment/treatment status, and improvement opportunities. Results must include decisions on improvement and ISMS changes, with documented evidence.

### Clause 10: Improvement
- **10.1** Continually improve the suitability, adequacy, and effectiveness of the ISMS.
- **10.2** On nonconformity: react and correct, evaluate root cause and recurrence risk, implement corrective action, review its effectiveness, change the ISMS if needed. Actions must be proportionate. Retain documented evidence of the nonconformity, actions taken, and results.

**Memory aid:** 4 = Context · 5 = Leadership (top management owns this) · 6 = Planning (risk assessment + treatment + SoA — the core GRC deliverable) · 7 = Support · 8 = Operation (run the risk process day-to-day) · 9 = Check (monitor, audit, review) · 10 = Act (fix, improve). This is PDCA with extra structure: Plan(4–6) → Do(7–8) → Check(9) → Act(10).

---

## 4. Annex A — Controls Reference (93 Controls, 4 Themes)

Annex A is directly aligned with ISO/IEC 27002:2022. Every control must be *considered*; only relevant ones must be *implemented*, with inclusion/exclusion justified in the SoA.

### 4.1 Organizational Controls (5.1–5.37) — 37 controls

| ID | Control | Requirement (paraphrased) |
|---|---|---|
| 5.1 | Policies for information security | Policy and topic-specific policies defined, approved, published, communicated, acknowledged, periodically reviewed |
| 5.2 | Information security roles and responsibilities | Roles/responsibilities defined and allocated per org needs |
| 5.3 | Segregation of duties | Conflicting duties/responsibility areas segregated |
| 5.4 | Management responsibilities | Management requires personnel to apply info-sec per policy/procedures |
| 5.5 | Contact with authorities | Maintain contact with relevant authorities |
| 5.6 | Contact with special interest groups | Maintain contact with security forums/professional associations |
| 5.7 | Threat intelligence | Collect and analyze threat info to produce intelligence |
| 5.8 | Information security in project management | Info-sec integrated into project management |
| 5.9 | Inventory of information and other associated assets | Maintain inventory of info/assets including owners |
| 5.10 | Acceptable use of information and other associated assets | Rules for acceptable use/handling identified, documented, implemented |
| 5.11 | Return of assets | Assets returned upon change/termination of employment or contract |
| 5.12 | Classification of information | Info classified per CIA and interested-party requirements |
| 5.13 | Labelling of information | Labelling procedures per the classification scheme |
| 5.14 | Information transfer | Rules/procedures/agreements for all transfer types |
| 5.15 | Access control | Rules for physical/logical access per business and info-sec requirements |
| 5.16 | Identity management | Full life cycle of identities managed |
| 5.17 | Authentication information | Allocation/management controlled via a management process |
| 5.18 | Access rights | Provisioned, reviewed, modified, removed per access control policy |
| 5.19 | Information security in supplier relationships | Manage info-sec risks from supplier products/services |
| 5.20 | Addressing information security within supplier agreements | Requirements established and agreed with each supplier |
| 5.21 | Managing information security in the ICT supply chain | Manage info-sec risks in the ICT supply chain |
| 5.22 | Monitoring, review and change management of supplier services | Regularly monitor/review/evaluate supplier practices |
| 5.23 | Information security for use of cloud services | Processes for acquiring/using/managing/exiting cloud services |
| 5.24 | Information security incident management planning and preparation | Processes, roles, responsibilities defined and communicated |
| 5.25 | Assessment and decision on information security events | Assess events and decide if they qualify as incidents |
| 5.26 | Response to information security incidents | Respond per documented procedures |
| 5.27 | Learning from information security incidents | Use incident knowledge to strengthen controls |
| 5.28 | Collection of evidence | Procedures for identification/collection/preservation of evidence |
| 5.29 | Information security during disruption | Plan to maintain info-sec during disruption |
| 5.30 | ICT readiness for business continuity | Planned/implemented/maintained/tested per continuity objectives |
| 5.31 | Legal, statutory, regulatory and contractual requirements | Identified, documented, kept up to date |
| 5.32 | Intellectual property rights | Appropriate procedures to protect IP rights |
| 5.33 | Protection of records | Protected from loss, destruction, falsification, unauthorized access |
| 5.34 | Privacy and protection of PII | Requirements identified and met per law/contract |
| 5.35 | Independent review of information security | Reviewed independently at planned intervals or on major change |
| 5.36 | Compliance with policies, rules and standards for information security | Compliance regularly reviewed |
| 5.37 | Documented operating procedures | Documented and available to those who need them |

### 4.2 People Controls (6.1–6.8) — 8 controls

| ID | Control | Requirement (paraphrased) |
|---|---|---|
| 6.1 | Screening | Background checks pre-hire and ongoing, proportional to role/risk |
| 6.2 | Terms and conditions of employment | Contracts state info-sec responsibilities |
| 6.3 | Information security awareness, education and training | Appropriate training and regular policy updates per role |
| 6.4 | Disciplinary process | Formal, communicated process for policy violations |
| 6.5 | Responsibilities after termination or change of employment | Surviving duties defined, enforced, communicated |
| 6.6 | Confidentiality or non-disclosure agreements | Identified, documented, reviewed, signed |
| 6.7 | Remote working | Security measures for remote personnel |
| 6.8 | Information security event reporting | Mechanism to report observed/suspected events promptly |

### 4.3 Physical Controls (7.1–7.14) — 14 controls

| ID | Control | Requirement (paraphrased) |
|---|---|---|
| 7.1 | Physical security perimeters | Perimeters defined to protect areas with info/assets |
| 7.2 | Physical entry | Secure areas protected by entry controls |
| 7.3 | Securing offices, rooms and facilities | Physical security designed and implemented |
| 7.4 | Physical security monitoring | Premises continuously monitored for unauthorized access |
| 7.5 | Protecting against physical and environmental threats | Protection against natural/physical threats designed and implemented |
| 7.6 | Working in secure areas | Security measures for secure-area work |
| 7.7 | Clear desk and clear screen | Rules defined and enforced |
| 7.8 | Equipment siting and protection | Equipment sited securely and protected |
| 7.9 | Security of assets off-premises | Off-site assets protected |
| 7.10 | Storage media | Managed through acquisition/use/transport/disposal per classification |
| 7.11 | Supporting utilities | Protected from power failures/utility disruptions |
| 7.12 | Cabling security | Protected from interception/interference/damage |
| 7.13 | Equipment maintenance | Maintained to ensure availability/integrity/confidentiality |
| 7.14 | Secure disposal or re-use of equipment | Storage media verified/wiped before disposal/re-use |

### 4.4 Technological Controls (8.1–8.34) — 34 controls

| ID | Control | Requirement (paraphrased) |
|---|---|---|
| 8.1 | User end point devices | Information on end-user devices protected |
| 8.2 | Privileged access rights | Restricted and managed |
| 8.3 | Information access restriction | Restricted per access control policy |
| 8.4 | Access to source code | Read/write access to code/tools/libraries managed |
| 8.5 | Secure authentication | Secure technologies/procedures implemented |
| 8.6 | Capacity management | Resource use monitored and adjusted to needs |
| 8.7 | Protection against malware | Implemented, supported by user awareness |
| 8.8 | Management of technical vulnerabilities | Info obtained, exposure evaluated, measures taken |
| 8.9 | Configuration management | Established, documented, monitored, reviewed |
| 8.10 | Information deletion | Deleted when no longer required |
| 8.11 | Data masking | Used per access control policy and business requirements |
| 8.12 | Data leakage prevention | Applied to systems handling sensitive info |
| 8.13 | Information backup | Maintained and regularly tested |
| 8.14 | Redundancy of information processing facilities | Sufficient to meet availability requirements |
| 8.15 | Logging | Produced, stored, protected, analyzed |
| 8.16 | Monitoring activities | Monitored for anomalous behavior |
| 8.17 | Clock synchronization | Synchronized to approved time sources |
| 8.18 | Use of privileged utility programs | Restricted and tightly controlled |
| 8.19 | Installation of software on operational systems | Securely managed |
| 8.20 | Networks security | Secured, managed, controlled |
| 8.21 | Security of network services | Identified, implemented, monitored |
| 8.22 | Segregation of networks | Groups of services/users/systems segregated |
| 8.23 | Web filtering | Access to external sites managed |
| 8.24 | Use of cryptography | Rules including key management defined and implemented |
| 8.25 | Secure development life cycle | Rules for secure development established and applied |
| 8.26 | Application security requirements | Identified/specified/approved when developing/acquiring apps |
| 8.27 | Secure system architecture and engineering principles | Established and applied to development activities |
| 8.28 | Secure coding | Principles applied to software development |
| 8.29 | Security testing in development and acceptance | Defined and implemented in the dev life cycle |
| 8.30 | Outsourced development | Directed, monitored, reviewed |
| 8.31 | Separation of development, test and production environments | Separated and secured |
| 8.32 | Change management | Subject to change management procedures |
| 8.33 | Test information | Appropriately selected, protected, managed |
| 8.34 | Protection of information systems during audit testing | Planned and agreed between tester and management |

---

## 5. Cheat Sheet — Quick Revision

### 5.1 Numbers to memorize
- Mandatory clauses: 4–10 (7 clauses, no exclusions allowed under conformity)
- Total Annex A controls: 93, across 4 themes
- Organizational: 37 (5.1–5.37) · People: 8 (6.1–6.8) · Physical: 14 (7.1–7.14) · Technological: 34 (8.1–8.34)
- Third edition, published 2022-10, replacing the 2013 edition — the major 2022 change realigned Annex A with ISO/IEC 27002:2022 (2013 had 114 controls in 14 categories; 2022 consolidated to 93 in 4 themes)

### 5.2 Fast-answer bank

- **What is an ISMS?** Information Security Management System — the org's overall system of policies, processes, and controls for managing info-sec risk, built per Clauses 4–10.
- **Are all 93 Annex A controls mandatory?** No — all must be *considered* during risk treatment, but only relevant ones implemented; exclusions justified in the SoA.
- **What is a Statement of Applicability (SoA)?** A document listing every necessary control, why it's included, whether it's implemented, and justification for excluding any Annex A control — required under Clause 6.1.3(d).
- **Risk assessment vs. risk treatment?** Assessment (6.1.2) identifies/analyzes/evaluates risks. Treatment (6.1.3) selects and implements the response — controls, SoA, treatment plan, risk owner sign-off.
- **Can Clauses 4–10 be excluded?** No — the standard explicitly prohibits excluding any Clause 4–10 requirement under a conformity claim.
- **The 4 Annex A themes?** Organizational, People, Physical, Technological.
- **Who's accountable for ISMS outcomes?** Top management — Clause 5.1 assigns leadership accountability, not just IT/security teams.
- **What's needed before certification?** A functioning ISMS per Clauses 4–10, a completed risk assessment/treatment cycle, an SoA, at least one internal audit, and at least one management review — all with documented evidence.
- **ISO 27001 vs. ISO/IEC 27002?** 27001 = certifiable requirements standard (Clauses 4–10 + Annex A list). 27002 = detailed implementation guidance for each Annex A control. Certification is against 27001; 27002 explains the how.

### 5.3 Glossary

- **ISMS** — Information Security Management System, the overall system per Clauses 4–10
- **Interested party** — any stakeholder with a relevant requirement (regulator, customer, employee, supplier, shareholder)
- **Risk owner** — person/entity accountable for managing a specific risk, approves the treatment plan and accepts residual risk
- **Residual risk** — risk remaining after treatment/controls are applied
- **Statement of Applicability (SoA)** — document justifying included/excluded Annex A controls and their implementation status
- **Nonconformity** — failure to meet a requirement of the standard or the org's own ISMS documentation
- **Corrective action** — action to eliminate the cause of a nonconformity so it doesn't recur
- **Documented information** — any document/record the ISMS is required to create and retain
- **Top management** — the person/group directing and controlling the organization at the highest level
- **Certification body** — accredited third party that audits and issues the ISO 27001 certificate

### 5.4 Where this fits GRC applications

- "ISO 27001 experience" in a job posting usually means: can you help build/maintain a risk register, SoA, internal audit evidence, or management review pack. Name these specifically on a CV rather than just "familiar with ISO 27001."
- Pairing NIST CSF + ISO 27001 knowledge is a strong signal: CSF for outcome-based risk communication, ISO 27001 for certifiable management-system structure and control mapping.
- Many Annex A controls map cleanly onto CSF Subcategories (e.g. ISO 8.16 Monitoring activities ≈ CSF DE.CM). Cross-mapping frameworks is a genuinely valuable, differentiating skill at entry level.
