# NIST SP 800-53 IA-2 Control Assessment

## Identification and Authentication — Organizational Users

---

## Document Control

| Field               | Value                                                    |
| ------------------- | -------------------------------------------------------- |
| Assessment ID       | SCA-IA2-2026-001                                         |
| Framework           | NIST SP 800-53 Revision 5                                |
| Assessment Guidance | NIST SP 800-53A Revision 5                               |
| Control Family      | Identification and Authentication                        |
| Control             | IA-2                                                     |
| Control Name        | Identification and Authentication — Organizational Users |
| Assessment Type     | Design and Operating Effectiveness Review                |
| Assessment Period   | Q2 2026                                                  |
| Environment         | Simulated Enterprise Environment                         |
| Assessor            | Abdilaahe Omar                                           |
| Role                | Governance, Risk, and Compliance Analyst                 |
| Document Status     | Final — Portfolio Case Study                             |

---

# 1. Executive Summary

A risk-based security control assessment was performed to evaluate the design and operating effectiveness of identification and authentication controls for organizational users.

The assessment focused on whether users were uniquely identified before receiving system access, whether authentication mechanisms were implemented consistently, whether multifactor authentication was enforced for privileged and non-privileged access, and whether authenticated identities remained attributable throughout system activity.

The simulated environment demonstrated a generally effective identity and authentication control structure. Unique user accounts, centralized authentication, privileged-account separation, multifactor authentication, and authentication-event monitoring were implemented across most in-scope systems.

Two control weaknesses were identified:

1. A legacy administrative interface permitted password-only authentication for a limited support population.
2. Two emergency access accounts were excluded from the standard quarterly authentication-control review.

Neither issue resulted in evidence of unauthorized access. However, both conditions reduced assurance that authentication safeguards were operating consistently across the environment.

### Overall Assessment Result

**Partially Satisfied**

### Overall Risk Rating

**Moderate**

### Assessor’s Opinion

The IA-2 control was appropriately designed and substantially implemented, but targeted remediation is required before the control can be considered fully effective.

---

# 2. Control Requirement

## IA-2 — Identification and Authentication

The assessment evaluates whether:

1. Organizational users are uniquely identified and authenticated.
2. The unique identity of authenticated users remains associated with processes acting on behalf of those users.

This assessment also evaluates the following selected control enhancements:

| Enhancement | Requirement Evaluated                                  |
| ----------- | ------------------------------------------------------ |
| IA-2(1)     | Multifactor authentication for privileged accounts     |
| IA-2(2)     | Multifactor authentication for non-privileged accounts |

---

# 3. Business and Security Context

Identification and authentication controls establish confidence that a person requesting access is the individual they claim to be.

Weak authentication can enable:

* Account takeover
* Unauthorized administrative access
* Credential-based attacks
* Fraudulent transactions
* Privilege escalation
* Data exposure
* Unattributed system activity
* Failure to establish accountability
* Regulatory or contractual noncompliance

Authentication is particularly important in environments using cloud services, remote access, privileged administration, and single sign-on because compromise of one identity may provide access to multiple connected systems.

---

# 4. Assessment Scope

## In-Scope Technologies

The simulated assessment covered:

* Microsoft Active Directory
* Microsoft Entra ID
* Microsoft 365
* Corporate virtual private network
* Privileged Access Management platform
* Windows administrative servers
* Enterprise business applications
* Security Information and Event Management platform
* Identity Governance and Administration workflow
* Service management ticketing platform

## In-Scope Account Types

* Standard workforce accounts
* Privileged administrative accounts
* Contractor accounts
* Remote-access accounts
* Emergency access accounts
* Service and application accounts, where user interaction was permitted

## Out-of-Scope Items

The following were excluded:

* Customer identities
* Public website users
* Non-human service identities that could not be used interactively
* Physical access credentials
* Development systems isolated from the enterprise identity provider

---

# 5. Assessment Objectives

The assessment was designed to determine whether:

1. Every organizational user receives a unique identifier.
2. Shared user accounts are prohibited or formally approved as exceptions.
3. Users are authenticated before system access is granted.
4. Authentication mechanisms are appropriate for the sensitivity of the system.
5. Multifactor authentication is enforced for privileged accounts.
6. Multifactor authentication is enforced for non-privileged remote and cloud access.
7. Authentication events are logged and attributable to unique identities.
8. Privileged activities can be traced to individual administrators.
9. Authentication exceptions are documented, approved, time-bound, and monitored.
10. Identity and authentication controls operate consistently across the assessment period.

