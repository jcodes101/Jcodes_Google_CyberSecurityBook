# Methods of detection: hunting, intelligence, and deception

During the **Detection and Analysis** phase of the **NIST Incident Response Lifecycle**, security teams are notified of a possible incident and work to **investigate and verify** it by collecting and analyzing data.

- **Detection**: prompt discovery of security events  
- **Analysis**: investigation and validation of alerts  

**Intrusion detection systems (IDS)** can detect possible intrusions and raise alerts for analysts. **Security information and event management (SIEM)** tools help detect, collect, and analyze security data.

---

## Why add more than IDS/SIEM?

Detection has limits. Tools only see what they are **configured** to monitor; poor configuration can mean missed activity and increased risk. Teams use **additional detection methods** to improve **coverage** and **accuracy**.

---

## Threat hunting

Threats and attacker tactics evolve. Automated, technology-only detection can lag the threat landscape.

**Threat hunting** is the **proactive search** for threats on a network. It combines **technology** with **human analysis** to find activity that automated tools missed, to dig deeper on alerts, and sometimes to catch threats **before** they cause damage.

Example: **Fileless malware** is hard for many tools to catch—it may live in **memory** and avoid traditional file-based detection (e.g., signature analysis). Threat hunting uses active human analysis plus tooling to surface threats like this.

**Threat hunters** are specialists who research emerging threats, estimate whether the organization could be affected, and hunt using **threat intelligence**, **indicators of compromise (IoC)**, **indicators of attack (IoA)**, and techniques such as **machine learning**.

---

## Threat intelligence

Organizations improve detection by understanding the threat landscape and how it relates to their environment.

**Threat intelligence** is **evidence-based** information about **existing or emerging** threats, with enough **context** to act on.

### Sources (examples)

- **Industry reports**: often describe attacker **tactics, techniques, and procedures (TTP)**  
- **Government advisories**: similar TTP-focused guidance  
- **Threat data feeds**: streams of threat-related data (e.g., IPs, domains, file hashes) useful against persistent, sophisticated actors such as **advanced persistent threats (APTs)**—long-term unauthorized access to a system  

Large volumes of intelligence are hard to manage. A **threat intelligence platform (TIP)** is an application that **collects, centralizes, and analyzes** intelligence from multiple sources so teams can **prioritize** relevant threats and strengthen posture.

**Note:** Feeds are best used to **add context** to detections. They should **not** fully drive detections without **assessment** for your organization.

---

## Cyber deception

**Cyber deception** uses techniques that **mislead** attackers to **improve detection** and defensive learning.

**Honeypots** are **decoy** systems or resources made to look vulnerable or valuable, to **attract** intruders. Example: a fake file named like “Client Credit Card Information - 2022” may lure an attacker; access attempts can **alert** the security team.

---

## Key takeaways

- **Detection and analysis** validate whether an alert represents a real incident; **IDS** and **SIEM** are core but not sufficient alone.  
- **Threat hunting** proactively finds hidden or advanced threats that automation misses.  
- **Threat intelligence** (reports, advisories, feeds, **TIPs**) adds context—use feeds thoughtfully, not blindly.  
- **Cyber deception** (e.g., **honeypots**) lures and reveals attacker behavior.  
- A **mix of methods, tools, and practices** helps organizations adapt as threats evolve.
