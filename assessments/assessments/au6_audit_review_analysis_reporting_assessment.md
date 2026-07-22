# NIST SP 800-53 AU-6 Control Assessment

## Audit Record Review, Analysis, and Reporting


---

## Document Control

| Field               | Value                                        |
| ------------------- | -------------------------------------------- |
| Assessment ID       | SCA-AU6-2026-001                             |
| Framework           | NIST SP 800-53 Revision 5                    |
| Assessment Guidance | NIST SP 800-53A Revision 5                   |
| Control Family      | Audit and Accountability                     |
| Control             | AU-6                                         |
| Control Name        | Audit Record Review, Analysis, and Reporting |
| Assessment Type     | Design and Operating Effectiveness Review    |
| Assessment Period   | Q2 2026                                      |
| Environment         | Simulated Enterprise Environment             |
| Assessor            | Abdilaahe Omar                               |
| Role                | Governance, Risk, and Compliance Analyst     |
| Document Status     | Final — Portfolio Case Study                 |
| Data Classification | Public Portfolio Content                     |

---

# 1. Executive Summary

A risk-based security control assessment was performed to evaluate the design and operating effectiveness of the organization’s audit record review, analysis, escalation, and reporting processes.

The assessment examined whether security and system audit records were:

* Reviewed at an established frequency
* Analyzed for inappropriate or unusual activity
* Correlated across systems and repositories
* Escalated to appropriate personnel
* Integrated with incident response processes
* Protected through role-based access
* Adjusted when organizational risk or threat intelligence changed
* Used to support enterprise situational awareness

The simulated organization maintained a centralized Security Information and Event Management platform that collected audit records from identity systems, Windows and Linux endpoints, cloud services, firewalls, virtual private network infrastructure, endpoint security tools, and critical business applications.

The organization demonstrated generally effective centralized monitoring and investigation capabilities. Security alerts were routed to the Security Operations Center, high-risk events were documented in the incident management platform, and audit information from multiple sources was correlated during investigations.

Two control deficiencies were identified:

1. Several high-value business applications did not have documented audit-review frequencies or formally assigned review owners.
2. The organization did not consistently document changes to monitoring intensity after receiving credible threat intelligence.

No evidence was identified indicating that either weakness resulted in an undetected confirmed compromise. However, the conditions reduced assurance that audit review and risk-based monitoring adjustments were applied consistently across the environment.

## Overall Assessment Result

**Partially Satisfied**

## Overall Risk Rating

**Moderate**

## Assessor’s Opinion

The AU-6 control was appropriately designed and substantially implemented. Centralized monitoring, alert analysis, investigation, and reporting processes were operating effectively for major enterprise systems.

Targeted remediation is required to formalize application-level review responsibilities and create a documented process for adjusting monitoring based on changes in risk.

---

# 2. Control Requirement

## AU-6 — Audit Record Review, Analysis, and Reporting

The assessment evaluates whether the organization:

1. Defines how frequently system audit records must be reviewed and analyzed.
2. Defines the types of inappropriate or unusual activity that require investigation.
3. Reviews audit records at the established frequency.
4. Analyzes the potential impact of identified activity.
5. Reports findings to designated personnel or roles.
6. Adjusts the level of audit review, analysis, and reporting when risk changes based on law enforcement information, threat intelligence, or other credible sources.

---

# 3. Selected Control Enhancements

The simulated assessment also evaluates the following AU-6 control enhancements:

| Enhancement | Assessment Area                                                                               |
| ----------- | --------------------------------------------------------------------------------------------- |
| AU-6(1)     | Automated integration of audit review, analysis, and reporting processes                      |
| AU-6(3)     | Correlation of audit records across different repositories                                    |
| AU-6(4)     | Central review and analysis of audit records                                                  |
| AU-6(5)     | Integration of audit information with vulnerability and system-monitoring data                |
| AU-6(7)     | Specification of permitted actions for users, roles, and processes handling audit information |
| AU-6(8)     | Full-text analysis of logged privileged commands                                              |

