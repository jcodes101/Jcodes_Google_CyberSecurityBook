# LAN connection diagram (emoji visualization)

This matches the **course story**: internet → **modem (ISP)** → **router** → **firewall** boundary → **LAN** with **server**, **switch**, **WAP**, and **end devices**. Optional **dual routers** on a **switch** for **load balancing** is included as in the reading.

---

## 1. Big picture — traffic flows downward “toward your stuff”

```
                         ┌─────────────────────────────────────────┐
                         │  🌐 INTERNET (untrusted, wide area)    │
                         │     billions of hosts / cloud / WAN      │
                         └───────────────────┬─────────────────────┘
                                             │
                                             │  packets in/out
                                             ▼
                         ┌─────────────────────────────────────────┐
                         │  📡 MODEM (ISP)                         │
                         │  ISP link: fiber / coax / DSL / etc.    │
                         │  converts ISP signal ↔ digital for edge   │
                         └───────────────────┬─────────────────────┘
                                             │
                                             ▼
                         ┌─────────────────────────────────────────┐
                         │  🔥 FIREWALL (policy checkpoint)        │
                         │  1st line of defense; allow / deny rules │
                         │  often: between trusted LAN & Internet   │
                         └───────────────────┬─────────────────────┘
                                             │
                                             ▼
                         ┌─────────────────────────────────────────┐
                         │  🛰️ ROUTER (routes by IP / networks)    │
                         │  chooses paths; may include firewall feat.│
                         └───────────────────┬─────────────────────┘
                                             │
              ┌──────────────────────────────┼──────────────────────────────┐
              │                              │                              │
              ▼                              ▼                              ▼
    ┌──────────────────┐         ┌──────────────────┐         ┌──────────────────┐
    │ 🖥️ SERVER        │         │ 🔀 SWITCH        │         │ 📶 WAP (Wi‑Fi)   │
    │ (e.g. file share)│         │ more ports; MAC  │         │ radio → Wi‑Fi    │
    │ clients request │         │ learning; VLANs  │         │ phones / laptops │
    └────────┬─────────┘         └────────┬─────────┘         └────────┬─────────┘
             │                            │                            │
             │              ┌─────────────┴─────────────┐              │
             │              │   optional load balance  │              │
             │              ▼                           ▼              │
             │     ┌──────────────┐           ┌──────────────┐       │
             │     │ 🛰️ Router A  │           │ 🛰️ Router B  │       │
             │     │ (LB path 1)  │           │ (LB path 2)  │       │
             │     └──────┬───────┘           └──────┬───────┘       │
             │            │                        │               │
             └────────────┴────────────────────────┴───────────────┘
                                    │
                    ┌───────────────┼───────────────┐
                    ▼               ▼               ▼
              💻 laptop      📱 phone       🖨️ printer
              (Ethernet or   (Wi‑Fi via    (LAN host)
               switch port)   WAP)
```

**Legend (quick)**

| Emoji | Idea |
|-------|------|
| 🌐 | Internet / WAN |
| 📡 | Modem — ISP handoff |
| 🔥 | Firewall — policy / inspection |
| 🛰️ | Router — IP forwarding between networks |
| 🔀 | Switch — LAN switching, MAC tables |
| 🖥️ | Server — services for **clients** |
| 📶 | Wireless AP — Wi‑Fi access |
| 💻📱🖨️ | Clients — request services, send/receive packets |

---

## 2. Same idea — linear “story” (easy to memorize)

🌐 **Internet**  
 ↓ (WAN packets)  
📡 **Modem (ISP)** — link into your site  
 ↓  
🔥 **Firewall** — allow/deny, monitor  
 ↓  
🛰️ **Router** — route to correct **network** / next hop  
 ↓ splits to LAN  
 • 🖥️ **Server** (files, DNS, mail, …) — **clients** ask, server answers  
 • 🔀 **Switch** — wired devices + optional **🛰️🛰️ two routers** for **load balancing**  
 • 📶 **WAP** — Wi‑Fi for 📱💻 **without cables**  
 ↓  
💻 📱 🖨️ **Devices** — each has **MAC** + **IP**, NIC sends/receives **packets**

---

## 3. Client–server on the LAN (emoji micro-diagram)

```
   💻 client ──request──► 🖥️ server
              ◄──response──
```

- **Clients** (laptops, phones, …) **request**.  
- **Server** **performs** the work (DNS lookup, file read, mail, …).

---

## 4. Hub vs switch (why switches won)

| | 🔁 Hub (legacy / small) | 🔀 Switch (typical LAN) |
|--|-------------------------|-------------------------|
| Sends to | **All** ports (broadcast-like behavior) | **Only** the **intended** port (uses **MAC** table) |
| Risk | Easier **eavesdropping** on that segment | **Better** isolation / performance |

---

## Related

- [01_network_devices_and_lan_architecture.md](01_network_devices_and_lan_architecture.md) — full prose notes  
- [../README.md](../README.md) — folder index  
