# Control Testing Workbook Template

| Field | Value |
|-------|-------|
| **Document ID** | CTW-Q1-2025 |
| **Organisation** | [Company Name] |
| **Test Period** | Q1 2025 (January – March 2025) |
| **Version** | 1.0 |
| **Framework** | ISO 27001:2022 / SOC 2 (Common Criteria) |
| **Lead Tester** | [Name / Role] |
| **Reviewed By** | [CISO / GRC Manager] |
| **Classification** | Confidential — Internal |

---

## Purpose

This Control Testing Workbook documents the results of quarterly internal control testing. It provides management and auditors with evidence that security controls are operating effectively. Results are reported to the Security Steering Committee and inform the external ISO 27001 surveillance audit / SOC 2 Type II opinion.

---

## Testing Methodology

### Control Testing Types

| Method | Definition | Evidence Collected |
|--------|------------|------------------|
| **Inquiry** | Interview control owner or responsible staff | Meeting notes / interview record |
| **Observation** | Watch the control being performed | Observation record; photograph/screenshot |
| **Inspection** | Examine documentary evidence (policies, records, reports) | Document copies; system exports |
| **Re-performance** | Independently re-execute the control to verify result | Independent execution record; output comparison |

### Sample Size Guidance

| Population Size | Recommended Sample |
|----------------|-------------------|
| 1–25 | Test all items |
| 26–60 | Test 25 items |
| 61–100 | Test 30 items |
| 101–250 | Test 40 items |
| 251–500 | Test 50 items |
| 501+ | Test 60 items |

### Control Assessment Ratings

| Rating | Definition |
|--------|------------|
| **Effective** | Control operated consistently as designed during the period; no exceptions |
| **Minor Deficiency** | Isolated exceptions (<5% exception rate); control generally effective |
| **Significant Deficiency** | Multiple exceptions (5–20% exception rate); control not consistently effective |
| **Material Weakness** | Pervasive exceptions (>20% exception rate); control fundamentally ineffective |
| **Not Tested** | Control not in scope for this period or evidence unavailable |

---

## Control Testing Results — Q1 2025

### Domain 1: Access Control

---

**Control CT-001**

| Field | Detail |
|-------|--------|
| **Control ID** | CT-001 |
| **Framework Reference** | ISO 27001 A.5.18 / SOC 2 CC6.3 |
| **Control Name** | Quarterly User Access Review |
| **Control Assertion** | User access rights are formally reviewed quarterly; access removed where no longer required |
| **Control Owner** | Head of IT |
| **Population** | 247 user accounts in Active Directory |
| **Sample Size** | 40 accounts |
| **Test Period** | Q1 2025 (Jan–Mar) |
| **Testing Method** | Inspection |

**Evidence Examined:**
| Evidence ID | Evidence Description | Date Collected | Source |
|-------------|---------------------|---------------|--------|
| EV-001 | Active Directory user account export (Jan 15, 2025) | 15-Jan-2025 | Active Directory |
| EV-002 | Q1 Access Review completion sign-off record | 20-Jan-2025 | SharePoint HR folder |
| EV-003 | Access removal tickets for Q1 2025 | 15-Jan to 31-Mar | ServiceNow |
| EV-004 | HR active employee list (matched against AD export) | 15-Jan-2025 | Workday HR |

**Test Procedure:**
1. Obtained AD user account export (EV-001) showing all 247 active accounts
2. Obtained Q1 access review sign-off record (EV-002) confirming review was conducted on 12-Jan-2025
3. Selected random sample of 40 accounts from the 247 population
4. Compared each sampled account against HR active employee list (EV-004)
5. For accounts with role changes in Q1, verified that prior access was removed (EV-003)

**Test Results:**
| Metric | Value |
|--------|-------|
| Sample Size | 40 of 247 accounts |
| Exceptions Found | 2 |
| Exception Rate | 5% |
| Exception Description | 2 accounts belonged to employees who changed roles in Q1; previous role access not removed within 30-day SLA |

**Assessment:** **Minor Deficiency** — Access review conducted quarterly as required. 2 exceptions (5%) related to role-change access removal. Control design is effective; operating effectiveness has a minor gap.

**Management Response Required:** Yes — process update for role-change access removal workflow.

---

**Control CT-002**

| Field | Detail |
|-------|--------|
| **Control ID** | CT-002 |
| **Framework Reference** | ISO 27001 A.6.5 / SOC 2 CC6.5 |
| **Control Name** | Terminated Employee Access Deprovisioning |
| **Control Assertion** | Access to all systems is disabled within 24 hours of employee termination notification |
| **Control Owner** | Head of IT |
| **Population** | 18 terminations in Q1 2025 |
| **Sample Size** | 18 (test all — population < 25) |
| **Testing Method** | Inspection |

