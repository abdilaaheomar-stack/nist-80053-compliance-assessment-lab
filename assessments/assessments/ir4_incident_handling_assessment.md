# NIST SP 800-53 IR-4 Control Assessment

## Incident Handling


---

## Document Control

| Field               | Value                                     |
| ------------------- | ----------------------------------------- |
| Assessment ID       | SCA-IR4-2026-001                          |
| Framework           | NIST SP 800-53 Revision 5                 |
| Assessment Guidance | NIST SP 800-53A Revision 5                |
| Control Family      | Incident Response                         |
| Control             | IR-4                                      |
| Control Name        | Incident Handling                         |
| Assessment Type     | Design and Operating Effectiveness Review |
| Assessment Period   | Q2 2026                                   |
| Environment         | Simulated Financial Services Enterprise   |
| Assessment Scenario | Ransomware and Credential Compromise      |
| Assessor            | Abdilaahe Omar                            |
| Role                | Governance, Risk, and Compliance Analyst  |
| Document Status     | Final — Portfolio Case Study              |
| Data Classification | Public Portfolio Content                  |

---

# 1. Executive Summary

A risk-based control assessment was performed to evaluate the design and operating effectiveness of the organization’s incident handling capability.

The assessment examined whether cybersecurity incidents were consistently prepared for, detected, analyzed, contained, eradicated, and recovered from in accordance with established incident response procedures.

Testing also evaluated whether the organization:

* Coordinated incident response with business continuity and disaster recovery teams
* Used automated technology to support incident handling
* Correlated incident information across security platforms
* Preserved forensic evidence
* Used dynamic containment actions
* Escalated major incidents to an integrated response team
* Validated recovery before returning systems to production
* Incorporated lessons learned into procedures, training, and technical controls
* Applied a predictable response methodology across business units

The organization demonstrated a mature incident response capability supported by a centralized Security Operations Center, endpoint security tooling, SIEM monitoring, incident management workflows, forensic procedures, and defined executive escalation paths.

A simulated ransomware incident involving a finance workstation and shared file service was used to evaluate the organization’s end-to-end response capability.

The organization successfully:

* Detected suspicious endpoint behavior
* Isolated the affected workstation
* Disabled the potentially compromised identity
* Blocked associated network indicators
* Preserved forensic evidence
* Activated business continuity procedures
* Restored affected data from a protected backup
* Conducted a formal lessons-learned review

Two control weaknesses were identified:

1. Recovery authorization criteria were not consistently documented before restored systems were returned to production.
2. Corrective actions resulting from lessons-learned reviews were not consistently tracked through verified closure.

No evidence indicated that the weaknesses caused material data loss or unauthorized disclosure during the simulated exercise. However, they reduced assurance that recovery and continuous improvement activities would be performed consistently during a real enterprise-wide incident.

## Overall Assessment Result

**Partially Satisfied**

## Overall Risk Rating

**Moderate**

## Assessor’s Opinion

The incident handling control was effectively designed and substantially implemented.

Detection, analysis, containment, eradication, technical coordination, and evidence preservation processes operated effectively during testing. Targeted improvements are required in recovery governance and post-incident corrective action management.

---

# 2. Control Requirement

## IR-4 — Incident Handling

The assessment evaluates whether the organization maintains an incident handling capability that:

1. Is consistent with the approved incident response plan.
2. Includes preparation.
3. Includes detection and analysis.
4. Includes containment.
5. Includes eradication.
6. Includes recovery.
7. Coordinates incident handling with contingency planning.
8. Incorporates lessons learned into procedures, training, testing, and technical safeguards.
9. Produces comparable and predictable incident handling results across the organization.

---

# 3. Selected Control Enhancements

The simulated assessment included the following IR-4 enhancements:

| Enhancement | Assessment Area                               |
| ----------- | --------------------------------------------- |
| IR-4(1)     | Automated incident handling processes         |
| IR-4(2)     | Dynamic reconfiguration during response       |
| IR-4(3)     | Continuity of operations                      |
| IR-4(4)     | Correlation of incident information           |
| IR-4(5)     | Configurable automatic disabling or isolation |
| IR-4(11)    | Integrated incident response team             |
| IR-4(12)    | Malicious code and forensic analysis          |
| IR-4(14)    | Security Operations Center capability         |

---

# 4. Business and Security Context

Incident handling protects the organization from operational disruption, financial loss, legal exposure, data compromise, reputational harm, and loss of customer trust.

A documented incident response plan alone does not establish an effective capability. The organization must be able to execute the plan under pressure while maintaining evidence integrity, business continuity, communication discipline, and accountability.

Weak incident handling can result in:

* Delayed containment
* Increased attacker dwell time
* Expanded malware propagation
* Destruction or contamination of evidence
* Incomplete incident scoping
* Premature restoration of compromised systems
* Failure to meet notification requirements
* Uncoordinated executive decisions
* Repeated incidents caused by unresolved root causes
* Business interruption exceeding established tolerance
* Inconsistent handling across departments
* Loss of stakeholder confidence

