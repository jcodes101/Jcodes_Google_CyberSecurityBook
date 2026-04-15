# Network devices and LAN architecture

## Networks vs network devices

**The network** is the overall **infrastructure** that lets devices **communicate** with each other.

**Network devices** are specialized equipment—such as **routers** and **switches**—that **manage** what is **sent** and **received** over that infrastructure. End-user gear (**computers**, **phones**) **attach** to the network **through** these devices.

### How traffic moves

After a device **connects** (wired or wireless), it sends **data packets**. Packets carry information about **source** and **destination** so data can be **routed** between devices.

---

## Endpoints: devices and desktop computers

Most users know **PCs**, **laptops**, **phones**, and **tablets**.

Each host typically has:

- A **unique MAC address** and **IP address** (identity on the network).  
- A **network interface** that **sends** and **receives** packets.  
- Connection by **Ethernet cable** or **Wi‑Fi**.

---

## Firewalls

A **firewall** is a **network security device** that **monitors** traffic **to** and **from** your network—often described as a **first line of defense**.

- Can **allow** or **block** traffic based on **rules** the **organization** defines.  
- Often sits between the **trusted internal** network and **untrusted** external networks (e.g., the **internet**).  
- **Not** the only control—defense is **layered**.

---

## Servers and the client–server model

**Servers** provide **information** and **services** to other hosts on the network. Hosts that **consume** those services are **clients**.

**Client–server model (summary):**

- **Clients** send **requests** (information or services).  
- The **server** **fulfills** those requests.

**Examples from the course:**

- **DNS servers** — domain name lookups for websites.  
- **File servers** — store and retrieve files (often backed by storage/database).  
- **Mail servers** — handle corporate email.

---

## Hubs and switches (local traffic)

**Hubs** and **switches** both participate in **local** connectivity, but behave very differently.

### Hub

- Gives a **common connection point** for everything plugged into it.  
- **Repeats** traffic out to **all** ports (everyone sees everything on that segment).  
- **Security:** vulnerable to **eavesdropping**; not preferred on **modern** enterprise LANs.  
- Still seen in **small** or **limited** setups (e.g., some **home office** contexts).

### Switch (preferred on most LANs)

- **Forwards** frames to the **intended** device based on **destination** information.  
- Keeps a **MAC address table** mapping **MAC → switch port** and forwards accordingly.  
- Operates at the **data link layer** in the **TCP/IP** model.  
- Improves **performance** and **security** compared with hubs.

---

## Routers

**Routers** **connect** different **networks** and **forward** traffic using **IP** addressing (especially the **destination network** in the **IP header**).

- Work at the **network layer** in the **TCP/IP** model.  
- Let devices on **different** networks talk to each other.  
- Forward packet-by-packet toward the **destination**, hop by hop.  
- May include **firewall-like** features to **allow** or **deny** traffic entering the **private** / **LAN** side—reducing risk to the **local area network**.

---

## Modems and wireless access points

### Modem

- Usually connects **home or office** to an **ISP**.  
- ISPs deliver connectivity over **phone**, **coax**, **fiber**, etc.  
- Receives signals from the ISP side and converts them to a form suitable for the **local link** to your **router** (router then serves the **LAN**).

**Note:** Large **enterprise** networks often use **other broadband / WAN** designs instead of a consumer-style **modem** for high volume.

### Wireless access point (WAP)

- Sends and receives **digital** signals over **radio** (Wi‑Fi).  
- Devices with **wireless adapters** associate to the **AP** using **Wi‑Fi** standards.  
- Traffic then goes to **routers** / **switches** and onward toward its **final destination**.

---

## Network diagrams for security analysts

**Network diagrams** are **maps**: devices as **icons** and **lines** showing **how** they connect.

**Why they matter:**

- **Visualize** **architecture** and **trust boundaries**.  
- **Plan** segmentation, monitoring, and **firewall** rules.  
- **Communicate** with admins and **incident** responders.

---

## Course diagram notes (text summary)

In the course’s example **home/small** style layout:

- A **router** reaches the **internet** through a **modem** supplied by the **ISP**.  
- A **firewall** **inspects** **inbound** and **outbound** traffic.  
- The **router** delivers traffic to **LAN** devices: PCs, laptops, phones, tablets, printers, etc.  
- A **server** may act as a **file server**—**all** those devices might **access** shared files there.  
- A **switch** is **optional** but adds **ports** and **Ethernet** capacity.  
- The course also shows **two routers** off a **switch** for **load balancing** to improve **performance** (more advanced design).

**Visual walkthrough (emoji version):** [02_lan_connection_diagram_emojis.md](02_lan_connection_diagram_emojis.md)

---

## Key takeaways

- **Client–server:** clients **request**; servers **serve**.  
- **Network devices** include **routers**, **workstations**, **servers**, **hubs**, **switches**, **modems**, **firewalls**, **access points**—each role is different.  
- **Security analysts** use **network diagrams** to understand and **harden** architecture.
