# Threat modeling (frameworks and application security)

**Threat modeling** is the process of identifying assets, their vulnerabilities, and how each is exposed to threats. It’s a strategic approach that combines security activities such as vulnerability management, threat analysis, and incident response. Teams use threat modeling to ensure systems are adequately protected and to proactively reduce risk in systems and business processes.

Threat modeling is traditionally associated with application development, where it helps design software that can withstand attacks.

---

## Why application security matters

Applications are essential to many organizations’ success:

- Web apps connect customers, partners, and other users globally.
- Mobile apps and smartphones are major channels for exchanging data between users and businesses.

Because applications process large volumes of data, securing them is critical to reducing risk for everyone connected.

Example: **Log4Shell** (**CVE-2021-44228**) affected Java-based logging libraries. If unpatched, it can enable **remote code execution**, giving attackers the ability to gain system access from anywhere. Critical vulnerabilities like this can impact millions of devices.

---

## Defending the application layer

Defending the application layer requires testing to uncover weaknesses that can lead to risk. Threat modeling is one of the primary ways to ensure applications meet security requirements. A **DevSecOps** team (development, security, operations) commonly performs these analyses.

A typical threat modeling cycle:

- **Define the scope**
- **Identify threats**
- **Characterize the environment**
- **Analyze threats**
- **Mitigate risks**
- **Evaluate findings**

Ideally, threat modeling happens **before**, **during**, and **after** development. Because thorough analysis takes time and resources, frameworks exist to streamline the process.

**Note:** Threat modeling should be incorporated at every stage of the **software development lifecycle (SDLC)**.

---

## Common threat modeling frameworks

Organizations choose frameworks based on context and the risks an application may face. Common approaches include:

- **STRIDE**
- **PASTA**
- **Trike**
- **VAST**

### STRIDE

**STRIDE** is a Microsoft framework used to identify vulnerabilities across six attack vectors:

- **Spoofing**
- **Tampering**
- **Repudiation**
- **Information disclosure**
- **Denial of service**
- **Elevation of privilege**

### PASTA

**PASTA** (Process of Attack Simulation and Threat Analysis) is a risk-centric process developed by two OWASP leaders and supported by VerSprite. It focuses on identifying evidence of viable threats and representing that evidence as a model.

PASTA can be applied to an application or the environment supporting it. Its seven-stage process can incorporate security artifacts such as vulnerability assessment reports.

### Trike

**Trike** is an open-source methodology and tool with a security-centric approach. It often emphasizes security permissions, use cases, privilege models, and other elements that support a secure environment.

### VAST

**VAST** (Visual, Agile, and Simple Threat Modeling) is part of an automated threat-modeling platform called ThreatModeler®. Teams may use VAST to automate and streamline threat modeling assessments.

---

## Participating in threat modeling

Threat modeling is usually led by experienced security professionals, but it’s rarely a solo effort—especially for complex applications that handle lots of data and commands.

A key to contributing is asking the right questions:

- What are we working on?
- What kinds of things can go wrong?
- What are we doing about it?
- Have we addressed everything?
- Did we do a good job?

Working with data flow diagrams and attack trees takes practice, but anyone can build threat modeling skills. Participation often starts with asking these questions and thinking critically about how data is handled.

---

## Key takeaways

- Application security is increasingly important as software usage and data volume grow.
- Threat modeling helps confirm security controls are in place to protect data privacy and reduce risk.
- Frameworks like STRIDE, PASTA, Trike, and VAST can streamline threat modeling.
- Analysts can be valuable contributors by applying an attacker mindset and asking strong questions.

