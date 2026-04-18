# IDS placement: HIDS vs NIDS, and detection techniques

An **intrusion detection system (IDS)** monitors activity and **alerts** on possible intrusions. IDS helps organizations watch **systems** and **networks** for signs of malicious behavior.

Depending on **where** you deploy an IDS, it can be **host-based** or **network-based**.

---

## Host-based intrusion detection system (HIDS)

A **host-based IDS (HIDS)** monitors activity **on the host** where it is installed. It is typically deployed as an **agent** on that host.

A **host** is also called an **endpoint**—any device on a network (e.g., workstation, server).

**Typical use:** Agents on **many** endpoints to monitor for threats. The HIDS watches **internal** host activity (not just packets leaving the box) to spot **unauthorized** or **abnormal** behavior—for example installation of an **unauthorized application**. Events are **logged** and **alerts** are sent.

Beyond inbound/outbound traffic flows, HIDS may also monitor:

- **File systems**  
- **System resource** usage  
- **User** activity  
- Other host-local signals  

**Conceptual diagram (course):** A dotted boundary around **one** computer shows the HIDS only sees **local** activity on that machine.

---

## Network-based intrusion detection system (NIDS)

A **network-based IDS (NIDS)** **collects** and **monitors** **network traffic** and **network data**. NIDS software runs on a device placed at a **chosen** point in the network path you want to observe.

The NIDS **inspects** traffic from **multiple** devices on the segment. If it sees **malicious** network traffic, it **logs** the activity and **generates an alert**.

**Conceptual diagram (course):** A NIDS on a **server** (or sensor appliance) monitors communications **between** several computers on the network.

---

## Using HIDS and NIDS together

**HIDS + NIDS** gives a **multi-layered** view: **network-wide** patterns (NIDS) plus **per-host** behavior (HIDS). Together they support a more **complete** picture of activity in the environment.

---

## Detection techniques

IDS products commonly use two analysis styles: **signature-based** and **anomaly-based**.

### Signature-based analysis

**Signature analysis** (signature-based detection) matches activity to **patterns** associated with malicious behavior. A **signature** can be byte sequences, binary patterns, or specific values (e.g., an IP tied to known badness).

**Pyramid of Pain** (see note **09**) ranks IoC types; **IoCs** and **IoAs** can inform **targeted** signatures.

**Example:** An **anti-malware** signature encodes patterns linked to malware (including malicious **scripts**). The IDS watches for events that **match** the signature, then **logs** and **alerts**.

**Advantages**

- **Fewer false positives** on **known** threats—matching is explicit and efficient.

**Disadvantages**

- **Evasion:** Small changes to malware or traffic can produce a **new** signature attackers can slip past until signatures update.  
- **Maintenance:** New exploits require **new** signatures in the **database**.  
- **Unknown threats:** Cannot catch **brand-new** malware families or **zero-day** exploits (previously unknown) without a signature.

### Anomaly-based analysis

**Anomaly-based** detection flags **deviations** from **normal** behavior.

**Two phases**

1. **Training:** Build a **baseline** of expected behavior from historical “normal” data.  
2. **Detection:** Compare **current** activity to the baseline; **departures** are logged and alerted.

**Advantages**

- Can surface **new** and **evolving** threats that have **no** signature yet.

**Disadvantages**

- **More false positives:** Benign changes (new software, unusual but legitimate usage) can look “abnormal.”  
- **Poisoned baseline:** If an attacker is already present during training, **malicious** behavior may be learned as “normal,” causing **missed** detections later (**pre-existing compromise** risk).

---

## Key takeaways

- **NIDS** monitors **network** traffic at strategic points; **HIDS** monitors **individual endpoints** via agents.  
- Combining both improves **coverage** and **context**.  
- **Signature-based** detection is strong for **known** threats but needs updates and can be evaded.  
- **Anomaly-based** detection can find **unknown** patterns but tends toward **false positives** and can be misled by a **bad training** period.
