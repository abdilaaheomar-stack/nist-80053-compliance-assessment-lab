# NIST SP 800-53 CM-6 Control Assessment

## Configuration Settings


---

## Document Control

| Field               | Value                                              |
| ------------------- | -------------------------------------------------- |
| Assessment ID       | SCA-CM6-2026-001                                   |
| Framework           | NIST SP 800-53 Revision 5                          |
| Assessment Guidance | NIST SP 800-53A Revision 5                         |
| Control Family      | Configuration Management                           |
| Control             | CM-6                                               |
| Control Name        | Configuration Settings                             |
| Assessment Type     | Design and Operating Effectiveness Review          |
| Assessment Period   | Q2 2026                                            |
| Environment         | Simulated Hybrid Enterprise Environment            |
| Assessment Scenario | Secure Baseline Governance and Configuration Drift |
| Assessor            | Abdilaahe Omar                                     |
| Role                | Governance, Risk, and Compliance Analyst           |
| Document Status     | Final — Portfolio Case Study                       |
| Data Classification | Public Portfolio Content                           |

---

# 1. Executive Summary

A risk-based security control assessment was performed to evaluate the design and operating effectiveness of the organization’s configuration settings program.

The assessment examined whether secure configuration settings were:

* Established and formally documented
* Based on recognized hardening standards
* Tailored to operational and business requirements
* Implemented consistently across system components
* Managed through authorized change processes
* Continuously monitored for configuration drift
* Supported by automated enforcement and verification
* Protected from unauthorized changes
* Governed through documented exception and risk-acceptance processes
* Periodically reviewed and updated

The simulated organization maintained secure configuration baselines for Windows workstations, Windows servers, Linux servers, network devices, cloud infrastructure, databases, and selected enterprise applications.

Baseline requirements were derived from a combination of:

* Internal security architecture standards
* CIS Benchmarks
* DISA Security Technical Implementation Guides
* Vendor hardening guidance
* Cloud security configuration standards
* Regulatory and contractual requirements

The organization used Microsoft Group Policy, Microsoft Intune, Azure Policy, AWS Config, infrastructure-as-code templates, endpoint management tools, configuration scanning, and SIEM alerting to apply and monitor configuration settings.

The overall configuration management program was appropriately designed and substantially implemented.

Testing identified two control deficiencies:

1. Emergency configuration deviations did not consistently include expiration dates, compensating controls, or evidence of post-change review.
2. Automated configuration verification did not provide complete coverage for Linux servers deployed outside the standard infrastructure-as-code pipeline.

A simulated configuration drift event was also evaluated. During emergency troubleshooting, an administrator disabled a host-based security setting on a production server. The change was detected by automated monitoring, but restoration was delayed because ownership and escalation requirements were unclear.

No confirmed compromise resulted from the tested conditions. However, the weaknesses increased the likelihood that insecure settings could remain in production longer than intended.

## Overall Assessment Result

**Partially Satisfied**

## Overall Risk Rating

**Moderate**

## Assessor’s Opinion

The CM-6 control was effectively designed and substantially implemented.

Secure baselines, centralized management, automated validation, change monitoring, and exception processes were established. Targeted remediation is required to improve deviation governance and complete automated coverage across the Linux server population.

---

# 2. Control Requirement

## CM-6 — Configuration Settings

The assessment evaluates whether the organization:

1. Establishes and documents configuration settings for system components.
2. Uses settings that reflect the most restrictive mode consistent with operational requirements.
3. Implements approved configuration settings.
4. Identifies and documents deviations from established baselines.
5. Obtains approval for configuration deviations.
6. Bases deviations on documented operational requirements.
7. Monitors and controls changes to configuration settings.
8. Manages configuration settings in accordance with organizational policies and procedures.

---

# 3. Selected Control Enhancements

The simulated assessment included the following active CM-6 enhancements:

| Enhancement | Assessment Area                                                               |
| ----------- | ----------------------------------------------------------------------------- |
| CM-6(1)     | Automated management, application, and verification of configuration settings |
| CM-6(2)     | Defined response to unauthorized changes                                      |

The assessment did not treat withdrawn enhancements as active control requirements.

---

# 4. Business and Security Context

Secure configuration settings reduce the attack surface of systems by removing unsafe defaults and enforcing approved security behavior.

Configuration weaknesses frequently arise from:

* Default passwords
* Excessive privileges
* Unnecessary services
* Weak authentication settings
* Insecure protocols
* Overly permissive firewall rules
* Unrestricted remote access
* Disabled logging
* Unsupported cryptographic settings
* Uncontrolled cloud permissions
* Improper storage exposure
* Unapproved administrator changes
* Configuration drift after maintenance
* Temporary exceptions that become permanent

