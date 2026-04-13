# Glossary — Manage Security Risks (Course 2)

Terms are listed **A–Z** by entry title (includes **Course 2, Module 3** additions). Earlier entries are updated only where the module wording **adds** clarity.

---

### Administrative controls

**People- and process-based** safeguards such as **separation of duties**, **authorization** rules, and **asset classification**.

---

### Antivirus software

A **technical control**: software used to **prevent**, **detect**, and remove **malware** (often grouped with anti-malware).

---

### Assess

The **fifth** step of the **NIST RMF**: determine whether established controls are implemented **correctly**.

---

### Asset

An item perceived as having **value** to an organization.

---

### Asset classification

An **administrative control**: labeling assets by **sensitivity** or **criticality** so **protections** match **risk**.

---

### Attack surface

All **potential** weaknesses or **exposures** a threat actor could try to exploit (**minimize** attack surface where possible).

---

### Attack vectors

The **pathways** attackers use to **penetrate** security defenses.

---

### Audit checklist

A structured list used **before** and during an audit: **scope**, **risk assessment**, **conduct**, **mitigation plan**, **stakeholder** reporting.

---

### Authentication

The process of **verifying who someone is** (proving identity).

---

### Authorization (administrative control)

The concept of **granting access** to **specific resources** in a system (and defining **who** may do **what** under **policy**). Distinct from **authentication** (proving identity) and from the RMF step **Authorize** (organizational sign-off on **residual risk**).

---

### Authorize

The **sixth** step of the **NIST RMF**: being **accountable** for security and privacy **risks** that may still exist in the organization.

---

### Availability

The idea that **authorized** users can **access** data when needed (one pillar of the **CIA triad**).

---

### Avoid security by obscurity (OWASP principle)

Do **not** rely on **secrecy** alone (hidden code, obscure URLs) for safety; use **defense in depth**, strong policies, architecture, and monitoring.

---

### Biometrics

**Unique physical characteristics** used to **verify** a person’s identity.

---

### Business continuity

An organization’s ability to maintain **everyday productivity** by establishing **disaster recovery** and related **risk** plans.

---

### Categorize

The **second** step of the **NIST RMF**: used to develop risk management **processes and tasks** (often tied to impact categories).

---

### Chronicle (Google SecOps SIEM)

A **cloud-native** tool designed to **retain**, **analyze**, and **search** data (in practice, security **log** and **event** data). Google’s **SecOps** SIEM offering for **threats**, **risks**, and **vulnerabilities**; includes dashboards for **IOCs**, **ingestion health**, **detections**, and **user sign-ins**.

---

### Confidentiality

The idea that only **authorized** users can access specific **assets** or **data** (CIA triad).

---

### Confidentiality, integrity, availability (CIA) triad

A model that helps inform how organizations consider **risk** when setting up **systems** and **security policies**.

---

### Corrective control

A control that **restores** an asset or environment **after** an incident (e.g., **backups**, some **AV** responses).

---

### Cryptography

Techniques to **protect** data (e.g., **confidentiality** and **integrity**) so **unauthorized** parties cannot easily **read** or **tamper** with it.

---

### Cyber Threat Framework (CTF)

A U.S. government framework that provides a **common language** to **describe** and **communicate** **cyber threat activity** (ODNI).

---

### Defense in depth

Layer **multiple** **different** controls so a single failure does not eliminate protection.

---

### Detect (NIST Cybersecurity Framework core function)

Related to **finding** potential security **incidents** and improving **monitoring** so detections are **faster** and more **efficient**.

---

### Detective control

A control used to **determine** whether an incident **occurred** or is **in progress** (e.g., **IDS**, **logging**, **CCTV** review).

---

### Deterrent control

A control meant to **discourage** attacks by increasing perceived **risk** or **effort** (e.g., signage, lighting).

---

### Encryption

The process of converting data from a **readable** format to an **encoded** format.

---

### Establish secure defaults (OWASP principle)

The **most secure** configuration should be the **default**; weakening security should require **explicit** action.

---

### External threat

Anything **outside** the organization that has the potential to **harm** organizational assets.

---

### Fail securely (principle)

When a control **fails**, it should default to the **safest** state (e.g., **firewall** **denies** traffic if it cannot enforce policy).

---

### Firewall

A **technical control** that **filters** network traffic according to **policy**.

---

### Firewall log

A record of **attempted** or **established** connections for **incoming** traffic from the internet and **outbound** requests from the network to the internet.

---

