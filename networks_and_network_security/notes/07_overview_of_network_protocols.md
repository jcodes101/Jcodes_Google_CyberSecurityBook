# Overview of network protocols

## What a network protocol is

A **network protocol** is a set of rules used by two or more devices on a network to describe the **order of delivery** and the **structure of data**.

- Protocols act like a **common language** for devices.
- They tell receiving devices **how to interpret** and **what to do with** transmitted data.
- Security analysts need to understand both **how protocols work** and their **security implications**.

Example security implication:

- A malicious actor could abuse **DNS** to redirect traffic from a legitimate site to a malicious one.

---

## Three categories of network protocols

This reading groups protocols into three broad categories:

1. **Communication protocols**
2. **Management protocols**
3. **Security protocols**

You do **not** need to memorize every protocol used on networks, but entry-level analysts should know the core ones below.

---

## 1) Communication protocols

Communication protocols govern how information is exchanged in network transmission.

They define:

- How data is transmitted between devices
- The timing of communication
- How lost data may be recovered

### Transmission Control Protocol (TCP)

**TCP** is an internet communication protocol that allows two devices to form a connection and stream data.

#### TCP three-way handshake

1. **SYN**: the client sends a synchronize request
2. **SYN/ACK**: the server acknowledges the request
3. **ACK**: the client acknowledges back, establishing the connection

In the TCP/IP model, **TCP** operates at the **transport layer**.

### User Datagram Protocol (UDP)

**UDP** is a **connectionless** protocol that does **not** establish a connection before transmission.

- Less reliable than TCP
- Faster / lower overhead for time-sensitive use cases
- Often used when speed matters more than guaranteed delivery

Example from the reading:

- **DNS** requests often use **UDP**

In the TCP/IP model, **UDP** operates at the **transport layer**.

### Hypertext Transfer Protocol (HTTP)

**HTTP** is an **application-layer** protocol used for communication between clients and website servers.

- Uses **port 80**
- Considered **insecure**
- Frequently replaced by **HTTPS**

In the TCP/IP model, **HTTP** operates at the **application layer**.

### Domain Name System (DNS)

**DNS** translates internet **domain names** into **IP addresses**.

Typical flow:

1. A client requests a website by name
2. A DNS server looks up the corresponding IP address
3. The client can then contact the correct server

- Normally uses **UDP port 53**
- Can switch to **TCP** when the reply is large

In the TCP/IP model, **DNS** operates at the **application layer**.

---

## 2) Management protocols

Management protocols are used to **monitor** and **manage** network activity.

They help with:

- Error reporting
- Performance visibility
- Device management

### Simple Network Management Protocol (SNMP)

**SNMP** is used for monitoring and managing devices on a network.

Examples of what SNMP can do:

- Reset a password on a network device
- Change a baseline configuration
- Request reports about bandwidth usage

In the TCP/IP model, **SNMP** operates at the **application layer**.

### Internet Control Message Protocol (ICMP)

**ICMP** is used by devices to report **data transmission errors** and **network status** information.

It is commonly used for:

- Troubleshooting connectivity
- Troubleshooting latency
- Supporting tools like **`ping`**

In the TCP/IP model, **ICMP** operates at the **internet layer**.

---

## 3) Security protocols

Security protocols help ensure that data is sent and received **securely** across a network.

They commonly rely on **encryption** to protect data **in transit**.

### Hypertext Transfer Protocol Secure (HTTPS)

**HTTPS** is the secure version of **HTTP**.

- Uses **SSL/TLS** encryption
- Helps prevent unintended readers from viewing transmitted data
- Uses **port 443**

In the TCP/IP model, **HTTPS** operates at the **application layer**.

### Secure File Transfer Protocol (SFTP)

**SFTP** is a secure protocol used to transfer files over a network.

- Uses **SSH**
- Typically uses **TCP port 22**
- Commonly used with **cloud storage**

The reading notes that **SSH** uses **AES** and other encryption methods to protect transmissions.

In the TCP/IP model, **SFTP** operates at the **application layer**.

---

## Important note about encryption

Even when traffic is encrypted, encryption does **not** hide everything.

- Encryption protocols do **not** conceal the **source IP address**
- They also do **not** conceal the **destination IP address**

This means an attacker who intercepts traffic may still learn basic metadata about the communication.

## Key takeaways

- Protocols are the shared rules that let devices communicate.
- Analysts should know the core protocols in the **communication**, **management**, and **security** categories.
- Understanding protocol behavior helps analysts investigate vulnerabilities, interpret traffic, and reduce the chance of future attacks.
