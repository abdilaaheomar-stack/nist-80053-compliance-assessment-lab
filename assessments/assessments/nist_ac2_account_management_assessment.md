# NIST 800-53 Security Control Assessment

## Control Family

Access Control (AC)

## Control Identifier

AC-2

## Control Name

Account Management

---

# Assessment Overview

## Assessment Objective

Evaluate the organization's ability to manage user accounts throughout the account lifecycle, including account creation, modification, review, disabling, and removal.

The assessment was conducted to determine compliance with NIST SP 800-53 Rev. 5 control AC-2 and identify opportunities to strengthen identity and access management practices.

---

# Business Justification

User account management is a foundational security control that directly impacts confidentiality, integrity, and availability of organizational information systems.

Improper account lifecycle management can result in:

* Unauthorized access
* Privilege misuse
* Insider threats
* Regulatory violations
* Increased attack surface

Effective account governance reduces organizational risk and supports security program maturity.

---

# Scope

The following systems were included in the assessment:

* Active Directory
* Microsoft 365
* Endpoint Management Platform
* Privileged Access Management Systems
* Internal Business Applications

Assessment Period:

Q2 2026

---

# Assessment Methodology

The assessment was performed using a risk-based auditing approach.

Activities included:

* Policy Review
* Procedure Review
* Evidence Collection
* Technical Validation
* Control Effectiveness Testing
* Stakeholder Interviews

---

# Evidence Reviewed

The following evidence was collected:

## Governance Documentation

* Access Control Policy
* Identity Management Procedures
* User Provisioning Standards
* Offboarding Procedures

## Technical Evidence

* Active Directory User Inventory
* Privileged Account Inventory
* Access Request Records
* Termination Records
* MFA Configuration Reports

---

# Assessment Procedures

## Procedure 1

Review account provisioning process.

Objective:

Verify new accounts require documented approval before access is granted.

Result:

PASS

Observation:

Formal approval workflow exists and is consistently enforced.

---

## Procedure 2

Review terminated employee accounts.

Objective:

Verify terminated users are disabled within organizational requirements.

Sample Size:

25 Accounts

Result:

PARTIAL PASS

Finding:

Two accounts remained active beyond the required deprovisioning window.

Risk:

Medium

---

## Procedure 3

Review privileged account management.

Objective:

Validate administrative accounts are assigned using least privilege principles.

Result:

PASS

Observation:

Administrative accounts are separated from standard user accounts.

Multifactor authentication is enforced.

---

## Procedure 4

Review periodic access reviews.

Objective:

Confirm user access is reviewed on a recurring basis.

Result:

PASS

Observation:

Quarterly access certification reviews are performed by system owners.

---

# Findings

## Finding 01

Title:

Delayed Account Deactivation

Description:

Two terminated employee accounts remained enabled beyond organizational requirements.

Potential Impact:

* Unauthorized access
* Privilege abuse
* Increased insider threat risk

Likelihood:

Medium

Impact:

Medium

Risk Rating:

Medium

---

# Control Effectiveness Evaluation

| Category                      | Rating              |
| ----------------------------- | ------------------- |
| Policy Design                 | Effective           |
| Technical Controls            | Effective           |
| Monitoring                    | Effective           |
| User Lifecycle Management     | Partially Effective |
| Overall Control Effectiveness | Effective           |

---

# Risk Assessment

Residual Risk Level:

Low

The organization demonstrates mature account governance processes with minor opportunities for improvement.

Existing controls significantly reduce the likelihood of unauthorized account usage.

---

# Recommendations

## Recommendation 1

Implement automated account disablement workflows integrated with HR termination systems.

Expected Outcome:

Reduce manual processing errors and improve deprovisioning timeliness.

---

## Recommendation 2

Increase access review frequency for privileged accounts.

Expected Outcome:

Improve visibility into elevated access assignments.

---

## Recommendation 3

Implement automated notifications for dormant accounts.

Expected Outcome:

Reduce account management risk and improve compliance posture.

---

# Management Response

Management agreed with all findings and recommendations.

Corrective actions will be incorporated into the next identity governance improvement cycle.

---

# Auditor Conclusion

Based on evidence reviewed, testing performed, and control validation activities completed, AC-2 Account Management is operating effectively with minor opportunities for improvement.

The organization demonstrates a mature identity governance process and maintains effective controls to manage account lifecycle activities.

Assessment Result:

SATISFACTORY

Control Status:

COMPLIANT WITH OBSERVATIONS

Assessor:

Abdilaahe Omar

Role:

Governance, Risk & Compliance Analyst
