# Operations at the network layer (IPv4 packets and IPv4 vs IPv6)

## What the network layer does

Functions at the **network layer** organize **addressing** and **delivery** of data from a **source host** to a **destination host** across interconnected networks.

- Traffic is often forwarded **from router to router** across the internet until it reaches the **destination network** associated with the destination **IP address**.
- The **destination IP address** sits in the **header** of each packet. Routers consult **routing tables** along the path to decide **next hops** toward that destination.

## IP packets, addressing, and names (TCP vs UDP)

- **All** these IP-layer packets carry **IP addresses** in their headers.
- A packet at this layer is commonly called an **IP packet**; the course also uses these terms:
  - **IP packet** — often used when describing **TCP**-carried traffic (conceptually the IP wrapper around the segment).
  - **Datagram** — often used when describing **UDP** traffic (**connectionless**).
- **Routers** use the **destination IP** (and routing information) to move traffic **from network to network**, based on fields in the **IP header** (not only the addresses).

### What else the IP header communicates

Beyond “where it’s going,” header information can include:

- **Source** IP address
- **Packet size** information
- Which **upper-layer protocol** carries the **payload** (the **data** portion)

---

## IPv4 packet structure (header + data)

An **IPv4** packet has **two** parts:

| Section | Role |
|---------|------|
| **Header** | Routing and control metadata (what devices use to forward and interpret the packet) |
| **Data** | Payload — e.g., website content, email body — carried for higher-layer protocols |

### Header size

- The **IPv4 header** is defined by the **IPv4** protocol.
- **Size**: typically **20 to 60 bytes** total.
  - The **first 20 bytes** are **fixed** baseline fields (includes source/destination addresses, lengths, etc.).
  - **0–40 optional bytes**: the **options** field (when present).

### Maximum packet size

- The **data** section length can vary widely.
- **Maximum** possible **entire IPv4 packet** size (**header + data**): **65,535 bytes**.

---

## IPv4 header: 13 fields (what each is for)

| Field | What it does (course summary) |
|-------|-------------------------------|
| **Version (VER)** | 4 bits — identifies the **IP version** (IPv4 in these examples). |
| **IP Header Length (HLEN / IHL)** | Indicates **where the header ends** and the **data** begins (header length). |
| **Type of Service (ToS)** | Helps routers **prioritize** traffic to support **quality of service (QoS)**. |
| **Total Length** | Total length of the **entire IPv4 packet** (**header + data**). Max **65,535** bytes. |
| **Identification** | When a large packet is **fragmented**, fragments share an ID so the receiver can **reassemble** the original. |
| **Flags** | Tells routers more about **fragmentation** (e.g., whether fragmentation occurred / more fragments exist). |
| **Fragmentation Offset** | Indicates **where** this fragment fits inside the **original** packet for reassembly. |
| **Time to Live (TTL)** | A **hop counter** decremented by routers; at **0** the packet is **dropped** and **ICMP Time Exceeded** may be sent to the source (prevents infinite looping). |
| **Protocol** | Identifies which **protocol** is used for the **data** portion (payload type). |
| **Header Checksum** | Detects **header corruption**; corrupted headers are typically **discarded**. |
| **Source IP Address** | IPv4 address of the **sending** host. |
| **Destination IP Address** | IPv4 address of the **intended destination** host/network context. |
| **Options** | Optional features (the course notes **security-related** options can exist here when **HLEN > 5**). |

---

## IPv4 vs IPv6 (why IPv6 exists and what changes)

### Why IPv6 was developed

- The internet outgrew **IPv4 address space** over time (**IPv4 address exhaustion**).
- IPv6 was created to address exhaustion and related scaling concerns.

### Address format and space (high level)

| Topic | IPv4 | IPv6 |
|-------|------|------|
| **Format** | Four **decimal** numbers (**0–255**) separated by **periods** | Eight **hex** groups separated by **colons** |
| **Size** | **4 bytes** of address | **16 bytes** of address |
| **Address count (order of magnitude)** | Up to ~**4.3 billion** | Up to ~**340 undecillion** (340 with **36** zeros after it, per course wording) |

**Examples (course-style)**

- IPv4: `198.51.100.0`
- IPv6: `2002:0db8:0000:0000:0000:ff21:0023:1234`

**IPv6 compression rule (course note)**

- One or more consecutive **all-zero** groups can be written as **`::`**.
- Example rewrite: `2002:0db8::ff21:0023:1234`

### Header layout differences (course highlights)

- **IPv6 headers are simpler** than IPv4 in several ways.
- Fields like **IHL**, **Identification**, and **Flags** exist in **IPv4** but are **not** in the same form in IPv6 (fragmentation handling differs in practice).
- IPv6 adds a **Flow Label** field used to mark packets needing **special handling** along IPv6 paths.

### Security-relevant differences called out in the course

- IPv6 can enable **more efficient routing** in some designs.
- IPv6 helps reduce certain **private address collision** scenarios that can happen in IPv4 when two devices conflict locally.

---

## Key takeaways (especially for analysts)

Inspecting IP headers helps answer security questions such as:

- **Where** did this packet come from (**source IP**)?
- **Where** is it going (**destination IP**)?
- **What** is the intended upper-layer handling (**protocol** field)?
- Is traffic being **fragmented** (**identification / flags / offset**)?
- Is the packet plausible (**TTL**, **length**, **checksum**)?

Understanding these fields supports triage decisions when reviewing captures, firewall logs, or SIEM-enriched network events.
