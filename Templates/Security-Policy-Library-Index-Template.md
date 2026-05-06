# Security Policy Library Index Template

| Field | Value |
|-------|-------|
| **Document ID** | PLI-001 |
| **Organisation** | [Company Name] |
| **Version** | 1.0 |
| **Owner** | CISO |
| **Reviewed By** | GRC Lead |
| **Last Updated** | DD-MMM-YYYY |
| **Classification** | Internal |
| **Framework Refs** | ISO 27001:2022 A.5.1 | ISO 27001:2022 Clause 7.5 |

---

## Purpose

This Policy Library Index provides a complete register of all information security policies, standards, and procedures maintained by [Company Name]. It serves as the authoritative list of all GRC documentation and enables audit readiness, policy lifecycle management, and governance oversight.

---

## Policy Hierarchy

```
Level 1 — Board Policies (Board/CEO approval required)
  ↓ Governed by
Level 2 — Management Standards (CISO approval required)
  ↓ Implemented by
Level 3 — Operational Procedures (IT Manager / GRC Lead approval)
  ↓ Supplemented by
Level 4 — Guidelines and Best Practices (CISO approval; advisory)
```

---

## Policy Lifecycle

| Stage | Description | Responsible |
|-------|-------------|-------------|
| **Draft** | Initial document created by policy author | GRC Lead / CISO |
| **Review** | Reviewed by Legal, IT, and relevant business stakeholders | GRC Lead |
| **Approval** | Formally approved by appropriate authority | CEO/Board (Level 1); CISO (Level 2–3) |
| **Publication** | Published to all staff via intranet/email | GRC Lead |
| **Monitor** | Compliance monitored via awareness training completion, control testing | GRC Lead |
| **Review Cycle** | Annual review of all Level 1–2 documents; 2-year for Level 3–4 | GRC Lead |
| **Update** | Revise when: regulation changes; business changes; incident findings; annual review | Policy Owner |
| **Retire** | Retire superseded documents with documented reason | CISO |

---

## Policy Exception Process

When an operational requirement prevents full compliance with a policy:

1. **Submit exception request** to GRC Lead using the Policy Exception Request form
2. **Risk assessment:** GRC Lead assesses risk of granting exception
3. **Approval:** Exceptions require CISO approval (Level 1 policies: CEO approval)
4. **Time-limited:** All exceptions are granted for maximum 90 days with a mandatory review
5. **Documentation:** All exceptions recorded in the Policy Exception Register
6. **Compensating controls:** All exceptions require compensating controls to mitigate the risk

---

## Policy Register — Level 1: Board-Approved Policies

| Policy ID | Policy Name | Version | Status | Owner | Approved By | Effective Date | Next Review | ISO 27001 Ref | PCI-DSS Ref | GDPR Ref | Training Req | Location |
|-----------|-------------|---------|--------|-------|------------|---------------|-------------|--------------|------------|---------|-------------|----------|
| POL-001 | Information Security Policy | 1.2 | Active | CISO | Board | 2025-01-01 | 2026-01-01 | A.5.1, Clause 5.2 | Req 12.1 | Art. 32 | All staff (annual) | SharePoint/Policies |
| POL-002 | Acceptable Use Policy | 1.1 | Active | CISO | CEO | 2025-01-01 | 2026-01-01 | A.5.10, A.6.2, A.8.1 | Req 12.4 | Art. 32 | All staff (onboarding + annual) | SharePoint/Policies |
| POL-003 | Access Control Policy | 1.0 | Active | Head of IT | CISO | 2025-02-01 | 2026-02-01 | A.5.15–5.22, A.8.2 | Req 7, 8 | Art. 32 | All staff (annual); IT (enhanced) | SharePoint/Policies |
| POL-004 | Password and Authentication Policy | 1.0 | Active | Head of IT | CISO | 2025-02-01 | 2026-02-01 | A.8.5 | Req 8 | Art. 32 | All staff (annual) | SharePoint/Policies |
| POL-005 | Incident Response Policy | 1.0 | Active | CISO | CEO | 2025-01-01 | 2026-01-01 | A.5.24–5.28 | Req 12.10 | Art. 33, 34 | IT + GRC (annual tabletop) | SharePoint/Policies |
| POL-006 | Data Classification Policy | 1.0 | Active | DPO | CISO | 2025-02-01 | 2026-02-01 | A.5.12, A.5.13 | Req 3.1 | Art. 5 | All staff (annual) | SharePoint/Policies |
| POL-007 | Remote Working Policy | 1.0 | Active | CISO | CISO | 2025-02-01 | 2026-02-01 | A.6.7, A.8.1 | Req 12.5 | Art. 32 | Remote staff (annual) | SharePoint/Policies |
| POL-008 | Vendor Management Policy | 1.0 | Active | GRC Lead | CISO | 2025-03-01 | 2026-03-01 | A.5.19–5.22 | Req 12.8 | Art. 28 | Procurement + Legal (annual) | SharePoint/Policies |
| POL-009 | Business Continuity Policy | 1.0 | Active | CISO | CEO | 2025-03-01 | 2026-03-01 | A.5.29, A.5.30 | Req 12.4 | — | All staff (annual) | SharePoint/Policies |
| POL-010 | Cryptography Policy | 1.0 | Active | Head of IT | CISO | 2025-02-01 | 2026-02-01 | A.8.24, A.8.25 | Req 3, 4 | Art. 32 | IT (annual) | SharePoint/Policies |
| POL-011 | Patch Management Policy | 1.0 | Active | Head of IT | CISO | 2025-02-01 | 2026-02-01 | A.8.8 | Req 6 | — | IT (annual) | SharePoint/Policies |
| POL-012 | Change Management Policy | 1.0 | Active | Head of IT | CISO | 2025-03-01 | 2026-03-01 | A.8.32 | Req 6.3 | — | IT + DevOps (annual) | SharePoint/Policies |
| POL-013 | Data Retention and Deletion Policy | 1.0 | Active | DPO | CISO | 2025-03-01 | 2026-03-01 | A.5.33, A.5.34 | Req 3.1, 3.2 | Art. 5(1)(e) | All staff (annual) | SharePoint/Policies |
| POL-014 | Physical Security Policy | 1.0 | Active | Facilities Director | CISO | 2025-02-01 | 2026-02-01 | A.7 | Req 9 | — | All staff (annual) | SharePoint/Policies |
| POL-015 | AI Use Policy | 1.0 | Active | CISO | CEO | 2025-04-01 | 2026-04-01 | A.5.1 | — | Art. 22 | All staff (annual) | SharePoint/Policies |