A technically strong baseline is not enough by itself.

A mature configuration settings program must also establish:

* Ownership
* Approval requirements
* Technical enforcement
* Monitoring
* Exception governance
* Evidence retention
* Remediation targets
* Risk escalation
* Periodic review
* Accountability for unauthorized changes

Poor configuration governance can allow a seemingly minor operational change to create a material security weakness.

---

# 5. Assessment Scope

## In-Scope Technologies

The simulated assessment covered:

* Windows 11 workstations
* Windows Server 2022
* Red Hat Enterprise Linux servers
* Ubuntu Linux servers
* Microsoft Active Directory
* Microsoft Entra ID
* Microsoft Intune
* Microsoft Azure
* Amazon Web Services
* Network firewalls
* Routers and switches
* Microsoft SQL Server
* PostgreSQL databases
* Kubernetes clusters
* Enterprise backup systems
* Endpoint security platforms
* Infrastructure-as-code repositories
* Configuration compliance scanners
* Security Information and Event Management platform

## In-Scope Configuration Categories

* Authentication settings
* Account lockout settings
* Password controls
* Local administrator membership
* Audit logging
* PowerShell logging
* Firewall configuration
* Endpoint protection
* Encryption
* Remote access
* Network protocols
* File and directory permissions
* Cloud storage permissions
* Cloud identity policies
* Database security settings
* Container security settings
* Service configuration
* Administrator interfaces
* Cryptographic protocols
* Security agent configuration

## Out-of-Scope Areas

The following were excluded:

* Personal devices
* Customer-managed infrastructure
* Development prototypes containing no production data
* Systems scheduled for retirement within 30 days
* Physical facility control systems
* Laboratory devices disconnected from enterprise networks

---

# 6. Assessment Objectives

The assessment was designed to determine whether:

1. Secure configuration standards were formally approved.
2. Configuration standards were based on authoritative guidance.
3. Baselines were tailored to system purpose and operational requirements.
4. Baselines were implemented consistently.
5. Automated mechanisms applied and verified settings.
6. Deviations had documented business justification.
7. Deviations were risk assessed and approved.
8. Exceptions included expiration dates and compensating controls.
9. Unauthorized changes were detected.
10. Unauthorized settings were restored or otherwise contained.
11. Configuration changes were attributable to authorized identities.
12. Baselines were reviewed after significant changes.
13. Configuration drift was measured and reported.
14. High-risk noncompliance was escalated.
15. Remediation was tracked through verified closure.

---

# 7. Assessment Methodology

The assessment used three principal methods.

## 7.1 Examine

The assessor reviewed:

* Policies
* Standards
* Baselines
* Benchmark mappings
* Configuration scan reports
* Cloud policy assignments
* Change tickets
* Exception records
* Risk acceptances
* Alert records
* Remediation evidence
* Infrastructure-as-code templates

## 7.2 Interview

Personnel responsible for security architecture, system administration, configuration management, cloud governance, security monitoring, and compliance oversight were interviewed.

## 7.3 Test

The assessor tested selected configuration settings, baseline enforcement mechanisms, exception records, drift-detection capabilities, and unauthorized-change response procedures.

---

# 8. Assessment Depth and Coverage

| Attribute                     | Selected Level        |
| ----------------------------- | --------------------- |
| Assessment Depth              | Moderate              |
| Assessment Coverage           | Representative        |
| Testing Strategy              | Risk-based sampling   |
| Evidence Period               | April 1–June 30, 2026 |
| System Components Sampled     | 60                    |
| Configuration Settings Tested | 180                   |
| Change Records Sampled        | 25                    |
| Exception Records Sampled     | 15                    |
| Drift Alerts Sampled          | 20                    |

The sample emphasized systems with:

* Privileged access
* Internet exposure
* Sensitive data
* Regulatory obligations
* Critical business functions
* Previous configuration findings
* High vulnerability exposure
* Significant cloud permissions

---

# 9. Organization-Defined Secure Configurations

The simulated organization established the following baseline hierarchy:

| Technology           | Baseline Source                                             |
| -------------------- | ----------------------------------------------------------- |
| Windows Workstations | Internal Windows Standard aligned with CIS guidance         |
| Windows Servers      | Internal Server Standard aligned with CIS and STIG guidance |
| Linux Servers        | Internal Linux Hardening Standard                           |
| Microsoft 365        | Cloud Identity and Collaboration Security Standard          |
| Microsoft Azure      | Azure Security Configuration Standard                       |
| Amazon Web Services  | AWS Account and Workload Security Standard                  |
| Network Devices      | Network Infrastructure Hardening Standard                   |
| Databases            | Database Security Configuration Standard                    |
| Kubernetes           | Container and Orchestration Security Standard               |

