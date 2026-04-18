# Packets, protocol analyzers, and packet captures (p-caps)

Detecting network intrusions often starts at the packet level. Packets form the basis of information exchange over a network, and they can provide valuable context for investigations.

---

## Packets (what they are)

A **data packet** is a basic unit of information that travels from one device to another. When you visit a website or upload a file, data is broken into multiple packets, routed to the destination, then reassembled.

Packets commonly include three components:

### Header

The header contains routing and delivery information. A packet can include multiple headers depending on the protocols in use (for example: Ethernet, IP, TCP).

Headers can include:
- source and destination IP addresses
- packet length
- protocol
- packet identification numbers

### Payload

The payload is the data being delivered.

Example: if you upload an image to a website, the payload contains the image data.

### Footer (trailer)

The footer (trailer) can include error-checking information (commonly in Ethernet). Some protocols (like IP) do not use footers.

Note: packet analyses may not always display footer information depending on network configurations.

---

## Network protocol analyzers (packet sniffers)

Network protocol analyzers are tools designed to capture and analyze network traffic. Common examples include:

- **tcpdump**
- **Wireshark**
- **TShark**

Beyond security investigations, these tools can also support:
- network statistics (bandwidth/speed)
- troubleshooting performance issues (slowdowns)

They can also be abused by attackers to capture sensitive data (like login credentials), which is why authorization and safe handling matter.

---

## How packet sniffers capture traffic (NIC + capture modes)

Packet sniffers use software plus hardware capabilities to collect traffic from a **network interface card (NIC)**.

By default, a NIC only listens to traffic addressed to it. To capture all visible traffic on a segment, interfaces can be switched into a special capture mode:

- **monitor mode** (commonly referenced for wireless interfaces)
- **promiscuous mode** (commonly referenced more generally)

Important limitations:
- This exposes your device to additional risk because it can capture sensitive information.
- Capturing “everything” usually only applies to the traffic visible on the segment where the analyzer is placed; placement matters for what you can observe.

---

## Packet sniffing and p-cap files

**Packet sniffing** is the practice of capturing and inspecting data packets across a network.

A **packet capture (p-cap)** is a file containing packets intercepted from an interface or network. Analysts can open and filter p-caps to focus on what’s relevant (for example: traffic to/from a specific IP).

Note: intercepting private network communications without permission is illegal in many places. Use these tools only with appropriate authorization.

---

## Common packet capture libraries and formats

Different tools and platforms may prefer different packet capture formats:

- **Libpcap**: packet capture library commonly used on Unix-like systems (Linux/macOS). Tools like `tcpdump` often use libpcap formats by default.
- **WinPcap**: older Windows packet capture library; less common today.
- **Npcap**: commonly used on Windows; associated with the Nmap ecosystem and used by modern tooling.
- **PCAPng**: “next generation” p-cap format that can capture packets and store additional data in a single file.

Pro tip: analyzing your home network (ethically and safely) can be a good way to practice reading p-caps and using filters.

---

## Key takeaways

- Packets contain **headers** (routing), **payloads** (data), and sometimes **footers** (error checking).
- Packet sniffers (e.g., **tcpdump/Wireshark**) help analysts observe and investigate network communications.
- Capturing traffic often requires special NIC modes (monitor/promiscuous) and careful placement to see the right segment.
- **p-caps** are packet capture files; filtering them is a core investigation skill.
- Know common capture formats: **Libpcap**, **WinPcap**, **Npcap**, and **PCAPng**.