---

# 6. Assessment Methodology

The assessment followed the NIST SP 800-53A methodology and applied three assessment methods.

## 6.1 Examine

Documents, records, configurations, and system-generated evidence were reviewed to determine whether the control was properly designed and documented.

## 6.2 Interview

Personnel responsible for identity operations, security administration, system ownership, and control oversight were interviewed to determine whether documented procedures reflected actual operating practices.

## 6.3 Test

Selected authentication mechanisms and user-access scenarios were tested to determine whether technical safeguards operated as expected.

---

# 7. Assessment Depth and Coverage

| Attribute           | Selected Level                                                   |
| ------------------- | ---------------------------------------------------------------- |
| Assessment Depth    | Moderate                                                         |
| Assessment Coverage | Representative                                                   |
| Testing Approach    | Risk-based sampling                                              |
| Evidence Period     | April 1–June 30, 2026                                            |
| Sample Selection    | Privileged, standard, contractor, remote, and emergency accounts |

The assessment prioritized accounts and systems with elevated privilege, remote accessibility, sensitive-data access, or broad enterprise reach.

---

# 8. Evidence Request List

## Governance Evidence

* Identification and Authentication Policy
* Access Control Policy
* Multifactor Authentication Standard
* Privileged Access Management Standard
* Remote Access Standard
* Authentication Exception Procedure
* Identity Governance Procedure
* Emergency Access Account Procedure

## Administrative Evidence

* Current account inventory
* Privileged-account inventory
* Emergency account inventory
* Contractor account inventory
* Authentication exception register
* Quarterly access-review results
* Account-owner attestations
* User provisioning records
* Approved access requests
* Identity-related incident tickets

## Technical Evidence

* Entra ID authentication-method report
* Conditional Access policy exports
* Active Directory authentication settings
* VPN authentication configuration
* PAM configuration screenshots
* MFA enrollment report
* Authentication failure logs
* Successful privileged logon records
* SIEM authentication dashboards
* Sample Windows security events
* Single sign-on configuration
* Break-glass account monitoring alerts

---

# 9. Stakeholders Interviewed

| Role                                       | Purpose                                                     |
| ------------------------------------------ | ----------------------------------------------------------- |
| Identity and Access Management Manager     | Understand identity lifecycle and authentication governance |
| Active Directory Administrator             | Validate directory authentication configuration             |
| Cloud Security Engineer                    | Review cloud authentication and Conditional Access          |
| Privileged Access Management Administrator | Evaluate privileged authentication controls                 |
| Security Operations Analyst                | Review monitoring and investigation procedures              |
| Application Owner                          | Confirm application-level authentication practices          |
| GRC Control Owner                          | Validate control ownership and evidence-retention practices |

---

# 10. Sample Selection

A representative sample of 40 accounts was selected.

| Account Category             | Population | Sample |
| ---------------------------- | ---------: | -----: |
| Standard workforce accounts  |      2,400 |     15 |
| Privileged accounts          |        110 |     10 |
| Contractor accounts          |        280 |      5 |
| Remote-access accounts       |      1,600 |      5 |
| Emergency access accounts    |          4 |      4 |
| Interactive service accounts |          8 |      1 |
| **Total**                    |  **4,402** | **40** |

The sample emphasized higher-risk identities rather than using an equal random distribution.

---

# 11. Control Test Procedures and Results

## Test IA2-01 — Unique User Identification

### Objective

Determine whether organizational users are assigned unique identifiers before access is granted.

### Procedure

1. Obtained the current account inventory.
2. Selected standard, contractor, privileged, and remote-access accounts.
3. Compared account identifiers against HR or contractor records.
4. Reviewed for duplicate, generic, or shared identifiers.
5. Confirmed that each sampled account had an identifiable owner.

### Evidence

* Active Directory account export
* Entra ID user inventory
* HR identity records
* Contractor authorization records

### Result

**Satisfied**

### Observation

All sampled workforce and contractor accounts were assigned unique identifiers and could be traced to an authorized individual.

No active generic user accounts were identified in the sample.

---