**Evidence Examined:**
| Evidence ID | Evidence Description | Date |
|-------------|---------------------|------|
| EV-005 | HR termination notifications Q1 2025 (18 records) | Various |
| EV-006 | Active Directory account deactivation log with timestamps | Various |
| EV-007 | ServiceNow deprovisioning tickets for Q1 terminations | Various |

**Test Results:**
| Metric | Value |
|--------|-------|
| Total Tested | 18 |
| Exceptions Found | 1 |
| Exception Rate | 5.6% |
| Exception Description | 1 account deactivated 72 hours after termination (HR notification delay — termination on Friday; IT not notified until Monday) |

**Assessment:** **Minor Deficiency** — Process generally effective. 1 exception due to communication gap over weekend. Recommend automating deprovisioning trigger from Workday to Active Directory.

---

**Control CT-003**

| Field | Detail |
|-------|--------|
| **Control ID** | CT-003 |
| **Framework Reference** | ISO 27001 A.8.5 / SOC 2 CC6.1 |
| **Control Name** | Multi-Factor Authentication — Microsoft 365 |
| **Control Assertion** | MFA is enforced for all Microsoft 365 user accounts via Azure AD Conditional Access |
| **Control Owner** | Head of IT |
| **Population** | 247 M365 user accounts |
| **Sample Size** | 40 accounts |
| **Testing Method** | Inspection |

**Evidence Examined:**
| Evidence ID | Evidence Description | Date |
|-------------|---------------------|------|
| EV-008 | Azure AD Conditional Access policy — "Require MFA for all users" export | 15-Jan-2025 |
| EV-009 | MFA registration status report for all 247 accounts | 15-Jan-2025 |

**Test Results:**
| Metric | Value |
|--------|-------|
| Accounts with MFA Enabled | 244 of 247 |
| Exceptions | 3 accounts: 2 service accounts, 1 user account |
| Exception Rate | 1.2% |
| Exception Description | 2 service accounts excluded from MFA CA policy (legacy app compatibility); 1 user account MFA not completed after onboarding |

**Assessment:** **Minor Deficiency** — 3 exceptions noted. Service accounts documented as exceptions with compensating controls in place. User account exception: user notified; MFA completed by test completion date. Recommend tracking service account MFA exclusions with formal exception log.

---

**Control CT-004**

| Field | Detail |
|-------|--------|
| **Control ID** | CT-004 |
| **Framework Reference** | ISO 27001 A.8.2 / SOC 2 CC6.3 |
| **Control Name** | Privileged Access Management — Admin Account Separation |
| **Control Assertion** | All IT administrators have separate admin accounts for privileged tasks; standard accounts not used for administrative functions |
| **Control Owner** | CISO |
| **Population** | 12 IT administrators |
| **Sample Size** | 12 (test all) |
| **Testing Method** | Inspection + Inquiry |

**Evidence Examined:**
| Evidence ID | Evidence Description | Date |
|-------------|---------------------|------|
| EV-010 | Active Directory admin account export (accounts with Admin group membership) | 15-Jan-2025 |
| EV-011 | CyberArk PAM session logs for Q1 2025 | Q1 2025 |
| EV-012 | Interview record — Head of IT confirming PAM rollout status | 20-Jan-2025 |

**Test Results:**
| Metric | Value |
|--------|-------|
| Total Admins | 12 |
| Using PAM Tool | 9 |
| Exceptions | 3 admins not yet enrolled in CyberArk PAM |
| Exception Rate | 25% |
| Exception Description | 3 legacy application server admins not yet onboarded to PAM; PAM rollout in progress (target Q2 2025) |

**Assessment:** **Significant Deficiency** — 25% of admin accounts not managed through PAM. Control is in remediation (documented in risk register as RR-002). Expected remediation: Q2 2025. Recommend monthly tracking until full PAM enrolment achieved.

---

### Domain 2: Change Management

---

**Control CT-005**

| Field | Detail |
|-------|--------|
| **Control ID** | CT-005 |
| **Framework Reference** | ISO 27001 A.8.32 / SOC 2 CC8.1 |
| **Control Name** | Change Management — Production Change Authorisation |
| **Control Assertion** | All changes to production systems are authorised via the Change Advisory Board (CAB) prior to deployment |
| **Control Owner** | Head of IT |
| **Population** | 47 production changes in Q1 2025 |
| **Sample Size** | 25 changes |
| **Testing Method** | Inspection |

