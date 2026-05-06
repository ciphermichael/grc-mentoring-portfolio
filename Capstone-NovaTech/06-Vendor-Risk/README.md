# Capstone — Section 06: Vendor Risk

> **NovaTech Corp | Week 23 Deliverables**

This folder contains NovaTech Corp's vendor risk management programme deliverables produced in Week 23 of the capstone project.

## Expected Deliverables

| File | Description | Status |
|------|-------------|--------|
| `NovaTech-Vendor-Risk-Register-v1.0.xlsx` | 15-vendor register with tier ratings, data accessed, DPA status, assessment due dates, current risk ratings | 🔴 Not Started |
| `NovaTech-VRAQ-CloudPay-v1.0.xlsx` | Full VRAQ for payment processor — SOC 2 Type II certified; sub-processor disclosure gap found; APPROVE WITH CONDITIONS | 🔴 Not Started |
| `NovaTech-VRAQ-DataInsights-Analytics-v1.0.xlsx` | Full VRAQ for US analytics vendor — NO ISO 27001 or SOC 2; US data transfer without SCCs; DO NOT APPROVE | 🔴 Not Started |
| `NovaTech-VRAQ-LegalEagle-LLP-v1.0.xlsx` | Limited VRAQ for legal counsel — Cyber Essentials Plus; limited scope; APPROVE | 🔴 Not Started |
| `NovaTech-VRAQ-TalentBridge-HR-v1.0.xlsx` | Full VRAQ for HR SaaS — ISO 27001 certified; good posture; APPROVE | 🔴 Not Started |
| `NovaTech-VRAQ-PenTest-Partners-v1.0.xlsx` | Full VRAQ for penetration testing firm — CREST certified; ISO 27001; APPROVE with enhanced controls during test windows | 🔴 Not Started |

## Vendor Tier Summary

| Vendor | Tier | Data | Key Risk |
|--------|------|------|---------|
| CloudPay Ltd. | 1 — Critical | Cardholder data | Never formally assessed; payment processor |
| Microsoft Azure/M365 | 1 — Critical | Identity + email | Large provider; review published SOC 2 |
| DataInsights Analytics | 1 — Critical | Customer behavioural data | US-based; no certs; NO SCCs — **CRITICAL ISSUE** |
| LegalEagle LLP | 2 — High | Legal/privileged docs | Professional privilege limits assessment scope |
| TalentBridge HR | 2 — High | 2,000 employee records | ISO 27001 certified; generally good |
| PenTest Partners | 1 — Critical | Network/system access | CREST certified; managed risk |

## GDPR Art. 28 Requirements

> Every vendor that processes NovaTech personal data **must** have a Data Processing Agreement (DPA) in place. This is a legal requirement, not a best practice. The DPA must include:
> - Processing only on NovaTech's documented instructions
> - Confidentiality obligations
> - Security measures (Art. 32)
> - Sub-processor approval requirements
> - Right to audit
> - 72-hour breach notification to NovaTech (to meet NovaTech's own ICO deadline)

## Framework References

- ISO 27001:2022 A.5.19–5.22 (Supplier relationships)
- GDPR Article 28 (Processor obligations)
- SOC 2 CC9 (Risk mitigation — vendor/supply chain)
- PCI-DSS v4.0 Req 12.8 (Third-party service providers)

## Instructions

See [Week 23 Assignment](../../Week-23/assignment.md) for full deliverable instructions.

---

> 🔴 Not Started | 🟡 In Progress | 🟢 Complete
