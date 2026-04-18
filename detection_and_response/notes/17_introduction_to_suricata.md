# Introduction to Suricata

**Suricata** is an **open-source** **intrusion detection system (IDS)**, **intrusion prevention system (IPS)**, and **network analysis** tool.

---

## Three main ways to use Suricata

### 1) Intrusion detection system (IDS)

As a **network-based IDS (NIDS)**, Suricata monitors **network traffic** and **alerts** on suspicious activity and intrusions.

Suricata can also run in a **host-based IDS (HIDS)** style configuration to monitor **system and network activity** of a **single host** (for example, one computer).

### 2) Intrusion prevention system (IPS)

Suricata can operate as an **IPS** to **detect and block** malicious activity and traffic. **IPS mode** requires **extra configuration** (for example, explicitly enabling IPS behavior) beyond a passive IDS deployment.

### 3) Network security monitoring (NSM)

In **NSM** mode, Suricata supports safety and visibility by **producing** and **storing** useful **network logs**. It can:

- analyze **live** network traffic  
- analyze existing **packet capture** files  
- create **full** or **conditional** packet captures  

Uses include **forensics**, **incident response**, and **testing or tuning signatures**—for example, trigger an alert and capture the related live traffic to refine detection logic.

---

## Rules and signatures

**Rules** (often called **signatures**) describe **patterns**, **behavior**, or **conditions** in traffic that may indicate malicious activity. In Suricata, **rule** and **signature** are commonly used **interchangeably**.

Analysts use signatures—patterns tied to malicious activity—to **detect** and **alert**. Rules can also add **context** and visibility to help spot threats or weaknesses.

Suricata’s detection here is **signature-based**: match activity to a defined pattern, then take the configured action.

### Three parts of a signature

1. **Action** — what to do when traffic matches (examples: `alert`, `pass`, `drop`, `reject`).  
2. **Header** — **network** match criteria such as source/destination **IP**, source/destination **port**, **protocol**, and **direction**.  
3. **Rule options** — additional tests and metadata (messages, byte matching, flow state, `sid`, `rev`, etc.).

**Illustrative example** (structure only; not a real threat rule):

```text
alert tcp $HOME_NET any -> $EXTERNAL_NET 443 (
    msg:"Example: outbound TLS connection";
    flow:established,to_server;
    sid:1000001;
    rev:1;
)
```

**Rule options ordering:** Options have a defined **syntax and order** requirements; **reordering** options can change how the rule is interpreted—follow Suricata documentation and validated examples.

**Note:** **Rule file order** (the sequence rules appear in configuration) matters for how Suricata evaluates them. Suricata also applies a **default action precedence** when multiple rules could apply: **`pass`**, then **`drop`**, then **`reject`**, then **`alert`**. When **conflicting** actions match the same packet (for example both **drop** and **alert**), this ordering affects the **final verdict**.

---

## Custom rules

Suricata ships with **community** and **vendor** rule sets, but teams usually **tune**, **disable**, or **author** rules for their environment.

There is **no** universal rule set: infrastructure and risk differ. Teams should **test** changes in non-production or monitored pilots to reduce **false positives** while keeping coverage.

Strong custom rules help you **leverage** detection tooling fully and reduce alert noise.

---

## Configuration: `suricata.yaml`

Before deployment, tools must be **configured**. A **configuration file** defines how an application behaves.

Suricata’s primary configuration file is **`suricata.yaml`**, which uses **YAML** syntax and structure.

---

## Log files: `eve.json` vs `fast.log`

When alerts fire, Suricata commonly produces:

### `eve.json` (preferred for analysis and SIEM)

The **standard** Suricata log in **JSON**. It includes rich **metadata** about events and alerts.

Example field: **`flow_id`** — correlates related logs or alerts to **one network flow**, which simplifies traffic analysis.

**Use cases:** deeper investigation, **parsing**, **SIEM ingestion**.

### `fast.log` (minimal / legacy)

Records **minimal** alert data—basic **IP** and **port** details.

**Use cases:** simple logging or quick human scans.

**Not** ideal as the sole source for **incident response** or **threat hunting** compared to `eve.json`.

**Summary:** `fast.log` is **sparse**; `eve.json` is **verbose** and structured for tooling.

---

## Key takeaways

- Suricata supports **IDS**, **IPS**, and **NSM** roles from one engine (with correct mode and wiring).  
- **Rules/signatures** combine **action**, **header**, and **options**; understand **option order** and **rule precedence** (`pass` → `drop` → `reject` → `alert`).  
- **Customize and test** rules for your environment.  
- Configure via **`suricata.yaml`**; prefer **`eve.json`** for rich, SIEM-friendly telemetry (including **`flow_id`**).
