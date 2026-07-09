# GRC-Notes

Study notes and applied exercises across GRC frameworks — NIST CSF 2.0 and ISO/IEC 27001:2022 — built as part of an ongoing purple team / GRC learning track. Each framework folder pairs reference notes with at least one applied exercise: either scoped to a real project (MediScan AI Pro) or a fictional company scenario built to demonstrate the framework's working process.

## Framework comparison

| | NIST CSF 2.0 | ISO/IEC 27001:2022 |
|---|---|---|
| Nature | Voluntary guidance / taxonomy | Certifiable international standard |
| Answers | *What* outcomes to achieve | *How* to structure the management system, plus a control list |
| Structure | 6 Functions → Categories → Subcategories (106 total) | Clauses 4–10 (mandatory) + Annex A, 93 controls in 4 themes |
| Core artifact | Organizational Profile (Current / Target) + gap analysis | Statement of Applicability (SoA) + risk treatment plan |
| Certifiable? | No — you build a Profile, not a certificate | Yes — accredited third-party audit and certificate |
| Typical use | Internal risk communication, maturity benchmarking | External/contractual proof to clients and regulators |

They're complementary, not competing — many organizations use CSF internally to talk about risk maturity and ISO 27001 externally to prove their ISMS meets a recognized bar. A number of Annex A controls map cleanly onto CSF Subcategories (e.g. ISO 8.16 Monitoring activities ≈ CSF DE.CM) — cross-mapping between the two is one of the more differentiating GRC skills at entry level.

## Contents

### [`iso-27001/`](./iso-27001)
| File | What it is |
|---|---|
| [`study-notes.md`](./iso-27001/study-notes.md) | Clauses 4–10 (mandatory ISMS requirements), full Annex A control list (93 controls, 4 themes), glossary, and a quick-revision cheat sheet |
| [`mediscan-mini-soa.md`](./iso-27001/mediscan-mini-soa.md) | A mini Statement of Applicability scoping ~20 Annex A controls against MediScan AI Pro, with implementation status and inclusion/exclusion justification |

### [`nist-csf/`](./nist-csf)
| File | What it is |
|---|---|
| [`study-notes.md`](./nist-csf/study-notes.md) | The six CSF 2.0 Functions (Govern, Identify, Protect, Detect, Respond, Recover) and how they map to SOC/GRC workflows |
| [`csf-applied-gap-analysis-example.md`](./nist-csf/csf-applied-gap-analysis-example.md) | A worked example walking a fictional company through the full Profile lifecycle — Current Profile, Target Profile, gap analysis, and POA&M |

## Skills demonstrated across this repo

- **Framework literacy**: reading primary-source standards (not summaries of them) and extracting what's actually mandatory vs. optional
- **Applied scoping**: deciding what's in/out of scope and justifying it, rather than treating every control/subcategory as equally relevant
- **Honest gap assessment**: both applied exercises deliberately show partial/not-achieved states rather than inflating maturity — that's what makes a gap analysis or SoA useful to an auditor
- **Cross-framework thinking**: recognizing where CSF and ISO 27001 overlap and where they diverge, rather than treating them as interchangeable

## Related repos

- [`htb-writeups`](https://github.com/Nida-creator/htb-writeups) — HackTheBox machine writeups
- [`portswigger-notes`](https://github.com/Nida-creator/portswigger-notes) — PortSwigger Web Security Academy lab notes
