# Playbooks, incident response, and how SIEM / SOAR fit in

Course 2, Module 3 — operational response and tooling context.

---

## Playbook — what it is

A **playbook** is a **manual** that documents **operational actions**. In practice it gives a **predefined**, **up-to-date** list of **steps** to run when responding to an **incident** or **vulnerability**.

Playbooks are often paired with a **strategy** that sets **expectations** for team members and may name **who** is **responsible**. A **plan** then spells out **how** each task must be completed.

### Living documents

Playbooks should be **living documents**: security staff **update** them when:

- A **failure** or **gap** appears (policy, procedure, or the playbook itself).  
- **Industry standards** or **laws** / **compliance** change.  
- The **threat landscape** shifts (**tactics** and **techniques**).

Updates are usually **collaborative** because team members bring **different expertise**.

### Runbook

The course also uses **runbook** as an alternate name for the same idea: **clear actions** for **incidents** or operations.

---

## Types of playbooks

Playbooks may target **specific** incident types—e.g. **ransomware**, **vishing**, **business email compromise (BEC)**—or broader **vulnerability** response.

**Organizations differ** in tools, **methodologies**, **protocols**, and **who** is involved at each step, especially across **countries**. **Notification** rules from **government** and **compliance** frameworks shape playbook **content** and can change with **where** the incident **originated** and **what data** was affected.

---

## Incident and vulnerability response playbooks

Common for **entry-level** roles. They align with goals in the **business continuity plan**—the path to **recover** and **keep operating** after disruption (e.g., a **breach**).

**Why follow steps:**

- Meet **legal** and **organizational** standards.  
- **Reduce mistakes** and ensure critical actions happen **on time**.  
- When **risk** is high (damage to **assets**), **urgency** matters—risk ties to **likelihood** of **threats** materializing.  
- For **forensics**, mishandling data can **ruin** evidence.

---

## Phases in incident / vulnerability playbooks (what each is for)

These phases are the **backbone** many playbooks use (names may vary slightly by framework). Each phase answers a different question in the **lifecycle** of an event.

| Phase | What it is for |
|-------|----------------|
| **1. Preparation** | **Before** anything goes wrong: tools, **training**, **contacts**, **baseline** logging, **playbooks** themselves, and **roles** so the team can act fast when needed. |
| **2. Detection** | **Notice** that something may be wrong: **alerts**, **SIEM** rules, **anomalies**, user reports—turning raw signals into a **suspected** incident or vulnerability to track. |
| **3. Analysis** | **Confirm** and **scope** the issue: what **systems**, **data**, and **users** are involved; **severity**; is it a **true positive**; what **evidence** to preserve. |
| **4. Containment** | **Limit** spread and **damage**: isolate hosts, **block** accounts, segment **network**, revoke **tokens**—short-term “stop the bleeding” while keeping needed **evidence** intact. |
| **5. Eradication** | **Remove** the **root cause**: delete **malware**, close **vulnerabilities**, reset **credentials**, patch **systems** so the attacker cannot **return** the same way. |
| **6. Recovery** | **Restore** normal operations **safely**: rebuild from **known-good** images, validate **backups**, turn services back on **gradually**, **monitor** for **re-infection**. |
| **7. Post-incident activity** | **After** the event: **report** to stakeholders and regulators as required, **lessons learned**, **update** playbooks and controls, **metrics** and **retrospectives** so the next response is **better**. |

**Coordination** across these stages is continuous: legal, IT, communications, and leadership often **parallel** technical work—especially for **notification** and **regulatory** deadlines.

---

## Playbooks and SIEM

Teams use playbooks **during** incidents. A **SIEM** may **flag** unusual behavior (e.g., odd **user** activity); the playbook tells analysts **what to do next** (verify, escalate, contain, etc.).

Playbooks can include **flowcharts** and **tables** so **order** of actions is unambiguous. **Ransomware** and other scenarios often have **dedicated** playbooks (**who** does **what**, **when**).

---

## Playbooks and SOAR

**SOAR** automates **repetitive** work that may be **triggered** by a **SIEM** or **managed detection and response (MDR)**. Example: too many **failed logins** → SOAR **blocks** the account automatically; analysts still use the **playbook** for **investigation**, **communication**, and **closure**.

---

## Incident response (definition)

An organization’s **quick** attempt to **identify** an attack, **contain** damage, and **correct** the effects of a **security breach**—aligned with the phased flow above.

---

## Key takeaways

- **Refine** playbooks after every significant incident (**lessons learned**).  
- Playbooks create **structure** and support **compliance**.  
- **Playbooks** + **SIEM** + **SOAR** together: **detect** → **automate** what is safe → **human** steps from the **playbook** for judgment and **recovery**.

---

## Related

- [../glossary/GLOSSARY.md](../glossary/GLOSSARY.md) — **Playbook**, **Runbook**, **Incident response**, **SIEM**, **SIEM tools**, **SOAR**, **MDR**, **Metrics**, **Log**  
- [08_siem_log_sources_and_evolution.md](08_siem_log_sources_and_evolution.md) — SIEM and **SOAR** context  
- [10_siem_tools_definition_and_products.md](10_siem_tools_definition_and_products.md) — SIEM products  
- [../../foundations_of_cybersecurity/notes/06_analyst_toolkit_and_forensics.md](../../foundations_of_cybersecurity/notes/06_analyst_toolkit_and_forensics.md) — chain of custody / evidence (forensics alignment)  