A mature incident response program combines technical response, governance, legal review, communications, business continuity, risk management, and executive decision-making.

---

# 5. Assessment Scope

## In-Scope Functions

* Security Operations Center
* Incident Response Team
* Digital Forensics
* Identity and Access Management
* Network Security
* Endpoint Security
* Cloud Security
* Business Continuity
* Disaster Recovery
* Information Technology Operations
* Legal and Privacy
* Corporate Communications
* Enterprise Risk Management
* Business Application Ownership

## In-Scope Technologies

* Security Information and Event Management platform
* Wazuh security monitoring platform
* Endpoint Detection and Response platform
* Microsoft Active Directory
* Microsoft Entra ID
* Microsoft 365
* Network firewalls
* Virtual private network platform
* Privileged Access Management platform
* Service management and incident ticketing platform
* Vulnerability management platform
* Backup and recovery platform
* Digital forensic collection tools
* Threat intelligence platform
* Windows workstations and servers
* Cloud infrastructure

## In-Scope Incident Categories

* Ransomware
* Malware
* Credential compromise
* Unauthorized privileged access
* Data exfiltration
* Cloud account compromise
* Insider threat
* Denial-of-service attack
* Third-party or supply chain incident
* Loss of sensitive information
* Security control failure

## Out-of-Scope Areas

* Physical emergency management
* Workplace safety investigations
* Fraud investigations unrelated to information systems
* Customer-managed systems
* Development environments containing no production information

---

# 6. Assessment Objectives

The assessment was designed to determine whether:

1. Incident handling roles were defined.
2. Personnel understood escalation responsibilities.
3. Incidents were classified consistently.
4. Relevant telemetry supported timely detection.
5. Analysts performed structured technical analysis.
6. Affected identities, endpoints, networks, and applications could be contained.
7. Evidence was preserved before destructive remediation.
8. Malware and residual artifacts could be analyzed safely.
9. Root causes and persistence mechanisms were identified.
10. Recovery followed documented validation criteria.
11. Incident response coordinated with business continuity.
12. Automated technologies supported response.
13. Security information was correlated across systems.
14. Major incidents activated an integrated response team.
15. Lessons learned resulted in measurable improvements.
16. Response quality was consistent across organizational units.

---

# 7. Assessment Methodology

The assessment used three control-assessment methods.

## 7.1 Examine

The assessor reviewed policies, plans, playbooks, tickets, technical configurations, investigation records, forensic evidence, recovery records, meeting notes, and corrective action documentation.

## 7.2 Interview

Personnel responsible for incident detection, investigation, containment, recovery, communications, legal review, and governance were interviewed.

## 7.3 Test

The assessor evaluated selected historical simulations and observed a controlled ransomware-response exercise.

Testing included:

* Alert generation
* Incident classification
* Escalation
* Endpoint isolation
* Identity containment
* Network blocking
* Evidence preservation
* Incident correlation
* Recovery validation
* Executive communication
* Lessons-learned processing

---

# 8. Assessment Depth and Coverage

| Attribute                        | Selected Level        |
| -------------------------------- | --------------------- |
| Assessment Depth                 | Moderate              |
| Assessment Coverage              | Representative        |
| Testing Strategy                 | Risk-based            |
| Evidence Period                  | April 1–June 30, 2026 |
| Incident Records Sampled         | 12                    |
| Major Incident Exercises Sampled | 3                     |
| Technical Playbooks Sampled      | 8                     |
| Corrective Actions Sampled       | 12                    |
| Business Units Sampled           | 4                     |

The sample prioritized incidents involving:

* Privileged identities
* Sensitive financial information
* Business-critical services
* Internet-facing systems
* Malware execution
* Potential regulatory impact
* Significant operational disruption

---

# 9. Organization-Defined Parameters

## Incident Severity Model

| Severity              | Description                                                                                                             | Required Response                                      |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| Severity 1 — Critical | Material business disruption, confirmed sensitive-data compromise, widespread ransomware, or significant safety concern | Immediate integrated response and executive escalation |
| Severity 2 — High     | Confirmed compromise with limited scope or significant risk of expansion                                                | Immediate incident response engagement                 |
| Severity 3 — Moderate | Suspicious activity requiring investigation with limited confirmed impact                                               | SOC-led investigation and escalation as required       |
| Severity 4 — Low      | Low-risk event or unsuccessful activity                                                                                 | Standard queue handling and documentation              |

## Response Targets

| Activity                     | Severity 1 Target | Severity 2 Target |
| ---------------------------- | ----------------: | ----------------: |
| Alert acknowledgement        |         5 minutes |        15 minutes |
| Incident declaration         |        15 minutes |        30 minutes |
| Initial containment          |        30 minutes |        60 minutes |
| Executive notification       |        30 minutes |       As required |
| Business continuity decision |        60 minutes |       As required |
| Initial situation report     |        60 minutes |           4 hours |

## Automated Response Mechanisms