---

# 4. Business and Security Context

Audit records provide evidence of activity occurring across systems, applications, identities, networks, and security technologies.

Collecting logs alone does not provide sufficient security assurance. Audit records must also be reviewed, correlated, interpreted, escalated, and used to support decisions.

An ineffective audit-review process can result in:

* Delayed detection of security incidents
* Failure to identify unauthorized access
* Incomplete investigation evidence
* Missed indicators of insider threats
* Unidentified privilege misuse
* Weak regulatory or audit support
* Inability to reconstruct security events
* Failure to recognize coordinated attacks
* Excessive false positives
* Inconsistent escalation decisions
* Failure to adapt monitoring to emerging threats

A mature AU-6 implementation connects audit information with incident response, threat intelligence, vulnerability management, identity monitoring, endpoint security, and risk management.

---

# 5. Assessment Scope

## In-Scope Technologies

The simulated assessment covered:

* Security Information and Event Management platform
* Wazuh security monitoring platform
* Microsoft Active Directory
* Microsoft Entra ID
* Microsoft 365
* Windows endpoints and servers
* Linux servers
* Endpoint Detection and Response platform
* Network firewalls
* Virtual private network infrastructure
* Cloud infrastructure audit logs
* Privileged Access Management platform
* Vulnerability management platform
* Incident management platform
* Critical enterprise business applications

## In-Scope Audit Sources

* Authentication events
* Privileged access events
* Account-management events
* Process-creation events
* PowerShell activity
* Endpoint security alerts
* Firewall traffic
* VPN activity
* Cloud administrative events
* Application security events
* Configuration changes
* Vulnerability scan results
* Administrative command logs
* Data-access events
* Incident-response records

## Out-of-Scope Items

The following were excluded:

* Development systems not connected to enterprise monitoring
* Customer-managed environments
* Physical surveillance records
* Archived systems scheduled for retirement
* Systems without production data or active users

---

# 6. Assessment Objectives

The assessment was designed to determine whether:

1. Audit-review frequencies were documented.
2. Inappropriate and unusual activities were defined.
3. Audit records were reviewed according to established schedules.
4. Alerts were analyzed for business and security impact.
5. Findings were reported to appropriate personnel.
6. Centralized monitoring included all critical systems.
7. Audit records from multiple sources were correlated.
8. Audit analysis was integrated with vulnerability and system-monitoring data.
9. Monitoring intensity was adjusted when risk changed.
10. Access to audit information followed least-privilege principles.
11. Privileged commands were logged and analyzed.
12. Investigation and reporting activities were documented.
13. Monitoring performance was measured and improved.
14. Corrective actions were tracked to closure.

---

# 7. Assessment Methodology

The assessment followed a risk-based methodology using the following methods.

## 7.1 Examine

The assessor reviewed policies, standards, procedures, configurations, reports, tickets, dashboards, access records, and technical evidence.

## 7.2 Interview

Personnel responsible for logging, monitoring, investigations, system administration, risk oversight, and incident response were interviewed.

## 7.3 Test

Selected log sources, alert scenarios, escalation workflows, access restrictions, and correlation capabilities were tested.

---

# 8. Assessment Depth and Coverage

| Attribute                   | Selected Level        |
| --------------------------- | --------------------- |
| Assessment Depth            | Moderate              |
| Assessment Coverage         | Representative        |
| Testing Approach            | Risk-based sampling   |
| Evidence Period             | April 1–June 30, 2026 |
| Systems Sampled             | 18                    |
| Log Sources Sampled         | 12                    |
| Alerts Sampled              | 30                    |
| Incident Tickets Sampled    | 10                    |
| Privileged Sessions Sampled | 10                    |

Higher-risk systems were prioritized based on:

* Data sensitivity
* Internet exposure
* Privileged access
* Regulatory significance
* Business criticality
* Previous security findings
* Threat intelligence relevance

