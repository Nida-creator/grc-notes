# NIST Cybersecurity Framework (CSF) 2.0 — Study Notes
*Plain-English breakdown for GRC beginners | Source: NIST CSWP 29, Feb 26, 2024*

---

## 1. The Big Picture — What Even Is the CSF?

Think of the CSF as a **common language / checklist of "what good looks like"** for managing cybersecurity risk. It does **NOT** tell you *how* to do something (no "install this firewall" instructions). It tells you **WHAT outcomes** you should be aiming for, and then points you to other resources for the "how."

**Key facts to memorize:**
| Fact | Detail |
|---|---|
| Full name | Cybersecurity Framework (CSF) 2.0 |
| Publisher | NIST (National Institute of Standards and Technology) |
| Published | February 26, 2024 |
| Old name (before v2.0) | "Framework for Improving Critical Infrastructure Cybersecurity" |
| Who is it for | ANY organization — any size, sector, or maturity level (not just critical infrastructure anymore — that's the big change in 2.0) |
| Is it mandatory? | No — voluntary, but can be adopted via policy/regulation |
| Is it country-specific? | No — sector-, country-, and technology-neutral |

**Why this matters for GRC:** This is the "universal translator" framework. You'll use it to talk to executives (who care about risk/money) and engineers (who care about controls) using the same vocabulary.

---

## 2. The Three Big Building Blocks of CSF 2.0

The CSF has **three main components**. Don't confuse these — they get tested/asked about constantly:

1. **CSF Core** — The taxonomy (list) of cybersecurity outcomes. The "what to do."
2. **CSF Organizational Profiles** — A snapshot of where YOUR org stands vs. where it wants to be.
3. **CSF Tiers** — A maturity rating for HOW WELL an org governs/manages cyber risk (not a maturity score for each outcome — that's a common mix-up).

---

## 3. CSF Core — The Heart of the Framework

The Core is organized as a **hierarchy**, like a family tree:

```
FUNCTION (6 total)
   └── CATEGORY (22 total)
          └── SUBCATEGORY (106 total — the specific outcomes)
```

- **Functions** = highest level, named after a verb (Govern, Identify, Protect...)
- **Categories** = groups of related outcomes within a Function
- **Subcategories** = the specific, detailed outcomes (this is where the real "checklist" items live)

> ⚠️ **Important nuance:** The order/numbering does NOT imply sequence or priority. You don't do GOVERN, then finish it, then move to IDENTIFY. They all happen **concurrently** (at the same time, continuously).

### 3.1 The 6 Functions (Memorize These Cold)

Picture the CSF wheel: **GOVERN sits in the center**, and the other 5 Functions surround it like spokes.

| # | Function | Code | One-line meaning |
|---|----------|------|-------------------|
| 1 | **GOVERN** | GV | Strategy, policy, and oversight are set — the "steering wheel" |
| 2 | **IDENTIFY** | ID | Know your risks — assets, threats, vulnerabilities |
| 3 | **PROTECT** | PR | Put safeguards in place to prevent/reduce bad outcomes |
| 4 | **DETECT** | DE | Find and analyze attacks/anomalies when they happen |
| 5 | **RESPOND** | RS | Take action once an incident is confirmed |
| 6 | **RECOVER** | RC | Restore normal operations after an incident |

**Memory trick:** G-I-P-D-R-R → "**G**ood **I**T **P**eople **D**etect **R**isks, **R**ecover" (or just remember: Govern → Identify → Protect → Detect → Respond → Recover, roughly the lifecycle of risk).

**How they relate to incidents (this is a favorite exam/interview point):**
- **Before an incident (prevent/prepare):** GOVERN, IDENTIFY, PROTECT
- **During/after an incident (discover/manage):** GOVERN, DETECT, RESPOND, RECOVER
- Notice GOVERN appears in **both** — it's the constant thread running through everything.

**What's NEW in CSF 2.0:** GOVERN is a brand-new 6th Function (didn't exist as its own Function in CSF 1.1). This reflects NIST's push to make cybersecurity a *board-level, enterprise risk management* topic — not just an IT problem.

### 3.2 Function Deep-Dive (Plain English)

**GOVERN (GV)** — *"Are we steering the ship on purpose?"*
- Sets strategy, expectations, and policy — and makes sure they're communicated and monitored.
- Covers: understanding your organization's context, setting risk strategy, defining roles/responsibilities, writing policy, executive oversight, and supply chain risk management.
- This Function tells the other 5 Functions **what to prioritize** based on mission and stakeholder needs.

**IDENTIFY (ID)** — *"What do we have, and what could hurt us?"*
- Understand your assets (data, hardware, software, systems, facilities, services, people) and your suppliers.
- Also covers finding ways to *improve* your processes over time.

**PROTECT (PR)** — *"Let's put locks on the doors."*
- Safeguards: identity/access management, security awareness training, data security, securing your tech platforms, and making your infrastructure resilient.

**DETECT (DE)** — *"Did something just happen?"*
- Continuous monitoring + analyzing events to spot attacks, compromises, or anomalies early.

**RESPOND (RS)** — *"Something happened — contain it."*
- Incident management, analysis, mitigation, reporting, and communication once an incident is declared.

**RECOVER (RC)** — *"Get back to normal, and tell people about it."*
- Restore systems/operations and communicate throughout the recovery process.

### 3.3 The 22 Categories (organized by Function)

| Function | Categories |
|---|---|
| **GOVERN** | Organizational Context (GV.OC) • Risk Management Strategy (GV.RM) • Roles, Responsibilities & Authorities (GV.RR) • Policy (GV.PO) • Oversight (GV.OV) • Cybersecurity Supply Chain Risk Mgmt (GV.SC) |
| **IDENTIFY** | Asset Management (ID.AM) • Risk Assessment (ID.RA) • Improvement (ID.IM) |
| **PROTECT** | Identity Mgmt, Authentication & Access Control (PR.AA) • Awareness & Training (PR.AT) • Data Security (PR.DS) • Platform Security (PR.PS) • Technology Infrastructure Resilience (PR.IR) |
| **DETECT** | Continuous Monitoring (DE.CM) • Adverse Event Analysis (DE.AE) |
| **RESPOND** | Incident Management (RS.MA) • Incident Analysis (RS.AN) • Incident Response Reporting & Communication (RS.CO) • Incident Mitigation (RS.MI) |
| **RECOVER** | Incident Recovery Plan Execution (RC.RP) • Incident Recovery Communication (RC.CO) |

**Note on Subcategories:** There are ~106 of them (the granular checklist items, like `GV.OC-01`, `ID.AM-01`, `PR.AA-03`, etc.). You don't need to memorize all of them, but understand the ID format: `[Category Code]-[Number]`. Gaps in numbering (e.g., ID.AM jumps from 05 to 07) exist because some old CSF 1.1 Subcategories got relocated elsewhere in 2.0 — this is normal, not a typo.

**Quick memorable highlights per Category (things GRC folks love to bring up):**
- **GV.SC** = Supply Chain Risk Management — brand new emphasis in 2.0, huge deal for vendor risk management work.
- **ID.AM** = Asset inventories (hardware, software, data, services, people) — "you can't protect what you don't know you have."
- **PR.AA** = Identity/Access — least privilege & separation of duties live here.
- **PR.DS** = Data Security — covers data at-rest, in-transit, AND in-use (new in 2.0), plus backups.
- **DE.AE** = Adverse Event Analysis — this is where "declaring an incident" officially happens (DE.AE-08).

---

## 4. CSF Organizational Profiles

**Plain English:** A Profile is basically a **snapshot document** — "here's where we are today" and/or "here's where we want to be." It's how you turn the generic CSF outcomes into something specific to YOUR organization.

### Types of Profiles

| Profile Type | What it captures |
|---|---|
| **Current Profile** | What outcomes you're *currently* achieving (or trying to), and how well |
| **Target Profile** | What outcomes you *want* to achieve — your goals, based on new requirements, tech changes, threat trends |
| **Community Profile** | A shared baseline built for a specific industry/sector/threat type by a *group* of organizations (not your own org) — you can use this as a starting point/template for your own Target Profile |

> 💡 **GRC exam tip:** Current Profile vs. Target Profile = the classic **gap analysis** setup. The difference between the two IS your risk register / action plan.

### The 5-Step Profile Lifecycle (memorize this — it's basically the GRC risk management cycle)

1. **Scope the Profile** — Decide what it covers (whole org? Just financial systems? Just ransomware risk?)
2. **Gather information** — Policies, risk priorities, business impact analyses, standards you follow, current tools/procedures
3. **Create the Profile** — Document current state (and/or target state) for chosen outcomes
4. **Analyze gaps + build an action plan** — Compare Current vs. Target → produce a risk register, risk detail report, or POA&M (Plan of Action & Milestones)
5. **Implement the plan + update the Profile** — Execute, then repeat the cycle (continuous improvement)

**Other uses of Profiles:**
- Share your Current Profile with partners/customers to show your cybersecurity maturity.
- Share a Target Profile with suppliers to set expectations of what THEY need to achieve.

---

## 5. CSF Tiers

**Plain English:** Tiers measure **HOW you manage risk** — not whether you've achieved specific outcomes. It's a maturity rating for your *governance style and process rigor*, applied at the organization level (or to a specific Profile).

⚠️ **Common misconception to avoid:** Tiers are **NOT** a maturity model for each Subcategory, and Tier 4 isn't automatically "better" for every org — it's about matching your rigor to your actual risk and resources (cost-benefit).

### The 4 Tiers

| Tier | Name | Governance flavor | Risk Mgmt flavor |
|---|---|---|---|
| **1** | **Partial** | Ad hoc, reactive, no formal prioritization | Limited awareness, case-by-case, little info sharing, unaware of supplier risk |
| **2** | **Risk Informed** | Approved by management but not org-wide policy yet | Awareness exists but no org-wide approach; informal info sharing; aware of supplier risk but inconsistent response |
| **3** | **Repeatable** | Formal, approved policy; reviewed & updated regularly | Org-wide approach; routine info sharing; consistent methods; supplier risk formally acted upon (contracts, governance structures) |
| **4** | **Adaptive** | Fully integrated into org culture and budget decisions; execs treat cyber risk like financial risk | Continuous improvement using lessons learned + predictive indicators; real-time supplier risk monitoring; constant info sharing |

**Memory trick:** Partial → Risk Informed → Repeatable → Adaptive = **P-R-R-A** ("**P**eople **R**arely **R**each **A**daptive" — because most orgs sit at Tier 2 or 3 realistically).

**Key line to remember:** *"Tiers should complement an organization's risk management methodology rather than replace it."* Progression to a higher Tier is encouraged when risk/mandates increase OR when a cost-benefit analysis justifies it — not just for the sake of it.

---

## 6. Online Resources That Supplement the CSF

Since the core document is deliberately generic and stable, NIST hosts **living, frequently-updated online resources** to help you actually implement it:

| Resource | What it is |
|---|---|
| **Informative References** | Mappings that link a CSF outcome to existing standards/regulations (e.g., a specific NIST SP 800-53 control might map to one Subcategory). Can be narrower OR broader than a Subcategory. |
| **Implementation Examples** | Notional, action-oriented example steps to help achieve a Subcategory's outcome (uses verbs like share, document, develop, monitor, analyze, assess, exercise). **Not** a required checklist — just illustrative. |
| **Quick-Start Guides (QSGs)** | Short, audience-specific guides with "first step" actionable advice (e.g., how to migrate from CSF 1.1 to 2.0) |
| **Community Profiles** | Sector/use-case-specific baseline Profiles (see Section 4) |
| **Organizational Profile Templates** | NIST-hosted templates to help you build your own Profile |

**Why this matters:** The Core document itself is updated *infrequently* (for stability), but these online resources update *often* — so always check the NIST CSF website for the latest versions, don't just rely on this PDF.

---

## 7. Communicating Risk Up and Down the Org (Section 5.1)

The CSF is designed to create a **two-way flow of information** between three organizational levels:

```
EXECUTIVES  ⇄  MANAGERS  ⇄  PRACTITIONERS
```

- **Executives → Managers:** Mission priority, risk appetite, budget
- **Managers → Executives:** Changes in current/future risk
- **Managers → Practitioners:** Framework Profiles (the target state to implement)
- **Practitioners → Managers:** Implementation progress (KPIs, KRIs)

**Plain English translation:**
- Execs decide *how much risk we're willing to accept* and *how much money we'll spend.*
- Managers translate that into a Target Profile (concrete goals).
- Practitioners (the technical staff) implement it and report back progress/metrics.
- This loop repeats continuously — it's the communication engine of the whole framework.

**GOVERN Function's special role here:** It's specifically what powers the exec-level conversation — strategy, supply chain risk, roles/authorities, policy, and oversight.

---

## 8. Integration With Other Risk Programs (Section 5.2)

The CSF isn't meant to run in isolation — it should plug into your organization's broader **Enterprise Risk Management (ERM)**. Key integration points:

### a) Cybersecurity Risk Assessment Programs
- Can complement **NIST RMF** (Risk Management Framework) — SP 800-37 (the process) and SP 800-30 (risk assessments) — and help prioritize SP 800-53 controls.

### b) Privacy Risk
- Cybersecurity and privacy are **related but separate disciplines** — they overlap only partially.
- **Cybersecurity risks** = come from loss of confidentiality, integrity, or availability (a breach).
- **Privacy risks** = come from *data processing itself* — even without any breach or hack (e.g., over-collecting data creates a privacy risk regardless of security).
- The overlap zone = "cybersecurity-related privacy events" (e.g., a data breach causing identity theft).
- Use the **NIST Privacy Framework** alongside CSF, and NIST's **PRAM** (Privacy Risk Assessment Methodology) for privacy-specific risk assessments.

### c) Supply Chain Risk (C-SCRM)
- Modern tech relies on complex, global, multi-tiered supply chains (acquirers, suppliers, developers, integrators, service providers).
- **C-SCRM** = Cybersecurity Supply Chain Risk Management — a systematic process to manage this exposure.
- Lives mainly in the **GV.SC** Category.
- Deep-dive reference: **SP 800-161r1**.

### d) Emerging Tech (AI)
- AI has its own risks beyond cyber/privacy (bias, safety, etc.).
- NIST built a companion **AI Risk Management Framework (AI RMF)** — uses the same Functions/Categories/Subcategories structure as CSF, so the two are designed to work together conceptually.

### Key NIST Documents for ERM Integration (good to recognize by name)
- NIST CSF 2.0 – Enterprise Risk Management Quick-Start Guide
- IR 8286 (and sub-parts A, B, C, D) — Integrating Cybersecurity and ERM
- SP 800-221 / SP 800-221A — ICT Risk within Enterprise Risk Portfolio

---

## 9. Glossary — Key Terms Cheat Sheet

| Term | Definition (plain English) |
|---|---|
| **CSF Core** | The full taxonomy of outcomes (Functions → Categories → Subcategories) |
| **CSF Function** | Top-level grouping (Govern, Identify, Protect, Detect, Respond, Recover) |
| **CSF Category** | Group of related outcomes within a Function |
| **CSF Subcategory** | Specific, detailed outcome — the most granular level |
| **Organizational Profile** | Your org's current/target cybersecurity posture, described using Core outcomes |
| **Current Profile** | What you're achieving *now* |
| **Target Profile** | What you *want* to achieve |
| **Community Profile** | Shared baseline built for a sector/use case by multiple orgs |
| **CSF Tier** | Rating of how mature/rigorous your risk governance & management practices are (1–4) |
| **Informative Reference** | A link/mapping from a CSF outcome to an existing standard or regulation |
| **Implementation Example** | A sample action step to help achieve an outcome |
| **Quick Start Guide (QSG)** | Short, audience-targeted "how to get started" guide |

---

## 10. Exam/Interview-Style Quick Recall Table

| Question | Answer |
|---|---|
| How many Functions? | 6 |
| How many Categories? | 22 |
| How many Subcategories? | ~106 |
| Which Function is new in 2.0? | GOVERN |
| Which Function sits in the center of the wheel? | GOVERN |
| Which Functions help *prevent* incidents? | Govern, Identify, Protect |
| Which Functions help *manage* incidents? | Govern, Detect, Respond, Recover |
| How many Tiers? | 4 (Partial, Risk Informed, Repeatable, Adaptive) |
| Do Tiers measure outcome achievement? | No — they measure governance/management rigor |
| What are the two types of Organizational Profile? | Current & Target |
| What powers exec-level risk conversations? | GOVERN Function |
| Where does Supply Chain Risk Management live? | GV.SC Category (under GOVERN) |
| Name the AI-focused companion framework | NIST AI RMF |
| Is the CSF mandatory? | No — voluntary (but can be adopted via policy/regulation) |
| Old name of the CSF before v2.0? | "Framework for Improving Critical Infrastructure Cybersecurity" |

---

*Notes compiled from NIST CSWP 29 (NIST Cybersecurity Framework 2.0), published February 26, 2024. For the full Subcategory list and Implementation Examples, visit the NIST CSF Reference Tool on the NIST CSF website.*
