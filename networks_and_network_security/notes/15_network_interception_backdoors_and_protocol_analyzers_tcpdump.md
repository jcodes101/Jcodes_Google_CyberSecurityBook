# Network interception attacks, backdoors, and protocol analyzers (tcpdump)

## Network interception attacks

**Network interception attacks** work by **intercepting network traffic** to:

- Steal valuable information
- Interfere with transmissions (alter messages, inject changes, interrupt operations)

Attackers may use hardware or software tools to capture/inspect data **in transit**. This is commonly called **packet sniffing**.

Example impact:

- An attacker intercepts a bank transfer and changes the recipient account to one they control.

The course later expands into other interception patterns (mentioned here as headings you’ll revisit):

- **On-path attacks**
- **Replay attacks**

---

## Backdoor attacks

A **backdoor** in cybersecurity is a weakness intentionally left (or later installed) to **bypass normal access controls**.

Why backdoors exist:

- Troubleshooting or administrative convenience (intended by programmers/admins)

Why they’re dangerous:

- Attackers can also install backdoors after initial compromise to maintain **persistent access**

Possible attacker outcomes after backdoor access:

- Installing malware
- Changing security settings to weaken defenses
- Performing a **denial of service (DoS)** attack
- Stealing or modifying sensitive information

---

## Potential impacts to an organization

### Financial

- Disrupted business operations can cause direct revenue loss.
- Recovery/rebuild costs can be high (and ransomware/extortion can add severe costs).
- Customer data exposure can lead to litigation and settlements.

### Reputation

- Reduced trust from customers and partners.
- Customer churn to competitors after public incidents.

### Public safety

- Government/critical infrastructure attacks can affect citizen safety.
- Compromises in power grids, water systems, or defense communications can cause physical harm.

---

## Network protocol analyzers (packet sniffers / packet analyzers)

A **network protocol analyzer** (also called a **packet sniffer** or **packet analyzer**) captures and analyzes network traffic.

These tools are used by defenders to:

- Monitor networks and investigate suspicious activity
- Troubleshoot network performance
- Establish baselines and utilization metrics
- Detect/identify malicious traffic
- Create customized alerts/notifications
- Locate unauthorized IM traffic or wireless access points

But attackers can also use them to capture sensitive data (for example usernames/passwords).

Common examples named in the course:

- SolarWinds NetFlow Traffic Analyzer
- ManageEngine OpManager
- Azure Network Watcher
- Wireshark
- tcpdump

---

## tcpdump (focus tool)

**tcpdump** is a command-line network protocol analyzer.

Key traits (as described in the course):

- Lightweight (low memory/CPU)
- Uses the open-source **libpcap** library
- Text-based (commands run in the terminal)
- Common on Linux/Unix systems; preinstalled on many Linux distributions

### What tcpdump shows you

tcpdump prints per-packet information to the terminal (and optionally to a capture/log file), including:

- **Timestamp** (hh:mm:ss.fraction)
- **Source IP**
- **Source port**
- **Destination IP**
- **Destination port**

Note:

- By default, tcpdump may resolve IPs to hostnames and replace port numbers with common service names.

## Key takeaways

- Interception and backdoor attacks can cause serious harm and enable follow-on actions (malware, DoS, data theft/modification).
- Protocol analyzers are critical investigative tools for defenders but can also be misused by attackers.
- tcpdump is a common entry-level tool for inspecting traffic using timestamps, IPs, and ports.
