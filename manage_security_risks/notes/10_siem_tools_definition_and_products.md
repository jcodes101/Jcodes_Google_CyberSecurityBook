# SIEM tools — what SIEM is and every SIEM product in these notes

This note is **only** about **SIEM** (security information and event management): the **idea**, what SIEM is **for**, and **each SIEM product named** in your certificate materials—**what it is**, **what it does**, and **how analysts use it**.

> Your course **names three SIEM offerings** by product: **Splunk Enterprise**, **Splunk Cloud**, and **Google Chronicle (SecOps)**. Other tools (e.g. **Suricata**) appear in the same lessons but are **not** SIEMs; they **feed** SIEMs with logs and alerts (see end of this note).

---

## Part 1 — What is SIEM?

**SIEM** stands for **security information and event management**.

It is an **application** (or platform) that:

1. **Collects** **log data** and security-related **events** from many **sources** across the organization.  
2. **Stores** that data in a **central** place (often indexed for fast search).  
3. **Monitors** activity in **near real time** and applies **rules** or **analytics** to spot suspicious patterns.  
4. **Alerts** analysts when something may be a **threat**, **risk**, or **vulnerability** worth investigating.  
5. **Reduces** how much raw log data people must read by hand—through **dashboards**, **filters**, and **correlation**.

SIEM must be **configured** and **tuned** for each organization and **updated** as threats and the environment change.

### What SIEM is used for (day-to-day)

| Use | Why it matters |
|-----|----------------|
| **Security monitoring** | Watch networks, systems, and accounts for abuse or intrusions. |
| **Investigation** | Search historical logs to answer “what happened?” and “who was affected?” |
| **Compliance & audit support** | Show that monitoring and retention align with policy and regulations. |
| **SOC workflows** | Give **security operations center** teams shared views (dashboards) and queues for triage. |
| **Risk visibility** | Highlight risky users, hosts, or IPs and prioritize remediation. |

**Logs** (e.g., firewall, network, server) are the **input** SIEM depends on. Definitions: [08_siem_log_sources_and_evolution.md](08_siem_log_sources_and_evolution.md).

---

## Part 2 — SIEM products listed in your notes (complete set)

The following are the **only** tools your materials treat as **SIEM products** (by name).

---

### 1. Splunk® Enterprise

| | |
|--|--|
| **What it is** | **Proprietary** SIEM and **data platform** from Splunk. **Self-managed**: your organization (or a partner) **installs and operates** the software on **your** infrastructure. |
| **What it does** | **Ingests** log and machine data from **many sources**, then **indexes** it so you can **search**, **monitor**, **report**, and **visualize** on **dashboards**. Built for broad **visibility** into IT and security operations—not only security use cases. |
| **What it is used for** | **SOC** monitoring, incident investigation, executive reporting, and **risk**-oriented views over **users**, **hosts**, and **IPs**. Same **dashboard concepts** as Cloud (below); deployment differs. |

**Dashboards (course)** — how analysts use them:

| Dashboard | Used for |
|-----------|----------|
| **Security posture** | Last **24 hours** of notable security events and **trends**; verify controls and infrastructure are behaving; **live** hunt (e.g., odd traffic from one **IP**). |
| **Executive summary** | **Trends** and **health** over time for **leadership**; summaries of incidents and patterns in a period. |
| **Incident review** | **Suspicious patterns** during an incident; **priority** items for analysts; **timeline** of events leading into the incident. |
| **Risk analysis** | Per-**object** risk (user, computer, **IP**); behavior changes (off-hours login, unusual volume); **prioritize** work on **critical** assets. |

---

### 2. Splunk® Cloud

| | |
|--|--|
| **What it is** | The **same Splunk** product family, delivered as a **cloud** service: Splunk **hosts** and **maintains** much of the **platform**; you **connect** data sources and use the product over the **internet**. |
| **What it does** | Same core capabilities as **Enterprise**: **collect**, **search**, **monitor**, **analyze** data with **dashboards**—without running Splunk’s **backend** on your own data center hardware. |
| **What it is used for** | Same **security operations** goals as Enterprise when the org prefers **SaaS** operations, faster rollout, or less **in-house** platform administration. |

**Dashboard usage** aligns with **Splunk Enterprise** (posture, executive summary, incident review, risk analysis)—the course treats them as one product line with two **deployment** options.

---

### 3. Chronicle (Google SecOps SIEM)

