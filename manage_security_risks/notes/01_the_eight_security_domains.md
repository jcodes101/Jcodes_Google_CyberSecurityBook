# The eight security domains (CISSP model)

These domains describe **focus areas** security programs use to organize work. Together they help organizations **build and maintain security posture**—the ability to **defend critical assets and data** and **adapt to change**.

---

## Domain 1 — Security and risk management

### Purpose

Set direction for the security program: **goals**, **risk treatment**, **compliance**, **resilience**, **law**, and **ethics**—all of which shape **security posture**.

### What it covers

Elements that impact posture include:

- **Security goals and objectives**  
- **Risk mitigation processes**  
- **Compliance**  
- **Business continuity plans**  
- **Legal regulations**  
- **Professional and organizational ethics**

### Information security (InfoSec)

**InfoSec** is the set of **processes** established to **secure information**. Organizations tailor programs using **playbooks**, **training**, and other controls based on **needs** and **perceived risk**.

Common **InfoSec design / process areas** include:

- **Incident response**  
- **Vulnerability management**  
- **Application security**  
- **Cloud security**  
- **Infrastructure security**

### Example

A security team changes how **personally identifiable information (PII)** is handled so the organization can meet the **EU General Data Protection Regulation (GDPR)**.

---

## Domain 2 — Asset security

### Purpose

Manage cybersecurity for **organizational assets** across the **lifecycle** of data and systems—especially **storage**, **maintenance**, **retention**, and **destruction** of **physical and virtual** data.

### Why it matters

Loss or theft of assets can **expose** the organization and **raise risk**. Tracking **what** you have and **what data** it holds is essential.

### Typical activities

Activities depend on **risk** per asset and may include:

- **Security impact analysis**  
- **Recovery planning**  
- **Managing data exposure**  
- **Backups** so the environment can be **restored** after an incident

### Example

Analysts **store**, **maintain**, and **retain** data with backups so operations can recover if an incident puts data at risk.

---

## Domain 3 — Security architecture and engineering

### Purpose

**Protect data** by ensuring the right **tools**, **systems**, and **processes** exist. **Security architects** and **engineers** design and build these protections.

### Shared responsibility

**Shared responsibility** means **everyone involved** takes an active role in **lowering risk** while a security system is designed and operated—not only the security team.

### Design principles (introduced here; explored later in the program)

- **Threat modeling**  
- **Least privilege**  
- **Defense in depth**  
- **Fail securely**  
- **Separation of duties**  
- **Keep it simple**  
- **Zero trust**  
- **Trust but verify**

### Example

Using a **security information and event management (SIEM)** tool to watch for **flags** tied to **unusual login or user activity** that might mean a **threat actor** is trying to reach **private data**.

---

## Domain 4 — Communication and network security

### Purpose

**Manage and secure** physical networks and **wireless** communications—including **on-site**, **remote**, and **cloud** paths.

### Practical challenge

Hybrid and remote work means data must stay protected while **external connections** (travel, home, coffee shop) make “**secure access to the corporate network**” harder.

### Typical controls

**Network security controls**—for example **restricted network access**—help protect users and keep the organization’s network safer when people work **outside** the main office.

---

## Domain 5 — Identity and access management (IAM)

### Purpose

Keep data safe by making sure **identities are trusted and authenticated** and that **access** to **physical and logical** assets is **authorized**—blocking **unauthorized** users while **authorized** users can work.

### Core idea: least privilege

**Least privilege** means granting only the **minimum access and permissions** needed to **complete a task**—no more.

### Example

Ensure **customer service** can **view** a customer’s private data (e.g., phone number) **only while** resolving the ticket, then **remove** that access when the case is closed.

---

## Domain 6 — Security assessment and testing

### Purpose

**Find and reduce** **risks**, **threats**, and **vulnerabilities**. Assessments show whether internal systems are **secure** or **at risk**.

### Typical work

- **Security control testing**  
- **Collecting and analyzing** security-relevant data  
- **Security audits** to **lower** breach probability  
- **Penetration testing** (“**pen testers**”) to find weaknesses a **threat actor** could abuse

### Example

**Auditing user permissions** to confirm people have the **correct** level of access to **internal systems**—not too much, not too little for their role.

---

## Domain 7 — Security operations

### Purpose

**Investigate** possible breaches and **implement preventive** and **responsive** measures **after** (and around) security incidents—day-to-day **defense** and **response**.

### Strategies, processes, and tools

- **Training and awareness**  
- **Reporting and documentation**  
- **Intrusion detection and prevention**  
- **SIEM tools**  
- **Log management**  
- **Incident management**  
- **Playbooks**  
- **Post-breach forensics**  
- **Lessons learned**

### Team role

Staff in this domain work as a **team** to **manage**, **prevent**, and **investigate** threats, risks, and vulnerabilities. They handle **active attacks**—for example **large data access** from the **internal network** **outside normal hours**—and work to keep **private data** away from **threat actors**.

---

## Domain 8 — Software development security

### Purpose

Use **secure programming practices** and **guidelines** so **applications** are **secure**, supporting **reliable services** for the organization and its users.

### Lifecycle rule

Security belongs in **every phase** of the **software development life cycle (SDLC)**—**design**, **development**, **testing**, and **release**. Security **cannot** be only a late add-on.

### Testing and quality

- **Application security testing** to find and **fix** vulnerabilities  
- Checks on **programming conventions**, **executables**, and **embedded security controls**  
- **Quality assurance** and **pen testers** help verify **security** and **performance**

### Example

An analyst at a **pharmaceutical** company verifies **encryption** is configured correctly on a new **medical device** that will store **private patient data**.

---

## Key takeaway

Knowing **which domain** a problem belongs to helps you **communicate**, **prioritize**, and **study**—whether the topic is policy (Domain 1), assets (2), engineering (3), networks (4), IAM (5), testing (6), operations (7), or secure development (8).
