# Triage process: receive, prioritize, collect and analyze

Incidents can seriously harm an organization. Security teams must respond **quickly** and **efficiently** to limit impact.

**Triage** is the **prioritization** of incidents by **importance** or **urgency**. It helps teams **evaluate** alerts, **allocate** resources, and handle the **most critical** work first.

---

## Three steps

1. **Receive and assess**  
2. **Assign priority**  
3. **Collect and analyze**  

---

## 1) Receive and assess

An analyst receives an alert from a system such as an **intrusion detection system (IDS)**—which monitors activity and alerts on possible intrusions—and **reviews** it to confirm understanding.

Gather context: what activity triggered the alert, which **systems** and **assets** are involved, and other relevant details.

### Questions to validate an alert

- **False positive?** Is this a real concern or a **false positive** (incorrect threat detection)?  
- **History:** Did this alert fire before? How was it **resolved**? New vs recurring changes response.  
- **Known vulnerability?** If tied to a **known** weakness, use existing knowledge to respond faster and reduce impact.  
- **Severity?** Severity helps set **priority** so critical issues are escalated quickly.

---

## 2) Assign priority

After the alert is assessed as a **genuine** security issue, **prioritize** it. Incidents differ in **impact**, **size**, and **scope**; teams cannot treat every incident the same.

### Factors for priority

**Functional impact**  
How does the incident affect **IT services** and **users**? Example: **ransomware** can severely harm **confidentiality, integrity, and availability**—data encrypted or deleted may be unusable. Consider effect on **business function** of affected systems.

**Information impact**  
How does it affect **data** (CIA)? Example: **data exfiltration** can expose sensitive data belonging to the organization or **third parties**. Think beyond internal impact.

**Recoverability**  
Recovery depends on **scope** and **available** resources. Sometimes recovery is **limited**—e.g., stolen proprietary data is **published** and cannot be “un-leaked.” Spending heavily on an incident with **no practical recovery** may be a poor use of effort; weigh **time** and **cost** against realistic outcomes.

**Note:** Many alerts already include **priority** or **severity** from the organization’s classification scheme.

---

## 3) Collect and analyze

Perform **deeper** analysis: gather evidence from multiple sources, do **outside research** as needed, and **document** the investigation. The goal is enough information to decide **next steps** (contain, escalate, close, etc.).

**Escalation:** Serious incidents may go to a **level two** analyst or **manager** who can use **advanced** techniques or approve major actions.

---

## Benefits of triage

- **Resource management:** Focus effort on **urgent** threats; avoid burning time on low-priority noise; can **shorten** response time for what matters.  
- **Standardized approach:** Repeatable steps—often supported by **playbooks**—help every alert get **assessed** and **validated** before deeper investigation, so only appropriate items move forward.

---

## Key takeaways

- **Triage** orders work by **urgency** and **importance** so critical incidents get attention first.  
- Steps: **receive/assess** → **assign priority** (functional impact, information impact, recoverability) → **collect and analyze** (and escalate when needed).  
- Strong triage supports **incident response goals** and realistic use of **team time** and **tools**.
