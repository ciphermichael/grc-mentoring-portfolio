# Compliance Gap Assessment Template

| Field | Value |
|-------|-------|
| **Document ID** | CGA-001 |
| **Organisation** | [Company Name] |
| **Version** | 1.0 |
| **Assessment Date** | DD-MMM-YYYY |
| **Assessor** | [Name / Role] |
| **Frameworks Assessed** | ISO 27001:2022 | GDPR / UK GDPR | PCI-DSS v4.0 |
| **Scope** | [Define systems, data, and processes in scope] |
| **Classification** | Confidential — Internal |

---

## Purpose

This Compliance Gap Assessment evaluates the organisation's current compliance status against applicable regulatory and standards requirements. It identifies gaps requiring remediation and prioritises actions based on risk and regulatory exposure.

---

## Compliance Status Definitions

| Status | Code | Definition |
|--------|------|------------|
| **Compliant** | C | Requirement fully met; evidence available and current |
| **Partially Compliant** | PC | Controls exist but gaps or inconsistencies remain |
| **Non-Compliant** | NC | Requirement not met; no controls or insufficient controls |
| **Not Applicable** | N/A | Requirement does not apply (justification documented) |

---

## Gap Risk Rating

| Rating | Definition | Remediation Priority |
|--------|------------|---------------------|
| **Critical** | Non-compliance creates immediate risk of regulatory action, significant fine, or material breach | Immediate — within 30 days |
| **High** | Non-compliance creates elevated risk of regulatory breach or significant business impact | Short-term — within 90 days |
| **Medium** | Compliance gap poses moderate risk; acceptable for short period | Medium-term — within 180 days |
| **Low** | Minor compliance gap; low risk; best practice improvement | Long-term — within 12 months |

---

## Part 1: ISO 27001:2022 Compliance Assessment

### Clause 4–5: Context and Leadership

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| ISO-4.1 | Context of the organisation documented | NC | No | No context analysis performed; stakeholders not identified | High | Conduct context analysis; document internal/external issues | CISO | Q1 |
| ISO-4.3 | ISMS scope defined and documented | PC | Partial | Scope informally known; no formal scope statement | Critical | Write and approve formal ISMS Scope Statement | CISO | Q1 |
| ISO-5.1 | Top management commitment demonstrated | PC | Partial | CISO appointed; no board-level governance structure | High | Establish board security committee; CISO reports to CEO | CEO | Q1 |
| ISO-5.2 | Information Security Policy approved | PC | Yes (outdated) | IS Policy exists (2021); not board-approved; outdated | Critical | Update IS Policy; obtain board approval | CISO | Q1 |
| ISO-5.3 | Security roles and responsibilities defined | NC | No | No RACI or formal role definitions | High | Define all security roles; publish RACI matrix | CISO | Q1 |

### Clause 6: Planning

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| ISO-6.1.2 | Risk assessment process defined and performed | NC | No | No formal risk assessment ever conducted | Critical | Establish risk assessment methodology; conduct initial assessment | GRC Lead | Q1 |
| ISO-6.1.3 | Statement of Applicability (SoA) produced | NC | No | No SoA exists | Critical | Produce SoA v1.0 covering all 93 controls | GRC Lead | Q1 |
| ISO-6.2 | Security objectives established and communicated | NC | No | No documented security objectives | High | Define 5 measurable security objectives | CISO | Q1 |

### Clause 9–10: Evaluation and Improvement

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| ISO-9.1 | Monitoring and measurement defined | NC | No | No security metrics programme | High | Define KPIs; implement monthly reporting | GRC Lead | Q2 |
| ISO-9.2 | Internal audit programme established | NC | No | No internal audit function | Critical | Establish audit programme; conduct first audit | GRC Lead | Q2 |
| ISO-9.3 | Management review conducted | NC | No | Management review never conducted | Critical | Schedule and conduct quarterly management reviews | CISO | Q1 |
| ISO-10.2 | Non-conformance and corrective action process | NC | No | No corrective action tracking | High | Implement NCR tracking system | GRC Lead | Q2 |

---

## Part 2: GDPR / UK GDPR Compliance Assessment