---

# 9. Organization-Defined Parameters

The simulated organization established the following AU-6 parameters.

## Audit-Review Frequency

| Audit Category             | Required Review Frequency    |
| -------------------------- | ---------------------------- |
| Critical security alerts   | Continuous or near real time |
| High-severity alerts       | Within 30 minutes            |
| Medium-severity alerts     | Within four business hours   |
| Low-severity alerts        | Daily queue review           |
| Privileged-access activity | Daily                        |
| Authentication anomalies   | Continuous                   |
| Critical application logs  | Daily                        |
| Standard application logs  | Weekly                       |
| Audit-program performance  | Monthly                      |
| Audit coverage review      | Quarterly                    |

## Defined Inappropriate or Unusual Activity

Examples included:

* Multiple failed authentication attempts
* Password spraying
* Impossible-travel activity
* Unusual administrative logons
* Unauthorized account creation
* Privilege escalation
* Disabled security controls
* Suspicious PowerShell activity
* Malware execution
* Unexpected outbound traffic
* Large data transfers
* Unapproved configuration changes
* Access outside approved business hours
* Log deletion or tampering
* Use of dormant accounts
* Unauthorized privileged commands

## Designated Recipients

Findings were required to be reported to appropriate personnel, including:

* Security Operations Center
* Incident Response Team
* Information Security Management
* System Owners
* Identity and Access Management Team
* Privacy Office
* Legal Department
* Human Resources
* Internal Audit
* Executive Leadership

The recipient depended on the severity, affected data, business impact, and nature of the activity.

---

# 10. Evidence Request List

## Governance Evidence

* Audit and Accountability Policy
* Logging and Monitoring Standard
* Security Event Escalation Procedure
* Incident Response Plan
* Threat Intelligence Procedure
* Vulnerability Management Standard
* Privileged Access Monitoring Standard
* Data Retention Standard
* Audit Record Access Matrix
* Security Monitoring Roles and Responsibilities

## Operational Evidence

* Daily alert-review records
* Security analyst shift reports
* Investigation tickets
* Incident escalation records
* Monthly monitoring reports
* Quarterly control-owner attestations
* Threat intelligence advisories
* Monitoring-adjustment records
* False-positive tuning records
* Detection engineering change records

## Technical Evidence

* SIEM architecture diagram
* SIEM data-source inventory
* Log ingestion dashboard
* Correlation rule inventory
* Wazuh rule configuration
* Alert severity definitions
* EDR alert records
* Firewall audit logs
* Cloud audit records
* Authentication dashboards
* Vulnerability scan exports
* PAM session records
* Privileged command logs
* Role-based access configuration
* Log-retention configuration

---

# 11. Stakeholders Interviewed

| Role                          | Assessment Purpose                                  |
| ----------------------------- | --------------------------------------------------- |
| SOC Manager                   | Validate monitoring governance and escalation       |
| Detection Engineering Lead    | Review correlation logic and rule management        |
| SOC Analyst                   | Validate daily review and investigation practices   |
| Incident Response Lead        | Confirm incident escalation and evidence use        |
| SIEM Administrator            | Review ingestion, availability, and access controls |
| Threat Intelligence Analyst   | Evaluate risk-based monitoring adjustments          |
| Vulnerability Management Lead | Validate integrated analysis                        |
| Identity Security Manager     | Review authentication and account monitoring        |
| Application Owner             | Confirm application-level review responsibilities   |
| GRC Control Owner             | Validate oversight and evidence retention           |

---

# 12. Sample Selection

## Log Source Sample

| Source Category               | Population | Sample |
| ----------------------------- | ---------: | -----: |
| Windows endpoints and servers |      1,900 |      4 |
| Linux servers                 |        220 |      2 |
| Cloud platforms               |          3 |      2 |
| Identity systems              |          2 |      2 |
| Network security devices      |         75 |      2 |
| Business applications         |         46 |      4 |
| Security platforms            |          5 |      2 |
| **Total**                     |  **2,251** | **18** |

