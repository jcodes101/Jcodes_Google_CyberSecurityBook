# Tips, examples, and quick review — Foundations of Cybersecurity

## Quick mental models

*Bullets **A–Z** by keyword.*

- **CIA** — Who can see it? (**C**) Is it tampered with? (**I**) Can the right people use it? (**A**)  
- **Controls** do the work; **frameworks** organize the program; **compliance** checks the box with regulators and policy.  
- **Threat actor** = intent to harm or break policy; **hacker** = skill at access (may be hired, ethical, or criminal).

---

## Memorizable examples (from course material)

*Examples **A–Z** by scenario title.*

### Accidental internal threat

An employee **clicks a malicious link** in email—unintentional, still an **internal threat** event to log, train, and control for.

### Incident response trigger

SIEM or IDS raises **malware alert** → analyst opens **runbook** → **investigate** scope and root cause → **remediate** per policy (contain, eradicate, recover, document).

### GDPR transparency failure

Company is **not clear** about what EU citizen data it holds and why → potential **regulatory fine** (course example pattern).

### GDPR breach notification (course timing)

Breach affecting EU residents → affected people often must be informed quickly; course cites **72-hour** notification framing for authorities/citizens in EU contexts—verify current legal text for your jurisdiction and counsel guidance.

### HIPAA breach duty

If **PHI** is exposed, patients may face **identity theft** or **insurance fraud**—organizations have duties to **notify** and **document** response; security helps **evidence** handling.

### Forensics + insurance (playbooks)

Medical practice breach → your IR firm collects and documents evidence using **chain of custody** and **preservation** rules → insurer uses findings for **coverage** decisions.

### USB baiting

Attacker drops **infected flash drive** in parking lot; curious employee plugs it in → **network compromise**.

### Watering hole

Finance employees always visit a niche **industry forum** → attacker **infects that site** to reach many targets at once.

---

## Study and career tips

1. **Re-read the glossary** before interviews; be able to explain **SIEM vs. IDS** in one sentence each.  
2. **Map an attack** you read in the news to **one CISSP domain**—builds pattern recognition.  
3. **Regulations change** — bookmark primary sources (**EU GDPR portal**, **HHS HIPAA**, **NIST**, **PCI SSC**) and review yearly.  
4. **Never counterattack** as a private or corporate analyst without explicit legal authority—course and law align on **defensive** posture.  
5. **OWASP Top 10** — skim quarterly if you touch web apps or appsec conversations.  
6. **Research suggestions** from course: **Gramm-Leach-Bliley**, **Sarbanes-Oxley**, **Tallinn Manual** (international cyber law perspective).

---

## One-line drill (self-test)

Answer without looking, then check [../glossary/GLOSSARY.md](../glossary/GLOSSARY.md):

- What is **posture** vs. a **control**?  
- How does a **worm** differ from a **virus**?  
- Name two **spear phishing** special cases.  
- What does **FedRAMP** standardize?  
- **Encoding** vs. **encryption** — different purpose in one phrase each.