The organization defined the following approved automation:

* EDR endpoint isolation
* Identity session revocation
* Conditional Access blocking
* Malicious hash blocking
* Domain and IP blocking
* Incident ticket creation
* Asset and identity enrichment
* Threat intelligence enrichment
* Evidence collection initiation
* Stakeholder notification
* Timeline generation

High-impact actions required analyst confirmation unless predetermined critical conditions were met.

---

# 10. Evidence Request List

## Governance Evidence

* Incident Response Policy
* Incident Response Plan
* Incident Classification Standard
* Major Incident Management Procedure
* Ransomware Response Playbook
* Credential Compromise Playbook
* Business Continuity Plan
* Disaster Recovery Plan
* Crisis Communications Plan
* Evidence Handling Standard
* Legal and Privacy Escalation Matrix
* Lessons-Learned Procedure

## Operational Evidence

* Incident tickets
* Investigation timelines
* Situation reports
* Executive notification records
* Containment approvals
* Evidence custody forms
* Recovery approvals
* Root cause analyses
* Lessons-learned meeting records
* Corrective action plans
* Tabletop exercise reports
* After-action reports

## Technical Evidence

* SIEM alerts
* Wazuh alerts
* EDR telemetry
* Endpoint isolation logs
* Firewall change records
* Identity disablement records
* Session revocation logs
* Forensic collection records
* File hash reports
* Malware analysis reports
* Backup restoration reports
* Vulnerability scan results
* Threat intelligence records
* Network packet data
* Cloud audit logs

---

# 11. Stakeholders Interviewed

| Role                          | Assessment Purpose                                  |
| ----------------------------- | --------------------------------------------------- |
| SOC Manager                   | Validate detection and escalation processes         |
| Incident Response Lead        | Evaluate incident command and handling              |
| Digital Forensics Analyst     | Review evidence collection and analysis             |
| Detection Engineering Lead    | Evaluate alert logic and technical coverage         |
| Identity Security Manager     | Review identity containment                         |
| Network Security Manager      | Review network isolation and blocking               |
| Business Continuity Manager   | Evaluate continuity coordination                    |
| Disaster Recovery Manager     | Review restoration and validation                   |
| Legal Counsel                 | Evaluate legal escalation and evidence requirements |
| Privacy Officer               | Review breach evaluation                            |
| Corporate Communications Lead | Evaluate stakeholder communications                 |
| GRC Control Owner             | Review governance and remediation tracking          |

---

# 12. Simulated Incident Scenario

## Scenario Name

Operation Locked Ledger

## Scenario Description

A finance employee opened a weaponized document delivered through a targeted phishing email.

Endpoint telemetry subsequently identified:

* Suspicious PowerShell execution
* Credential access behavior
* Connections to a newly registered external domain
* Rapid file modifications on the local workstation
* Attempts to access a finance department shared file service
* Encryption-like activity consistent with ransomware behavior

The scenario was designed to test whether the organization could contain the affected identity and endpoint before ransomware spread to business-critical systems.

## Simulated Assets

| Asset        | Criticality | Function                        |
| ------------ | ----------- | ------------------------------- |
| FIN-WS-104   | Medium      | Finance employee workstation    |
| FIN-FS-01    | High        | Finance department file service |
| ID-CORE-01   | Critical    | Enterprise identity service     |
| BCK-VAULT-01 | Critical    | Protected backup repository     |
| SIEM-01      | Critical    | Central security monitoring     |

## Simulated Business Impact

Potential impact included:

* Finance department disruption
* Loss of access to accounting records
* Unauthorized use of employee credentials
* Ransomware propagation
* Delayed payment operations
* Potential exposure of confidential financial information

---

# 13. Simulated Incident Timeline

| Time              | Activity                                                        |
| ----------------- | --------------------------------------------------------------- |
| 09:12             | EDR detected suspicious PowerShell execution                    |
| 09:14             | SIEM correlated endpoint, identity, and network alerts          |
| 09:16             | SOC analyst acknowledged the alert                              |
| 09:21             | Incident escalated to Severity 2                                |
| 09:24             | Endpoint automatically isolated with analyst confirmation       |
| 09:27             | User account disabled and active sessions revoked               |
| 09:31             | Malicious domain and IP indicators blocked                      |
| 09:34             | Encryption-like activity identified against the finance share   |
| 09:37             | Incident upgraded to Severity 1                                 |
| 09:42             | Integrated incident response team activated                     |
| 09:48             | Business continuity and legal teams notified                    |
| 09:55             | Volatile evidence and endpoint artifacts preserved              |
| 10:18             | Enterprise search identified no additional infected endpoints   |
| 10:34             | Finance file service removed from normal access                 |
| 11:05             | Malicious persistence mechanism identified and removed          |
| 11:40             | Backup integrity validation completed                           |
| 12:15             | Restored finance data placed in isolated validation environment |
| 12:48             | Security and business-owner validation completed                |
| 13:05             | Finance file service returned to limited production             |
| 14:10             | Full service restored                                           |
| 15:30             | Executive situation report issued                               |
| Next Business Day | Lessons-learned review initiated                                |