## Alert Sample

| Alert Severity | Sample Size |
| -------------- | ----------: |
| Critical       |           5 |
| High           |          10 |
| Medium         |          10 |
| Low            |           5 |
| **Total**      |      **30** |

---

# 13. Control Test Procedures and Results

## Test AU6-01 — Defined Review Frequency

### Objective

Determine whether the organization documented how frequently audit records must be reviewed and analyzed.

### Procedure

1. Reviewed the Audit and Accountability Policy.
2. Compared policy requirements with monitoring procedures.
3. Reviewed severity-based service targets.
4. Examined application monitoring requirements.
5. Verified that control owners were assigned.

### Evidence

* Audit and Accountability Policy
* SOC Operating Procedure
* Alert Severity Matrix
* Application Monitoring Standard
* Control Ownership Register

### Result

**Partially Satisfied**

### Observation

Review frequencies were clearly defined for SIEM alerts, authentication events, endpoint alerts, and privileged access.

However, six high-value business applications did not have documented review frequencies or formally assigned audit-review owners.

### Related Finding

F-AU6-001 — Incomplete Application Audit-Review Governance

---

## Test AU6-02 — Definition of Unusual or Inappropriate Activity

### Objective

Determine whether the organization defined the activity that required review and investigation.

### Procedure

1. Reviewed monitoring standards.
2. Examined the detection use-case catalog.
3. Compared use cases with current threat scenarios.
4. Reviewed alert-severity definitions.
5. Confirmed ownership for detection logic.

### Evidence

* Detection Use-Case Catalog
* Threat Monitoring Standard
* Alert Severity Matrix
* Detection Rule Inventory
* MITRE ATT&CK Mapping

### Result

**Satisfied**

### Observation

The organization maintained documented detection scenarios for credential attacks, unauthorized access, malware, privilege escalation, suspicious scripting, data movement, and security-control interference.

---

## Test AU6-03 — Timely Review and Analysis

### Objective

Determine whether audit records and alerts were reviewed within established timeframes.

### Procedure

1. Selected 30 alerts.
2. Compared alert-generation timestamps with analyst acknowledgement.
3. Reviewed investigation notes.
4. Verified disposition and closure.
5. Examined overdue-alert reporting.

### Evidence

* SIEM Alert Records
* Investigation Tickets
* SOC Queue Metrics
* Shift Reports
* Escalation Records

### Result

**Satisfied**

### Observation

Twenty-nine of 30 sampled alerts were reviewed within the required service target.

One medium-severity alert exceeded the target by 18 minutes. The delay was documented and did not affect incident containment.

The exception rate did not indicate a systemic control failure.

---

## Test AU6-04 — Findings Reporting and Escalation

### Objective

Determine whether material audit findings were reported to designated personnel.

### Procedure

1. Selected 10 investigation tickets.
2. Reviewed escalation paths.
3. Compared notification recipients with the escalation matrix.
4. Verified documentation of business impact.
5. Confirmed management notification for high-risk events.

### Evidence

* Incident Tickets
* Escalation Matrix
* Email Notification Records
* Management Reports
* Incident Timeline Documents

### Result

**Satisfied**

### Observation

High-severity findings were escalated to incident response, security leadership, system owners, and other stakeholders based on the nature of the event.

Escalation decisions were documented within the incident management platform.

---

## Test AU6-05 — Risk-Based Adjustment of Monitoring

### Objective

Determine whether monitoring depth, frequency, or coverage was adjusted after changes in threat or risk.

### Procedure

1. Selected five threat intelligence advisories.
2. Reviewed monitoring changes made in response.
3. Compared advisory dates with detection-rule changes.
4. Examined temporary monitoring directives.
5. Reviewed change approval and closure documentation.

### Evidence

* Threat Intelligence Advisories
* Detection Engineering Tickets
* Monitoring Change Records
* SIEM Rule History
* Risk Committee Minutes

