# Firewalls: types, stateful vs stateless, and next-generation firewalls (NGFW)

## What a firewall does

A **firewall** is a network security device that **monitors traffic** to and from a network. It **allows** or **blocks** traffic based on a **defined set of security rules** (aligned with the organization’s **security policy**).

Common techniques:

- **Port filtering**: allow or block traffic based on **port numbers** (and often other criteria).
- Example rules (illustrative):
  - Allow **TCP 443** for **HTTPS**
  - Allow **TCP 25** for **email** (when appropriate)
  - Block everything else not explicitly permitted

## Types of firewalls (deployment form factor)

### Hardware firewall

- Often described as a **basic** perimeter defense for a network.
- **Inspects packets** before they are allowed into the network.
- Physical appliance at the network edge.

### Software firewall

- Performs the **same general functions** as a hardware firewall, but as **software** installed on a host (computer/server).
- **Host-based**: if installed on a computer, it analyzes traffic **for that computer**.
- **Server-based**: if installed on a server, it can protect **devices/clients** depending on deployment and architecture.
- Trade-offs:
  - Typically **lower cost** than buying a separate appliance
  - **No extra physical space**
  - Can add **CPU/processing burden** on the device running the software

### Cloud-based firewall (Firewall as a Service)

- Cloud service providers may offer **firewalls as a service** (**FaaS**).
- These are **software firewalls hosted by the CSP**.
- Organizations configure rules in the provider’s interface.
- The firewall can inspect **incoming traffic before it reaches** on-site networks and can also protect **cloud-hosted assets**.

## Stateful vs stateless firewalls

These terms describe **how** the firewall makes decisions.

### Stateless firewall

- Operates using **predefined rules** only.
- Does **not** track session/state information from packets over time.
- Does **not** store analyzed information for trend detection.
- Typically **less secure** than stateful inspection (per course framing).

### Stateful firewall

- **Tracks information** about traffic passing through it (connection/session awareness).
- Can identify suspicious **characteristics/behaviors** and block them proactively.
- Generally stronger than basic stateless rule matching alone.

### Next-generation firewall (NGFW)

An **NGFW** provides **more** than traditional stateful inspection.

Typical capabilities called out in course materials:

- **Stateful inspection** of inbound/outbound traffic
- **Deep packet inspection (DPI)** (examining packet contents beyond headers; a form of inspection related to **packet sniffing** concepts)
- **Intrusion prevention** / threat-oriented enforcement
- Often **application-aware** (can enforce based on **applications**, not only IP/port)
- May integrate **cloud threat intelligence** for faster updates against emerging threats
- Optional/extra features mentioned: malware sandboxing, network anti-virus, URL/DNS filtering

## Key takeaways

- Firewalls enforce policy through rules; **port filtering** is a common control mechanism.
- Deployments include **hardware**, **software**, and **cloud/FaaS**.
- **Stateful** firewalls track session/state; **stateless** firewalls rely on static rules without that tracking.
- **NGFWs** add deeper inspection and modern threat-focused capabilities beyond basic allow/deny rules.
