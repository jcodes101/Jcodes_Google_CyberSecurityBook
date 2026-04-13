# Frameworks, controls, and the CIA triad

## Security frameworks

**Security frameworks** are **guidelines** for building plans that **mitigate risk** and **threats** to data and privacy. They help organizations **meet compliance** obligations under laws and regulations.

### Example (healthcare)

The healthcare sector uses frameworks to support compliance with **HIPAA**, which requires **medical professionals** to **protect patient information**.

---

## Security controls

**Security controls** are **safeguards** meant to **reduce specific** security risks. They are the **practical measures** organizations use to lower risk to data and privacy, often **alongside** frameworks.

### Example (HIPAA + MFA)

A hospital might use **multi-factor authentication (MFA)** so patients **prove identity** before accessing **medical records**. MFA is a **control** that supports **framework-aligned** compliance and reduces risk to **private data**.

---

## How frameworks and controls work together

- Frameworks provide **structure**, **language**, and **expected outcomes**.  
- Controls **implement** protection (prevent, detect, correct).  
- Together they support **security posture** and **regulatory** alignment.  

Frameworks and controls are often **voluntary**, but organizations are **strongly encouraged** to adopt them to protect **critical assets**.

---

## Specific frameworks (this reading)

### Cyber Threat Framework (CTF)

Per the **Office of the Director of National Intelligence (ODNI)**, the U.S. government developed the **CTF** to provide **“a common language for describing and communicating information about cyber threat activity.”**

**Why it matters:** Shared vocabulary helps professionals **analyze**, **share**, and **coordinate** faster, improving response as the **threat landscape** and **tactics** evolve.

---

### ISO/IEC 27001

**ISO/IEC 27001** is an **internationally recognized** standard. The broader **ISO/IEC 27000** family helps organizations of **all sectors and sizes** protect assets such as:

- **Financial** information  
- **Intellectual property**  
- **Employee** data  
- Information **entrusted to third parties**

**What it defines:** Requirements for an **information security management system (ISMS)**, **best practices**, and **controls** that support **risk management**.

**Note:** The standard does not mandate **one fixed list** of controls for every organization, but it offers a **control catalog** organizations can select from to **improve posture**.

---

## Control types

Controls work **with frameworks** to reduce the **likelihood** and **impact** of threats, risks, and vulnerabilities. They can be **physical**, **technical**, or **administrative**, and are commonly used to **prevent**, **detect**, or **correct** issues.

### Physical controls

- **Gates, fences, and locks**  
- **Security guards**  
- **Closed-circuit television (CCTV)**, **surveillance cameras**, **motion detectors**  
- **Access cards** or **badges** for office entry  

### Technical controls

- **Firewalls**  
- **MFA**  
- **Antivirus software**  

### Administrative controls

- **Separation of duties**  
- **Authorization** (who may access what, and under what rules)  
- **Asset classification** (labeling sensitivity/criticality so protections match risk)  

**See also:** Control **types** (preventative, detective, corrective, deterrent) and example matrix: [07_control_categories_matrix.md](07_control_categories_matrix.md).

### Further reading (health sector)

For **physical access** and related protections for **health-related** assets, see U.S. **HHS** materials on **physical safeguards** and access control—for example the HIPAA Security Rule guidance hub: [HHS HIPAA security guidance](https://www.hhs.gov/hipaa/for-professionals/security/guidance/index.html) (search there for **physical access** / facility controls as your course directs).

---

## Key takeaway (frameworks + controls)

Frameworks and controls **combine** to define **posture**, reach **security goals**, and support **compliance**. They are usually **not** laws by themselves, but they map cleanly to **regulated** environments like healthcare.

---

## The CIA triad for analysts

The **CIA triad** is a model for how organizations think about **risk** when designing **systems** and **policies**. Analysts and organizations work to uphold:

1. **Confidentiality**  
2. **Integrity**  
3. **Availability**

Keeping **risk** at an acceptable level and designing with **CIA** in mind helps build **successful security posture**—the organization’s ability to **defend** critical assets and data and **react to change**.

---

### Confidentiality

Only **authorized users** should access specific **assets** or **data**.

**Reinforcing confidentiality:** Design ideas such as **least privilege**—users get **only** the access needed for **work tasks**. Limiting access protects **private** data.

---

### Integrity

Data should be **verifiably correct**, **authentic**, and **reliable**.

**How to support integrity:**

- **Cryptography** can transform data so **unauthorized** parties cannot easily **read** or **tamper** with it (see NIST guidance on cryptographic practices).  
- **Encryption** converts data from **readable** to **encoded** form, limiting **tampering** and unauthorized access—for example for **internal chat** or other sensitive channels.

---

### Availability

**Authorized** users can **access** data when they need it.

**Balance with confidentiality:** A system can be both **available** and **confidential**. Example: **Remote employees** use the **internal network** for work, but **access** is still **limited by role**—e.g., **accounting** may use **corporate financial** data but not **unrelated** project data.

---

## Key takeaway (CIA)

The CIA triad is **core** to posture. Knowing **what each letter means** and **how organizations apply** them clarifies how teams **protect** the organization and **people** it serves.

---

## NIST Cybersecurity Framework (CSF) — update (v2.0)

The **NIST Cybersecurity Framework** is a **voluntary** framework of **standards**, **guidelines**, and **best practices** to manage **cybersecurity risk**. It is **widely used** and relevant **across** employer types.

### What changed in CSF 2.0

- A new **Govern** function was added, stressing **cybersecurity governance** as a first-class part of the program.  
- The CSF is described as having **six core functions**: **Govern**, **Identify**, **Protect**, **Detect**, **Respond**, and **Recover** (details in later course material).  
- **CSF 2.0** also puts **more emphasis** on **supply chain risk management**.

> **Note:** **NIST CSF** (risk-based security outcomes, lifecycle functions) complements but is **not the same** as **NIST RMF** (structured authorization steps for federal systems). Your org may use **one or both**. See [02_risk_management.md](02_risk_management.md) for the **RMF** seven-step overview.