### Result

**Partially Satisfied**

### Observation

The organization adjusted monitoring after three of five sampled advisories.

For two advisories, analysts stated that existing controls were considered sufficient. However, no formal analysis or approval record documented that decision.

### Related Finding

F-AU6-002 — Inconsistent Documentation of Risk-Based Monitoring Adjustments

---

## Test AU6-06 — Automated Process Integration

### Related Enhancement

AU-6(1)

### Objective

Determine whether automated mechanisms integrated review, analysis, reporting, and response processes.

### Procedure

1. Reviewed SIEM integrations.
2. Traced alerts into the incident management platform.
3. Verified enrichment from identity, asset, and threat intelligence systems.
4. Reviewed automated escalation workflows.
5. Confirmed analyst approval for containment actions.

### Evidence

* SIEM Integration Diagram
* SOAR Workflow Configuration
* Incident Ticket Records
* Asset Enrichment Data
* Threat Intelligence Enrichment

### Result

**Satisfied**

### Observation

High-risk alerts were automatically enriched with asset criticality, identity information, threat intelligence, and vulnerability context.

Qualified alerts generated investigation tickets and routed them to the correct response queue.

---

## Test AU6-07 — Correlation Across Repositories

### Related Enhancement

AU-6(3)

### Objective

Determine whether records from separate systems were correlated to provide enterprise situational awareness.

### Procedure

1. Selected authentication and endpoint alerts.
2. Reviewed correlation with VPN, firewall, cloud, and identity logs.
3. Traced multi-stage activity across data sources.
4. Examined correlation rules.
5. Verified that timestamps and identity fields were normalized.

### Evidence

* SIEM Correlation Rules
* Authentication Logs
* Firewall Logs
* EDR Records
* Cloud Audit Events
* Investigation Timeline

### Result

**Satisfied**

### Observation

The platform successfully correlated identity, endpoint, cloud, VPN, and network activity during sampled investigations.

This enabled analysts to reconstruct activity across multiple systems.

---

## Test AU6-08 — Central Review and Analysis

### Related Enhancement

AU-6(4)

### Objective

Determine whether audit records from multiple system components could be reviewed and analyzed centrally.

### Procedure

1. Reviewed centralized logging architecture.
2. Verified ingestion from sampled systems.
3. Compared the asset inventory with the log-source inventory.
4. Tested analyst search capabilities.
5. Reviewed ingestion-health monitoring.

### Evidence

* SIEM Architecture Diagram
* Data-Source Inventory
* Log Ingestion Dashboard
* Search Results
* Collector Health Reports

### Result

**Satisfied**

### Observation

The SIEM provided centralized search, correlation, dashboards, and alerting for the majority of critical systems.

Log-ingestion failures generated monitoring alerts for SIEM administrators.

---

## Test AU6-09 — Integrated Analysis with Vulnerability Data

### Related Enhancement

AU-6(5)

### Objective

Determine whether audit analysis was integrated with vulnerability and system-monitoring information.

### Procedure

1. Selected high-severity endpoint alerts.
2. Reviewed asset vulnerability context.
3. Confirmed integration of endpoint and network-monitoring information.
4. Compared alert prioritization before and after enrichment.
5. Interviewed analysts regarding risk-based triage.

### Evidence

* Vulnerability Scanner Results
* EDR Records
* SIEM Enrichment Fields
* Asset Criticality Ratings
* Investigation Tickets

### Result

**Satisfied**

### Observation

Analysts could view asset criticality, vulnerability exposure, endpoint telemetry, and identity context from the investigation interface.

Alerts involving vulnerable, internet-facing, or business-critical assets received elevated priority.

---

## Test AU6-10 — Permitted Actions and Least Privilege

### Related Enhancement

AU-6(7)

### Objective

Determine whether permitted actions involving audit information were defined and restricted.

### Procedure

