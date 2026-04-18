# Indicators of compromise, indicators of attack, and the Pyramid of Pain

---

## Indicators of compromise (IoC)

**Indicators of compromise (IoCs)** are **observable evidence** that suggests a **potential** security incident. IoCs point to **specific artifacts** tied to an attack—for example, a **file name** associated with a type of malware.

You can think of an IoC as evidence that **something already happened**, like noticing that **valuables were stolen** from inside a car.

**Note:** An IoC is **not** always proof of a malicious incident. IoCs can also come from **human error**, **system malfunction**, or other non-security causes.

---

## Indicators of attack (IoA)

**Indicators of attack (IoAs)** are **observed events** that suggest a **real-time** incident. IoAs emphasize **behavioral** evidence of an attacker—their **methods** and **intent**.

In short:

- **IoCs** tend to support **who** and **what** after activity has occurred.  
- **IoAs** support **why** and **how** during an **ongoing** or **not-yet-understood** attack.

**Example:** A **process** that opens a **network connection** is an **IoA**. The **process file name** and the **IP address** it contacted are related **IoCs**.

---

## Pyramid of Pain (David J. Bianco)

Not all IoCs are equally valuable. Security researcher **David J. Bianco** introduced the **Pyramid of Pain** to improve how IoCs are used in detection and response.

The pyramid relates **types of IoCs** to how much **difficulty (“pain”)** an attacker faces when defenders **block** activity tied to those indicators. **Lower** layers are **easier** for attackers to swap out; **higher** layers are **harder** to change and more disruptive to the adversary.

### Levels (summary)

**Hash values**  
Cryptographic hashes of known malicious files. Often used as unique references to malware samples or intrusion-related files.  
*Blocking impact:* attackers can often recompile or repack files to get new hashes (relatively **low** pain for them).

**IP addresses**  
Example: `192.168.1.1`. Easy for attackers to change; blocking one IP may only slow them briefly.

**Domain names**  
Example format: `www.example.com`. In incidents, analysts track **malicious** domains; attackers can register or rotate them.

**Network artifacts**  
Observable evidence on the **network**—for example, unusual values in protocols such as **User-Agent** strings.

**Host artifacts**  
Observable evidence on a **host** (any network-connected device)—for example, a **file name** created by malware.

**Tools**  
Software adversaries use to reach their goals (e.g., password-cracking tools such as **John the Ripper**). Blocking or detecting tool use can force more operational change than swapping an IP.

**Tactics, techniques, and procedures (TTPs)**  
The **behavior** of the adversary:  
- **Tactics** — high-level goals  
- **Techniques** — detailed behaviors under a tactic  
- **Procedures** — very specific implementations of a technique  

TTPs are often the **hardest** to detect and the **most painful** for attackers when defenders disrupt them, because changing **behavior** is more costly than changing an IP or hash.

---

## Key takeaways

- **IoCs** and **IoAs** both help detection; IoCs often describe **artifacts** of past or associated activity, while IoAs emphasize **ongoing behavioral** evidence.  
- IoCs alone **do not always** mean a confirmed security incident.  
- The **Pyramid of Pain** ranks IoC types by how much defender action hurts the adversary; **TTPs** sit at the top as the most impactful—and often hardest—layer.