When multiple sources applied, the organization selected the most restrictive setting that remained consistent with operational requirements.

---

# 10. Representative Baseline Settings

## Windows Workstations

* Microsoft Defender enabled
* Host firewall enabled
* PowerShell Script Block Logging enabled
* SMBv1 disabled
* Guest account disabled
* Local administrator access restricted
* BitLocker encryption enabled
* Automatic screen lock enforced
* Unapproved remote desktop access disabled
* Audit policy centrally enforced

## Windows Servers

* Unnecessary services disabled
* Administrative access restricted
* Secure protocols required
* PowerShell activity logged
* Endpoint security agent protected
* Local account usage restricted
* Security logs forwarded centrally
* Insecure cipher suites disabled
* Remote administration limited to approved networks
* Critical configuration changes monitored

## Linux Servers

* Root remote login disabled
* SSH password authentication restricted
* Privileged commands logged
* File permissions hardened
* Unnecessary packages removed
* Firewall rules enforced
* Audit daemon enabled
* Time synchronization configured
* Security logs forwarded
* Integrity monitoring enabled

## Cloud Infrastructure

* Public storage prohibited by default
* Administrative accounts protected by MFA
* Audit logging enabled
* Encryption enabled
* Security groups restricted
* Root account usage monitored
* Default networks restricted
* Privileged changes logged
* Approved regions enforced
* Infrastructure-as-code required for standard deployments

---

# 11. Organization-Defined Parameters

## Configuration Review Frequency

| Configuration Category                    | Review Frequency |
| ----------------------------------------- | ---------------- |
| Critical security settings                | Continuous       |
| Internet-facing systems                   | Daily            |
| Privileged access settings                | Daily            |
| Cloud policy compliance                   | Continuous       |
| Standard server compliance                | Weekly           |
| Workstation compliance                    | Weekly           |
| Network device compliance                 | Monthly          |
| Baseline standards                        | Annually         |
| Baselines affected by significant threats | Within 30 days   |
| Approved exceptions                       | Monthly          |

## Configuration Compliance Targets

| Asset Category              | Minimum Compliance Target |
| --------------------------- | ------------------------: |
| Critical production systems |                       98% |
| Internet-facing systems     |                       98% |
| Standard production servers |                       95% |
| Corporate workstations      |                       95% |
| Development systems         |                       90% |

## Remediation Targets

| Severity | Required Remediation |
| -------- | -------------------- |
| Critical | 24 hours             |
| High     | 7 calendar days      |
| Medium   | 30 calendar days     |
| Low      | 90 calendar days     |

## Response to Unauthorized Changes

Authorized response actions included:

* Generate an alert
* Create a security incident or change ticket
* Identify the responsible identity
* Restore the approved setting
* Isolate the affected system when necessary
* Restrict administrative access
* Preserve audit evidence
* Investigate possible compromise
* Notify the system owner
* Escalate repeated or high-risk violations
* Initiate disciplinary review when appropriate

---

# 12. Evidence Request List

## Governance Evidence

* Configuration Management Policy
* Secure Configuration Standard
* Baseline Development Procedure
* Change Management Policy
* Configuration Exception Procedure
* Risk Acceptance Standard
* Cloud Governance Standard
* Endpoint Hardening Standard
* Network Hardening Standard
* Configuration Monitoring Procedure

## Technical Evidence

* Group Policy exports
* Microsoft Intune compliance policies
* Azure Policy assignments
* AWS Config rules
* Infrastructure-as-code templates
* Ansible configuration files
* Configuration scanner reports
* Endpoint management reports
* Cloud security posture reports
* Firewall configuration exports
* Linux hardening results
* Database configuration reports
* SIEM drift alerts
* File integrity monitoring alerts

## Administrative Evidence

* Approved baselines
* Change tickets
* Exception requests
* Risk approvals
* Compensating control documentation
* System owner approvals
* Remediation tickets
* Quarterly compliance dashboards
* Governance meeting minutes
* Follow-up test results

---

# 13. Stakeholders Interviewed

