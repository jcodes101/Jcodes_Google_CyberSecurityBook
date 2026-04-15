# NAT, DHCP, ARP, and common remote/email protocols

## Network Address Translation (NAT)

Devices on a home/office LAN usually use **private IP addresses** for local communication.

To communicate with the public internet, traffic typically exits through a router/firewall that uses a **public IP address**.

NAT is the process where the edge device:

- Replaces a private **source IP** with a public IP for outbound traffic
- Performs the reverse mapping for return traffic

NAT is generally configured on a **router** or **firewall**.

### Private vs public IP (course framing)

**Private IP addresses**:

- Assigned inside private networks (commonly via router/DHCP)
- Unique within the local/private scope
- RFC1918 private ranges:
  - `10.0.0.0` - `10.255.255.255`
  - `172.16.0.0` - `172.31.255.255`
  - `192.168.0.0` - `192.168.255.255`

**Public IP addresses**:

- Routable on the global internet
- Assigned through ISP/public allocation processes
- Globally unique (public routing context)

---

## Dynamic Host Configuration Protocol (DHCP)

**DHCP** is a management-family protocol used to automatically configure devices on a network.

DHCP can provide:

- A unique IP address
- DNS server information
- Default gateway information

Ports:

- **UDP 67**: DHCP server
- **UDP 68**: DHCP client

In the TCP/IP model, DHCP is treated as an **application-layer** protocol.

---

## Address Resolution Protocol (ARP)

**ARP** resolves IP-to-MAC mappings on local networks.

- IP addresses can change (e.g., DHCP leases), while a NIC’s MAC is hardware-bound.
- ARP helps devices discover the destination MAC for local delivery.
- Devices cache mappings in an **ARP cache**.

Port note:

- **ARP has no TCP/UDP port number**, because it operates at the network access/link context, not the application layer.

---

## Telnet and SSH (remote access)

### Telnet

- Remote command-line access protocol
- Sends information in **clear text**
- Not considered secure
- Uses **TCP 23**

### SSH (Secure Shell)

- Secure remote access protocol
- Supports encrypted communication and secure authentication
- Common replacement for Telnet
- Uses **TCP 22**

---

## Mail protocols: POP3, IMAP, SMTP

### POP3 (Post Office Protocol v3)

Used to retrieve incoming mail from a mail server to a local device.

- Unencrypted: **TCP/UDP 110**
- Encrypted (SSL/TLS): **TCP/UDP 995**

Behavior to remember:

- Mail is downloaded locally before full reading
- Messages may or may not be removed from the server
- Multi-device sync is less flexible than IMAP

### IMAP (Internet Message Access Protocol)

Used for incoming mail while keeping messages on the server.

- Unencrypted: **TCP 143**
- Encrypted (TLS): **TCP 993**

Benefits:

- Better multi-device synchronization
- Users can start reading before full local download

### SMTP (Simple Mail Transfer Protocol)

Used to send and route email from sender to recipient.

- Unencrypted: **TCP/UDP 25**
- Encrypted submission (TLS): **TCP/UDP 587**

SMTP commonly works with MTA software that can query DNS to route mail toward the proper destination infrastructure.

---

## Protocols and port numbers: analyst perspective

Port numbers help destination systems decide which service should process incoming data.

Security teams also use ports in controls and detection, for example:

- Firewall allow/deny rules by protocol + port
- Triage of suspicious activity on high-risk ports
- Validation that encrypted vs unencrypted services are configured as intended

## Key takeaways

- NAT allows many private hosts to access the internet through public addressing at the network edge.
- DHCP, ARP, Telnet/SSH, and mail protocols are core entry-level analyst knowledge.
- You should know both **where these protocols fit in the TCP/IP model** and the **common ports** tied to each one.
