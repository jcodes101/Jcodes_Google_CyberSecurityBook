# NIST Incident Response Lifecycle, teams, and detection tools

Incident response (IR) is the structured process organizations use to prepare for, detect, contain, and learn from security incidents. This note covers the **NIST Incident Response Lifecycle**, common IR team structures (**CSIRT** and **SOC**), and core detection tooling (**IDS/IPS/EDR/SIEM**).

---

## NIST Incident Response Lifecycle (4 phases)

NIST describes incident response as a continuous lifecycle with four phases:

### 1) Preparation

Build readiness to respond effectively.

Common outcomes:
- clear roles and escalation paths
- documented playbooks/runbooks
- logging, monitoring, and alerting in place
- communication plans and stakeholder lists

### 2) Detection and Analysis

Identify potential incidents and determine what’s actually happening.

Typical work:
- monitor and triage alerts
- validate whether activity is malicious
- scope affected users/systems/data
- prioritize based on severity, impact, and business context

### 3) Containment, Eradication, and Recovery

Stop the incident from getting worse, remove the cause, and restore operations.

Typical work:
- isolate affected hosts/accounts
- block malicious IPs/domains/processes
- patch vulnerabilities / rotate credentials
- restore from clean backups and confirm normal operations

### 4) Post-incident activity

Learn and improve so the same incident is less likely (and less impactful) next time.

Typical work:
- lessons learned / postmortem
- update detections, playbooks, controls
- identify process gaps and training needs
- track remediation to completion

---

## Incident response teams: CSIRT and SOC

As a security professional, you’ll work with teams that **monitor, detect, and respond** to incidents. Two common structures are **CSIRTs** and **SOCs**.

### Command, control, and communication (CSIRT fundamentals)

Effective incident response requires:

- **Command**: leadership and direction to oversee the response
- **Control**: coordination of technical work (resources, tasking, sequencing)
- **Communication**: keeping stakeholders informed with clear status updates

Establishing a CSIRT structure with clear roles helps a response stay efficient and aligned.

---

## Roles in CSIRTs

CSIRTs vary by organization. They may be a dedicated team or an on-demand task force. They often include both:

- **Security professionals** (core IR roles)
- **Nonsecurity professionals** who contribute expertise during incidents (e.g., HR, PR, management, IT, legal)

Three common security roles in a CSIRT are:

### Security analyst

Continuously monitors the environment for threats and handles early IR work:
- analyzing and triaging alerts
- performing root-cause investigations
- escalating or resolving alerts

If a critical threat is identified, analysts escalate to appropriate leadership (often the technical lead).

### Technical lead

Owns the technical execution of response:
- determines root cause
- designs and implements containment, eradication, and recovery strategies
- coordinates technical changes (patches, updates, tooling changes)

Technical leads often collaborate with other teams to balance security priorities with business priorities (like minimizing customer disruption).

### Incident coordinator

Owns cross-team coordination and keeps communication flowing:
- coordinates with relevant departments during incidents
- ensures updates are clear and consistent
- maintains situational awareness across stakeholders

Other titles for this role include **incident commander** and **incident manager**.

### Other CSIRT roles (examples)

Depending on the organization, you might also see:
- communications lead
- legal lead
- planning lead
- additional specialists (forensics, malware analysis, etc.)

---

## Security operations center (SOC)

A **security operations center (SOC)** is an organizational unit dedicated to monitoring networks, systems, and devices for threats. A SOC may exist as its own unit or within a CSIRT. SOC work maps to “blue team” defensive activities: monitoring, analysis, and incident response.

### SOC organization (tiers)

SOC analysts are often organized into tiers, with increasing experience and responsibility:

#### Tier 1 SOC analyst (L1)

Typically the least experienced; focuses on intake and triage:
- monitoring/reviewing/prioritizing alerts based on severity
- creating and closing alerts in ticketing systems
- escalating alert tickets to Tier 2 or Tier 3

#### Tier 2 SOC analyst (L2)

Handles deeper investigation and tool refinement:
- receives escalations from L1 and investigates further
- configures/refines security tools
- reports to the SOC lead

#### Tier 3 SOC lead (L3)

Highly experienced; runs operations and advanced detection:
- manages team operations
- performs advanced detection techniques (e.g., malware/forensics analysis)
- reports to the SOC manager

#### SOC manager

Leads the SOC program:
- hires, trains, evaluates SOC team members
- defines metrics and manages performance
- develops incident/compliance/audit reporting
- communicates findings to stakeholders (including executive management)