1. Reviewed SIEM role definitions.
2. Examined analyst and administrator permissions.
3. Tested read, search, export, modification, and deletion restrictions.
4. Reviewed privileged access logs.
5. Confirmed periodic entitlement reviews.

### Evidence

* SIEM Role Matrix
* User Access Export
* Privileged Activity Logs
* Quarterly Access Review
* Administrative Procedures

### Result

**Satisfied**

### Observation

SOC analysts could search and export authorized audit data but could not delete source logs or modify collection configurations.

Administrative actions required elevated roles and were separately logged.

---

## Test AU6-11 — Full-Text Analysis of Privileged Commands

### Related Enhancement

AU-6(8)

### Objective

Determine whether logged privileged commands and their parameters were available for analysis.

### Procedure

1. Selected 10 privileged sessions.
2. Reviewed command and parameter capture.
3. Verified storage in a separate monitoring environment.
4. Tested keyword and behavioral searches.
5. Confirmed administrator access restrictions.

### Evidence

* PAM Session Records
* Linux Command Audit Logs
* PowerShell Script Block Logs
* SIEM Search Results
* Privileged Monitoring Procedure

### Result

**Satisfied**

### Observation

The organization captured command text and relevant parameters for selected privileged sessions.

Records were transmitted to the centralized monitoring environment, where privileged users on the source systems could not alter them.

---

# 14. Test Summary

| Test ID | Control Area                          | Result              |
| ------- | ------------------------------------- | ------------------- |
| AU6-01  | Defined review frequency              | Partially Satisfied |
| AU6-02  | Definition of unusual activity        | Satisfied           |
| AU6-03  | Timely review and analysis            | Satisfied           |
| AU6-04  | Findings reporting and escalation     | Satisfied           |
| AU6-05  | Risk-based monitoring adjustment      | Partially Satisfied |
| AU6-06  | Automated process integration         | Satisfied           |
| AU6-07  | Cross-repository correlation          | Satisfied           |
| AU6-08  | Central review and analysis           | Satisfied           |
| AU6-09  | Integrated vulnerability analysis     | Satisfied           |
| AU6-10  | Permitted actions and least privilege | Satisfied           |
| AU6-11  | Analysis of privileged commands       | Satisfied           |

---

# 15. Findings

## F-AU6-001 — Incomplete Application Audit-Review Governance

### Condition

Six high-value business applications did not have formally documented audit-review frequencies or assigned review owners.

The applications transmitted selected events to the SIEM, but responsibility for reviewing application-specific audit activity was not clearly assigned.

### Criteria

The organization should define how frequently audit records are reviewed, what activity requires analysis, and which personnel receive findings.

### Cause

Application onboarding focused on technical log ingestion but did not require completion of a formal monitoring ownership record.

### Effect

Important application-level events may not receive consistent review, escalation, or subject-matter analysis.

### Likelihood

Possible

### Impact

Major

### Inherent Risk

High

### Existing Compensating Controls

* Selected events transmitted to the SIEM
* Infrastructure alerts reviewed by the SOC
* Application access reviews performed quarterly
* Critical incidents escalated through the standard incident process
* Application administrators maintained local logs

### Residual Risk

Moderate

### Recommendation

1. Assign an audit-review owner for every high-value application.
2. Define required review frequency.
3. Document reportable activity.
4. Integrate requirements into the application onboarding process.
5. Establish evidence-retention requirements.
6. Perform quarterly monitoring-owner attestation.
7. Track applications without confirmed monitoring coverage.

### Proposed Owner

Application Security Manager

### Target Completion

September 30, 2026

---

## F-AU6-002 — Inconsistent Documentation of Risk-Based Monitoring Adjustments

### Condition

Two of five sampled threat advisories did not have documented monitoring-impact analyses.

Personnel stated that existing detections were sufficient, but the decision, supporting analysis, and approval were not recorded.

### Criteria

The organization should adjust, or formally evaluate whether to adjust, audit-review depth, scope, frequency, and reporting when credible information changes risk.