## Response Metrics

| Metric                              |             Result |
| ----------------------------------- | -----------------: |
| Mean time to acknowledge            |          4 minutes |
| Time to initial containment         |         12 minutes |
| Time to incident declaration        |         25 minutes |
| Time to integrated team activation  |         30 minutes |
| Time to complete initial scoping    |         66 minutes |
| Time to limited service restoration | 3 hours 53 minutes |
| Confirmed data exfiltration         |    None identified |
| Additional compromised endpoints    |    None identified |

---

# 14. Control Test Procedures and Results

## Test IR4-01 — Incident Preparation

### Objective

Determine whether the organization maintained the plans, playbooks, personnel, tools, and communication channels required to handle incidents.

### Procedure

1. Reviewed the incident response plan.
2. Reviewed ransomware and credential-compromise playbooks.
3. Verified current response-team contact information.
4. Confirmed access to required security tools.
5. Reviewed training and exercise records.
6. Confirmed availability of out-of-band communications.

### Evidence

* Incident Response Plan
* Ransomware Playbook
* Contact Roster
* Training Records
* Exercise Reports
* Tool Access Records

### Result

**Satisfied**

### Observation

Incident handling responsibilities, escalation paths, technical playbooks, and communication channels were documented and available to response personnel.

The organization maintained an out-of-band communication method for major incidents.

---

## Test IR4-02 — Detection and Analysis

### Objective

Determine whether the organization could detect, validate, classify, and scope suspected incidents.

### Procedure

1. Generated simulated endpoint and identity telemetry.
2. Reviewed alert correlation.
3. Observed analyst triage.
4. Evaluated incident classification.
5. Reviewed scoping queries across the enterprise.
6. Confirmed documentation of facts, assumptions, and investigative decisions.

### Evidence

* EDR Alert
* SIEM Correlation Alert
* Wazuh Event Records
* Analyst Investigation Notes
* Incident Timeline
* Enterprise Threat Hunt Results

### Result

**Satisfied**

### Observation

The SOC correlated suspicious PowerShell, identity, and network activity into a consolidated investigation.

The analyst correctly distinguished confirmed facts from unvalidated hypotheses and escalated the incident based on potential business impact.

---

## Test IR4-03 — Containment

### Objective

Determine whether affected endpoints, identities, network indicators, and services could be contained within defined response targets.

### Procedure

1. Observed endpoint isolation.
2. Verified account disablement.
3. Confirmed session revocation.
4. Reviewed firewall and domain blocks.
5. Evaluated the decision to restrict the finance file service.
6. Confirmed containment actions were documented and approved.

### Evidence

* EDR Isolation Record
* Identity Disablement Log
* Session Revocation Record
* Firewall Change
* DNS Blocking Record
* Incident Commander Approval

### Result

**Satisfied**

### Observation

The organization contained the workstation and identity before the simulated ransomware activity propagated to additional systems.

Containment decisions considered both security risk and operational impact.

---

## Test IR4-04 — Eradication

### Objective

Determine whether malicious artifacts, persistence, compromised credentials, and contributing vulnerabilities were removed.

### Procedure

1. Reviewed forensic findings.
2. Confirmed removal of malicious artifacts.
3. Verified credential reset and token revocation.
4. Reviewed persistence searches.
5. Confirmed vulnerability scanning.
6. Verified that indicators were added to enterprise detection tools.

### Evidence

* Forensic Analysis Report
* Malware Hash Report
* Credential Reset Record
* Persistence Search Results
* Vulnerability Scan
* Detection Engineering Change Record

### Result

**Satisfied**

### Observation

The response team identified and removed the simulated persistence mechanism, reset affected credentials, rescanned the endpoint, and distributed identified indicators across monitoring tools.

---

## Test IR4-05 — Recovery

### Objective

Determine whether affected services were restored securely and validated before normal operations resumed.

### Procedure

1. Reviewed backup integrity checks.
2. Observed restoration in an isolated environment.
3. Reviewed malware and vulnerability scans.
4. Confirmed business-owner testing.
5. Reviewed production restoration approval.
6. Compared results with recovery objectives.

### Evidence

* Backup Integrity Report
* Restoration Logs
* Security Validation Results
* Business Owner Test Record
* Recovery Approval
* Service Monitoring Results

### Result

**Partially Satisfied**

### Observation

The finance file service was restored from a protected backup, scanned, tested, and returned to operation within the established recovery objective.

However, the recovery checklist did not clearly require documented approval from both the incident commander and business owner before production restoration.

During two earlier sampled exercises, infrastructure personnel restored services before formal security approval was documented.

### Related Finding

F-IR4-001 — Inconsistent Recovery Authorization Criteria

---

## Test IR4-06 — Coordination with Contingency Planning

### Related Enhancement

IR-4(3)

### Objective

Determine whether incident handling was coordinated with business continuity and disaster recovery activities.

