# Control categories and control types (reference matrix)

Controls are grouped into **three categories**. Each control also has a **type** that describes **when** it acts (before, during, or after an event).

---

## Three control categories

| Category | Focus |
|----------|--------|
| **Administrative / managerial** | **People** and **governance**: policies, procedures, roles, and how the org **manages** data and workforce responsibilities. Policies are often enforced with **technical** or **physical** controls. |
| **Technical** | **Technology**: firewalls, **IDS**/**IPS**, **antivirus**, **encryption**, etc.—used in many ways to meet **goals**. |
| **Physical** | **Physical access**: door locks, cabinet locks, **CCTV**, **badge** readers—limit **physical** access to **assets** by **unauthorized** people. |

---

## Four control types

Types **combine** to support **defense in depth**:

| Type | Role |
|------|------|
| **1. Preventative** | Stop an incident **before** it happens. |
| **2. Corrective** | **Restore** an asset **after** an incident. |
| **3. Detective** | **Determine** whether an incident **occurred** or is **in progress**. |
| **4. Deterrent** | **Discourage** attacks (raise effort or perceived risk). |

---

## Administrative / managerial controls (examples)

| Control name | Control type | Control purpose |
|--------------|--------------|-----------------|
| **Least privilege** | Preventative | Reduce risk and impact of **malicious insider** or **compromised** accounts. |
| **Disaster recovery plans** | Corrective | Support **business continuity**. |
| **Password policies** | Preventative | Reduce **account compromise** from **brute force** or **dictionary** attacks. |
| **Access control policies** | Preventative | Strengthen **confidentiality** and **integrity** by defining **who** may **access** or **modify** data. |
| **Account management policies** | Preventative | Manage **account lifecycle**, reduce **attack surface**, limit impact from **former** employees and **default** accounts. |
| **Separation of duties** | Preventative | Reduce risk and impact of **malicious insider** or **compromised** accounts. |

---

## Technical controls (examples)

| Control name | Control type | Control purpose |
|--------------|--------------|-----------------|
| **Firewall** | Preventative | **Filter** unwanted or **malicious** traffic from entering the network. |
| **IDS / IPS** | Detective (and preventive for IPS) | **Detect** (and **block**) anomalous traffic matching **signatures** or **rules**. |
| **Encryption** | Deterrent (also supports confidentiality) | Protect **confidentiality** of sensitive information (course classification). |
| **Backups** | Corrective | **Restore** / **recover** after an event. |
| **Password management** | Preventative | Reduce **password fatigue** and unsafe reuse. |
| **Antivirus (AV) software** | Corrective | **Detect** and **quarantine** known threats. |
| **Manual monitoring, maintenance, and intervention** | Preventative | Identify and manage threats, risks, or **vulnerabilities** on **out-of-date** systems. |

---

## Physical controls (examples)

| Control name | Control type | Control purpose |
|--------------|--------------|-----------------|
| **Time-controlled safe** | Deterrent | Reduce attack surface and impact from **physical** threats. |
| **Adequate lighting** | Deterrent | Deter threats by reducing **hiding** places. |
| **Closed-circuit television (CCTV)** | Preventative / Detective | Presence can **prevent** some events; footage supports **detection** and **after-action** review. |
| **Locking cabinets** (e.g., for network gear) | Preventative | Strengthen **integrity** by blocking **unauthorized** physical **access** or **tampering** with infrastructure. |
| **Signage** (e.g., alarm service provider) | Deterrent | Make successful attack seem **less likely**. |
| **Locks** | Deterrent / Preventative | **Deter** and **prevent** unauthorized physical access to assets. |
| **Fire detection and prevention** (alarm, sprinklers, etc.) | Detective / Preventative | **Detect** fire and **limit** damage to physical assets (inventory, **servers**, equipment). |

---

## Key takeaway

Use **category** (administrative, technical, physical) to assign **ownership** and **evidence**; use **type** (preventative, detective, corrective, deterrent) to explain **how** the control reduces risk in the **lifecycle** of an event.

---

## Related notes

- Higher-level examples (MFA, guards, policies): [04_frameworks_controls_and_cia_triad.md](04_frameworks_controls_and_cia_triad.md)  
- **OWASP** design principles: [05_security_principles_owasp.md](05_security_principles_owasp.md)  
- **Audits** and checklists: [06_security_audits_and_checklists.md](06_security_audits_and_checklists.md)  
