# CIA triad, controls, frameworks, and compliance

## How controls, frameworks, and compliance fit together

### Confidentiality, integrity, availability (CIA) triad

A **model** for thinking about **risk** when designing systems and security policies.

| Pillar | Meaning |
|--------|---------|
| **Availability** | **Authorized** users can access data when needed. |
| **Confidentiality** | Only **authorized** users access specific assets or data. |
| **Integrity** | Data is **accurate**, authentic, and reliable. |

*Table sorted A–Z; the common mnemonic is still **C**–**I**–**A** (confidentiality, integrity, availability).*

CIA guides which **controls** to choose to reduce **threats, risks, and vulnerabilities**.

### Relationships (one sentence each)

- **Security controls** = safeguards that reduce **specific** risks; chosen and operated in line with frameworks and legal requirements.  
- **Security frameworks** = **guidance** for building security programs and processes.  
- **Compliance** = proving and maintaining adherence to **internal rules** and **external laws/regulations**.

Together they help organizations keep **risk** at an acceptable level.

---

## Security frameworks — four core components

1. **Identify and document** security goals.  
2. **Set guidelines** to reach those goals.  
3. **Implement** strong security processes.  
4. **Monitor** and **communicate** results.

---

## NIST and common frameworks

**National Institute of Standards and Technology (NIST)** — U.S. agency that publishes **voluntary** frameworks organizations worldwide use for risk management. Stronger alignment with compliance generally supports **lower risk**.

**Examples from the course:**

- **NIST Cybersecurity Framework (CSF)** — standards, guidelines, best practices for cybersecurity risk.  
- **NIST Risk Management Framework (RMF)** — structured approach to managing risk (especially in federal/regulated contexts).

Specifications change by **industry and employer**; always confirm which framework your organization adopts.

---

## Regulations and programs (high level)

*Subsections **A–Z** by program / standard name.*

### CIS® (Center for Internet Security)

Nonprofit providing **controls** and practical guidance to defend systems and networks and to respond when incidents occur.

---

### FERC–NERC (Critical Infrastructure Protection)

Applies to organizations tied to **electricity** and the **North American power grid**. Obligations include preparing for, mitigating, and **reporting** incidents that could harm the grid. Must follow **CIP Reliability Standards** under FERC.

---

### FedRAMP® (Federal Risk and Authorization Management Program)

U.S. federal program that **standardizes** security assessment, authorization, and continuous monitoring for **cloud services** used by government and aligns expectations with **cloud providers**.

---

### GDPR (General Data Protection Regulation)

EU law on processing **EU residents’** personal data and **privacy**—applies to processing **inside and outside** the EU when EU data is involved.

**Examples from course:**

- Lack of transparency about **what** data is held and **why** can mean **fines**.  
- After a breach affecting EU citizens, organizations often must notify within **72 hours** (course framing).

---

### HIPAA (Health Insurance Portability and Accountability Act)

U.S. law (1996) protecting **patient health information**; generally **no sharing without consent**. Three rule areas: **Breach notification**, **Privacy**, **Security**.

Organizations holding patient data must **notify patients** of breaches when **PHI** is exposed—identity theft and insurance fraud are real risks.

**PHI:** Information about past, present, or future **health**, **care**, or **payment** for care.

**HITRUST®:** Framework and assurance program that helps organizations **meet HIPAA** and related expectations.

---

### ISO (International Organization for Standardization)

International standards for **technology, manufacturing, management** across borders—helps improve processes (quality, planning, services, etc.). Security teams often encounter **ISO 27001** and related families in the wild (course introduces ISO at a high level).

---

### PCI DSS (Payment Card Industry Data Security Standard)

International standard for organizations that **store, accept, process, or transmit** cardholder data—goal is to reduce **card fraud**.

---

### SOC 1 / SOC 2 (System and Organization Controls)

From **AICPA** auditing standards—reports on controls at a service organization, including **user access** patterns across roles (associate through vendor, etc.). Relevant to **financial compliance** and **risk**; covers confidentiality, privacy, integrity, availability, security, and data safety. Control failures can enable **fraud**.

---

## Professional habit

Many regulations **change**. Analysts should **track updates** and learn adjacent frameworks.

**Suggested further research (from course):**

- Gramm-Leach-Bliley Act  
- Sarbanes-Oxley Act  

---

## Module 3 glossary cross-reference

Terms such as **security architecture**, **security governance**, **security ethics**, **asset**, and expanded **NIST CSF** wording appear in [../glossary/GLOSSARY.md](../glossary/GLOSSARY.md).
