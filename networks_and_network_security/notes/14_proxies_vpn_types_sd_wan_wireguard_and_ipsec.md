# Proxies, VPN types, SD-WAN, and VPN protocols (WireGuard vs IPsec)

## Protocol categories (quick recap)

Network protocols are the shared rules devices use to transfer data. Three common categories:

1. **Communication protocols** (establish data exchange; examples include **TCP**, **UDP**, **SMTP**)
2. **Management protocols** (monitor/troubleshoot; example **ICMP**)
3. **Security protocols** (protect data in transit; examples **IPsec**, **SSL/TLS**)

Other common examples referenced:

- **HTTP** (application-layer web communication)
- **DNS** (maps hostnames to IP addresses)
- **ARP** (maps IP addresses to MAC addresses on a LAN)

## Firewalls (recap in later course materials)

Firewalls may be implemented as **hardware appliances** or **network virtual appliances (NVAs)**. Traditional firewalls often filter using **IP address** and **port** rules.

### Stateless vs stateful (recap)

- **Stateless**: rule-based without connection state tracking.
- **Stateful**: tracks sessions using a **state table**; can reduce the need to duplicate rules for return traffic compared to basic stateless designs (per course comparison).

### Next-generation firewall (NGFW)

NGFWs add capabilities like **deep packet inspection**, intrusion prevention, application awareness, and sometimes cloud intelligence feeds.

## Proxy servers

A **proxy server** can add security by sitting between clients and destinations.

- Uses **network address translation (NAT)** concepts as a barrier between internal clients and external threats.
- **Forward proxy**: internal clients → external resources.
- **Reverse proxy**: external clients → internal services.
- Proxies can enforce **filters** (example: block known malicious sites).

## VPNs (enterprise patterns)

A **VPN** encrypts data in transit and helps conceal/change how your traffic appears to external systems (IP/location privacy themes from earlier videos).

Organizations may combine **VPN** with **SD-WAN**:

- **Software-defined wide area network (SD-WAN)** is a virtual WAN approach to connect users to applications across locations and long distances with security features integrated into modern architectures (per course summary).

## Remote access VPN vs site-to-site VPN

### Remote access VPN

- Connects an **individual device** to a **VPN server** through the internet.
- Encrypts/decrypts traffic for that device’s session.

### Site-to-site VPN

- Connects **entire networks** (for example, offices/locations).
- Common for global organizations.
- **IPsec** is commonly used to build encrypted tunnels between sites.
- Trade-off: can be **more complex** to configure/manage than remote access VPNs.

## VPN protocols: WireGuard vs IPsec

Both are **VPN protocols** (rules for how encrypted tunnels operate).

### WireGuard

- Designed to be **fast** and comparatively **simple** to deploy/maintain.
- **Open source**
- Often highlighted for performance and smaller codebase (per course)
- Can be used for **site-to-site** and **client/server** style connections

### IPsec

- Long-established VPN protocol suite used to **encrypt and authenticate** packets for secure tunnels.
- Broad OS/vendor support due to long history
- Often considered **older and more complex** than WireGuard; some environments prefer it for maturity and compatibility

## Key takeaways

- Proxies add policy and isolation between clients and services; forward vs reverse roles matter.
- VPNs support both **user remote access** and **site-to-site** network extension; **IPsec** is common for site-to-site.
- **WireGuard** and **IPsec** are two protocol options with different trade-offs (speed/simplicity vs maturity/ecosystem).
- Many organizations blend **VPN** with **SD-WAN** capabilities for modern distributed connectivity.