### Procedure

1. Reviewed escalation to continuity personnel.
2. Evaluated service criticality and recovery objectives.
3. Reviewed alternate business processes.
4. Confirmed recovery dependencies.
5. Examined communication between incident response and recovery teams.

### Evidence

* Business Impact Analysis
* Business Continuity Plan
* Disaster Recovery Plan
* Incident Bridge Records
* Recovery Status Reports

### Result

**Satisfied**

### Observation

The incident response team coordinated with continuity and recovery personnel before restricting the finance file service.

The finance department activated approved alternate processes while technical recovery was completed.

---

## Test IR4-07 — Lessons Learned and Continuous Improvement

### Objective

Determine whether lessons learned resulted in changes to procedures, training, testing, and controls.

### Procedure

1. Reviewed three after-action reports.
2. Selected 12 corrective actions.
3. Examined ownership and due dates.
4. Verified completed technical changes.
5. Reviewed overdue actions.
6. Confirmed reporting to governance committees.

### Evidence

* After-Action Reports
* Corrective Action Register
* Updated Playbooks
* Training Records
* Detection Rule Changes
* Risk Committee Reports

### Result

**Partially Satisfied**

### Observation

Lessons-learned sessions were consistently performed, and several improvements were implemented.

Four of 12 sampled corrective actions were overdue. Closure evidence was incomplete for two actions marked complete.

### Related Finding

F-IR4-002 — Incomplete Tracking and Validation of Lessons-Learned Actions

---

## Test IR4-08 — Consistency Across the Organization

### Objective

Determine whether incident handling produced predictable and comparable results across business units.

### Procedure

1. Sampled incidents from four business units.
2. Compared severity classification.
3. Reviewed required incident fields.
4. Evaluated escalation decisions.
5. Compared response timing.
6. Reviewed exception documentation.

### Evidence

* Incident Tickets
* Severity Matrix
* Response Metrics
* Escalation Records
* Quality Assurance Reviews

### Result

**Satisfied**

### Observation

All sampled incidents used the same classification model, required documentation fields, escalation process, and closure requirements.

Minor differences were based on documented business impact rather than inconsistent analyst practices.

---

## Test IR4-09 — Automated Incident Handling

### Related Enhancement

IR-4(1)

### Objective

Determine whether approved automated mechanisms supported incident handling.

### Procedure

1. Reviewed SIEM and SOAR integrations.
2. Tested ticket creation.
3. Verified asset and identity enrichment.
4. Observed containment workflow.
5. Reviewed automation safeguards.
6. Confirmed logging of automated actions.

### Evidence

* SOAR Workflow
* SIEM Integration Diagram
* Automated Ticket
* Enrichment Records
* Response Action Logs
* Approval Configuration

### Result

**Satisfied**

### Observation

Automation reduced manual investigation time and supported consistent enrichment, ticketing, notification, and containment.

High-impact actions required analyst confirmation unless predefined critical criteria were met.

---

## Test IR4-10 — Dynamic Reconfiguration

### Related Enhancement

IR-4(2)

### Objective

Determine whether security controls could be reconfigured rapidly to limit incident impact.

### Procedure

1. Reviewed firewall rule deployment.
2. Tested malicious domain blocking.
3. Reviewed Conditional Access changes.
4. Confirmed endpoint isolation.
5. Evaluated emergency change documentation.
6. Reviewed rollback procedures.

### Evidence

* Firewall Change Record
* DNS Security Record
* Conditional Access Change
* EDR Isolation Log
* Emergency Change Ticket
* Rollback Plan

### Result

**Satisfied**

### Observation

The organization dynamically changed network, identity, and endpoint controls to restrict simulated attacker activity.

Emergency changes were documented and had defined rollback procedures.

---

## Test IR4-11 — Information Correlation

### Related Enhancement

IR-4(4)

### Objective

Determine whether incident data from multiple sources was correlated into an organization-wide view.

### Procedure

1. Reviewed endpoint telemetry.
2. Reviewed identity events.
3. Reviewed network connections.
4. Reviewed email security data.
5. Compared timestamps.
6. Reconstructed the incident sequence.

### Evidence

* EDR Events
* Authentication Logs
* Firewall Logs
* Email Security Alert
* SIEM Timeline
* Analyst Investigation

### Result

**Satisfied**

### Observation

The SIEM correlated endpoint, identity, network, email, and threat intelligence data.

This allowed the response team to reconstruct the simulated attack chain and determine that no additional endpoints were compromised.

---

## Test IR4-12 — Automatic Disabling and Isolation

### Related Enhancement

IR-4(5)

### Objective

Determine whether the organization maintained configurable capabilities to isolate or disable affected systems when defined security violations were detected.

### Procedure

1. Reviewed automatic isolation criteria.
2. Tested endpoint isolation.
3. Confirmed analyst notification.
4. Reviewed safeguards against accidental disruption.
5. Tested release from isolation.
6. Reviewed continuity considerations.

