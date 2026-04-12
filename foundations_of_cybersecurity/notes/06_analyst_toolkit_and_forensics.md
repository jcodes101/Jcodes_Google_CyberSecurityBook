# Analyst toolkit: SIEM, packet capture, and playbooks

## Toolkit varies by employer

Every organization ships a different stack. Learning **common categories** of tools (and being able to learn new products in the same category) is what interviews and on-the-job success reward.

---

## Security information and event management (SIEM)

**What it does**

- Collects and analyzes **log data** (events across systems).  
- Surfaces **alerts** for suspicious or policy-relevant activity.  
- Reduces manual log review by **filtering and prioritizing** what analysts see.

**How analysts use it**

- **Dashboards** group data so you can drill into categories relevant to an investigation.  
- Vendors differ in **dashboard layout** and **data sources** available to you.

**Deployment options**

- **On-premise** — more control; often more ops burden.  
- **Cloud-hosted** — often faster to deploy and maintain; sometimes chosen when the team is **less experienced** or needs quicker time-to-value.

---

## Network protocol analyzers (packet sniffers)

Tools that **capture and analyze** traffic on a network.

- Record data that devices on the network **see** or **exchange**.  
- Used for troubleshooting, investigation, and understanding **malicious or abnormal** traffic.

You will get hands-on exposure to common tools **later in the program** (course promise).

---

## Playbooks

**Definition:** A **manual** describing **operational steps**—especially **how to respond** to security events. Organizations maintain **many** playbooks (IR, malware, access abuse, vendor process, etc.).

**Purpose:** Guide analysts through **consistent**, **repeatable**, **policy-aligned** actions.

---

## Example: forensic investigation playbooks

**Scenario (from course):** You work for an **incident response** firm. A **small medical practice** suffered a breach. You support **forensics** and gather evidence for a **cyber insurance** decision.

### 1. Chain of custody playbook

**Chain of custody:** Document **who** held evidence, **when**, **where**, and **why** throughout the incident lifecycle.

- Evidence is **your responsibility** while in your possession.  
- **Track every movement** of evidence; **report** transfers.  
- Everyone involved can **account** for evidence location and handling.

### 2. Protecting and preserving evidence playbook

**Goal:** Handle **fragile** and **volatile** digital evidence correctly.

**Order of volatility:** Ordered list of what to preserve **first → last**, prioritizing data that **disappears** if power is lost or systems change.

- **Volatile data** can vanish on shutdown or overwrite—capture **early**.  
- Mishandling can **alter or destroy** evidence so it is **inadmissible** or useless.

**Practice:** Prefer **working on copies**; preserve originals per policy.

---

## Key takeaway

SIEM and sniffers support **detection and analysis**; playbooks support **correct response**. Forensics has **many** more steps and tools than this introduction—explore further if investigations interest you.
