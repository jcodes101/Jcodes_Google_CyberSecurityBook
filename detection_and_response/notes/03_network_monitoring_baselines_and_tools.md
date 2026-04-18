# Network monitoring: baselines, what to watch, and tools

Network communication can be noisy: sending email, streaming video, and visiting websites all generate network traffic and network data. Monitoring and analyzing that activity helps organizations maintain situational awareness and detect suspicious behavior.

---

## Network traffic vs network data

- **Network traffic**: the amount of data that moves across a network (and can include the type of data transferred, such as HTTP)
- **Network data**: the data transmitted between devices on a network

---

## Know your network (build a baseline)

Networks connect devices, and those devices communicate using protocols. Network communications can reveal:
- source and destination IP addresses
- amount of data transferred
- date and time of communications
- protocols/ports involved

This information is useful for establishing a **baseline** of normal behavior.

### Baseline

A **baseline** is a reference point used for comparison. In security, baselines establish expected/normal behavior for systems, devices, and networks. Once you know “normal,” you’re better equipped to spot “abnormal.”

---

## Monitor your network (deviations from baseline)

Monitoring involves examining network components and communications to detect unusual activity (for example, large or unexpected data transfers). Common areas to monitor include:

### Flow analysis

**Flow** refers to the movement of network communications and includes information related to packets, protocols, and ports.

Ports are often (but not always) associated with particular protocols. Example: **port 443** is commonly associated with **HTTPS**.

Attackers may intentionally use unusual protocol/port pairings to maintain communications with compromised systems. These communications are often part of **command and control (C2)**—techniques used to maintain communication with compromised systems.

Example: using **HTTPS over port 8088** instead of the more typical port **443**.

Defenders should know which ports are approved/expected and investigate mismatches between protocols and ports.

### Packet payload information

Packets contain payloads (the data being transmitted). Payloads are often encrypted and may require decryption to read.

Monitoring payload information can help identify:
- unusual content
- sensitive data leaving the organization (possible **data exfiltration**)

### Temporal patterns

Time-based patterns help identify “off baseline” behavior.

Example: if a North America business typically has bulk traffic between **9 a.m. and 5 p.m.**, large transfers occurring far outside those hours may warrant investigation.

---

## Protect your network (SOC vs NOC)

Organizations may have different operations teams with different goals:

- **SOC (security operations center)**: focuses on detection and response to security threats and attacks
- **NOC (network operations center)**: focuses on network performance, availability, and uptime; responds to disruptions like outages

Security analysts monitor networks for **indicators of compromise (IoC)** and work to detect suspicious network activity.

---

## Network monitoring tools

Monitoring can be automated or manual. Common tools include:

### Intrusion detection systems (IDS)

IDS tools monitor activity and alert on potential intrusions based on configured detections. They commonly inspect packet content (including payload patterns) to detect threats such as malware or phishing attempts.

### Network protocol analyzers (packet sniffers)

Network protocol analyzers capture and analyze network traffic in detail. They support manual investigation of communications via packet captures.

Examples:
- **tcpdump**
- **Wireshark**

Packet captures can be investigated to identify potentially malicious activity.

---

## Key takeaways

- You can’t protect what you don’t understand—start by learning network components and normal communications.
- **Baselines** help you identify deviations that may indicate malicious behavior.
- Useful monitoring lenses include **flows** (packets/protocols/ports), **payload** content, and **time patterns**.
- A **SOC** focuses on security detection/response; a **NOC** focuses on availability and performance.
- **IDS** and **packet sniffers** are common tools used to monitor and investigate network activity.

