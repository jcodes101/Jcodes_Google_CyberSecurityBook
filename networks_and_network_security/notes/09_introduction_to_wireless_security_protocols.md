# Introduction to wireless communication and security protocols (Wi‑Fi)

## Wi‑Fi basics (what “Wi‑Fi” means)

Many people use “wireless internet” and “Wi‑Fi” interchangeably.

- **Wi‑Fi** refers to a set of standards that define communication for **wireless LANs**.
- “Wi‑Fi” is a marketing term originally commissioned by the **Wireless Ethernet Compatibility Alliance (WECA)**, now the **Wi‑Fi Alliance**.
- Wi‑Fi is based on the **IEEE 802.11** family of standards (so you may see Wi‑Fi referred to as **IEEE 802.11**).

## Why security analysts care

Wireless security protocols have evolved over time to address vulnerabilities. Analysts should recognize:

- What protocol is in use (WEP vs WPA vs WPA2 vs WPA3)
- The security strengths/weaknesses of each
- Why “older but still present” configurations are high risk

---

## Evolution of Wi‑Fi security protocols

### WEP (Wired Equivalent Privacy) — 1999

**WEP** was designed to provide privacy on wireless connections comparable to wired connections.

- Oldest common wireless security standard (introduced 1999)
- Largely out of use today
- Still important to recognize because:
  - Some routers shipped with WEP as a default and were never updated
  - Some devices are too old to support newer protocols
- Considered **high risk** because WEP encryption can be broken by attackers

### WPA (Wi‑Fi Protected Access) — 2003

**WPA** was created to replace WEP and address its weaknesses.

- Intended as a **transitional** protocol for backward compatibility with older hardware
- Key improvements (per reading):
  - Introduced **TKIP (Temporal Key Integrity Protocol)** to address weaknesses in WEP’s approach
  - Uses larger secret keys than WEP, making guessing harder
  - Includes a **message integrity check** (message authentication tag) to detect tampering or replay

#### WPA vulnerability highlighted: KRACK

WPA (and the reading notes the handshake weakness) can be vulnerable to **KRACK (Key Reinstallation Attack)**:

- An attacker interferes with the authentication handshake to force key reinstallation
- If an attacker can set a key to a weak value (e.g., all zeros), traffic may effectively be unencrypted

Because of significant vulnerabilities, WPA was replaced by WPA2.

### WPA2 — 2004

**WPA2** improved WPA by strengthening encryption and integrity:

- Uses **AES (Advanced Encryption Standard)**
- Uses **CCMP** (Counter Mode Cipher Block Chain Message Authentication Code Protocol) for encapsulation + message authentication/integrity
- Considered the major Wi‑Fi security standard for a long time

The reading notes WPA2 can still be vulnerable to **KRACK**, which helped drive the need for WPA3.

#### WPA2 modes: Personal vs Enterprise

**WPA2 Personal**:

- Best suited for home networks
- Easier setup than enterprise
- Uses a shared/global passphrase across devices and the access point
- Becomes unmanageable for organizations at scale

**WPA2 Enterprise**:

- Designed for business environments
- More complex setup
- Enables centralized control with individualized user access management
- Users don’t have direct access to the shared encryption keys, reducing key-recovery risk on endpoints

### WPA3 — 2018

**WPA3** is the modern secure Wi‑Fi protocol, growing in adoption as WPA3-capable devices become common.

Key differences highlighted in the reading:

- Addresses the handshake weakness associated with KRACK-style attacks present in WPA2
- Uses **SAE (Simultaneous Authentication of Equals)**, a password-authenticated key agreement method
  - Reduces the usefulness of captured traffic for offline password decoding attempts
- Stronger encryption defaults:
  - Uses **128-bit** encryption
  - WPA3-Enterprise can support optional **192-bit** encryption

---

## Key takeaways

- Wi‑Fi is based on **IEEE 802.11** standards and administered/marketed by the **Wi‑Fi Alliance** (formerly WECA).
- Wireless security evolved from **WEP → WPA → WPA2 → WPA3** to address real-world vulnerabilities.
- Analysts should recognize which protocol is used and treat legacy protocols (especially **WEP**) as high risk.