### Other SOC roles (examples)

- **Forensic investigators**: commonly L2/L3; collect, preserve, and analyze digital evidence to determine what happened
- **Threat hunters**: typically L3; proactively detect and investigate advanced threats using threat intelligence

---

## Why you need detection tools

Detection tools are like a home security system: they continuously monitor activity and generate alerts when something suspicious happens. Without detection, organizations may not realize an intrusion is occurring until after damage is done.

---

## Detection tools: IDS vs IPS vs EDR

You’ll commonly encounter three detection tool categories:

### IDS (Intrusion Detection System)

An **IDS** monitors system/network activity and **alerts** on possible intrusions.

Key point: an IDS **detects** and **alerts**, but typically does **not** block activity.

Example: alert on a suspicious login (unknown IP, unusual time), but no automatic block.

Examples: **Zeek**, **Suricata**, **Snort**, **Sagan**.

### Detection categories (alert outcomes)

When evaluating alerts, four outcomes matter:

- **True positive**: correctly detects an actual attack
- **True negative**: correctly shows no malicious activity (no alert when nothing is wrong)
- **False positive**: incorrectly flags benign activity as malicious (wastes time/resources)
- **False negative**: fails to detect real malicious activity (dangerous; defenders stay unaware)

### IPS (Intrusion Prevention System)

An **IPS** monitors activity and can **take action to stop** intrusive behavior.

Example: generate an alert and modify an ACL (access control list) on a router to block traffic.

Note: some tools can run in IDS and IPS modes (e.g., **Suricata**, **Snort**, **Sagan**).

### EDR (Endpoint Detection and Response)

An **EDR** monitors endpoints (devices on a network), records and analyzes endpoint activity, and can alert and respond.

Distinctive capabilities:
- collects endpoint telemetry and performs deeper analysis
- can perform **behavioral analysis** (often ML/AI-assisted) to identify unusual patterns
- can use automation to stop attacks without manual intervention

Example: if an unusual process starts on a workstation, the EDR can automatically block it.

Examples: **Open EDR**, **Bitdefender Endpoint Detection and Response**, **FortiEDR**.

---

## SIEM advantages and how SIEM works

**Security information and event management (SIEM)** tools collect and manage security-relevant data that helps investigators understand what’s happening across an environment.

### SIEM advantages

- **Access to event data**: central access to logs and activity data (including near real-time)
- **Monitoring, detecting, and alerting**: applies detection rules to ingested data and generates alerts
- **Log storage**: provides retention for historical investigation and compliance needs

### The SIEM process (3 steps)

#### 1) Collect and aggregate data

SIEMs ingest logs from many sources (firewalls, servers, routers, applications, endpoints) and consolidate them centrally.

Parsing may happen here. Parsing maps raw log text into fields and values.

Example raw log:

April 3 11:01:21 server sshd[1088]: Failed password for user nuhara from 218.124.14.105 port 5023

Example parsed fields:
- host = server
- process = sshd
- source_user = nuhara
- source_ip = 218.124.14.105
- source_port = 5023

#### 2) Normalize data

Different sources format logs differently. Normalization converts collected data into a consistent structured format so it can be searched and analyzed uniformly.

#### 3) Analyze data

SIEMs apply detection logic (rules/conditions) to normalized data and generate alerts when patterns match.

Correlation is often part of this step: comparing multiple events to identify patterns that indicate threats.

### Common SIEM tools (examples)

- AlienVault OSSIM
- Chronicle
- Elastic
- Exabeam
- IBM QRadar Security Intelligence Platform
- LogRhythm
- Splunk

---

## Key takeaways

- The **NIST IR Lifecycle** has four phases: **Preparation**, **Detection and Analysis**, **Containment/Eradication/Recovery**, and **Post-incident activity**.
- **CSIRTs** emphasize clear **command**, **control**, and **communication**, and commonly include **security** and **nonsecurity** stakeholders.
- Common CSIRT roles include **security analyst**, **technical lead**, and **incident coordinator** (incident manager/commander).
- SOCs are often tiered (**L1/L2/L3**) with a **SOC manager**; specialized roles can include **forensics** and **threat hunting**.
- **IDS** detects and alerts; **IPS** can prevent/block; **EDR** focuses on endpoints and can perform behavioral analysis and automated response.
- SIEMs help defenders by centralizing logs and enabling **collection/aggregation**, **normalization**, and **analysis/correlation** to generate actionable alerts.

