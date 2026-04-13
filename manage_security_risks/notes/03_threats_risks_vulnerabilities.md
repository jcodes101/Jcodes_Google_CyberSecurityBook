# Threats, risks, and vulnerabilities

## Threat

A **threat** is any **circumstance or event** that can **negatively impact** assets.

Entry-level analysts help defend assets from **inside and outside** threats. Common examples:

| Threat type | Summary |
|-------------|---------|
| **Insider threats** | Staff or **vendors** abuse **authorized access** to obtain data that may **harm** the organization |
| **Advanced persistent threats (APTs)** | A threat actor keeps **unauthorized access** for an **extended** time |

---

## Risk

**Risk** is anything that can affect the **confidentiality**, **integrity**, or **availability** of an asset.

### Simple framing from the course

One way to think about level of risk: **risk** relates to the **likelihood** of a **threat** materializing. A useful analogy:

- **Risk** = being **late to work**  
- **Threats** = **traffic**, **accident**, **flat tire**, etc.

(Other models also weigh **impact** and **vulnerabilities**; your employer’s framework may go deeper than this introduction.)

### Factors that affect likelihood / organizational exposure

| Factor | Description |
|--------|-------------|
| **External risk** | **Outside** the organization—e.g., attackers seeking **private information** |
| **Internal risk** | **Insider** risk: employee, **vendor**, or **partner** who poses a security risk |
| **Legacy systems** | Old systems **not** fully inventoried or **updated** but still tied to assets—e.g., old **payment kiosk**, workstation on a **legacy accounting** system |
| **Multiparty risk** | **Outsourcing** gives vendors access to **IP**: trade secrets, designs, inventions |
| **Software compliance / licensing** | **Unpatched** or **non-compliant** software; **patches** not applied in time |

---

## References for risk lists

- **NIST** and other bodies publish **cybersecurity risk** guidance and catalogs.  
- **OWASP** maintains a widely used document on the **top 10** most critical **web application** security risks, **updated over time**.

### OWASP Top 10 — 2017 vs 2021 (course note)

The **2017 → 2021** update added emphasis on three areas (among broader changes):

1. **Insecure design**  
2. **Software and data integrity failures**  
3. **Server-side request forgery (SSRF)**

**Takeaway:** Security **evolves**; staying current on **tactics and techniques** improves readiness.

---

## Vulnerability

A **vulnerability** is a **weakness** that a **threat** can **exploit**. Organizations should **inspect** systems **regularly** for vulnerabilities.

### Examples from the course

| Name | What it is (high level) |
|------|-------------------------|
| **ProxyLogon** | **Pre-authenticated** issue affecting **Microsoft Exchange**; attacker can complete authentication and deploy **malicious code** from a **remote** location |
| **ZeroLogon** | Flaw in Microsoft’s **Netlogon** authentication protocol (service that helps **verify identity** before access) |
| **Log4Shell** | Lets attackers run **Java** code on others’ systems or **exfiltrate** data; remote control of **internet-connected** devices and **malicious code** execution |
| **PetitPotam** | Affects **Windows NTLM**; **LAN-based** attacker can **trigger** an authentication request (theft technique) |
| **Security logging and monitoring failures** | **Weak** logging/monitoring so attackers exploit issues **without** the organization noticing |
| **Server-side request forgery (SSRF)** | Tricks a **server-side** app into accessing/updating **backend** resources; can enable **data theft** |

---

## Vulnerability management (analyst work)

**Vulnerability management** means **monitoring** systems to **identify** and **mitigate** vulnerabilities.

- **Patches** and **updates** only help if they are **actually applied**.  
- **Continuous monitoring** shortens the window between **discovery** and **remediation**.  
- Faster **identify → patch/update → verify** reduces **exposure**.

### Deeper reading (course pointers)

- [NIST National Vulnerability Database](https://nvd.nist.gov/)  
- [CISA Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)

---

## Key takeaway

**Threats** are events that can harm assets; **risks** tie threats (and weaknesses) to **CIA** impact; **vulnerabilities** are fixable weaknesses. Your job often overlaps **assessment** (finding), **operations** (detecting), and **governance** (prioritizing fixes) across the **eight domains**.