| Role                             | Assessment Purpose                              |
| -------------------------------- | ----------------------------------------------- |
| Configuration Management Manager | Validate program governance                     |
| Security Architecture Lead       | Review baseline development                     |
| Windows Engineering Manager      | Evaluate endpoint and server settings           |
| Linux Engineering Manager        | Evaluate Linux enforcement                      |
| Cloud Security Architect         | Review cloud policies and automation            |
| Network Security Engineer        | Evaluate infrastructure hardening               |
| DevSecOps Lead                   | Review infrastructure-as-code controls          |
| SOC Manager                      | Review drift monitoring and escalation          |
| Vulnerability Management Lead    | Evaluate configuration scan integration         |
| GRC Control Owner                | Validate evidence and oversight                 |
| Change Management Manager        | Review authorization workflows                  |
| System Owners                    | Confirm operational requirements and exceptions |

---

# 14. Sample Selection

## System Sample

| Technology Category               |       Population |      Sample |
| --------------------------------- | ---------------: | ----------: |
| Windows workstations              |            2,800 |          15 |
| Windows servers                   |              420 |          10 |
| Linux servers                     |              310 |          10 |
| AWS accounts and workloads        |      18 accounts | 8 resources |
| Azure subscriptions and resources | 12 subscriptions | 7 resources |
| Network devices                   |              165 |           5 |
| Databases                         |               48 |           5 |
| **Total sampled components**      |                  |      **60** |

## Configuration Test Sample

| Configuration Domain              | Settings Tested |
| --------------------------------- | --------------: |
| Authentication and access         |              30 |
| Audit logging                     |              25 |
| Endpoint protection               |              25 |
| Network security                  |              25 |
| Encryption                        |              20 |
| Remote administration             |              20 |
| Cloud security                    |              20 |
| Service and protocol restrictions |              15 |
| **Total**                         |         **180** |

---

# 15. Simulated Configuration Drift Scenario

## Scenario Name

Operation Open Door

## Scenario Description

A production application server experienced performance problems during a high-volume business period.

To troubleshoot the issue, a system administrator temporarily:

* Added an antivirus exclusion for an application directory
* Disabled a host-based firewall rule
* Enabled remote administration from a broad internal network range

The administrator created an emergency change ticket but did not:

* Record an expiration date
* Document compensating controls
* Identify who was responsible for restoring the baseline
* Schedule a post-change security review

The automated configuration platform detected the deviation 11 minutes after implementation.

A SIEM alert was generated, but restoration was delayed for 19 hours because the operations team believed the emergency change remained authorized while the security team believed the setting should have been automatically restored.

## Simulated Risk

The combined configuration changes increased the possibility of:

* Unmonitored remote access
* Malware execution within an excluded directory
* Lateral movement
* Unauthorized administrative activity
* Reduced endpoint protection
* Delayed detection of compromise

## Outcome

No compromise was identified.

The settings were restored after security review, and the server was scanned for malicious activity.

The event revealed weaknesses in exception expiration, ownership, and automated restoration requirements.

---

# 16. Control Test Procedures and Results

## Test CM6-01 — Baseline Establishment and Documentation

### Objective

Determine whether secure configuration settings were formally established and documented.

### Procedure

1. Obtained approved configuration baselines.
2. Confirmed ownership and approval.
3. Reviewed benchmark source references.
4. Evaluated tailoring decisions.
5. Verified version history.
6. Confirmed applicability by technology.

### Evidence

* Approved Baseline Standards
* Security Architecture Approval
* Benchmark Mapping
* Version History
* System Applicability Matrix

### Result

**Satisfied**

### Observation

The organization maintained formally approved baselines for major technology categories.

Standards included setting requirements, rationale, applicability, implementation guidance, and exceptions.

---

## Test CM6-02 — Restrictive Settings Consistent with Operations

### Objective

Determine whether selected settings reflected the most restrictive mode consistent with business and operational requirements.

### Procedure

1. Selected 40 high-impact settings.
2. Compared settings with authoritative hardening guidance.
3. Reviewed operational tailoring.
4. Interviewed system owners.
5. Confirmed documented rationale for less restrictive settings.

### Evidence

* Baseline Comparison
* Architecture Decision Records
* Operational Requirement Documents
* Risk Assessments
* System Owner Approvals

### Result

**Satisfied**

### Observation

Selected settings generally followed restrictive security configurations.

Settings that differed from external benchmarks had documented technical or operational justification.

---

## Test CM6-03 — Configuration Implementation

### Objective

Determine whether approved configuration settings were implemented across in-scope systems.

### Procedure

1. Selected 60 system components.
2. Tested 180 configuration settings.
3. Compared actual values with approved baselines.
4. Reviewed deployment records.
5. Evaluated noncompliant systems.

### Evidence

* Configuration Scanner Results
* Group Policy Reports
* Intune Reports
* Linux Configuration Results
* Cloud Compliance Reports
* Network Configuration Exports