## Test IA2-02 — Authentication Before Access

### Objective

Determine whether users are authenticated before receiving access to in-scope systems.

### Procedure

1. Reviewed authentication configuration for selected systems.
2. Attempted access without valid credentials.
3. Confirmed failed access attempts were rejected.
4. Verified successful authentication generated security logs.
5. Confirmed inactive sessions did not bypass reauthentication requirements.

### Evidence

* Authentication configuration exports
* Application access tests
* VPN test results
* Security logs
* SIEM event records

### Result

**Satisfied**

### Observation

Selected systems required successful authentication before access was granted. Invalid credentials were rejected and generated auditable events.

---

## Test IA2-03 — Identity Attribution

### Objective

Determine whether authenticated identities remain associated with processes and activities performed on behalf of users.

### Procedure

1. Selected successful user logons.
2. Traced authentication events to user sessions.
3. Reviewed process-creation and administrative activity records.
4. Confirmed that events included user identifiers, timestamps, systems, and source information.
5. Compared privileged activity with PAM session records.

### Evidence

* Windows Security Event logs
* Entra ID sign-in logs
* PAM session logs
* SIEM correlation records
* Administrative activity reports

### Result

**Satisfied**

### Observation

Authentication and administrative activity could be attributed to unique identities across the selected sample.

Privileged sessions initiated through the PAM platform included individual user attribution and session-recording references.

---

## Test IA2-04 — Multifactor Authentication for Privileged Accounts

### Related Enhancement

IA-2(1)

### Objective

Determine whether multifactor authentication is implemented for privileged-account access.

### Procedure

1. Obtained the privileged-account inventory.
2. Compared accounts against MFA registration records.
3. Reviewed authentication policies for administrative roles.
4. Tested access to selected administrative systems.
5. Reviewed emergency and exception accounts separately.

### Evidence

* Privileged-account inventory
* MFA registration report
* Conditional Access policy
* PAM configuration
* Administrative sign-in logs

### Result

**Partially Satisfied**

### Observation

MFA was enforced for Active Directory administrators, cloud administrators, PAM users, and remote privileged access.

However, a legacy infrastructure-management interface allowed five authorized support administrators to authenticate with username and password only when connecting from the internal management network.

### Risk Statement

An attacker who obtains a support administrator’s password and gains access to the management network may access the legacy interface without satisfying an additional authentication factor.

### Related Finding

F-IA2-001 — Password-Only Authentication on Legacy Administrative Interface

---

## Test IA2-05 — Multifactor Authentication for Non-Privileged Accounts

### Related Enhancement

IA-2(2)

### Objective

Determine whether MFA is implemented for applicable non-privileged account access.

### Procedure

1. Reviewed cloud and remote-access authentication requirements.
2. Selected non-privileged workforce and contractor accounts.
3. Compared accounts with MFA enrollment records.
4. Tested Microsoft 365 and VPN access.
5. Reviewed Conditional Access exclusions.

### Evidence

* MFA enrollment report
* Conditional Access policies
* VPN configuration
* User sign-in records
* Exception register

### Result

**Satisfied**

### Observation

MFA was enforced for Microsoft 365, remote access, and selected sensitive business applications.

All sampled non-privileged accounts were enrolled in an approved MFA method. No unauthorized exclusions were identified.

---

## Test IA2-06 — Emergency Access Account Governance

### Objective

Determine whether emergency access accounts are uniquely controlled, monitored, and periodically reviewed.

### Procedure

1. Obtained the emergency access account inventory.
2. Reviewed account ownership and business justification.
3. Confirmed MFA or compensating-control requirements.
4. Reviewed alerting for account use.
5. Inspected quarterly control-review evidence.

### Evidence

* Emergency account inventory
* Credential-vault records
* SIEM alerts
* Account review documentation
* Exception approvals

### Result

**Partially Satisfied**

### Observation

All four emergency access accounts were maintained in a controlled credential vault, and account use generated high-priority SIEM alerts.

Two accounts, however, were omitted from the Q2 quarterly authentication review because ownership metadata was not synchronized with the identity-governance platform.

### Risk Statement

Failure to include all emergency accounts in periodic reviews may allow outdated ownership, unnecessary access, or control exceptions to remain undetected.

### Related Finding

F-IA2-002 — Incomplete Review of Emergency Access Accounts

---

