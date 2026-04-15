# Security zones, DMZ, and network segmentation

## Security zones and segmentation

A **security zone** is a **segment** of a network designed to protect internal systems from broader exposure (especially from the internet).

**Network segmentation** divides a network into segments so each segment can have:

- Its own **access permissions**
- Its own **security rules**
- Stronger **blast-radius reduction** (limiting how far an issue spreads)

### Example: guest Wi‑Fi vs staff network

A hotel may isolate:

- **Guest Wi‑Fi** (untrusted/public-style use)
- A separate **encrypted staff network** for operations

### Example: departmental subnets

A university might separate:

- **Faculty** subnets
- **Student** subnets

If one segment is compromised, administrators can **isolate** it while keeping other segments safer.

## Two high-level zone types (course framing)

### Uncontrolled zone

- Networks **outside** the organization’s control (commonly the **internet**).

### Controlled zone

- Internal subnets and controls that sit between untrusted zones and protected assets.

## Inside the controlled zone: DMZ, internal network, restricted zone

### Demilitarized zone (DMZ)

The **DMZ** is an outer layer inside the controlled environment that hosts **public-facing services** that must reach/reach from the internet, such as:

- Web servers
- **Proxy servers** hosting public sites
- **DNS** servers publishing public records
- Email/file servers handling **external** communications

The DMZ acts as a **network perimeter** boundary relative to the internal network.

### Internal network

Contains private servers and data the organization must protect.

### Restricted zone

A tighter zone for **highly confidential** information, accessible only to **privileged** users/systems.

## Defense in depth with firewalls (conceptual layout)

Ideally:

- A **DMZ** sits between **two firewalls**:
  - One filters traffic **entering/leaving** the DMZ from the outside
  - Another filters traffic **between the DMZ and internal network**
- If a **restricted zone** exists, it may be protected by **another firewall** so compromises are harder to propagate.

## Analyst relevance

Security teams often regulate **firewall policies** controlling:

- Which **IPs** and **ports** can reach DMZ services (example: **HTTPS-only** access to web servers)
- Lateral movement constraints between zones

## Key takeaways

- **Segmentation** and **zones** reduce risk by isolating trust levels.
- The **DMZ** hosts internet-exposed services; **internal** and **restricted** zones protect more sensitive assets.
- **Firewall policy** is a primary lever analysts help maintain for zone boundaries.