### Result

**Satisfied with Observations**

### Observation

A total of 170 of 180 tested settings matched the approved baseline.

Ten deviations were identified:

* Six had approved exceptions.
* Two were corrected during the assessment.
* Two required further investigation.

The overall sampled compliance rate was 94.4%.

No critical configuration failures were identified.

---

## Test CM6-04 — Deviation Documentation and Approval

### Objective

Determine whether deviations were documented, justified, risk assessed, approved, and periodically reviewed.

### Procedure

1. Selected 15 configuration exceptions.
2. Reviewed business justification.
3. Confirmed risk rating.
4. Reviewed approval authority.
5. Checked expiration dates.
6. Verified compensating controls.
7. Reviewed periodic recertification.

### Evidence

* Exception Register
* Risk Assessments
* Approval Records
* Compensating Control Evidence
* Review Records
* Change Tickets

### Result

**Partially Satisfied**

### Observation

Eleven of 15 exceptions included complete justification, approval, expiration, and compensating controls.

Four emergency deviations did not include all required governance information:

* Three lacked expiration dates.
* Two lacked documented compensating controls.
* One did not identify a remediation owner.
* Two had not received post-change security review.

### Related Finding

F-CM6-001 — Incomplete Governance of Emergency Configuration Deviations

---

## Test CM6-05 — Monitoring and Control of Configuration Changes

### Objective

Determine whether configuration changes were monitored and controlled.

### Procedure

1. Selected 25 change records.
2. Compared approved changes with observed configuration events.
3. Verified attribution to individual administrators.
4. Reviewed preimplementation testing.
5. Confirmed postimplementation validation.
6. Reviewed unauthorized-change investigations.

### Evidence

* Change Tickets
* Configuration Event Logs
* Administrator Activity Logs
* Test Results
* Validation Records
* Investigation Tickets

### Result

**Satisfied**

### Observation

Approved changes were generally traceable to authorized requests and named administrators.

High-risk changes generated centralized audit records and were included in postimplementation validation.

---

## Test CM6-06 — Automated Management, Application, and Verification

### Related Enhancement

CM-6(1)

### Objective

Determine whether automated mechanisms managed, applied, and verified configuration settings.

### Procedure

1. Reviewed configuration-management tools.
2. Evaluated automated baseline deployment.
3. Tested configuration scans.
4. Reviewed compliance dashboards.
5. Confirmed ticket generation.
6. Compared automation coverage with the asset inventory.

### Evidence

* Group Policy Configuration
* Intune Policy Assignments
* Azure Policy Dashboard
* AWS Config Dashboard
* Infrastructure-as-Code Repositories
* Configuration Scanner Reports
* Asset Inventory

### Result

**Partially Satisfied**

### Observation

Automated enforcement and verification covered:

* 98% of corporate Windows workstations
* 97% of Windows servers
* 99% of managed cloud resources
* 82% of Linux servers

Fifty-six Linux servers deployed outside the standard infrastructure-as-code pipeline were not included in continuous configuration verification.

These systems received quarterly manual reviews, but the reduced frequency created a higher risk of undetected drift.

### Related Finding

F-CM6-002 — Incomplete Automated Verification Coverage for Linux Servers

---

## Test CM6-07 — Response to Unauthorized Changes

### Related Enhancement

CM-6(2)

### Objective

Determine whether unauthorized configuration changes triggered defined response actions.

### Procedure

1. Reviewed 20 configuration drift alerts.
2. Evaluated alert severity.
3. Confirmed ticket creation.
4. Reviewed attribution and investigation.
5. Verified restoration of approved settings.
6. Reviewed escalation of repeated violations.
7. Tested a simulated unauthorized change.

### Evidence

* Drift Alerts
* SIEM Records
* Remediation Tickets
* Administrator Logs
* Configuration Restoration Records
* Incident Investigation Notes

### Result

**Satisfied with Observations**

### Observation

Nineteen of 20 sampled alerts were investigated and resolved within the required target.

The Operation Open Door scenario was detected rapidly, but restoration was delayed because the emergency change did not identify a clear expiration time or responsible restoration owner.

The monitoring control operated as intended. The weakness related primarily to exception governance rather than detection capability.

---

## Test CM6-08 — Configuration Drift Reporting

### Objective

Determine whether configuration drift was measured, reported, and escalated.

### Procedure

1. Reviewed compliance dashboards.
2. Compared compliance rates with established targets.
3. Reviewed monthly management reports.
4. Evaluated overdue remediation.
5. Confirmed escalation of high-risk noncompliance.

### Evidence