### Data Governance Principles (Article 5)

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| GDPR-5.1a | Lawfulness, fairness, transparency | PC | Partial | Processing activities not mapped to lawful bases | High | Map all processing to lawful bases; document in RoPA | DPO | Q1 |
| GDPR-5.1b | Purpose limitation | PC | Partial | Some data used for secondary purposes without documentation | Medium | Audit data uses; update privacy notices | DPO | Q2 |
| GDPR-5.1e | Storage limitation | NC | No | No data retention policy; data retained indefinitely | High | Develop and implement data retention policy | DPO | Q1 |
| GDPR-5.2 | Accountability | PC | Partial | GDPR programme exists but not mature | High | Implement accountability framework; document compliance | DPO | Q2 |

### Individual Rights (Articles 15–22)

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| GDPR-15 | Right of access (SAR) — 30-day response | PC | Partial | 2 of 3 SARs responded to on time in last 6 months | High | Implement SAR tracking system; designate SAR coordinator | DPO | Q1 |
| GDPR-17 | Right to erasure | NC | No | No erasure process documented | High | Develop erasure procedure; test with IT | DPO | Q1 |
| GDPR-20 | Right to data portability | NC | No | No portability process | Medium | Develop data portability procedure | DPO | Q2 |

### Documentation Requirements (Article 30)

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| GDPR-30 | Record of Processing Activities (RoPA) | PC | Partial | RoPA exists but last updated 18 months ago; 3 processing activities not documented | Critical | Update RoPA; include all processing activities; review quarterly | DPO | Q1 |

### Data Breach (Articles 33–34)

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| GDPR-33 | ICO breach notification — 72 hours | NC | No | No breach notification procedure | Critical | Develop GDPR breach notification procedure; train staff | DPO | Q1 |
| GDPR-35 | DPIA for high-risk processing | NC | No | DPIAs not conducted for high-risk processing activities | High | Identify high-risk processing; conduct DPIAs | DPO | Q2 |

### International Transfers (Articles 44–49)

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| GDPR-44 | International transfers with adequate protection | NC | No | 1 US-based vendor receiving personal data without SCCs | Critical | Execute SCCs with all non-UK/EU processors; halt US transfer pending | Head of Legal | Q1 — Immediate |

---

## Part 3: PCI-DSS v4.0 Compliance Assessment

### Core Requirements

| Req ID | Requirement | Status | Evidence Available | Gap Description | Risk | Recommendation | Owner | Target Date |
|--------|-------------|--------|-------------------|----------------|------|----------------|-------|------------|
| PCI-1 | Install and maintain network security controls | PC | Partial | Firewalls in place; segmentation incomplete — cardholder systems not fully segmented | Critical | Complete network segmentation; DMZ for payment servers | Head of IT | Q2 |
| PCI-3 | Protect stored account data | PC | Partial | Encryption at rest confirmed; truncation of PAN not verified in all systems | High | Verify PAN truncation in all card-data systems | Head of IT | Q2 |
| PCI-5 | Protect all systems from malicious software | PC | Partial | AV on endpoints; 2 legacy servers lack endpoint protection | High | Deploy AV/EDR to all in-scope systems | Head of IT | Q1 |
| PCI-6 | Develop and maintain secure systems and software | PC | Partial | Patch management inconsistent; Critical patches averaging 5 days (vs 1-day requirement for CDE) | Critical | Implement separate patch SLA for CDE systems (Critical: 24hr) | Head of IT | Q1 |
| PCI-7 | Restrict access to cardholder data — need to know | PC | Partial | Access controls in place; no formal access review for CDE specifically | High | Implement quarterly CDE-specific access reviews | Head of IT | Q2 |
| PCI-8 | Identify users and authenticate access | PC | Partial | MFA on O365; not enforced for CDE systems specifically | Critical | Enforce MFA for all access to cardholder data environment | Head of IT | Q1 |
| PCI-10 | Log and monitor all access to cardholder data | NC | No | Logging enabled; daily review of CDE logs not occurring | Critical | Implement daily CDE log review procedure; SIEM alerting | Head of IT | Q1 |
| PCI-11 | Test security systems regularly | PC | Partial | Internal scans: quarterly; external scans: last conducted 15 months ago (overdue) | Critical | Schedule ASV external scan immediately; quarterly thereafter | GRC Lead | Immediate |
| PCI-12 | Support information security with policies and programs | PC | Partial | IS Policy exists; not formally covering all PCI-DSS Req 12 requirements | High | Update IS Policy and supporting standards for PCI alignment | CISO | Q1 |
| PCI-12.3.1 | Annual policy review | NC | No | Policies not reviewed in last 24 months | High | Conduct immediate policy review; establish annual review calendar | CISO | Q1 |
| PCI-12.8 | Manage third-party service provider risk | NC | No | CloudPay (payment processor) never formally assessed | Critical | Conduct VRAQ for CloudPay within 30 days | GRC Lead | Immediate |
| PCI-12.10 | Incident response plan for cardholder data breaches | NC | No | No IR plan covering PCI-DSS breach scenarios | Critical | Develop IR plan covering cardholder data breach response | CISO | Q1 |