### Fix security issues correctly (OWASP principle)

After incidents: find **root cause**, **contain**, identify **vulnerabilities**, and **verify** remediation with **testing**.

---

### Govern (NIST Cybersecurity Framework core function)

Ensures the organization **establishes**, **oversees**, and **improves** cybersecurity **strategy**, **policies**, **roles**, and **risk management** so they align with **business goals** and **regulations**.

---

### Identify (NIST Cybersecurity Framework core function)

Related to **managing** cybersecurity **risk** and its effect on the organization’s **people** and **assets**.

---

### Implement

The **fourth** step of the **NIST RMF**: implement security and privacy **plans** for the organization.

---

### Incident response

An organization’s **rapid** effort to **identify** an attack, **contain** damage, and **correct** the effects of a **security breach**.

---

### Indicators of compromise (IOCs)

Observable artifacts—such as **suspicious domain names** or **known-bad** **IP addresses**—that suggest a **threat** or intrusion; often surfaced on SIEM dashboards (e.g., Chronicle **enterprise insights**).

---

### Integrity

The idea that data is **correct**, **authentic**, and **reliable** (CIA triad); often supported by **cryptography** and **encryption**.

---

### Internal threat

A **current or former** employee, **external vendor**, or **trusted partner** who poses a security risk.

---

### ISO/IEC 27001

International standard specifying requirements for an **information security management system (ISMS)** and related **controls** and practices (**ISO/IEC 27000** family).

---

### Keep security simple (OWASP principle)

Avoid **unnecessary** complexity—complex systems are harder to secure and operate safely.

---

### Least privilege

Principle of granting only the **minimum** access and permissions needed to complete a **task**—supports **confidentiality**.

---

### Linux

An **open-source** **operating system** (interface between **hardware** and **user**); widely customized via a **command-line interface**.

---

### Log

A **record of events** that occur within an organization’s **systems** (and, in practice, often **networks** and **services**).

---

### Managed detection and response (MDR)

A **vendor-delivered** service that **monitors** environments and helps **detect** and **respond** to threats; **SOAR** may automate tasks triggered by **SIEM** or **MDR** tooling.

---

### Metrics

**Key technical attributes**—such as **response time**, **availability**, and **failure rate**—used to judge **performance** of a **software** application or system.

---

### Monitor

The **seventh** step of the **NIST RMF**: stay **aware** of how systems are **operating** and whether risk posture changes.

---

### Multi-factor authentication (MFA)

A **technical control** requiring **two or more** factors to **verify identity** before access (e.g., patient portal, remote access).

---

### National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF)

A **voluntary** framework of **standards**, **guidelines**, and **best practices** to manage **cybersecurity risk**. **CSF 2.0** adds **Govern** and organizes **six** core functions; it also emphasizes **supply chain** risk. See individual entries for **Govern**, **Identify**, **Protect**, **Detect**, **Respond**, and **Recover**.

---

### National Institute of Standards and Technology (NIST) Special Publication (SP) 800-53

A **unified** catalog of **controls** for protecting **federal information systems** (widely referenced outside government as well).

---

### Network log

A record of **computers and devices** that **enter and leave** the network, and of **connections** between **devices** and **services** on the network.

---

### Open Information Security Foundation (OISF)

Nonprofit that stewards **Suricata** and promotes **open-source** network security tooling.

---

### Open Worldwide Application Security Project (OWASP)

A nonprofit (formerly *Open Web Application Security Project*) focused on **improving software security**.

---

### Open-source tools

Software whose **source code** is **public** and developed **collaboratively**, typically under a **license**; users may **inspect**, **modify**, and **extend** it—often **free** to use.

---

### Operating system (OS)

The **interface** between **computer hardware** and the **user**; manages hardware and **applications** (e.g., **Linux**, **Windows**, **macOS**).

---

### Physical controls

**Facility- and hardware-oriented** safeguards: **gates/fences/locks**, **guards**, **CCTV** and **motion detectors**, **badges** / **access cards**, etc.

---

### Playbook

A **manual** that documents **operational actions**—especially **predefined**, **current** steps for **incident** or **vulnerability** response, **roles**, and **expectations**; often a **living document** updated for **failures**, **regulations**, and new **threats**. Sometimes called a **runbook**.

---

### Prepare

The **first** step of the **NIST RMF**: activities necessary to manage security and privacy risks **before** a breach occurs.

---

### Preventative control

A control designed to **stop** an incident **before** it occurs (e.g., **firewall**, **least privilege** policies).

