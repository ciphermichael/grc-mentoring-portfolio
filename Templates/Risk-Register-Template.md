# Cybersecurity Risk Register Template

| Field | Value |
|-------|-------|
| **Document ID** | RR-001 |
| **Organisation** | [Company Name] |
| **Version** | 1.0 |
| **Owner** | CISO / Head of Risk |
| **Last Reviewed** | DD-MMM-YYYY |
| **Review Frequency** | Monthly |
| **Classification** | Confidential — Internal |
| **Framework Refs** | ISO 27001:2022 Clause 6.1.2 | ISO 27005:2022 | NIST CSF 2.0 ID.RA |

---

## Purpose

This Risk Register documents identified information security risks, their assessment, current controls, and treatment decisions. It is reviewed monthly by the Security Committee and quarterly by the Board Risk Committee. It supports the organisation's ISO 27001 ISMS risk assessment requirements (Clause 6.1.2).

---

## Risk Scoring Methodology

### Likelihood Scale (1–5)

| Score | Rating | Description | Frequency |
|-------|--------|-------------|-----------|
| 1 | Rare | Very unlikely to occur | Less than once in 5 years |
| 2 | Unlikely | Unlikely to occur | Once every 3–5 years |
| 3 | Possible | May occur in normal circumstances | Approximately once per year |
| 4 | Likely | Will probably occur in most circumstances | Multiple times per year |
| 5 | Almost Certain | Expected to occur frequently | Monthly or more frequent |

### Impact Scale (1–5)

| Score | Rating | Financial | Operational | Reputational | Regulatory |
|-------|--------|-----------|-------------|--------------|------------|
| 1 | Negligible | <£1K | No disruption | No coverage | No regulatory breach |
| 2 | Minor | £1K–£10K | Short disruption (<4hr) | Local coverage | Minor regulatory interest |
| 3 | Moderate | £10K–£100K | Significant disruption (<24hr) | National coverage | Formal regulatory enquiry |
| 4 | Major | £100K–£1M | Serious disruption (1–7 days) | Major news coverage | Regulatory enforcement action |
| 5 | Catastrophic | >£1M | Critical disruption (>7 days) | Sustained national/international | Criminal prosecution / licence revocation |

### Risk Rating Matrix

| Score | Rating | Colour | Action Required |
|-------|--------|--------|----------------|
| 1–4 | Low | Green | Monitor; annual review |
| 5–9 | Medium | Yellow | Treat within 90 days; quarterly review |
| 10–16 | High | Orange | Treat within 30 days; monthly review |
| 17–25 | Critical | Red | Treat immediately; weekly escalation |

---

## Risk Register

