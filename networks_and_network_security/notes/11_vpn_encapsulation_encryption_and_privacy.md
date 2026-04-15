# Virtual private networks (VPNs): encapsulation, encryption, and privacy

## Why VPNs exist

When you use the internet, traffic can expose information that ties activity to **identity** and **location**. If traffic is intercepted, sensitive data may be exposed (for example, financial information).

A **virtual private network (VPN)** is a **network security service** that helps protect privacy on untrusted networks (like public internet paths).

Common goals:

- **Hide or change** the apparent **public IP / virtual location** from external observers
- **Encrypt** data **in transit** to protect **confidentiality**

## Encapsulation (how VPNs route traffic while staying private)

**Encapsulation** is a process where sensitive payload data is **wrapped inside other packets** so it can traverse networks while protecting inner contents.

Why it matters:

- Plain encryption alone can make it hard for routers to forward traffic if they cannot interpret needed headers.
- VPN approaches encrypt and **encapsulate** so outer headers remain routable while inner data stays protected.

The course also describes VPNs as using an **encrypted tunnel** between a device and a VPN server, where encryption is intended to prevent unauthorized reading of payload contents without proper keys.

## What a VPN does not always solve by itself

Even with encryption, organizations still need defense-in-depth (identity, endpoint protection, logging, policy, etc.). The course emphasizes VPNs as a strong **privacy/confidentiality** tool for transit, not a single control for every threat.

## Key takeaways

- VPNs help protect **data in transit** and reduce exposure of **IP/location** details to outsiders.
- **Encapsulation** helps VPN traffic remain **forwardable** while keeping inner content protected.
- VPNs are widely used by **individuals** and **enterprises** accessing sensitive resources across public networks.
