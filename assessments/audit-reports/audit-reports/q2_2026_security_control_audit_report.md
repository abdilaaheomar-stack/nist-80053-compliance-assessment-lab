# Q2 2026 Security Control Audit Report

## Executive Summary

A security control audit was conducted during Q2 2026 to evaluate the effectiveness of selected cybersecurity controls aligned with NIST SP 800-53 Revision 5.

The assessment focused on access management, authentication controls, security monitoring, incident response capabilities, and configuration management practices.

The objective of this audit was to identify compliance gaps, evaluate residual risk, and provide recommendations to improve the organization's overall security posture.

---

# Audit Scope

The following systems and processes were reviewed:

* Active Directory
* Microsoft 365
* Endpoint Security Controls
* Security Information and Event Management (SIEM)
* Incident Response Procedures
* User Account Lifecycle Management

Assessment Period:

April 2026 – June 2026

---

# Controls Reviewed

| Control | Description                          | Status                      |
| ------- | ------------------------------------ | --------------------------- |
| AC-2    | Account Management                   | Compliant with Observations |
| IA-2    | Identification and Authentication    | Compliant                   |
| AU-6    | Audit Review, Analysis and Reporting | Compliant                   |
| IR-4    | Incident Handling                    | Compliant                   |
| CM-6    | Configuration Settings               | Partially Compliant         |

---

# Key Findings

## Finding 1

### Delayed Account Deprovisioning

Description:

Two terminated employee accounts remained active beyond organizational requirements.

Potential Impact:

* Unauthorized system access
* Insider threat exposure
* Compliance violations

Risk Rating:

Medium

Recommendation:

Implement automated account disablement integrated with HR workflows.

---

## Finding 2

### Excessive Local Administrator Privileges

Description:

Several workstations contained local administrative privileges that exceeded business requirements.

Potential Impact:

* Privilege escalation
* Malware execution
* Lateral movement

Risk Rating:

Medium

Recommendation:

Implement least privilege controls and periodic privilege reviews.

---

# Positive Observations

The audit identified several strengths within the cybersecurity program:

* Multifactor authentication enabled for privileged accounts
* Centralized log collection implemented
* SIEM monitoring procedures established
* Formal incident response process documented
* Quarterly access reviews performed

These controls contribute to overall security program maturity and reduce organizational risk exposure.

---

# Risk Summary

| Risk Level    | Number of Findings |
| ------------- | ------------------ |
| High          | 0                  |
| Medium        | 2                  |
| Low           | 3                  |
| Informational | 4                  |

---

# Remediation Roadmap

## Priority 1

Identity Governance Improvements

Actions:

* Automate account disablement
* Improve HR integration
* Increase access certification frequency

Target Completion:

Q3 2026

---

## Priority 2

Privilege Management Enhancements

Actions:

* Review administrative access assignments
* Reduce unnecessary privileged accounts
* Implement periodic privilege audits

Target Completion:

Q3 2026

---

## Priority 3

Continuous Monitoring Improvements

Actions:

* Expand SIEM alert coverage
* Improve correlation rules
* Increase threat hunting activities

Target Completion:

Q4 2026

---

# Overall Audit Opinion

Based on evidence reviewed and testing performed, the organization maintains an effective cybersecurity control environment.

The majority of reviewed controls are operating as intended and provide reasonable assurance that information systems are protected against common threats.

Several moderate-risk observations were identified; however, no critical deficiencies were observed.

Overall Audit Rating:

SATISFACTORY

---

# Auditor

Abdilaahe Omar

Governance, Risk & Compliance Analyst

NIST 800-53 Assessment & Security Control Review
