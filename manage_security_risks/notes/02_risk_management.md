# Risk management — assets, strategies, and frameworks

## Protecting assets

A primary organizational goal is to **protect assets**.

### Asset

An **asset** is anything that has **value** to the organization. Assets can be **digital** or **physical**.

### Digital asset examples

Personal or sensitive data about **employees**, **clients**, or **vendors**, such as:

- **Social Security numbers (SSNs)** or other **national ID** numbers  
- **Dates of birth**  
- **Bank account numbers**  
- **Mailing addresses**

### Physical asset examples

- **Payment kiosks**  
- **Servers**  
- **Desktop computers**  
- **Office spaces**

---

## Risk management strategies

Organizations commonly treat risk using:

| Strategy | Meaning |
|----------|---------|
| **Acceptance** | Accept a risk (documented) to **avoid disrupting** business continuity when cost or impact trade-offs warrant it |
| **Avoidance** | **Change plans or scope** so the risk does not apply |
| **Transference** | Shift financial or operational burden (e.g., **insurance**, **vendor** contracts) to a **third party** |
| **Mitigation** | **Reduce likelihood or impact** (controls, patches, monitoring) |

---

## Frameworks

Risk management is often structured using **widely accepted frameworks** so policies and processes protect **digital and physical** assets from **threats**, **risks**, and **vulnerabilities**.

**Examples called out in the course:**

- **NIST Risk Management Framework (NIST RMF)**  
- **HITRUST** (Health Information Trust Alliance)

### NIST Cybersecurity Framework (CSF) — how it fits

**NIST CSF** is a separate, **voluntary** product from NIST: **standards**, **guidelines**, and **best practices** focused on **cybersecurity risk** (outcomes and core functions), not the same as the **RMF** stepwise process below.

**Update (CSF 2.0):** Adds a **Govern** function; **six** core functions (**Govern**, **Identify**, **Protect**, **Detect**, **Respond**, **Recover**); stronger emphasis on **supply chain** risk. Full detail: [04_frameworks_controls_and_cia_triad.md](04_frameworks_controls_and_cia_triad.md).

---

## NIST RMF — seven steps (overview)

The RMF orders security and privacy work from preparation through ongoing monitoring:

| Step | Term (Module 1) | Role |
|------|-----------------|------|
| 1 | **Prepare** | Activities needed to manage security and privacy risks **before** a breach |
| 2 | **Categorize** | Develop risk management **processes and tasks** based on impact |
| 3 | **Select** | Choose, customize, and **document** controls that protect the organization |
| 4 | **Implement** | Put security and privacy **plans** into practice |
| 5 | **Assess** | Determine whether controls are implemented **correctly** |
| 6 | **Authorize** | **Accountability** for remaining security and privacy **risks** |
| 7 | **Monitor** | **Ongoing awareness** of how systems operate and whether risk changes |

Full definitions: [../glossary/GLOSSARY.md](../glossary/GLOSSARY.md).

---

## How this ties to domains and posture

- **Security posture** depends on **governance**, **architecture**, **operations**, and **assurance** working together—not a single tool.  
- **Shared responsibility** (Domain 3) and **least privilege** (Domain 5) reduce **blast radius** when something goes wrong.  
- **Vulnerability management** and **patching** (often spanning Domains 2, 6, and 7) directly support **mitigation**.

---

## Key takeaway

Risk management connects **business value** (assets) to **choices** (accept, avoid, transfer, mitigate) and **repeatable processes** (frameworks like **NIST RMF**). Analysts help **identify gaps**, **evidence controls**, and **track** whether mitigations actually run in production.
