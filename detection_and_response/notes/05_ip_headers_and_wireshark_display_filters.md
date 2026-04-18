# Internet Protocol (IP) and Wireshark display filters

Packets are the foundation of data exchange over networks, so detection and investigation often start at the packet level. **Internet Protocol (IP)** defines standards for **addressing and routing** packets between devices, forming the foundation for communication over the internet.

---

## IP basics

IP helps ensure packets reach their destination. Two versions are commonly used today:

- **IPv4**
- **IPv6**

Both versions use different header structures that contain investigation-relevant fields.

---

## IPv4 header (13 fields)

**Version**: Indicates the IP version (IPv4).

**Internet Header Length (IHL)**: Length of the IPv4 header (including Options).

**Type of Service (ToS)**: Packet priority/handling information.

**Total Length**: Total length of the entire IP packet (header + data).

**Identification**: Unique identifier used for fragmented packets so fragments can be reassembled.

**Flags**: Fragmentation control (whether fragmented and whether more fragments follow).

**Fragment Offset**: Fragment sequencing information.

**Time to Live (TTL)**: Limits how long the packet can circulate (prevents indefinite forwarding).

**Protocol**: Identifies the protocol used for the data portion (e.g., TCP/UDP/ICMP).

**Header Checksum**: Error-checking value for the header.

**Source Address**: Sender’s IP address.

**Destination Address**: Receiver’s IP address.

**Options**: Optional field; can apply additional options (including some security-related options).

---

## IPv6 header (8 fields)

IPv6 adoption is increasing due to its much larger address space.

**Version**: Indicates the IP version (IPv6).

**Traffic Class**: Similar to IPv4 ToS; prioritization/class for delivery.

**Flow Label**: Identifies packets belonging to a flow (sequence of packets from a specific source).

**Payload Length**: Length of the data portion of the packet.

**Next Header**: Type of header that follows the IPv6 header (e.g., TCP).

**Hop Limit**: Similar to IPv4 TTL; limits how long a packet can travel before discard.

**Source Address**: Sender’s IPv6 address.

**Destination Address**: Receiver’s IPv6 address.

---

## Wireshark (packet analysis)

**Wireshark** is an open-source network protocol analyzer with a GUI. It displays packet header fields in a human-readable way and supports filtering to quickly find relevant packets in large captures.

---

## Wireshark display filters (basics)

Display filters let you filter packet capture views by almost any packet property (protocols, IPs, ports, fields, etc.).

### Comparison operators

Operators can be written as symbols or abbreviations:

| Operator type | Symbol | Abbreviation |
|---|---|---|
| Equal | `==` | `eq` |
| Not equal | `!=` | `ne` |
| Greater than | `>` | `gt` |
| Less than | `<` | `lt` |
| Greater than or equal to | `>=` | `ge` |
| Less than or equal to | `<=` | `le` |

Pro tip: combine with Boolean operators like `and` / `or`. Parentheses can group expressions.

### `contains` operator

Use `contains` to filter packets that contain an exact match string.

Example concept: filter HTTP content that contains the word `"moved"`.

### `matches` operator

Use `matches` to filter using a regular expression (regex) pattern.

---

## Common filter patterns

### Filter by protocol

Type the protocol name, for example:
- `dns`
- `http`
- `ftp`
- `ssh`
- `arp`
- `telnet`
- `icmp`

### Filter by IP address

- Any packet with an IP (either side):
  - `ip.addr == 172.21.224.2`
- Packets from a source:
  - `ip.src == 10.10.10.10`
- Packets to a destination:
  - `ip.dst == 4.4.4.4`

### Filter by MAC address

Filter Ethernet traffic by MAC:

- `eth.addr == 00:70:f4:23:18:c4`

### Filter by port

- UDP port (example DNS):
  - `udp.port == 53`
- TCP port (example SMTP):
  - `tcp.port == 25`

---

## Follow streams (reconstruct conversations)

Wireshark can “follow” a stream to reconstruct a protocol conversation (a sequence of request/response messages). This is useful when you need to understand the content and order of an exchange (for example, the details of an HTTP conversation).

---

## Key takeaways

- **IP** is foundational for routing/addressing packets; modern networks commonly use **IPv4** and **IPv6**.
- IPv4 and IPv6 headers contain fields that add investigative context (e.g., addresses, TTL/hop limit, protocol/next header).
- **Wireshark display filters** are essential for isolating relevant packets by protocol, IP, MAC, port, and more.
- “Follow stream” helps you understand full conversations instead of isolated packets.

