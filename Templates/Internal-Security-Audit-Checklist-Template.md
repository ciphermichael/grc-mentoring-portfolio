# Internal Security Audit Checklist Template

| Field | Value |
|-------|-------|
| **Audit Reference** | AUD-2025-001 |
| **Audit Title** | [e.g., Access Control Audit — Q1 2025] |
| **Organisation** | [Company Name] |
| **Audit Scope** | [Systems/domains in scope] |
| **Audit Criteria** | ISO 27001:2022 Annex A [control references] |
| **Audit Type** | Internal audit (First Party) |
| **Lead Auditor** | [Name] |
| **Audit Team** | [Names/Roles] |
| **Auditee** | [Department / Process Owner] |
| **Audit Period** | DD-MMM-YYYY to DD-MMM-YYYY |
| **Report Date** | DD-MMM-YYYY |
| **Classification** | Confidential — Internal |
| **Framework Refs** | ISO 27001:2022 Clause 9.2 | ISO 19011:2018 |

---

## Audit Objectives

1. Assess whether access control controls are implemented and effective as required by ISO 27001:2022 Annex A controls A.5.15 through A.5.22, A.8.2, A.8.3, and A.8.5.
2. Identify any non-conformances, observations, or areas of improvement.
3. Provide management with an independent opinion on the effectiveness of the access control programme.

---

## Testing Methods Reference

| Method | Description | When Used |
|--------|-------------|-----------|
| **Inquiry** | Ask the control owner or responsible staff how the control works | Understand the process; identify gaps in awareness |
| **Observation** | Watch the control being performed in real-time | Validate that the control operates as described |
| **Inspection** | Examine documentation, records, system outputs | Verify that activities have been performed and recorded |
| **Re-performance** | Independently re-execute the control procedure | Verify accuracy of output; validate the control works |

---

## Finding Severity Definitions

| Severity | Definition | Management Response Required |
|---------|-----------|------------------------------|
| **Critical** | Major non-conformance against ISO 27001 requirement or regulatory obligation; immediate risk of harm or audit failure | Immediate escalation; remediation plan within 5 business days |
| **High** | Significant control gap; elevated risk of breach or non-conformance | Remediation plan within 30 days |
| **Medium** | Control exists but operating below required standard; moderate risk | Remediation plan within 90 days |
| **Low** | Minor gap; best practice improvement; no immediate risk | Remediation within 180 days |
| **Informational** | Observation; no immediate remediation required; noted for future consideration | No immediate action; consider in next planning cycle |
| **Positive** | Control found to be effective and well-implemented | No action; document as good practice |

---

## Section 1: Access Control Policy and Governance

*Tests: Do documented policies and procedures exist and are they current?*

| Test ID | Control Ref | Test Description | Method | Criterion | Result | Finding? | Severity | Evidence Reference |
|---------|------------|-----------------|--------|-----------|--------|---------|----------|-------------------|
| T1.1 | A.5.15, A.5.1 | Access Control Policy exists, is approved by management, and was reviewed within the last 12 months | Inspection | Policy document present; approval signature; date ≤ 12 months | ☐ Pass ☐ Fail ☐ Partial | | | |
| T1.2 | A.5.15 | Access Control Policy is communicated to all relevant staff | Inquiry + Inspection | Training completion records; policy acknowledgement records | ☐ Pass ☐ Fail ☐ Partial | | | |
| T1.3 | A.5.16 | User account provisioning procedure is documented | Inspection | Procedure document present; includes manager approval workflow | ☐ Pass ☐ Fail ☐ Partial | | | |
| T1.4 | A.5.18 | Access review process is documented and defines frequency | Inspection | Review process document; frequency stated (quarterly minimum) | ☐ Pass ☐ Fail ☐ Partial | | | |
| T1.5 | A.8.2 | Privileged access management policy/procedure exists | Inspection | PAM policy document; defines what constitutes privileged access | ☐ Pass ☐ Fail ☐ Partial | | | |

**Section 1 Summary:** __ tests Pass | __ Fail | __ Partial

---

## Section 2: User Account Management

*Tests: Are user accounts created, modified, and removed according to policy?*

**Sample Selection:** Select [N] user accounts from the population of [Total] accounts. Risk-based sample: include recently created accounts (last 30 days), modified accounts, and accounts for sensitive roles.

