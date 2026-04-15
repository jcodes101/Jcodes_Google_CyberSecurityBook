# The TCP/IP model vs. the OSI model

## Why these models matter (for security + troubleshooting)

The **TCP/IP** model is a framework used to visualize how data is **organized** and **transmitted** across a network.

The **OSI** model is a standardized concept that describes the **seven layers** computers use to communicate and send data.

Both models help network engineers and security analysts:

- **Conceptualize** network processes
- **Communicate** where disruptions or security threats may have occurred (“Which layer was involved?”)
- **Analyze** incidents by correlating symptoms with the protocols/processes tied to a layer

Some organizations lean heavily on **TCP/IP**, while others prefer **OSI**. As an analyst, you should be familiar with **both**.

## TCP/IP model (4 layers)

The TCP/IP model has four layers:

1. **Network access layer**
2. **Internet layer**
3. **Transport layer**
4. **Application layer**

When analyzing network events, security professionals can often determine what layer (or layers) an attack “lived in” based on which processes/protocols were involved.

### 1) Network access layer (sometimes called the data link layer in older texts)

Focus: **creating/transmitting frames** on the local side of the network and interfacing with hardware.

- **Hardware and media examples**: hubs, modems, cables, wiring
- **Key protocol**: **ARP (Address Resolution Protocol)**
  - ARP maps **IP addresses → MAC addresses** for devices on the same physical network.

### 2) Internet layer (sometimes called the network layer)

Focus: **delivering packets to a destination host** that may be on a **different network**.

- **IP addresses** are attached to packets to identify sender/receiver locations.
- **Routers** use IP information to route traffic between networks.

Common internet-layer protocols:

- **IP (Internet Protocol)**: routing packets between networks; relies on **TCP/UDP** to deliver to the correct service; TCP can retransmit lost/corrupt data.
- **ICMP (Internet Control Message Protocol)**: error/status information for troubleshooting (drops, connectivity issues, redirects, etc.).

### 3) Transport layer

Focus: delivering data **between systems** and controlling **flow** across the network.

- **Segmentation**: large transmissions are split into smaller segments for transport, then **reassembled** at the destination (so upper layers can process the full message).
- **TCP** and **UDP** are transport protocols.
- **Ports** identify destination services (commonly in TCP/UDP headers).

### 4) Application layer

Focus: **requests and responses** for internet services used by applications.

Examples commonly discussed:

- **HTTP / HTTPS** (web)
- **SMTP** (email sending as used by mail applications)
- **DNS** (name resolution so browsers can map domains → IPs)

Application-layer protocols depend on lower layers to move bits across the network.

---

## OSI model (7 layers), top to bottom

The OSI model labels seven layers:

**Application → Presentation → Session → Transport → Network → Data link → Physical**

### Layer 7: Application layer

The application layer includes processes that directly involve the **end user** day-to-day.

- Includes networking protocols that software applications use to connect users to network services.
- Typical examples referenced in coursework:
  - **HTTP/HTTPS** for web browsing
  - **SMTP** for email applications (send/receive mail-related information)
  - **DNS** to translate domain names into IP addresses (identifying the server hosting the site)

### Layer 6: Presentation layer

Presentation layer functions focus on **data translation** and preparing data so applications can understand it.

- Handles formatting differences between systems (sender vs receiver may use different representations).
- Common functions include **encryption**, **compression**, and ensuring the character/code representation can be interpreted on the receiving system.
- Example called out in the reading: **SSL/TLS encryption** used with **HTTPS** to protect data between browsers and web servers.

### Layer 5: Session layer

A **session** is an established connection between devices that remains open while data is transferred.

Session layer responsibilities include:

- Keeping the session **open** during transfers and **terminating** it when done
- **Authentication** and **reconnection** behaviors
- **Checkpoints** during transfers so a disrupted session can resume near the last known good point
- Interacts “up” with presentation-layer processes and “down” with the transport layer

### Layer 4: Transport layer

The transport layer delivers data between devices and manages:

- **Segmentation** (splitting transmissions into manageable pieces)
- **Reassembly** at the destination before handing data up to the session layer
- **Flow control** so transfer rates match what the receiver can handle
- **TCP** and **UDP** operate here

### Layer 3: Network layer

The network layer focuses on delivering traffic **between networks** using logical addressing.

- Receives frames from the data link layer and forwards toward the intended destination based on addresses in packets.
- **IP addresses** guide routers on where to send packets across network boundaries.

### Layer 2: Data link layer

The data link layer organizes sending/receiving within a **single network** (local networking context).

- Common “local networking” touchpoints include **switches** and **NICs** (network interface cards).
- Example protocols mentioned in the reading (varies by environment, but these are named): **NCP**, **HDLC**, **SDLC**.

### Layer 1: Physical layer

The physical layer corresponds to **physical hardware** involved in transmission.

- Examples: hubs, modems, cables, wiring
- Data is represented as a stream of **bits (0s and 1s)** that travel across physical media (Ethernet/coax/etc.), then move upward into higher layers after reception.

---

## TCP/IP model vs OSI model (how they relate)

- **OSI**: **7 layers**—very common for describing problems precisely.
- **TCP/IP**: **4 layers**—a simplified grouping aligned strongly with the real internet protocol suite.
- **Relationship**: TCP/IP’s **application layer** broadly maps to OSI **layers 5–7** combined; TCP/IP’s **network access** broadly maps to OSI **layers 1–2** combined.

### Quick mapping (study-friendly)

| OSI layer (7) | Typical OSI layer names | Maps into TCP/IP layer (4) |
|---------------|-------------------------|---------------------------|
| 7 | Application | Application |
| 6 | Presentation | Application |
| 5 | Session | Application |
| 4 | Transport | Transport |
| 3 | Network | Internet |
| 2 | Data link | Network access |
| 1 | Physical | Network access |

## Key takeaways

- Both models are **conceptual** and help professionals design and reason about **data transmission** between systems.
- **OSI** provides a **7-layer** communication model for discussing issues/threats with teammates.
- **TCP/IP** provides a **4-layer** model that maps closely to how modern internet protocols are implemented.
- Analysts use both to **locate disruptions** and **explain incidents** in terms of affected processes and protocols.