**Evidence Examined:**
| Evidence ID | Evidence Description | Date |
|-------------|---------------------|------|
| EV-013 | ServiceNow change request list Q1 2025 (47 changes) | Various |
| EV-014 | CAB meeting minutes Q1 2025 (3 CAB meetings) | Jan, Feb, Mar 2025 |
| EV-015 | Change deployment logs from AWS CloudTrail | Q1 2025 |

**Test Results:**
| Metric | Value |
|--------|-------|
| Sample Tested | 25 of 47 |
| Exceptions | 0 |
| Exception Rate | 0% |

**Assessment:** **Effective** — All 25 sampled production changes had documented CAB approval prior to deployment. CAB minutes confirm approval for each change. CloudTrail logs confirm deployment occurred after CAB approval.

---

### Domain 3: Vulnerability Management

---

**Control CT-006**

| Field | Detail |
|-------|--------|
| **Control ID** | CT-006 |
| **Framework Reference** | ISO 27001 A.8.8 / SOC 2 CC7.1 |
| **Control Name** | Critical Vulnerability Remediation SLA |
| **Control Assertion** | Critical vulnerabilities (CVSS ≥ 9.0) are patched within 48 hours of identification |
| **Control Owner** | Head of IT |
| **Population** | 8 Critical CVEs identified in Q1 2025 |
| **Sample Size** | 8 (test all) |
| **Testing Method** | Inspection |

**Evidence Examined:**
| Evidence ID | Evidence Description | Date |
|-------------|---------------------|------|
| EV-016 | Qualys vulnerability scan reports Q1 2025 | Weekly |
| EV-017 | Patch deployment records from SCCM/AWS SSM | Q1 2025 |
| EV-018 | Vulnerability remediation tracker (JIRA) | Q1 2025 |

**Test Results:**
| CVE ID | Identified Date | Patch Applied Date | Days to Patch | SLA Met? |
|--------|----------------|-------------------|---------------|---------|
| CVE-2025-0001 | Jan 8 | Jan 9 | 1 day | Yes |
| CVE-2025-0002 | Jan 22 | Jan 23 | 1 day | Yes |
| CVE-2025-0003 | Feb 5 | Feb 7 | 2 days | Yes |
| CVE-2025-0004 | Feb 14 | Feb 21 | 7 days | **No — exceeded 48hr SLA** |
| CVE-2025-0005 | Mar 1 | Mar 2 | 1 day | Yes |
| CVE-2025-0006 | Mar 10 | Mar 11 | 1 day | Yes |
| CVE-2025-0007 | Mar 18 | Mar 18 | 0 days | Yes |
| CVE-2025-0008 | Mar 25 | Mar 27 | 2 days | Yes |

**Exception Rate:** 1 of 8 (12.5%) — CVE-2025-0004 patched in 7 days (legacy server required extended testing)

**Assessment:** **Minor Deficiency** — 1 exception with documented justification (legacy server compatibility testing). Recommend updating SLA to include exception process for legacy systems with compensating controls documented.

---

## Deficiency Summary

| Deficiency ID | Control | Finding | Severity | Owner | Target Date | Status |
|--------------|---------|---------|----------|-------|------------|--------|
| DEF-001 | CT-001 (Access Review) | Role-change access removal gap | Minor | Head of IT | [Date] | Open |
| DEF-002 | CT-002 (Termination) | Weekend notification gap | Minor | HR/IT | [Date] | Open |
| DEF-003 | CT-003 (MFA) | 3 accounts without MFA | Minor | Head of IT | [Date] | 1 Closed; 2 ongoing (service accounts) |
| DEF-004 | CT-004 (PAM) | 3 admins not enrolled in PAM | Significant | CISO | Q2 2025 | Open — remediation in progress |
| DEF-005 | CT-006 (Vuln SLA) | 1 CVE exceeded 48hr SLA | Minor | Head of IT | [Date] | Closed — exception documented |

---

## Control Effectiveness Summary Dashboard

| Domain | Controls Tested | Effective | Minor Deficiency | Significant Deficiency | Material Weakness |
|--------|----------------|-----------|-----------------|----------------------|------------------|
| Access Control | 4 | 0 | 3 | 1 | 0 |
| Change Management | 1 | 1 | 0 | 0 | 0 |
| Vulnerability Management | 1 | 0 | 1 | 0 | 0 |
| **Total** | **6** | **1** | **4** | **1** | **0** |
| **%** | | **17%** | **67%** | **17%** | **0%** |

---

## Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Lead Tester | | | |
| GRC Manager / CISO | | | |

---

*Control Testing Workbook | Q1 2025 | ISO 27001:2022 | SOC 2 Common Criteria | Version 1.0*