* Compliance Dashboard
* Monthly Security Report
* Overdue Remediation Report
* Risk Committee Minutes
* System Owner Notifications

### Result

**Satisfied**

### Observation

Configuration compliance was reported by technology, business unit, severity, and age.

Critical and high-risk deviations were escalated to system owners and security leadership.

---

## Test CM6-09 — Baseline Review and Maintenance

### Objective

Determine whether configuration baselines were periodically reviewed and updated.

### Procedure

1. Reviewed baseline revision dates.
2. Examined changes resulting from threats and vulnerabilities.
3. Reviewed vendor security updates.
4. Confirmed approval of revised standards.
5. Evaluated communication to implementation teams.

### Evidence

* Baseline Review Calendar
* Change History
* Threat Advisory Records
* Architecture Approval
* Implementation Communications

### Result

**Satisfied**

### Observation

Baselines were reviewed annually and after significant vulnerabilities, vendor changes, or security events.

Updated requirements were communicated through engineering standards and change-management processes.

---

# 17. Test Summary

| Test ID | Control Area                                    | Result                      |
| ------- | ----------------------------------------------- | --------------------------- |
| CM6-01  | Baseline establishment and documentation        | Satisfied                   |
| CM6-02  | Restrictive settings consistent with operations | Satisfied                   |
| CM6-03  | Configuration implementation                    | Satisfied with Observations |
| CM6-04  | Deviation documentation and approval            | Partially Satisfied         |
| CM6-05  | Monitoring and control of changes               | Satisfied                   |
| CM6-06  | Automated management and verification           | Partially Satisfied         |
| CM6-07  | Response to unauthorized changes                | Satisfied with Observations |
| CM6-08  | Drift reporting and escalation                  | Satisfied                   |
| CM6-09  | Baseline review and maintenance                 | Satisfied                   |

---

# 18. Findings

## F-CM6-001 — Incomplete Governance of Emergency Configuration Deviations

### Condition

Four emergency configuration deviations did not include all required exception information.

Identified deficiencies included:

* Missing expiration dates
* Missing compensating controls
* Unassigned remediation ownership
* Missing post-change security review
* Unclear restoration criteria

### Criteria

Configuration deviations should be:

* Documented
* Justified by operational requirements
* Risk assessed
* Approved by authorized personnel
* Time limited
* Supported by compensating controls
* Assigned to an accountable owner
* Periodically reviewed
* Closed after baseline restoration

### Cause

The emergency change workflow allowed implementation before completion of all configuration exception fields.

The change-management and security exception processes were not fully integrated.

### Effect

Temporary insecure settings may remain active longer than intended and may not receive appropriate risk treatment or monitoring.

### Likelihood

Possible

### Impact

Major

### Inherent Risk

High

### Existing Compensating Controls

* Automated drift detection
* SIEM alerting
* Administrator activity logging
* Endpoint monitoring
* Weekly configuration reporting
* Security operations escalation

### Residual Risk

Moderate

### Recommendation

1. Integrate emergency changes with the configuration exception workflow.
2. Require an expiration date before approval.
3. Require compensating controls for high-risk deviations.
4. Assign a named restoration owner.
5. Generate automated expiration reminders.
6. Automatically escalate expired deviations.
7. Require post-change security validation.
8. Link unresolved deviations to the risk register.
9. Prevent ticket closure until restoration evidence is attached.

### Proposed Owner

Configuration Management Manager

### Target Completion

September 30, 2026

---

## F-CM6-002 — Incomplete Automated Verification Coverage for Linux Servers

### Condition

Fifty-six Linux servers deployed outside the standard infrastructure-as-code pipeline were not included in continuous automated configuration verification.

These systems were reviewed manually each quarter.

### Criteria

The organization’s selected CM-6 implementation requires automated management and verification for production servers.

### Cause

The servers were acquired through a legacy business-unit migration and had not been onboarded to the centralized automation platform.

### Effect

Unauthorized or insecure configuration changes may remain undetected between manual reviews.

### Likelihood

Possible

### Impact

Major

### Inherent Risk

High

### Existing Compensating Controls

* Quarterly manual assessments
* Endpoint security agents
* Centralized audit logging
* Vulnerability scanning
* Network segmentation
* Restricted administrative access

### Residual Risk

Moderate

### Recommendation

1. Add the servers to the centralized asset inventory.
2. Onboard them to automated configuration management.
3. Apply the approved Linux baseline.
4. Implement continuous configuration verification.
5. Generate SIEM alerts for high-risk drift.
6. Track onboarding through a formal remediation plan.
7. Increase manual reviews to monthly until automation is implemented.
8. Retire or rebuild systems that cannot support required controls.