### Evidence

* EDR Policy
* Isolation Trigger Configuration
* Isolation Record
* Analyst Notification
* Release Approval
* Business Impact Review

### Result

**Satisfied**

### Observation

Endpoints exhibiting high-confidence ransomware behavior could be automatically isolated.

The process included safeguards for critical systems where automatic shutdown could create greater operational risk.

---

## Test IR4-13 — Integrated Incident Response Team

### Related Enhancement

IR-4(11)

### Objective

Determine whether the organization could rapidly activate a cross-functional response team.

### Procedure

1. Reviewed team composition.
2. Tested activation procedures.
3. Evaluated attendance during the exercise.
4. Reviewed role assignment.
5. Confirmed decision authority.
6. Evaluated communication channels.

### Evidence

* Incident Team Roster
* Activation Record
* Incident Bridge Attendance
* Responsibility Matrix
* Decision Log
* Communication Record

### Result

**Satisfied**

### Observation

The integrated team included technical responders, business leadership, legal, privacy, continuity, communications, and risk personnel.

An incident commander was assigned, and material decisions were recorded.

---

## Test IR4-14 — Malicious Code and Forensic Analysis

### Related Enhancement

IR-4(12)

### Objective

Determine whether malicious artifacts and residual evidence could be preserved and analyzed safely.

### Procedure

1. Reviewed evidence acquisition.
2. Confirmed cryptographic hash validation.
3. Reviewed custody documentation.
4. Evaluated isolated malware analysis.
5. Reviewed persistence findings.
6. Confirmed distribution of resulting indicators.

### Evidence

* Evidence Collection Record
* Cryptographic Hash Record
* Chain-of-Custody Form
* Malware Analysis Report
* Forensic Timeline
* Indicator Distribution Record

### Result

**Satisfied**

### Observation

Evidence was preserved before endpoint remediation.

Malicious artifacts were analyzed in an isolated environment, and resulting indicators were distributed to detection and prevention tools.

---

## Test IR4-15 — Security Operations Center

### Related Enhancement

IR-4(14)

### Objective

Determine whether the SOC provided continuous detection, analysis, coordination, and response capabilities.

### Procedure

1. Reviewed SOC operating coverage.
2. Evaluated analyst staffing.
3. Reviewed monitoring technology.
4. Sampled alert investigations.
5. Evaluated escalation procedures.
6. Reviewed operational performance metrics.

### Evidence

* SOC Operating Procedure
* Staffing Schedule
* SIEM Dashboard
* Alert Investigations
* Escalation Matrix
* Monthly SOC Metrics

### Result

**Satisfied**

### Observation

The SOC operated as the focal point for cybersecurity monitoring and initial incident response.

The SOC maintained centralized visibility, documented escalation paths, and access to incident handling resources.

---

# 15. Test Summary

| Test ID | Control Area                | Result              |
| ------- | --------------------------- | ------------------- |
| IR4-01  | Incident preparation        | Satisfied           |
| IR4-02  | Detection and analysis      | Satisfied           |
| IR4-03  | Containment                 | Satisfied           |
| IR4-04  | Eradication                 | Satisfied           |
| IR4-05  | Recovery                    | Partially Satisfied |
| IR4-06  | Continuity coordination     | Satisfied           |
| IR4-07  | Lessons learned             | Partially Satisfied |
| IR4-08  | Organizational consistency  | Satisfied           |
| IR4-09  | Automated incident handling | Satisfied           |
| IR4-10  | Dynamic reconfiguration     | Satisfied           |
| IR4-11  | Information correlation     | Satisfied           |
| IR4-12  | Automatic isolation         | Satisfied           |
| IR4-13  | Integrated response team    | Satisfied           |
| IR4-14  | Forensic analysis           | Satisfied           |
| IR4-15  | Security Operations Center  | Satisfied           |

---

# 16. Findings

## F-IR4-001 — Inconsistent Recovery Authorization Criteria

### Condition

The recovery checklist did not explicitly require documented approval from both the incident commander and affected business owner before a restored service was returned to production.

Two earlier exercises showed that infrastructure personnel restored services before formal security approval was recorded.

### Criteria

Recovery activities should confirm that:

* Malicious artifacts have been removed
* Credentials have been secured
* Required vulnerabilities have been addressed
* Restored systems have passed security validation
* Business functionality has been tested
* Authorized personnel approve production restoration

### Cause

The disaster recovery procedure and incident response procedure were developed separately and contained different approval requirements.

### Effect

A system may be returned to production before the organization has reasonable assurance that it is secure and operationally ready.

### Likelihood

Possible

### Impact

Major

### Inherent Risk

High

### Existing Compensating Controls

* Backup integrity testing
* Malware scanning
* Vulnerability scanning
* Business-owner testing
* Incident bridge review
* Post-restoration monitoring

### Residual Risk

Moderate

### Recommendation