### Cause

The threat intelligence and detection engineering teams did not use a standardized monitoring-impact assessment form.

### Effect

The organization may be unable to demonstrate that emerging threats were evaluated consistently or that monitoring remained appropriate.

### Likelihood

Possible

### Impact

Moderate

### Inherent Risk

Moderate

### Existing Compensating Controls

* Weekly threat intelligence meetings
* Existing behavior-based detections
* Detection engineering backlog
* Emergency SIEM change process
* Security leadership oversight

### Residual Risk

Low to Moderate

### Recommendation

1. Create a standardized monitoring-impact assessment.
2. Require a documented decision for each material advisory.
3. Record affected systems and detection coverage.
4. Define temporary monitoring changes and expiration dates.
5. Require detection engineering or SOC management approval.
6. Link threat advisories to change and validation records.
7. Report unresolved monitoring gaps to the security risk committee.

### Proposed Owner

Threat Detection Manager

### Target Completion

August 31, 2026

---

# 16. Risk Summary

| Finding   | Inherent Risk | Residual Risk   | Priority | Treatment |
| --------- | ------------- | --------------- | -------- | --------- |
| F-AU6-001 | High          | Moderate        | High     | Mitigate  |
| F-AU6-002 | Moderate      | Low to Moderate | Medium   | Mitigate  |

No critical-risk findings were identified.

---

# 17. Positive Control Observations

The assessment identified the following strengths:

* Centralized audit collection was implemented.
* Critical alerts were reviewed continuously.
* Severity-based response targets were documented.
* Audit information was correlated across multiple repositories.
* SIEM and incident management workflows were integrated.
* Vulnerability and asset context supported alert prioritization.
* Privileged activity was logged and attributable.
* Analysts had role-based access to audit information.
* Administrative actions against logging systems were monitored.
* Alert investigation records supported management reporting.
* Log-ingestion health was actively monitored.
* Detection rules were mapped to recognized adversary behaviors.
* High-risk incidents were escalated to appropriate stakeholders.

These capabilities improved the organization’s ability to identify, analyze, communicate, and respond to suspicious activity.

---

# 18. Corrective Action Plan

| Action ID   | Corrective Action                                     | Owner                         | Priority | Due Date   | Status      |
| ----------- | ----------------------------------------------------- | ----------------------------- | -------- | ---------- | ----------- |
| CAP-AU6-001 | Assign monitoring owners to high-value applications   | Application Security Manager  | High     | 2026-08-31 | Planned     |
| CAP-AU6-002 | Define application audit-review frequencies           | Application Governance Lead   | High     | 2026-09-30 | Planned     |
| CAP-AU6-003 | Add monitoring requirements to application onboarding | Security Architecture Manager | High     | 2026-09-30 | Planned     |
| CAP-AU6-004 | Create threat monitoring-impact assessment template   | Threat Detection Manager      | Medium   | 2026-07-31 | In Progress |
| CAP-AU6-005 | Link threat advisories to detection changes           | Detection Engineering Lead    | Medium   | 2026-08-31 | Planned     |
| CAP-AU6-006 | Perform targeted remediation validation               | GRC Control Assurance         | Medium   | 2026-10-15 | Not Started |

---

# 19. Management Response

Management agreed with both findings.

The Application Security function will establish documented audit-review requirements and owners for high-value applications. Monitoring responsibilities will become a required component of security architecture review and application onboarding.

The Threat Detection function will implement a standardized process for documenting whether new threat intelligence requires:

* Additional log sources
* New detection rules
* Increased review frequency
* Expanded reporting
* Temporary enhanced monitoring
* No change to existing coverage

Management acknowledged the residual risks and assigned corrective-action owners and target dates.

---

# 20. Assessor Conclusion

Based on the documentation examined, personnel interviewed, configurations reviewed, alert samples tested, and reporting processes evaluated, the organization substantially implemented NIST SP 800-53 AU-6 and the selected control enhancements.

