<div align="center">

# 🏥 Healthcare Cybersecurity GRC Portfolio – BrightCare Health Clinic

### Security Policy & Incident Response Playbook Development

![Domain](https://img.shields.io/badge/Domain-GRC%20%26%20Policy%20Development-blue?style=for-the-badge)
![Framework](https://img.shields.io/badge/Framework-NIST%20CSF%20%7C%20NIST%20SP%20800--63B-green?style=for-the-badge)
![Compliance](https://img.shields.io/badge/Compliance-HIPAA%20Security%20Rule-red?style=for-the-badge)

<img src="https://img.shields.io/badge/Scenario-Fictional%20Healthcare%20Clinic-lightblue?style=flat-square" />
<img src="https://img.shields.io/badge/Documents-2%20GRC%20Artefacts-blue?style=flat-square" />
<img src="https://img.shields.io/badge/NIST%20CSF-6%20Controls%20Mapped-green?style=flat-square" />
<img src="https://img.shields.io/badge/HIPAA-45%20CFR%20164%20Aligned-red?style=flat-square" />
<img src="https://img.shields.io/badge/NIST%20SP%20800--63B-Password%20Guidance-orange?style=flat-square" />
<img src="https://img.shields.io/badge/ISO%2027001-2022%20Aligned-blueviolet?style=flat-square" />

---

**Prepared by:** Bikash Raya
**Project Type:** GRC Portfolio — Security Policy & Incident Response Playbook (Scenario-Based)

> **Note:** BrightCare Health Clinic is a fictional organization created for portfolio and learning purposes. All policies and procedures are original work and do not represent any real organization.

</div>

---

## 📁 Repository Structure

| File | Description |
| --- | --- |
| [BCHC-IR-PB-001_Phishing_Incident_Response_Playbook.pdf](./BCHC-IR-PB-001_Phishing_Incident_Response_Playbook.pdf) | Phishing Incident Response Playbook — aligned to NIST CSF and HIPAA |
| [BCHC-IS-POL-002_Password_Authentication_Policy.docx](./BCHC-IS-POL-002_Password_Authentication_Policy.docx) | Password & Authentication Policy — aligned to NIST SP 800-63B and HIPAA |
| README.md | Project overview |

---

## 📋 Overview

This repository contains two professional GRC (Governance, Risk & Compliance) artefacts developed for a fictional small healthcare clinic — **BrightCare Health Clinic**. The documents are written as if for a real organization, demonstrating practical knowledge of security policy development, incident response planning, regulatory compliance, and industry framework alignment.

Healthcare was chosen as the scenario because:
* 🏥 Healthcare is one of the most heavily regulated sectors for cybersecurity
* 📋 HIPAA compliance is a critical requirement for any healthcare organization
* 💼 GRC skills aligned to healthcare are highly valued in entry-level security analyst and GRC analyst roles
* 🎯 Phishing and credential-based attacks are the leading cause of healthcare data breaches

---

## 🛠️ Frameworks & Standards Applied

| Framework | Application |
| --- | --- |
| **NIST Cybersecurity Framework (CSF)** | Control mapping for both documents (DE, RS, RC, PR functions) |
| **NIST SP 800-63B** | Password length over complexity guidance, no mandatory rotation |
| **HIPAA Security Rule (45 CFR 164)** | Access control, audit controls, incident procedures, breach notification |
| **HIPAA Breach Notification Rule (45 CFR 164.400)** | PHI breach assessment and patient notification requirements |
| **ISO/IEC 27001:2022** | Annex A controls mapped in both documents (A.5.16-A.5.28, A.8.2-A.8.18) |

---

## 📄 Document 1 — Phishing Incident Response Playbook

**File:** `BCHC-IR-PB-001_Phishing_Incident_Response_Playbook.docx`

### What it covers:

A structured, step-by-step playbook for responding to phishing incidents in a healthcare environment where patient Protected Health Information (PHI) is at risk.

| Section | Content |
| --- | --- |
| Scope | Phishing, BEC, credential harvesting, malicious attachments, suspicious logins |
| Trigger Conditions | When and how this playbook is initiated |
| Severity Classification | Low / Medium / High / Critical with HIPAA implications per level |
| Roles & Responsibilities | 6 roles defined (staff, IT, security, management, legal, HR) |
| Investigation Steps | 3-step process: triage, user interaction, log & alert review |
| Containment Actions | 4 severity-based response tracks with specific action items |
| Eradication & Recovery | Mailbox cleanup, endpoint remediation, account restoration |
| Communication Plan | Audience-specific messaging including patient breach notification |
| Evidence Collection | Chain-of-custody requirements for HIPAA proceedings |
| Post-Incident Actions | Timeline documentation, lessons learned, playbook updates |
| Framework Alignment | NIST CSF (DE.CM-4, DE.AE-2, RS.RP-1, RS.MI-1, RS.AN-1, RC.IM-1) |
| HIPAA Alignment | 45 CFR 164.308(a)(1), 164.308(a)(6), 164.312(b), 164.400 |
| **ISO 27001:2022** | A.5.24 (Incident planning) \| A.5.25 (Event assessment) \| A.5.26 (Incident response) \| A.5.27 (Lessons learned) \| A.5.28 (Evidence) \| A.6.8 (Reporting) \| A.8.16 (Monitoring) |

### Severity Classification Summary:

| Severity | Condition | HIPAA Action |
| --- | --- | --- |
| 🟢 Low | Email delivered, no interaction | No breach notification required |
| 🟠 Medium | Link clicked, no credentials | Precautionary response |
| 🔴 High | Credentials submitted or attachment opened | HIPAA Risk Assessment required |
| 🚨 Critical | Confirmed account compromise | Breach Notification Rule may apply — 60-day clock |

---

## 📄 Document 2 — Password & Authentication Policy

**File:** `BCHC-IS-POL-002_Password_Authentication_Policy.docx`

### What it covers:

A comprehensive policy governing password creation, management, MFA requirements, account lockout, and credential compromise response — aligned to NIST SP 800-63B and HIPAA access control requirements.

| Section | Content |
| --- | --- |
| Password Length | 12 chars standard / 14 chars EHR / 16 chars privileged |
| Complexity | NIST 800-63B aligned — length over complexity, no forced rotation |
| Prohibited Practices | No sharing, no reuse, no plain text storage, no hardcoding |
| MFA Requirements | Mandatory for all PHI-accessing systems and remote access |
| Approved MFA Methods | Authenticator app (preferred), FIDO2 hardware key, biometric |
| Account Lockout | 5 failed attempts — 15 min standard / immediate for privileged |
| Privileged Accounts | Separate credentials, FIDO2 MFA, JIT access, quarterly review |
| Password Storage | bcrypt/Argon2/PBKDF2 hashing, TLS 1.2+ in transit |
| Monitoring & Logging | Full authentication event logging — 6-year HIPAA retention |
| Credential Compromise | 6-step response procedure including HIPAA Risk Assessment |
| Framework Alignment | NIST CSF (PR.AC-1, PR.AC-7, PR.IP-1, DE.CM-7) |
| HIPAA Alignment | 45 CFR 164.308(a)(5), 164.312(a), 164.312(b), 164.312(d) |
| **ISO 27001:2022** | A.5.16 (Identity mgmt) \| A.5.17 (Authentication info) \| A.5.18 (Access rights) \| A.8.2 (Privileged access) \| A.8.5 (Secure authentication) \| A.8.15 (Logging) \| A.8.18 (Privileged programs) |

### Key NIST SP 800-63B Alignments:

```
✅ Minimum 12-character password length (not arbitrary complexity)
✅ No mandatory periodic rotation unless compromise suspected
✅ Block commonly used and breached passwords
✅ SMS MFA discouraged — authenticator app or hardware key preferred
✅ Password length over complexity rules
```

---

## 🎯 Framework Controls Covered

| Control ID | Function | Description | Document |
| --- | --- | --- | --- |
| DE.CM-4 | Detect | Malicious code detection | Playbook |
| DE.AE-2 | Detect | Detected events analyzed | Playbook |
| RS.RP-1 | Respond | Response plan execution | Playbook |
| RS.MI-1 | Respond | Incident containment | Playbook |
| RS.AN-1 | Respond | Detection investigation | Playbook |
| RC.IM-1 | Recover | Recovery improvement | Playbook |
| PR.AC-1 | Protect | Identity and credential management | Policy |
| PR.AC-7 | Protect | User authentication | Policy |
| PR.IP-1 | Protect | Security policies established | Policy |
| DE.CM-7 | Detect | Monitoring unauthorized access | Policy |

---

## 🎯 Skills Demonstrated

* Security Policy Development (healthcare context)
* Incident Response Playbook Writing
* NIST Cybersecurity Framework (CSF) Control Mapping
* NIST SP 800-63B Password & Authentication Guidance
* HIPAA Security Rule Compliance (45 CFR 164)
* ISO/IEC 27001:2022 Annex A Control Mapping
* HIPAA Breach Notification Rule Understanding
* Risk-Based Severity Classification
* Governance, Risk & Compliance (GRC) Documentation
* Roles & Responsibilities Definition
* Evidence Collection & Chain of Custody Procedures
* Communication Planning (internal & regulatory)

---

## 🎯 Key Takeaway

> These documents demonstrate practical GRC skills including security policy writing, incident response planning, and multi-framework compliance alignment for a regulated healthcare environment. Both documents follow real-world structure and reference NIST CSF, NIST SP 800-63B, and HIPAA Security Rule controls — the same frameworks referenced in cybersecurity analyst, GRC analyst, and security consultant job descriptions. The healthcare scenario adds HIPAA compliance depth which is highly relevant to entry-level security roles in healthcare, insurance, and regulated industries.

---

## 🔗 Connect With Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/bikash-raya/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=for-the-badge&logo=github)](https://github.com/Bikash-Raya)

</div>

---

<div align="center">

⭐ If you find this project useful, feel free to star the repository ⭐

</div>