---

### Proprietary tools

Software **owned** by a **vendor**; **source code** is **not** customer-modifiable; usage and **updates** are usually **paid** and **vendor-controlled** (e.g., **Splunk**, **Chronicle**).

---

### Protect (NIST Cybersecurity Framework core function)

Used to **protect** the organization through **policies**, **procedures**, **training**, and **tools** that help **mitigate** cybersecurity threats.

---

### Ransomware

A malicious attack where threat actors **encrypt** an organization’s data and **demand payment** to restore access.

---

### Recover (NIST Cybersecurity Framework core function)

Related to **returning** affected **systems** to **normal operation** after disruption.

---

### Respond (NIST Cybersecurity Framework core function)

Ensures **proper procedures** to **contain**, **neutralize**, and **analyze** security incidents and to **improve** the security process afterward.

---

### Risk

Anything that can impact the **confidentiality**, **integrity**, or **availability** of an asset.

---

### Risk mitigation

Having the right **procedures and rules** in place to **quickly reduce** the impact of a risk such as a **breach**.

---

### Runbook

A term often used interchangeably with **playbook**: **step-by-step** operational guidance for **incidents** or **tasks**.

---

### SIEM tools (software platform)

A **software platform** that **collects**, **analyzes**, and **correlates** security data from **many** sources across **IT** infrastructure to **identify** and **respond** to threats **in real time**, **investigate** incidents, and support **compliance** (see also **Security information and event management (SIEM)**).

---

### Security audit

A review of an organization’s **security controls**, **policies**, and **procedures** against a set of **expectations**.

---

### Security controls

Safeguards designed to reduce **specific** security risks.

---

### Security frameworks

Guidelines used for building plans to help **mitigate** risk and threats to **data** and **privacy**.

---

### Security information and event management (SIEM)

An application that **collects** and **analyzes** **log data** to monitor **critical** activities in an organization; typically also provides **real-time** visibility, **centralized** storage, and **alerts**—with **human** analysis still central in many programs.

---

### Security operations center (SOC)

A team and operating model focused on **monitoring**, **detecting**, **analyzing**, and **responding** to security events—often using **SIEM** dashboards (e.g., **security posture** views).

---

### Security orchestration, automation, and response (SOAR)

A collection of **applications**, **tools**, and **workflows** that use **automation** to respond to security **events**—often fed by **SIEM** or **managed detection and response (MDR)**—so repetitive tasks (e.g., **account lockout** after failed logins) run without waiting on an analyst.

---

### Security posture

An organization’s ability to manage its **defense** of critical assets and data and **react to change**.

---

### Security principles

Guiding ideas (e.g., **OWASP** principles such as **least privilege**, **defense in depth**, **fail securely**) applied in daily security work.

---

### Select

The **third** step of the **NIST RMF**: **choose**, **customize**, and **capture documentation** of the controls that protect an organization.

---

### Separation of duties

An **administrative control** that **splits** responsibilities so **no single person** can abuse a process end-to-end.

---

### Server log

A record of events related to **services** such as **websites**, **email**, or **file shares**—including **login**, **password**, and **username** requests.

---

### Shared responsibility

The idea that **all individuals** within an organization take an active role in **lowering risk** and maintaining **physical and virtual** security.

---

### Social engineering

A manipulation technique that exploits **human error** to gain private information, access, or valuables.

---

### Splunk® Cloud

A **cloud-hosted** tool used to **collect**, **search**, and **monitor** **log data** as part of the Splunk **SIEM** platform.

---

### Splunk® Enterprise

A **self-hosted** tool used to **retain**, **analyze**, and **search** an organization’s **log data** to deliver **security** insight and **alerts** in **real time** (Splunk **SIEM** deployment you operate).

---

### Suricata

**Open-source** **network analysis** and **threat detection** engine that inspects traffic, finds suspicious behavior, and generates **logs**; integrates with many **SIEM** tools (**OISF** project).

---

### Technical controls

**Technology-based** safeguards such as **firewalls**, **MFA**, and **antivirus** software.

---

### Third-party trust (OWASP: don’t trust services)

Do **not assume** vendors’ or partners’ systems are secure; **verify** data and controls (e.g., **reward** balances before showing customers).

---

### Threat

Any circumstance or event that can **negatively impact** assets.

---

### Vulnerability

A **weakness** that can be **exploited** by a threat.

---

### Vulnerability scanner

A tool used to **discover** known or common **misconfigurations** and **vulnerabilities** in systems and applications.
