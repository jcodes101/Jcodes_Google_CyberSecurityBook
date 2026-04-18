# Business continuity planning (BCP)

Security teams work to **limit** how much incidents disrupt **normal business operations**. Incidents can interrupt systems and services; long outages can drive **legal**, **financial**, and **reputational** harm.

**Business continuity planning** helps organizations **stay operational** through major disruptions.

---

## Business continuity plan (BCP)

Like an **incident response plan**, a **business continuity plan (BCP)** is a document that defines **procedures** to **sustain** business operations **during and after** a significant disruption.

A BCP helps ensure **critical business functions** can **continue** or be **restored quickly** when an incident occurs.

**Analyst note:** Entry-level analysts are not usually responsible for **writing** or **testing** the full BCP, but you should know **why** it exists and how it fits with incident response and recovery.

### BCP vs disaster recovery (DR)

**Business continuity plans** and **disaster recovery plans** are **not** the same.

- **BCP**: keeping **business operations** going (or restoring them in an organized way) across a disruption.  
- **Disaster recovery (DR) plan**: recovering **information systems** after a major disaster—examples include **hardware failure** or **facility loss** (e.g., flooding).

DR is often **part of** continuity thinking but has a **systems/infrastructure** focus.

---

## Example: ransomware and business continuity

Incidents such as **ransomware** can severely disrupt operations. Attacks on **critical infrastructure** (e.g., **healthcare**) may affect **availability** and **delivery** of essential services.

Ransomware may **encrypt** data, blocking access to systems such as **electronic health records**, which can prevent providers from using patient information when it is needed most.

At larger scale, incidents against **critical infrastructure** can affect **national security**, **economic security**, and **public health and safety**. **BCPs** aim to **reduce interruptions** so essential services remain available or return to service as safely and quickly as practical.

---

## Recovery strategies and resilience

After an outage caused by a security incident, organizations need a **workable** path to **restore** capability and return toward **normal** operations. BCPs may describe **recovery strategies** for that journey.

**Resilience** is the ability to **prepare for**, **respond to**, and **recover from** disruptions. Systems can be designed so services **continue** despite problems.

### Site resilience

**Site resilience** supports **availability** of networks, data centers, or other infrastructure when something fails. Organizations use **recovery sites**—commonly described as:

**Hot site**  
A **fully operational** facility that **mirrors** the primary environment. Can often be **activated immediately** when the primary site fails.

**Warm site**  
Contains **updated**, **configured** infrastructure similar to a hot site but is **not** fully live for instant cutover. Can be brought to full operation **relatively quickly** after a disruption.

**Cold site**  
A backup location with **some** required infrastructure. May **not** be ready for immediate use and may need **additional** setup, equipment, or data restoration before it is fully operational.

---

## Key takeaways

- Incidents can **disrupt** business; **BCPs** document how to **sustain** or **restore** critical operations.  
- **BCP** complements but differs from **disaster recovery** (DR focuses on recovering **systems** after disasters).  
- **Ransomware** and other attacks show why continuity matters for services and public impact.  
- **Site resilience** options (**hot**, **warm**, **cold**) trade **readiness** and **cost** against **speed** of recovery.
