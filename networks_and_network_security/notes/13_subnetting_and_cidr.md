# Subnetting and CIDR (overview)

## Subnetting

**Subnetting** is the process of dividing one larger network into smaller, organized groups called **subnets**.

Mental model (from the course):

- A company network is like a **city**
- Each subnet is a **neighborhood** inside that city

### What subnetting achieves

- Devices are grouped using a combination of **IP addressing** and **subnet mask** assignments.
- Subnets can behave like a **network within a network**.
- Benefits called out:
  - More **efficient** communication (traffic can stay local when appropriate)
  - Improved **performance**
  - Support for **security zones** and isolation strategies

When two devices on the **same subnet** communicate, switching can keep the traffic **on-subnet** more efficiently (per course explanation).

## CIDR (Classless Inter-Domain Routing)

**CIDR** is a method of assigning **subnet masks** to IP addresses to define subnets.

### Why “classless” matters (high level)

- Older **classful** addressing grouped IPv4 into fixed classes (Class A–E) and eventually became too limiting as the internet grew.
- **Classless** CIDR addressing improved flexibility and helped expand usable IPv4 addressing approaches through finer segmentation.

### CIDR notation

CIDR IPv4 addresses look like normal IPv4 addresses but add a **slash** and a **prefix length**:

- Example IPv4: `198.51.100.0`
- Example CIDR: `198.51.100.0/24`

The number after `/` is the **IP network prefix** length. A `/24` example commonly spans the host range for that /24 network (course example range: `198.51.100.0` through `198.51.100.255`).

### Practical note from the course

- CIDR can reduce routing table entries compared to less flexible legacy schemes (high-level benefit described in the reading).
- For practice, the course suggests using online conversion tools (example name mentioned: **IPAddressGuide**) to build intuition.

### Study guidance

Focus on the **concept** of CIDR as a flexible modern subnetting tool; deeper binary math can be learned later if needed.

## Security benefits of subnetting

Subnetting helps teams build **isolated subnetworks** using:

- Physical isolation
- Routing configuration
- Firewalls

## Key takeaways

- Subnetting creates **smaller networks** inside a larger private network.
- **CIDR** is the modern flexible notation/method for defining those subnets.
- Subnetting supports both **operational efficiency** and **security segmentation**.
