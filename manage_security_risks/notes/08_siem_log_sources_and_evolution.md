# SIEM, log sources, and how SIEM is evolving

## Security information and event management (SIEM)

A **SIEM** is an application that **collects** and **analyzes** **log data** to **monitor** important activity across the organization.

From the analyst workflow (transcript summary):

- **Real-time** visibility into events  
- **Monitoring** and **analysis** of security-related activity  
- **Automated alerts** when rules or patterns match  
- **Central** storage of log data  
- **Indexing** and **filtering** so analysts review **fewer** raw logs manually—**saving time**  
- Must be **configured** and **customized** to each organization’s needs, and **re-tuned** as new **threats** and **vulnerabilities** appear  

> Hands-on practice with different SIEM products appears **later** in the certificate program.

---

## Log sources (definitions)

### Log

A **record of events** that occur within an organization’s **systems** and **networks**.

### Firewall log

A record of **attempted** or **established** connections for **incoming** traffic from the internet, and **outbound** requests from inside the network to the internet.

### Network log

A record of **computers and devices** that **join or leave** the network, and of **connections** between **devices** and **services** on the network.

### Server log

A record of events for **services** such as **websites**, **email**, or **file shares**—including actions like **login**, **password**, and **username** requests.

### Why logs matter

Monitoring these logs helps teams spot **vulnerabilities** and possible **data breaches**. SIEM tools **depend on logs** to detect security issues.

---

## Current SIEM solutions (course framing)

- **Real-time** monitoring and **tracking** of security **event** logs  
- Data supports **deep analysis** of potential **threats**, **risks**, and **vulnerabilities**  
- **Multiple dashboards** help team members **manage** and **monitor** organizational data  
- **Today**, meaningful analysis of security events still requires **human** involvement  

---

## Future direction of SIEM

### Cloud models

| Model | Idea |
|-------|------|
| **Cloud-hosted SIEM** | Vendor **runs** and **maintains** the infrastructure; your team **uses** the tool over the **internet**. Fits orgs that do not want to **build** and **operate** their own SIEM infrastructure. |
| **Cloud-native SIEM** | Also vendor-managed and internet-accessible, but **built** to use **cloud** strengths: **availability**, **flexibility**, **scalability**. |

### Broader trends

- **Internet of Things (IoT)** — more connected devices **expand attack surface** and the volume of data attackers might abuse.  
- **Artificial intelligence (AI)** and **machine learning (ML)** — expected to improve **threat-related language** handling, **dashboards**, and **storage** features.  
- **Automation** — faster response to many events **without** waiting on a person.  
- **SOAR** (**Security orchestration, automation, and response**) — applications, tools, and workflows that use **automation** for common security incidents, often alongside SIEM. Analysts still handle **complex** or **rare** cases that are **hard to automate**.  
- **Interoperability** — expectation that security **platforms** will **integrate** more cleanly; still **evolving**.

---

## Key takeaways

- **SIEM** is central to **monitoring** organizational data; **dashboards** are a common daily task for entry-level analysts.  
- Stay curious about **cloud**, **integration**, and **automation**—the field keeps moving.  
- **Logs** (firewall, network, server) are the **fuel** SIEM runs on; understanding them helps you interpret alerts and investigations.

---

## Related

- [10_siem_tools_definition_and_products.md](10_siem_tools_definition_and_products.md) — **full SIEM-only** note: definition + **Splunk** + **Chronicle** + how each is used  
- [../reference/SIEM_tools_quick_reference.md](../reference/SIEM_tools_quick_reference.md) — **short index** pointing to **10**  
- [09_open_source_proprietary_and_siem_dashboards.md](09_open_source_proprietary_and_siem_dashboards.md) — **open-source** vs **proprietary** SIEM, **Splunk** and **Chronicle** dashboards  
- [../glossary/GLOSSARY.md](../glossary/GLOSSARY.md) — terms such as **SIEM**, **log**, **SOAR**, **threat**, **attack vectors**  
- [01_the_eight_security_domains.md](01_the_eight_security_domains.md) — Domain 7 (operations) and SIEM in context  