1. Establish one recovery authorization standard.
2. Require incident commander approval.
3. Require business-owner approval.
4. Require documented security validation.
5. Define emergency exceptions.
6. Record all approvals in the incident ticket.
7. Require enhanced monitoring after restoration.
8. Test the updated process during the next exercise.

### Proposed Owner

Incident Response Director

### Target Completion

September 30, 2026

---

## F-IR4-002 — Incomplete Tracking and Validation of Lessons-Learned Actions

### Condition

Four of 12 sampled corrective actions were overdue.

Two actions marked complete did not include sufficient evidence demonstrating that the intended improvement had been implemented and tested.

### Criteria

Lessons learned should result in documented and verifiable improvements to:

* Response procedures
* Technical safeguards
* Training
* Exercises
* Detection logic
* Recovery processes
* Governance and oversight

### Cause

Corrective actions were tracked in separate team backlogs instead of a centralized governance process.

### Effect

Known incident response weaknesses may remain unresolved and contribute to repeated control failures.

### Likelihood

Possible

### Impact

Moderate

### Inherent Risk

Moderate

### Existing Compensating Controls

* After-action meetings
* Assigned action owners
* Security governance meetings
* Detection engineering backlog
* Quarterly control reviews

### Residual Risk

Low to Moderate

### Recommendation

1. Establish a centralized corrective action register.
2. Assign one accountable owner to each action.
3. Define due dates and completion criteria.
4. Require evidence before closure.
5. Require independent validation for high-risk actions.
6. Escalate overdue actions to the security risk committee.
7. Link unresolved actions to the enterprise risk register.
8. Report closure performance to executive leadership.

### Proposed Owner

GRC Control Assurance Manager

### Target Completion

August 31, 2026

---

# 17. Root Cause Analysis

## Finding F-IR4-001

### Problem

Recovery approval was not consistently documented.

### Root Cause

Incident response and disaster recovery procedures were maintained by different teams without a shared control owner or unified approval standard.

### Contributing Factors

* Separate policy ownership
* Different ticketing workflows
* No mandatory approval fields
* Emphasis on service restoration speed
* Incomplete exercise evaluation criteria

## Finding F-IR4-002

### Problem

Post-incident improvements were not consistently completed or validated.

### Root Cause

Corrective actions were decentralized and lacked a single governance workflow.

### Contributing Factors

* Multiple team backlogs
* No common evidence standard
* No automated overdue escalation
* Ambiguous closure authority
* Limited independent validation

---

# 18. Risk Summary

| Finding   | Inherent Risk | Residual Risk   | Priority | Treatment |
| --------- | ------------- | --------------- | -------- | --------- |
| F-IR4-001 | High          | Moderate        | High     | Mitigate  |
| F-IR4-002 | Moderate      | Low to Moderate | Medium   | Mitigate  |

No critical-risk deficiencies were identified.

---

# 19. Positive Control Observations

The assessment identified the following strengths:

* Incident roles and responsibilities were documented.
* Severity criteria supported consistent escalation.
* SOC analysts rapidly correlated multiple alert sources.
* Endpoint and identity containment operated effectively.
* Network indicators were blocked promptly.
* Business continuity personnel participated in response decisions.
* Forensic evidence was preserved before remediation.
* Malicious artifacts were analyzed in an isolated environment.
* The integrated response team included technical and business stakeholders.
* Executive situation reports were issued during major incidents.
* Protected backups supported recovery.
* Restored services received heightened monitoring.
* Technical indicators were converted into new detection content.
* Incident handling produced generally consistent results across business units.

---

# 20. Corrective Action Plan

| Action ID   | Corrective Action                                    | Owner                         | Priority | Due Date   | Status      |
| ----------- | ---------------------------------------------------- | ----------------------------- | -------- | ---------- | ----------- |
| CAP-IR4-001 | Establish unified recovery authorization standard    | Incident Response Director    | High     | 2026-08-31 | In Progress |
| CAP-IR4-002 | Add mandatory security and business approval fields  | Service Management Owner      | High     | 2026-09-15 | Planned     |
| CAP-IR4-003 | Update ransomware and recovery playbooks             | Incident Response Lead        | High     | 2026-09-30 | Planned     |
| CAP-IR4-004 | Centralize lessons-learned corrective actions        | GRC Control Assurance Manager | Medium   | 2026-07-31 | In Progress |
| CAP-IR4-005 | Require independent validation for high-risk actions | Internal Control Testing Lead | Medium   | 2026-08-31 | Planned     |
| CAP-IR4-006 | Retest recovery and action closure processes         | GRC Assessment Team           | Medium   | 2026-10-15 | Not Started |

---

# 21. Management Response

Management agreed with both findings.

The Incident Response and Disaster Recovery functions will establish a unified production-restoration process requiring documented security and business approval.

The service management platform will be updated to prevent closure of recovery tasks until required evidence and approvals are attached.

The GRC function will create a centralized corrective action register for lessons-learned items. High-risk actions will require independent validation before closure.

Management accepted the temporary residual risk while remediation activities are completed.

---

# 22. Assessor Conclusion