Centralized review, automated integration, cross-repository correlation, privileged activity analysis, incident escalation, and vulnerability-context enrichment were operating effectively.

The control was not rated fully satisfied because:

1. Review ownership and frequency were not formally defined for six high-value business applications.
2. Risk-based monitoring decisions were not consistently documented after material threat intelligence was received.

## Final Determination

**Control Status:** Partially Satisfied
**Design Effectiveness:** Effective
**Operating Effectiveness:** Partially Effective
**Residual Risk:** Moderate
**Follow-Up Required:** Yes

The organization should complete corrective actions and perform targeted retesting before changing the control determination to fully satisfied.

---

# 21. Follow-Up Validation Plan

The assessor will:

1. Review completed monitoring ownership records.
2. Confirm approved review frequencies for affected applications.
3. Inspect updated application onboarding requirements.
4. Select new threat advisories and review monitoring-impact assessments.
5. Confirm linkage between advisories, detection changes, and validation results.
6. Review evidence that corrective actions were implemented.
7. Test SIEM coverage for selected applications.
8. Update the assessment conclusion and risk register.

---

# 22. Metrics and Key Risk Indicators

The following measures should support ongoing oversight:

| Metric or KRI                                                     | Purpose                             |
| ----------------------------------------------------------------- | ----------------------------------- |
| Percentage of critical systems sending logs                       | Measures audit coverage             |
| Percentage of high-value applications with assigned review owners | Measures governance completeness    |
| Percentage of critical alerts reviewed within target              | Measures monitoring responsiveness  |
| Number of failed log sources                                      | Measures visibility risk            |
| Mean time to acknowledge alerts                                   | Measures analyst responsiveness     |
| Mean time to investigate alerts                                   | Measures operational efficiency     |
| Percentage of material advisories assessed for monitoring impact  | Measures threat-informed monitoring |
| Number of overdue corrective actions                              | Measures remediation risk           |
| Percentage of privileged activity reviewed                        | Measures elevated-access oversight  |
| False-positive rate by detection rule                             | Measures detection quality          |

---

# 23. Cross-Framework Alignment

| Framework                    | Related Area                                                                      |
| ---------------------------- | --------------------------------------------------------------------------------- |
| NIST SP 800-53 Rev. 5        | AU-6 and selected enhancements                                                    |
| NIST Cybersecurity Framework | Continuous monitoring, adverse event analysis, incident management, and reporting |
| ISO/IEC 27001                | Logging, monitoring activities, event assessment, and incident management         |
| CIS Controls                 | Audit Log Management and Security Monitoring                                      |
| MITRE ATT&CK                 | Threat-informed detection and behavioral analysis                                 |
| Zero Trust Architecture      | Continuous monitoring, analytics, and risk-based decision-making                  |

Cross-framework mappings should be validated against the organization’s selected framework versions, implementation statements, system scope, and regulatory obligations.

---

# 24. Authoritative References

* NIST SP 800-53 Revision 5 — Security and Privacy Controls for Information Systems and Organizations
* NIST SP 800-53A Revision 5 — Assessing Security and Privacy Controls in Information Systems and Organizations
* Organization Audit and Accountability Policy
* Organization Logging and Monitoring Standard
* Organization Incident Response Plan
* Organization Threat Intelligence Procedure

---

# 25. Portfolio Skills Demonstrated

* NIST control interpretation
* Audit and accountability assessment
* Security monitoring governance
* SIEM control assessment
* Evidence request development
* Risk-based sampling
* Alert and incident-ticket testing
* Design-effectiveness evaluation
* Operating-effectiveness evaluation
* Threat-informed monitoring
* Log-source coverage analysis
* Detection engineering oversight
* Cross-platform event correlation
* Privileged activity monitoring
* Control deficiency analysis
* Root-cause documentation
* Risk-rating methodology
* Corrective action planning
* Management response tracking
* Executive security reporting