---

## Executive Summary Dashboard

### Compliance by Framework

| Framework | Total Requirements Assessed | Compliant | Partially Compliant | Non-Compliant | Compliance % |
|-----------|---------------------------|-----------|--------------------|--------------|--------------| 
| ISO 27001:2022 (Clauses 4–10) | 18 | 0 | 6 | 12 | 17% |
| GDPR / UK GDPR | 15 | 3 | 5 | 7 | 27% |
| PCI-DSS v4.0 | 12 | 0 | 7 | 5 | 29% |
| **TOTAL** | **45** | **3** | **18** | **24** | **24%** |

### Gap Risk Summary

| Risk Level | Count | % of All Gaps |
|-----------|-------|--------------|
| Critical | 12 | 50% |
| High | 9 | 38% |
| Medium | 3 | 13% |
| Low | 0 | 0% |
| **Total Gaps** | **24** | |

---

## Prioritised Remediation Roadmap

### Immediate Actions (Within 30 Days)

| # | Action | Framework | Risk | Owner |
|---|--------|-----------|------|-------|
| 1 | Halt US data transfer to DataInsights pending SCCs | GDPR Art. 44 | Critical | Head of Legal |
| 2 | Schedule PCI-DSS ASV external vulnerability scan (overdue) | PCI-DSS Req 11 | Critical | GRC Lead |
| 3 | Conduct VRAQ for CloudPay payment processor | PCI-DSS Req 12.8 | Critical | GRC Lead |
| 4 | Enforce MFA for all CDE system access | PCI-DSS Req 8 | Critical | Head of IT |

### Short-Term Actions (31–90 Days)

| # | Action | Framework | Risk | Owner |
|---|--------|-----------|------|-------|
| 1 | Conduct formal ISO 27001 risk assessment | ISO 6.1.2 | Critical | GRC Lead |
| 2 | Develop GDPR breach notification procedure | GDPR Art. 33 | Critical | DPO |
| 3 | Update RoPA | GDPR Art. 30 | Critical | DPO |
| 4 | Develop IR plan for cardholder data breach scenarios | PCI-DSS Req 12.10 | Critical | CISO |
| 5 | Update Information Security Policy; board approval | ISO 5.2 | Critical | CISO |
| 6 | Implement CDE daily log review procedure | PCI-DSS Req 10 | Critical | Head of IT |
| 7 | Establish internal audit programme | ISO 9.2 | Critical | GRC Lead |

### Medium-Term Actions (91–180 Days)

| # | Action | Framework | Risk | Owner |
|---|--------|-----------|------|-------|
| 1 | Develop data retention policy | GDPR Art. 5(1)(e) | High | DPO |
| 2 | Complete network segmentation for CDE | PCI-DSS Req 1 | Critical | Head of IT |
| 3 | Conduct DPIAs for high-risk processing activities | GDPR Art. 35 | High | DPO |
| 4 | Implement SAR tracking system | GDPR Art. 15 | High | DPO |
| 5 | Define and publish security objectives | ISO 6.2 | High | CISO |
| 6 | Conduct first management review | ISO 9.3 | Critical | CISO |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | YYYY-MM-DD | [Name] | Initial gap assessment |

---

*Compliance Gap Assessment | v1.0 | ISO 27001:2022 | GDPR / UK GDPR | PCI-DSS v4.0*