### Proposed Owner

Linux Engineering Manager

### Target Completion

October 31, 2026

---

# 19. Root Cause Analysis

## Finding F-CM6-001

### Problem

Emergency deviations remained open without complete risk governance.

### Root Cause

Emergency change and security exception processes used separate workflows with different mandatory fields.

### Contributing Factors

* Operational urgency
* No automated expiration
* Unclear restoration ownership
* Missing workflow integration
* Limited post-change review
* Ambiguous closure criteria

## Finding F-CM6-002

### Problem

A portion of the Linux population lacked continuous verification.

### Root Cause

Legacy servers were migrated without being incorporated into the standard infrastructure automation process.

### Contributing Factors

* Incomplete asset onboarding
* Decentralized system ownership
* Unsupported legacy configurations
* Competing engineering priorities
* Manual baseline management
* Incomplete migration acceptance criteria

---

# 20. Risk Summary

| Finding   | Inherent Risk | Residual Risk | Priority | Treatment |
| --------- | ------------- | ------------- | -------- | --------- |
| F-CM6-001 | High          | Moderate      | High     | Mitigate  |
| F-CM6-002 | High          | Moderate      | High     | Mitigate  |

No critical-risk findings were identified.

---

# 21. Positive Control Observations

The assessment identified the following strengths:

* Secure configuration baselines were formally approved.
* Baselines were mapped to recognized hardening guidance.
* Technology-specific standards were maintained.
* Most systems received automated configuration enforcement.
* Cloud policy compliance was continuously monitored.
* High-risk drift generated SIEM alerts.
* Configuration changes were attributable to named administrators.
* Baselines were updated after significant vulnerabilities.
* Compliance dashboards supported management oversight.
* Critical deviations received elevated remediation priority.
* Infrastructure-as-code reduced manual configuration errors.
* Configuration evidence supported audit and investigation activities.
* System owners participated in exception approval.
* Security and operational requirements were balanced through documented tailoring.

---

# 22. Corrective Action Plan

| Action ID   | Corrective Action                                  | Owner                            | Priority | Due Date   | Status      |
| ----------- | -------------------------------------------------- | -------------------------------- | -------- | ---------- | ----------- |
| CAP-CM6-001 | Integrate emergency change and exception workflows | Change Management Manager        | High     | 2026-08-31 | In Progress |
| CAP-CM6-002 | Require exception expiration and restoration owner | Configuration Management Manager | High     | 2026-08-15 | Planned     |
| CAP-CM6-003 | Implement automated expired-exception escalation   | Service Management Owner         | High     | 2026-09-30 | Planned     |
| CAP-CM6-004 | Onboard legacy Linux servers to automation         | Linux Engineering Manager        | High     | 2026-10-31 | In Progress |
| CAP-CM6-005 | Increase interim Linux reviews to monthly          | Security Engineering Manager     | Medium   | 2026-07-31 | Planned     |
| CAP-CM6-006 | Validate remediation and retest CM-6               | GRC Control Assurance            | Medium   | 2026-11-15 | Not Started |

---

# 23. Management Response

Management agreed with both findings.

The Change Management and Information Security functions will implement a unified workflow for emergency configuration deviations.

The updated process will require:

* Documented business justification
* Risk rating
* Compensating controls
* Expiration date
* Restoration owner
* Required approvals
* Post-change validation
* Closure evidence

The Linux Engineering function will onboard the identified systems to the centralized automation platform.

Until onboarding is complete, the servers will receive monthly manual configuration reviews and enhanced monitoring.

Management acknowledged the temporary residual risk and assigned accountable owners and completion dates.

---

# 24. Assessor Conclusion

Based on the policies examined, personnel interviewed, configuration records reviewed, systems sampled, settings tested, and drift-response procedures evaluated, the organization substantially implemented NIST SP 800-53 CM-6 and selected enhancements CM-6(1) and CM-6(2).

The following capabilities operated effectively:

* Secure baseline development
* Technical baseline implementation
* Configuration monitoring
* Automated enforcement
* Drift detection
* Management reporting
* Change attribution
* Risk-based remediation
* Baseline maintenance

The control was not rated fully satisfied because:

1. Emergency configuration deviations did not consistently include complete risk-governance information.
2. Continuous automated verification did not cover the complete production Linux server population.

## Final Determination

**Control Status:** Partially Satisfied
**Design Effectiveness:** Effective
**Operating Effectiveness:** Partially Effective
**Residual Risk:** Moderate
**Follow-Up Required:** Yes