---

## Policy Register — Level 2: Management Standards

| Standard ID | Standard Name | Version | Owner | Approved By | Review Date | Linked Policy | ISO 27001 Ref |
|-------------|--------------|---------|-------|------------|-------------|--------------|--------------|
| STD-001 | Password Standard | 1.0 | Head of IT | CISO | 2026-02-01 | POL-004 | A.8.5 |
| STD-002 | Network Security Standard | 1.0 | Head of IT | CISO | 2026-03-01 | POL-001 | A.8.20, A.8.21 |
| STD-003 | Encryption Standard | 1.0 | Head of IT | CISO | 2026-02-01 | POL-010 | A.8.24 |
| STD-004 | Cloud Security Standard | 1.0 | Head of IT | CISO | 2026-04-01 | POL-001 | A.5.23, A.8.25 |
| STD-005 | Data Classification Standard | 1.0 | DPO | CISO | 2026-02-01 | POL-006 | A.5.12, A.5.13 |
| STD-006 | Vulnerability Management Standard | 1.0 | Head of IT | CISO | 2026-02-01 | POL-011 | A.8.8 |

---

## Policy Register — Level 3: Operational Procedures

| Procedure ID | Procedure Name | Version | Owner | Review Date | Linked Policy | Frequency of Use |
|-------------|---------------|---------|-------|-------------|--------------|----------------|
| PRO-001 | User Account Provisioning Procedure | 1.0 | Head of IT | 2026-01-01 | POL-003 | Per event (new hire) |
| PRO-002 | User Account Deprovisioning Procedure | 1.0 | Head of IT | 2026-01-01 | POL-003 | Per event (termination) |
| PRO-003 | Quarterly Access Review Procedure | 1.0 | Head of IT | 2026-02-01 | POL-003 | Quarterly |
| PRO-004 | Incident Reporting Procedure | 1.0 | CISO | 2026-01-01 | POL-005 | Per event |
| PRO-005 | GDPR Breach Notification Procedure | 1.0 | DPO | 2026-01-01 | POL-005 | Per event |
| PRO-006 | Vendor Risk Assessment Procedure | 1.0 | GRC Lead | 2026-03-01 | POL-008 | Per vendor / Annual |
| PRO-007 | Secure Device Disposal Procedure | 1.0 | Head of IT | 2026-02-01 | POL-014 | Per event |
| PRO-008 | Backup and Recovery Procedure | 1.0 | Head of IT | 2026-03-01 | POL-009 | Regular + per incident |
| PRO-009 | SAR (Subject Access Request) Procedure | 1.0 | DPO | 2026-01-01 | POL-013 | Per event |
| PRO-010 | Change Management Procedure (CAB) | 1.0 | Head of IT | 2026-03-01 | POL-012 | Per change |

---

## Policy Compliance Summary

| Policy | Training Required | Last Training Date | Completion Rate | Status |
|--------|-----------------|-------------------|----------------|--------|
| POL-001 Information Security Policy | All staff — annual | 2025-01-15 | 91% | Amber (target 95%) |
| POL-002 Acceptable Use Policy | All staff — onboarding | Ongoing | 100% new hires | Green |
| POL-003 Access Control Policy | All staff — annual | 2025-01-15 | 91% | Amber |
| POL-005 Incident Response Policy | IT/GRC — annual tabletop | 2025-03-10 | 100% of IR team | Green |
| [All other policies] | | | | |

---

## Annual Policy Review Calendar

| Quarter | Policies Due for Review |
|---------|------------------------|
| Q1 (Jan–Mar) | POL-001, POL-005, POL-009 (board-level policies) |
| Q2 (Apr–Jun) | POL-002, POL-003, POL-004, POL-006 |
| Q3 (Jul–Sep) | POL-007, POL-008, POL-010, POL-011 |
| Q4 (Oct–Dec) | POL-012, POL-013, POL-014, POL-015 |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | YYYY-MM-DD | [Name] | Initial policy library index |

---

*Security Policy Library Index | v1.0 | ISO 27001:2022 A.5.1 | Clause 7.5 — Documented Information*