## Test IA2-07 — Authentication Monitoring

### Objective

Determine whether authentication events are centrally logged, reviewed, and escalated when suspicious patterns occur.

### Procedure

1. Reviewed SIEM data-source coverage.
2. Confirmed collection of successful and failed authentication events.
3. Evaluated detections for password spraying, impossible travel, repeated MFA denial, and privileged-account anomalies.
4. Traced a sample alert through investigation and closure.
5. Reviewed log-retention settings.

### Evidence

* SIEM ingestion dashboard
* Authentication detection rules
* Alert investigation ticket
* Log-retention configuration
* SOC operating procedure

### Result

**Satisfied**

### Observation

Authentication events were centrally collected and monitored. The SOC maintained detections for common identity threats and documented alert investigation outcomes.

---

# 12. Test Summary

| Test ID | Control Area                    | Result              |
| ------- | ------------------------------- | ------------------- |
| IA2-01  | Unique user identification      | Satisfied           |
| IA2-02  | Authentication before access    | Satisfied           |
| IA2-03  | Identity attribution            | Satisfied           |
| IA2-04  | MFA for privileged accounts     | Partially Satisfied |
| IA2-05  | MFA for non-privileged accounts | Satisfied           |
| IA2-06  | Emergency account governance    | Partially Satisfied |
| IA2-07  | Authentication monitoring       | Satisfied           |

---

# 13. Findings

## F-IA2-001 — Password-Only Authentication on Legacy Administrative Interface

### Condition

A legacy infrastructure-management interface permitted five support administrators to authenticate using only a username and password from the internal management network.

### Criteria

Privileged access should use multifactor authentication in accordance with the organization’s authentication standard and selected implementation of IA-2(1).

### Cause

The legacy platform did not support modern federation or native MFA integration. A modernization project had been planned but not completed.

### Effect

Compromise of an administrator’s password, combined with access to the management network, could result in unauthorized privileged access.

### Likelihood

Possible

### Impact

Major

### Inherent Risk

High

### Existing Compensating Controls

* Management-network restriction
* Privileged workstation requirement
* PAM credential checkout
* SIEM monitoring
* Administrator activity logging
* Quarterly password rotation

### Residual Risk

Moderate

### Recommendation

1. Integrate the platform with an MFA-capable access proxy.
2. Restrict access to privileged access workstations.
3. Apply just-in-time authorization.
4. Generate alerts for every successful login.
5. Establish a formal retirement date for the legacy interface.
6. Document temporary risk acceptance until remediation is complete.

### Proposed Owner

Infrastructure Security Manager

### Target Completion

September 30, 2026

---

## F-IA2-002 — Incomplete Review of Emergency Access Accounts

### Condition

Two of four emergency access accounts were not included in the Q2 authentication-control review.

### Criteria

Emergency accounts should have documented ownership, approved purpose, controlled authentication, continuous monitoring, and recurring review.

### Cause

Account ownership metadata did not synchronize correctly between the credential vault and identity-governance platform.

### Effect

Emergency account access requirements, ownership, or safeguards may not be reassessed within the required period.

### Likelihood

Unlikely

### Impact

Major

### Inherent Risk

Moderate

### Existing Compensating Controls

* Credentials stored in a controlled vault
* Alerts generated upon account use
* Restricted account membership
* Manual review by cloud security personnel

### Residual Risk

Low to Moderate

### Recommendation

1. Correct ownership synchronization.
2. Add emergency accounts to a dedicated certification campaign.
3. Require monthly attestation until automation is validated.
4. Reconcile the PAM, directory, and identity-governance inventories.
5. Create an exception alert when an account is missing from a review campaign.

### Proposed Owner

Identity Governance Manager

### Target Completion

August 31, 2026

---

# 14. Risk Summary

| Finding   | Risk                          | Priority | Treatment |
| --------- | ----------------------------- | -------- | --------- |
| F-IA2-001 | Moderate residual risk        | High     | Mitigate  |
| F-IA2-002 | Low-to-moderate residual risk | Medium   | Mitigate  |

No critical-risk findings were identified.

---

# 15. Positive Control Observations

The assessment identified several control strengths:

* Unique identifiers were assigned to sampled users.
* Shared workforce accounts were prohibited.
* Privileged accounts were separated from standard user accounts.
* MFA was broadly deployed for cloud, VPN, and privileged access.
* Authentication events were centrally collected.
* Privileged sessions were attributable to individual administrators.
* Emergency account use generated high-priority alerts.
* Authentication policies and standards had defined owners.
* Security personnel maintained identity-focused monitoring use cases.

These strengths reduce the likelihood of unauthorized access and improve accountability during security investigations.

---

# 16. Corrective Action Plan

| Action ID   | Corrective Action                                         | Owner                           | Priority | Due Date   | Status      |
| ----------- | --------------------------------------------------------- | ------------------------------- | -------- | ---------- | ----------- |
| CAP-IA2-001 | Place legacy interface behind MFA-capable access proxy    | Infrastructure Security Manager | High     | 2026-09-30 | Planned     |
| CAP-IA2-002 | Restrict legacy administration to privileged workstations | Endpoint Security Manager       | High     | 2026-08-31 | Planned     |
| CAP-IA2-003 | Correct emergency-account ownership synchronization       | Identity Governance Manager     | Medium   | 2026-08-31 | In Progress |
| CAP-IA2-004 | Perform monthly emergency-account certification           | IAM Operations Manager          | Medium   | 2026-07-31 | Planned     |
| CAP-IA2-005 | Validate remediation through follow-up testing            | GRC Control Assurance           | Medium   | 2026-10-15 | Not Started |

---

# 17. Management Response

Management agreed with both findings.

The infrastructure team will implement an MFA-capable access path while completing the long-term retirement of the legacy interface.

The identity governance team will correct ownership synchronization and conduct monthly emergency-account reviews until automated certification is demonstrated to operate effectively.

Management acknowledged the remaining residual risk and assigned accountable owners and completion dates.

---

# 18. Assessor Conclusion

Based on the documentation examined, personnel interviewed, configurations reviewed, and authentication mechanisms tested, the organization substantially implemented NIST SP 800-53 IA-2 and selected enhancements IA-2(1) and IA-2(2).

The base requirements for unique identification, authentication, and user attribution were operating effectively within the representative sample.

The control was not rated fully satisfied because:

1. One legacy privileged-access pathway did not enforce MFA.
2. Two emergency access accounts were omitted from the scheduled quarterly review.

## Final Determination

**Control Status:** Partially Satisfied
**Design Effectiveness:** Effective
**Operating Effectiveness:** Partially Effective
**Residual Risk:** Moderate
**Follow-up Required:** Yes

The organization should complete corrective actions and perform targeted retesting before changing the control determination to fully satisfied.

---

# 19. Follow-Up Validation Plan

The assessor will:

1. Confirm deployment of the MFA-capable access path.
2. Test privileged authentication using positive and negative scenarios.
3. Verify that all emergency accounts appear in the certification campaign.
4. Inspect completed account-owner attestations.
5. Review authentication alerts after remediation.
6. Confirm closure evidence against each corrective action.
7. Update the assessment conclusion and risk register.

---

# 20. Cross-Framework Alignment

| Framework                    | Related Area                                                       |
| ---------------------------- | ------------------------------------------------------------------ |
| NIST SP 800-53 Rev. 5        | IA-2, IA-2(1), IA-2(2)                                             |
| NIST Cybersecurity Framework | Identity Management, Authentication, and Access Control            |
| ISO/IEC 27001                | Identity management, authentication information, and access rights |
| CIS Controls                 | Account Management and Access Control Management                   |
| Zero Trust Architecture      | Continuous identity verification and least-privilege access        |

Cross-framework mappings should be validated against the organization’s selected framework versions, scope, implementation statements, and regulatory obligations.

---

# 21. Authoritative References

* NIST SP 800-53 Revision 5 — Security and Privacy Controls for Information Systems and Organizations
* NIST SP 800-53A Revision 5 — Assessing Security and Privacy Controls in Information Systems and Organizations

---

# 22. Portfolio Skills Demonstrated

* NIST control interpretation
* Security control assessment planning
* Evidence request development
* Risk-based sampling
* Design-effectiveness testing
* Operating-effectiveness testing
* Identity and access management governance
* Multifactor authentication assessment
* Privileged-access review
* Control deficiency analysis
* Root-cause documentation
* Risk-rating methodology
* Corrective action planning
* Management response tracking
* Executive-level security reporting