The organization should complete corrective actions and perform targeted retesting before changing the control determination to fully satisfied.

---

# 25. Follow-Up Validation Plan

The assessor will:

1. Review the integrated emergency change workflow.
2. Confirm that expiration dates are mandatory.
3. Verify assignment of restoration owners.
4. Inspect compensating control documentation.
5. Test automated expiration notifications.
6. Confirm onboarding of Linux servers.
7. Review continuous verification results.
8. Select new configuration drift alerts for testing.
9. Confirm closure evidence for corrective actions.
10. Update the control assessment and enterprise risk register.

---

# 26. Configuration Metrics and Key Risk Indicators

| Metric or KRI                                                       | Purpose                              |
| ------------------------------------------------------------------- | ------------------------------------ |
| Percentage of systems compliant with approved baselines             | Measures configuration effectiveness |
| Percentage of critical systems under automated enforcement          | Measures control coverage            |
| Number of critical configuration deviations                         | Measures immediate exposure          |
| Number of expired exceptions                                        | Measures exception governance        |
| Average age of configuration deviations                             | Measures remediation performance     |
| Percentage of exceptions with compensating controls                 | Measures risk treatment quality      |
| Percentage of unauthorized changes restored within target           | Measures response effectiveness      |
| Number of unmanaged assets                                          | Measures visibility gaps             |
| Percentage of baselines reviewed on schedule                        | Measures governance maturity         |
| Number of repeated drift events by system owner                     | Identifies systemic control failures |
| Percentage of systems deployed through approved infrastructure code | Measures deployment consistency      |
| Number of overdue configuration corrective actions                  | Measures residual risk               |

---

# 27. Internal Maturity Evaluation

| Capability                     |  Rating |
| ------------------------------ | ------: |
| Baseline Governance            | 4.1 / 5 |
| Configuration Implementation   | 4.0 / 5 |
| Automated Enforcement          | 3.8 / 5 |
| Drift Detection                | 4.2 / 5 |
| Exception Management           | 3.0 / 5 |
| Unauthorized Change Response   | 3.8 / 5 |
| Reporting and Oversight        | 4.0 / 5 |
| Linux Configuration Coverage   | 3.1 / 5 |
| Cloud Configuration Governance | 4.2 / 5 |
| Overall Maturity               | 3.8 / 5 |

### Maturity Interpretation

The organization maintains a defined and operational configuration settings program supported by automation, centralized monitoring, and formal security standards.

Continued maturity depends on strengthening exception governance, completing automation coverage, reducing manual processes, and integrating configuration evidence into continuous control monitoring.

---

# 28. Cross-Framework Alignment

| Framework                    | Related Area                                                           |
| ---------------------------- | ---------------------------------------------------------------------- |
| NIST SP 800-53 Rev. 5        | CM-6, CM-6(1), and CM-6(2)                                             |
| NIST Cybersecurity Framework | Platform security, configuration management, and continuous monitoring |
| ISO/IEC 27001                | Secure configuration and change management                             |
| CIS Controls                 | Secure Configuration of Enterprise Assets and Software                 |
| DISA STIGs                   | Product-specific system hardening                                      |
| Cloud Security Alliance      | Cloud configuration and control governance                             |
| Infrastructure as Code       | Repeatable and controlled technical implementation                     |
| Zero Trust Architecture      | Continuous verification and secure system posture                      |

Cross-framework mappings should be validated against the organization’s selected framework versions, scope, implementation statements, architecture, and regulatory obligations.

---

# 29. Authoritative References

* NIST SP 800-53 Revision 5 — Security and Privacy Controls for Information Systems and Organizations
* NIST SP 800-53A Revision 5 — Assessing Security and Privacy Controls in Information Systems and Organizations
* NIST SP 800-128 — Guide for Security-Focused Configuration Management of Information Systems
* NIST SP 800-70 — National Checklist Program for IT Products
* Security Content Automation Protocol guidance
* Organization Configuration Management Policy
* Organization Secure Configuration Standard
* Organization Change Management Policy

---

# 30. Portfolio Skills Demonstrated

* NIST configuration control interpretation
* Secure baseline governance
* Configuration compliance assessment
* Evidence request development
* Design-effectiveness testing
* Operating-effectiveness testing
* Windows and Linux hardening oversight
* Cloud configuration governance
* Infrastructure-as-code assurance
* Configuration drift analysis
* Automated control validation
* Exception and risk-acceptance review
* Change-management integration
* Root-cause analysis
* Risk-rating methodology
* Corrective action planning
* Continuous control monitoring
* Security metrics development
* Executive reporting
* Cross-functional security oversight