| Test ID | Control Ref | Test Description | Method | Criterion | Population | Sample | Pass | Fail | Exception Rate | Finding? |
|---------|------------|-----------------|--------|-----------|-----------|--------|------|------|---------------|---------|
| T2.1 | A.5.16, A.5.18 | All active accounts have a valid, current owner in the organisation | Inspection (AD export vs HR records) | Active account status matches HR active employee status | [Total accounts] | [Sample] | | | | |
| T2.2 | A.5.16 | User accounts were provisioned with documented manager approval | Inspection (provisioning tickets) | ServiceNow/Jira ticket with manager approval prior to account creation | [Accounts created last 90 days] | [Sample] | | | | |
| T2.3 | A.6.5 | Terminated employee accounts deactivated within 24 hours of HR notification | Inspection (HR termination dates vs AD deactivation timestamps) | Deactivation timestamp ≤ 24 hours after HR termination date | [Terminations last 90 days] | [Sample] | | | | |
| T2.4 | A.5.18 | Access rights are reviewed at minimum quarterly | Inspection (access review completion records) | Signed completion record for each quarter; accounts reviewed match current population | [4 quarters] | All | | | | |
| T2.5 | A.5.18 | Access review results in removals where access is no longer required | Inspection + Inquiry | Evidence that review process triggers access removal; removal tickets present | [Last access review] | Sample findings | | | | |

**Section 2 Summary:** __ tests Pass | __ Fail | Total exceptions: __ / __ tested

---

## Section 3: Privileged Access Management

*Tests: Are privileged accounts separated from regular accounts and appropriately managed?*

**Population:** [Total privileged/admin accounts in Active Directory and cloud platforms]

| Test ID | Control Ref | Test Description | Method | Criterion | Population | Sample | Pass | Fail | Exception Rate | Finding? |
|---------|------------|-----------------|--------|-----------|-----------|--------|------|------|---------------|---------|
| T3.1 | A.8.2 | IT administrators have separate accounts for privileged tasks (not using regular accounts for admin) | Inspection (AD export; PAM tool) | Each admin user has two accounts: regular (domain\username) and admin (domain\admin_username) | [Admin count] | All | | | | |
| T3.2 | A.8.2 | Privileged accounts are managed via a PAM tool | Inspection | PAM tool in use; all privileged accounts enrolled | [Admin count] | All | | | | |
| T3.3 | A.8.2 | Privileged accounts are reviewed monthly | Inspection | Monthly review records; sign-off by CISO or Head of IT | Last 3 months | All | | | | |
| T3.4 | A.8.5 | MFA enforced on all privileged accounts | Inspection (Azure AD / PAM tool) | MFA status = Enabled for all admin accounts; no exceptions | [Admin count] | All | | | | |
| T3.5 | A.8.2 | Privileged account usage is logged and reviewed | Inspection (PAM tool logs; SIEM) | Logs present for privileged sessions; reviewed weekly | Last 30 days | Sample | | | | |
| T3.6 | A.8.2 | Admin rights are not permanently assigned (just-in-time access where possible) | Inquiry + Inspection | JIT access enabled in PAM; time-limited sessions | [N/A if no JIT] | | | | | |

**Section 3 Summary:** __ tests Pass | __ Fail | Critical gaps identified: Y/N

---

## Section 4: Multi-Factor Authentication

*Tests: Is MFA enforced across all required systems?*

| Test ID | Control Ref | Test Description | Method | Criterion | Evidence | Pass/Fail |
|---------|------------|-----------------|--------|-----------|---------|----------|
| T4.1 | A.8.5 | MFA enforced for all Microsoft 365 accounts | Inspection (Azure AD Conditional Access policy) | Conditional Access policy: "Require MFA for all users" — enabled; no exclusions | Azure AD CA policy export | |
| T4.2 | A.8.5 | MFA enforced for VPN access | Inspection (VPN gateway configuration) | MFA required before VPN session established | VPN configuration screenshots | |
| T4.3 | A.8.5 | MFA enforced for cloud platform console access (AWS/Azure) | Inspection (IAM/Azure AD policy) | MFA required for AWS Console and Azure portal; no exceptions | IAM policy; Azure AD policy | |
| T4.4 | A.8.5 | MFA enforced for remote desktop / remote access tools | Inquiry + Inspection | RDP and remote tools require MFA; documented in AUP | Configuration evidence | |
| T4.5 | A.8.5 | MFA status verified for sample of user accounts | Inspection (Azure AD MFA status export) | MFA status = Enabled for 100% of sampled accounts | MFA status export | |

**Section 4 Summary:** MFA coverage: __% of required systems

---

## Section 5: Password Policy

*Tests: Does the password policy meet minimum security requirements?*

