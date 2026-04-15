# Denial of service (DoS), DDoS, and common network-level attacks

## Denial of service (DoS)

A **denial of service (DoS)** attack targets a network or server and **floods it with network traffic** to disrupt normal operations.

Goal:

- Overload a system so it crashes or can’t respond to legitimate users.

Why it matters:

- Downtime can cost money and time.
- A crash can also create opportunities for other attacks.

## Distributed denial of service (DDoS)

A **distributed denial of service (DDoS)** attack is a DoS attack launched from **multiple devices/servers** in different locations.

- The combined traffic makes it more likely the target is overwhelmed.

Important mindset:

- If an attacker overloads *any* critical component (network, router, server, etc.), the DoS objective is achieved.

The course also notes that sometimes “volume” isn’t the only lever:

- A carefully crafted packet can force extra processing time, degrading performance even without massive traffic volume.

---

## Common network-level DoS attacks (course examples)

### SYN flood

A **SYN flood** simulates the first step of the TCP connection process and overwhelms a server with **SYN** packets.

TCP handshake reminder:

1. Client sends **SYN**
2. Server responds **SYN/ACK** and reserves resources/keeps a port open
3. Client sends **ACK** to complete the connection

Attack idea:

- Flooding with SYN requests can consume the server’s available connection resources/ports so it can’t serve legitimate clients.

### ICMP flood

An **ICMP flood** repeatedly sends ICMP packets to a target so the target spends resources responding.

Impact:

- Can consume inbound/outbound bandwidth and contribute to a crash or severe slowdown.

### Ping of death

A **ping of death** sends an oversized ICMP packet intended to exceed normal handling limits (the course references “bigger than 64 kilobytes”).

Impact:

- On vulnerable systems, the oversized packet can overload processing and crash the target.

---

## Key takeaways

- DoS/DDoS attacks aim to disrupt operations by overwhelming systems or links.
- SYN flood and ICMP flood abuse common communication behavior at scale.
- Ping of death is an example of a single malformed/oversized request causing failure on vulnerable systems.
