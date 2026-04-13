# Open-source vs proprietary tools; Splunk and Chronicle SIEM dashboards

## Open-source tools

- Often **free** to use and can be **user-friendly**.  
- Built **collaboratively** in public; many eyes can improve **security** and **quality**.  
- **Source code** and often **training** material are **public**, so users can **inspect**, **modify**, and **extend** the software (within the project’s **license**).  
- Customization leads to **many services** and distributions built from the same **upstream** project.

**Engineers** create open-source projects to improve software and make it **available to anyone** who follows the license.

---

## Proprietary tools

- Developed and **owned** by a **person or company**.  
- Users typically **pay** for **usage** and **training**.  
- **Only the vendor** may access and change **source code**; customers **wait** for vendor **updates** (sometimes **paid**).  
- **Limited** configurability compared with open-source stacks you fully control.

**Examples (course):** **Splunk**® and **Google SecOps (Chronicle)** SIEM offerings.

---

## Misconception: “open source is weak or unsafe”

- Open-source projects have become **industry standards** over many years.  
- Threat actors **have** tried to tamper with open projects; **visibility** means **many defenders** can **review** code and **patch** issues **quickly** when found.  
- Broad exposure by **informed** users and professionals can make **sustained** malicious change **harder**, not easier.

---

## Examples of open-source tools (security)

### Linux

- **Open-source operating system**, widely deployed.  
- Tailor the OS using a **command-line interface (CLI)**.  
- **Operating system:** interface between **hardware** and the **user**—manages hardware communication and **applications**.  
- Many **distributions** exist for different roles. **Linux** and the CLI are covered in depth **later** in the certificate program.

### Suricata

- **Open-source** **network analysis** and **threat detection** software.  
- **Inspects** network traffic for **suspicious** behavior and produces **network data logs**.  
- Correlates activity across **users**, **computers**, or **IP addresses** to surface **threats**, **risks**, or **vulnerabilities**.  
- Maintained under the **Open Information Security Foundation (OISF)** so the project stays **free** and **public**; used in **public and private** sectors and **integrates** with many **SIEM** and security tools. More detail **later** in the program.

---

## Key takeaway (tooling models)

Cybersecurity relies on **both** open-source and **proprietary** products; the program will revisit **both** in depth.

---

## Splunk® (proprietary SIEM)

**Offerings:** **Splunk® Enterprise** (self-managed) and **Splunk® Cloud**.

**Role:** Collect, **search**, **monitor**, and **analyze** log data from **many sources** on **dashboards**—giving visibility into **internal** infrastructure and **day-to-day** operations.

### Splunk dashboards (course)

| Dashboard | Purpose |
|-----------|---------|
| **Security posture** | For **SOCs**: last **24 hours** of **notable** security events and **trends**; check whether **infrastructure** and **policies** behave as designed; **real-time** monitoring and investigation (e.g., suspicious activity from a **specific IP**). |
| **Executive summary** | **Health** of security over **time**; supports improving controls that **reduce risk**; **high-level** views for **stakeholders** (e.g., incident and trend summary for a period). |
| **Incident review** | Surfaces **suspicious patterns** during incidents; **prioritizes** higher-risk items for **analyst** review; **visual timeline** of events **before** and during the incident. |
| **Risk analysis** | Risk per **risk object** (user, computer, **IP**); highlights changes in **risky** behavior (e.g., login **outside** normal hours, **unusual** traffic from one host); helps **prioritize** mitigation on **critical** assets. |

---

## Chronicle (Google SecOps) — cloud-native SIEM

**Chronicle** is a **cloud-native** SIEM from **Google** that **retains**, **analyzes**, and **searches** log data to find **threats**, **risks**, and **vulnerabilities**.

**Pivoting / filtering data** (examples):

- A specific **asset**  
- A **domain** name  
- A **user**  
- An **IP** address  

Supports **dashboards**, **filters**, **alerts**, and tracking **suspicious** domains.

### Chronicle dashboards (course)

| Dashboard | Purpose |
|-----------|---------|
| **Enterprise insights** | Recent **alerts**; **suspicious domains** in logs (**indicators of compromise** / IOCs); **confidence** scores and **severity**; e.g., monitor access to **critical** apps/systems from **odd** locations or devices. |
| **Data ingestion and health** | Volume of **event** logs, **log sources**, and **success** of ingestion into Chronicle; validate **source** configuration and that logs arrive **without errors** so the team has the data it needs. |
| **IOC matches** | Top **threats**, **risks**, and **vulnerabilities**; trends for **domains**, **IPs**, and **device** IOCs over time; drill into alert-related activity (e.g., suspicious login **geography**). |
| **Main** | High-level view of **ingestion**, **alerting**, and **event** activity over time; **timelines** (e.g., spike in **failed logins**) across sources, devices, IPs, and **locations**. |
| **Rule detections** | Stats on incidents by **frequency**, **severity**, and **detections** over time; list alerts from a **specific detection rule** (e.g., user opens a **known malicious** email attachment); supports **recurring** incident handling and **mitigation** tactics. |
| **User sign-in overview** | **Sign-in** behavior org-wide; spot **anomalies** (e.g., same user signed in from **multiple locations** at once); supports protecting **accounts** and **applications**. |

---

## Key takeaway (SIEM dashboards)

Dashboards **organize** work so analysts **focus** on the **highest-priority** items **faster**—**identify**, **analyze**, and **remediate** in a timely way. Hands-on **search** and SIEM features come **later** in the program.

---

## Related

- [10_siem_tools_definition_and_products.md](10_siem_tools_definition_and_products.md) — **SIEM-only** consolidated note (what SIEM is + every SIEM product + usage)  
- [08_siem_log_sources_and_evolution.md](08_siem_log_sources_and_evolution.md) — SIEM role, logs, cloud trends, **SOAR**  
- [../glossary/GLOSSARY.md](../glossary/GLOSSARY.md) — **IOC**, **SOC**, **Splunk**, **Chronicle**, **Suricata**, **Linux**, open vs proprietary  