Based on the documentation examined, personnel interviewed, incident records sampled, technical safeguards tested, and ransomware exercise observed, the organization substantially implemented NIST SP 800-53 IR-4 and the selected enhancements.

The following capabilities operated effectively:

* Preparation
* Detection and analysis
* Containment
* Eradication
* Automated response
* Dynamic reconfiguration
* Information correlation
* Integrated team activation
* Forensic analysis
* SOC coordination
* Continuity integration

The control was not rated fully satisfied because:

1. Recovery authorization requirements were not consistently documented.
2. Lessons-learned corrective actions were not consistently validated and closed.

## Final Determination

**Control Status:** Partially Satisfied
**Design Effectiveness:** Effective
**Operating Effectiveness:** Partially Effective
**Residual Risk:** Moderate
**Follow-Up Required:** Yes

The organization should complete the corrective action plan and conduct targeted retesting before changing the control determination to fully satisfied.

---

# 23. Follow-Up Validation Plan

The assessor will:

1. Review the unified recovery approval procedure.
2. Inspect required workflow fields.
3. Observe a future recovery exercise.
4. Confirm incident commander and business-owner approval.
5. Review the centralized corrective action register.
6. Sample closed actions for supporting evidence.
7. Verify escalation of overdue actions.
8. Confirm updates to playbooks and training.
9. Review executive reporting metrics.
10. Update the control assessment and risk register.

---

# 24. Incident Response Metrics and Key Risk Indicators

| Metric or KRI                                                    | Purpose                            |
| ---------------------------------------------------------------- | ---------------------------------- |
| Mean time to acknowledge                                         | Measures SOC responsiveness        |
| Mean time to contain                                             | Measures ability to limit impact   |
| Mean time to eradicate                                           | Measures remediation efficiency    |
| Mean time to recover                                             | Measures restoration capability    |
| Percentage of incidents classified correctly                     | Measures process consistency       |
| Percentage of critical incidents meeting escalation targets      | Measures governance performance    |
| Percentage of restored systems with documented approval          | Measures recovery assurance        |
| Percentage of incidents with completed root cause analysis       | Measures investigative maturity    |
| Percentage of lessons-learned actions completed on time          | Measures continuous improvement    |
| Number of repeat incidents caused by known issues                | Measures remediation effectiveness |
| Percentage of evidence collections with complete custody records | Measures forensic integrity        |
| Number of unresolved high-risk corrective actions                | Measures residual exposure         |

---

# 25. Internal Maturity Evaluation

| Capability                       |  Rating |
| -------------------------------- | ------: |
| Preparation                      | 4.0 / 5 |
| Detection and Analysis           | 4.2 / 5 |
| Containment                      | 4.3 / 5 |
| Eradication                      | 4.0 / 5 |
| Recovery Governance              | 3.2 / 5 |
| Forensic Capability              | 4.0 / 5 |
| Business Continuity Coordination | 3.8 / 5 |
| Lessons Learned                  | 3.0 / 5 |
| Executive Coordination           | 4.0 / 5 |
| Overall Maturity                 | 3.8 / 5 |

### Maturity Interpretation

The organization maintains a defined and operational incident handling capability with meaningful automation and cross-functional coordination.

Continued maturity depends on strengthening recovery authorization, corrective action governance, evidence validation, and executive oversight of unresolved improvements.

---

# 26. Cross-Framework Alignment

| Framework                      | Related Area                                            |
| ------------------------------ | ------------------------------------------------------- |
| NIST SP 800-53 Rev. 5          | IR-4 and selected enhancements                          |
| NIST Cybersecurity Framework   | Incident management, response, mitigation, and recovery |
| ISO/IEC 27001                  | Information security incident management                |
| CIS Controls                   | Incident Response Management                            |
| MITRE ATT&CK                   | Threat-informed analysis and defensive response         |
| Business Continuity Management | Continuity and restoration coordination                 |

Cross-framework mappings should be validated against the organization’s selected framework versions, scope, risk profile, implementation statements, and regulatory requirements.

---

# 27. Authoritative References

* NIST SP 800-53 Revision 5 — Security and Privacy Controls for Information Systems and Organizations
* NIST SP 800-53A Revision 5 — Assessing Security and Privacy Controls in Information Systems and Organizations
* Organization Incident Response Policy
* Organization Incident Response Plan
* Organization Business Continuity Plan
* Organization Disaster Recovery Plan
* Organization Evidence Handling Standard

---

# 28. Portfolio Skills Demonstrated

* NIST incident response control interpretation
* Incident handling assessment
* Ransomware response governance
* Security control testing
* Evidence request development
* Risk-based sampling
* SOC oversight
* SIEM and EDR control validation
* Incident classification
* Containment and eradication review
* Digital forensic governance
* Business continuity coordination
* Recovery control assessment
* Root cause analysis
* Lessons-learned governance
* Corrective action planning
* Risk-rating methodology
* Executive incident reporting
* Control maturity analysis
* Cross-functional security leadership