| Test ID | Control Ref | Test Description | Method | Criterion | Evidence | Pass/Fail |
|---------|------------|-----------------|--------|-----------|---------|----------|
| T5.1 | A.8.5 | Password minimum length ≥ 12 characters (14+ recommended) | Inspection (AD Default Domain Policy) | Minimum password length setting | GPO screenshot | |
| T5.2 | A.8.5 | Password complexity enforced | Inspection | Complexity enabled: upper, lower, number, special character | GPO screenshot | |
| T5.3 | A.8.5 | Password history enforced (minimum 10 passwords) | Inspection | Password history = 10 or more | GPO screenshot | |
| T5.4 | A.8.5 | Account lockout policy exists | Inspection | Lockout after ≤ 10 failed attempts; lockout duration ≥ 15 minutes | GPO screenshot | |
| T5.5 | A.8.5 | Common/breached passwords blocked | Inquiry + Inspection | Azure AD Password Protection or equivalent; custom banned password list | Configuration evidence | |

---

## Section 6: System Access for External Parties

*Tests: Is third-party access controlled and monitored?*

| Test ID | Control Ref | Test Description | Method | Criterion | Evidence | Pass/Fail |
|---------|------------|-----------------|--------|-----------|---------|----------|
| T6.1 | A.5.19, A.5.20 | All external party access is governed by a written contract including security requirements | Inspection | Contract for each third party with system access; security clauses present | Vendor contract review | |
| T6.2 | A.8.2 | Third-party remote access requires MFA | Inspection | Vendor remote access sessions require MFA; no shared accounts | VPN/remote access logs | |
| T6.3 | A.5.19 | Third-party accounts are time-limited and deactivated after use | Inspection + Inquiry | Third-party account termination process; accounts deactivated after engagement | Account lifecycle records | |
| T6.4 | A.5.19 | Third-party access is logged and reviewed | Inspection | Logs of all third-party access sessions; reviewed by IT security | Access logs | |

---

## Audit Findings Register

| Finding ID | Test ID | Finding Title | Control Ref | Severity | Condition (What Was Found) | Criteria (What Was Required) | Cause (Root Cause) | Effect/Risk | Recommendation | Owner | Target Date |
|-----------|--------|--------------|------------|---------|--------------------------|---------------------------|--------------------|------------|---------------|-------|------------|
| F-001 | T2.3 | Terminated accounts not deactivated within 24-hour SLA | A.6.5 | High | 3 of 20 sampled terminations (15%) had accounts active beyond 24 hours — longest: 47 days post-termination | Access must be removed within 24 hours of HR notification per ACP v1.2 | Manual process — IT reliant on email from HR; HR sends email 1–3 days after termination date | Active accounts for departed employees create insider threat risk and violate ISO 27001 | Implement automated deprovisioning via ServiceNow integration with HR system | Head of IT | [Date] |
| F-002 | T3.1 | IT administrators using standard accounts for admin tasks | A.8.2 | Critical | 8 of 12 IT admins (67%) do not have separate admin accounts; use their regular account for all tasks including admin changes | All privileged users must use a separate, dedicated admin account for privileged tasks per IT Security Standard | Historical practice; no PAM tool enforced separation | Any compromise of an IT admin's regular account gives full admin access to all systems | Deploy PAM tool (CyberArk or equivalent); enforce admin account separation | CISO | [Date] |
| F-003 | T4.2 | MFA not enforced for VPN access | A.8.5 | High | VPN access requires username/password only; MFA not configured | MFA required for all remote access per ACP v1.2 | VPN gateway does not support MFA natively; workaround not implemented | Remote access without MFA is a primary attack vector for phishing and credential theft | Configure VPN to require Azure AD MFA via RADIUS | Head of IT | [Date] |
| F-POSITIVE-01 | T5.1–5.5 | Password policy meets ISO 27001 requirements | A.8.5 | Positive | Password policy: 14-char minimum; complexity enforced; history 12; lockout after 5 attempts | Policy meets ISO 27001 requirements | n/a | n/a | No action required — maintain current policy | Head of IT | n/a |

---

## Audit Conclusion

**Overall Audit Opinion:** ☐ Effective | ☐ Partially Effective | ☐ Not Effective

**Summary:**
The access control programme at [Organisation] was found to be [partially effective / not effective] against the ISO 27001:2022 requirements assessed. [X] findings were identified: [X] Critical, [X] High, [X] Medium, [X] Positive observations.

**Critical findings requiring immediate action:**
1. [F-002] — IT administrators using standard accounts for privileged tasks

**Areas of good practice:**
1. [F-POSITIVE-01] — Password policy meets ISO 27001 requirements

---

## Auditor Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Lead Auditor | | | |
| Audit Reviewer | | | |
| Auditee (acknowledgement) | | | |

---

## Management Response

Management responses to all findings must be completed within 10 business days of receiving the draft report.

| Finding ID | Management Agrees? | Management Response | Committed Date | Responsible Owner |
|-----------|-------------------|---------------------|---------------|------------------|
| F-001 | | | | |
| F-002 | | | | |
| F-003 | | | | |

---

*Internal Security Audit Checklist | v1.0 | ISO 27001:2022 Clause 9.2 | ISO 19011:2018*