| | |
|--|--|
| **What it is** | **Google’s** **cloud-native** **SIEM**: designed for **large-scale** log **retention**, **search**, and **security analytics** in **Google’s** cloud. Often discussed under **Google SecOps**. |
| **What it does** | **Retains**, **analyzes**, and **searches** security-relevant log data to surface **threats**, **risks**, and **vulnerabilities**. Supports **filters**, **alerts**, and **dashboards**; investigation often **pivots** on **asset**, **domain**, **user**, or **IP**. |
| **What it is used for** | **Detection** and **hunting** with **IOC**-style context, **ingestion** health checks, **detection rule** tuning, and **user** sign-in anomaly review. |

**Dashboards (course)** — how analysts use them:

| Dashboard | Used for |
|-----------|----------|
| **Enterprise insights** | Recent **alerts**; **suspicious domains** / **IOCs**; **confidence** and **severity**; monitoring access to **critical** systems from unusual **locations** or **devices**. |
| **Data ingestion and health** | Volume of events, **sources**, and **success** of pipeline ingestion—fix **gaps** so analysts **trust** the data. |
| **IOC matches** | Top issues and **trends** for domains, **IPs**, device IOCs; drill into activity (e.g., login **geography**). |
| **Main** | High-level **ingestion**, **alerting**, and **events** over time; **timelines** (e.g., failed-login spikes) across sources and **locations**. |
| **Rule detections** | **Frequency** / **severity** of rule hits; lists of alerts per **rule** (e.g., malicious **attachment** opened); supports **repeat** incidents and **mitigation** planning. |
| **User sign-in overview** | Org-wide **sign-in** patterns; anomalies like **concurrent** sign-ins from **multiple** locations; **account** and **app** protection. |

---

## Part 3 — At a glance: the three SIEM offerings

| Product | Vendor | Deployment (how it runs) | Primary jobs |
|---------|--------|---------------------------|--------------|
| **Splunk Enterprise** | Splunk | **You** operate (on-prem / your cloud) | Ingest, search, monitor, dashboards for SOC + risk + leadership |
| **Splunk Cloud** | Splunk | **Splunk**-hosted SaaS | Same jobs as Enterprise, less self-hosted ops |
| **Chronicle** | Google | **Cloud-native** SecOps / Google cloud | Retain, search, detect, IOC-focused dashboards, ingestion health |

All three are **used** to **centralize** security **visibility**, **detect** suspicious activity, and **support** analyst **workflows**—with different **ownership** of infrastructure and **UI** patterns.

---

## Part 4 — Not SIEM (but related in your notes)

These tools are **important** next to SIEM but are **not** SIEM products:

| Tool | What it actually is | How it relates to SIEM |
|------|---------------------|-------------------------|
| **Suricata** | **Open-source** **network** **IDS/IPS** and **threat detection** | Inspects traffic, generates **logs** and alerts; **integrates** with **Splunk**, **Chronicle**, and other SIEMs as a **data source**. |
| **SOAR** | **Orchestration** and **automation** for playbooks and case handling | Sits **beside** SIEM to **automate** responses; does **not** replace log collection and correlation as the SIEM’s core job. |

---

## Part 5 — How SIEM fits the bigger picture

- **Domain 7 (security operations)** in the eight-domain model is where SIEM **daily work** usually lives: [01_the_eight_security_domains.md](01_the_eight_security_domains.md).  
- **Evolution** (cloud-hosted vs cloud-native, AI, IoT, automation): [08_siem_log_sources_and_evolution.md](08_siem_log_sources_and_evolution.md).  
- **Open vs proprietary** context for Splunk and Chronicle: [09_open_source_proprietary_and_siem_dashboards.md](09_open_source_proprietary_and_siem_dashboards.md).  
- **Terms**: [../glossary/GLOSSARY.md](../glossary/GLOSSARY.md) (*SIEM*, *Splunk*, *Chronicle*, *IOC*, *SOC*, *SOAR*).

---

## Summary

- **SIEM** = central **log** collection, **monitoring**, **alerting**, and **analysis** for security (and often IT) operations.  
- Your notes name **three** SIEM offerings: **Splunk Enterprise**, **Splunk Cloud**, **Chronicle**—each described above with **purpose** and **typical analyst use**.  
- **Suricata** is **not** a SIEM; it **feeds** SIEMs. **SOAR** **automates** beside SIEM but is **not** a SIEM.

When you learn more tools in later courses, add them under **Part 2** in the same format.