| Risk ID | Risk Title | Category | Risk Description | Threat Source | Vulnerability Exploited | Asset Affected | Risk Owner | Likelihood (1–5) | Impact (1–5) | Inherent Score | Inherent Rating | Current Controls | Control Effectiveness | Residual Likelihood | Residual Impact | Residual Score | Residual Rating | Treatment Option | Treatment Actions | Treatment Owner | Target Date | Status |
|---------|------------|----------|-----------------|---------------|------------------------|----------------|------------|-----------------|-------------|---------------|----------------|-----------------|----------------------|--------------------|-----------------|--------------|-----------------|-----------------|--------------------|----------------|-------------|--------|
| RR-001 | Ransomware encryption of production file servers | Technology | Financially motivated ransomware actor encrypts production file servers via compromised IT administrator credentials, halting business operations | External attacker — organised crime | No PAM; developer admin access unconstrained; no network segmentation | Production file servers; customer data | CISO | 4 | 5 | 20 | Critical | AWS backups enabled; basic AV deployed | Low | 3 | 5 | 15 | High | Mitigate: Deploy PAM (CyberArk); implement network segmentation; deploy EDR (CrowdStrike); enable S3 Object Lock for immutable backups | Head of IT | Q2 2025 | Open |
| RR-002 | Unauthorised access via compromised third-party vendor | Third-Party | Supply chain attack via trusted IT support vendor; attacker uses vendor's privileged remote access to access production systems | External attacker via supply chain | Vendor remote access not MFA-protected; no time-limited access sessions | Corporate network; customer systems | CISO | 3 | 4 | 12 | High | Basic vendor contracts in place; no VRAQ conducted | None | 3 | 4 | 12 | High | Mitigate: Implement vendor risk assessment programme; require MFA for all vendor access; implement just-in-time (JIT) privileged access | Head of IT | Q1 2025 | Open |
| RR-003 | GDPR enforcement action — data breach notification failure | Compliance | Failure to notify ICO within 72 hours of a personal data breach, resulting in regulatory enforcement action and fine | ICO regulatory action (triggered by breach) | No formal breach detection and notification procedure | Customer personal data; HR employee data | Head of Legal | 3 | 4 | 12 | High | GDPR DPO appointed; no formal breach procedure | Low | 2 | 4 | 8 | Medium | Mitigate: Develop GDPR breach notification procedure; conduct tabletop exercise; update RoPA | DPO | Q1 2025 | Open |
| RR-004 | Insider data exfiltration by privileged user | Technology | Trusted IT administrator exfiltrates customer database records via authorised access to personal cloud storage | Malicious insider | No DLP controls; no user activity monitoring; no detection of large data transfers | Customer database; financial records | CISO | 2 | 5 | 10 | High | Background checks on hire; HR controls only | Low | 2 | 5 | 10 | High | Mitigate: Deploy DLP solution; implement UEBA (User Entity Behaviour Analytics); review and restrict bulk data export rights | CISO | Q2 2025 | Open |
| RR-005 | Third-party cloud provider outage | Third-Party | Primary cloud provider (AWS) experiences regional outage, causing customer-facing services to become unavailable | Cloud provider infrastructure failure | No multi-region DR; single-region deployment | Customer-facing services; payment processing | CTO | 2 | 4 | 8 | Medium | AWS SLA in place; backups to separate S3 bucket | Medium | 2 | 3 | 6 | Medium | Mitigate: Implement cross-region failover; define RTO/RPO for critical services; test recovery annually | CTO | Q3 2025 | Open |
| RR-006 | Phishing attack leading to credential theft | Technology | Phishing email delivers convincing login page; employee submits Office 365 credentials; attacker accesses email and internal systems | External attacker | No email anti-phishing controls; no MFA on all accounts | Employee email accounts; SharePoint; HR system | CISO | 4 | 3 | 12 | High | Basic spam filter; annual security training | Low | 3 | 3 | 9 | Medium | Mitigate: Implement advanced email filtering (Defender for O365 P2); enforce MFA on all accounts; quarterly phishing simulations | CISO | Q1 2025 | Open |
| RR-007 | Unpatched critical vulnerability exploited | Technology | Publicly disclosed critical CVE exploited against unpatched internet-facing server before patch applied | External attacker | No patch management SLA; 45-day average patching cycle for servers | Internet-facing web servers; API gateway | Head of IT | 3 | 4 | 12 | High | Qualys scanner deployed; no SLA for remediation | Medium | 2 | 4 | 8 | Medium | Mitigate: Establish patch management SLA (Critical: 48hr, High: 7 days); automate patching where possible | Head of IT | Q1 2025 | Open |
| RR-008 | DDoS attack on customer-facing services | Technology | Distributed Denial of Service attack overwhelming customer-facing API and web services, causing service unavailability | External attacker / hacktivism | No DDoS mitigation service; no traffic scrubbing | Customer-facing API; web application; payment gateway | CTO | 2 | 3 | 6 | Medium | AWS Shield Basic (free tier) only | Medium | 1 | 3 | 3 | Low | Mitigate: Enable AWS Shield Advanced (£2,500/month); implement CloudFront rate limiting | CTO | Q2 2025 | Open |

---

## Risk Summary Dashboard

| Category | Critical | High | Medium | Low | Total |
|----------|---------|------|--------|-----|-------|
| Technology/Cyber | 1 | 4 | 2 | 1 | 8 |
| Third-Party | 0 | 2 | 1 | 0 | 3 |
| Compliance | 0 | 1 | 1 | 0 | 2 |
| Operational | 0 | 0 | 0 | 0 | 0 |
| Physical | 0 | 0 | 0 | 0 | 0 |
| **Total** | **1** | **7** | **4** | **1** | **13** |

---

## Risk Appetite Statement

The organisation accepts **Low** risks with monitoring. All **Medium**, **High**, and **Critical** risks require documented treatment plans and named owners. Risks rated **Critical** require escalation to the Board Risk Committee within 30 days of identification.

---

## Risk Treatment Options Reference

| Option | Description | When to Use |
|--------|-------------|-------------|
| **Mitigate** | Implement controls to reduce likelihood or impact | When cost of control is less than expected loss |
| **Accept** | Document and accept the risk | When cost of mitigation exceeds benefit or risk is within appetite |
| **Transfer** | Use insurance or outsourcing to shift financial burden | Cyber insurance; outsourcing high-risk activities |
| **Avoid** | Stop the activity that creates the risk | When risk is unacceptably high and no cost-effective mitigation exists |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | YYYY-MM-DD | [Name] | Initial register created |
| 1.1 | YYYY-MM-DD | [Name] | Added Risks RR-006 through RR-008 |

---

*Risk Register | Version 1.0 | ISO 27001:2022 Clause 6.1.2 | ISO 27005:2022 | Review: Monthly*
