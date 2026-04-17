# Penetration testing

A **penetration test** (pen test) is a simulated attack used to identify vulnerabilities in systems, networks, websites, applications, and processes. Pen tests use the same tools and techniques as malicious actors to mimic real-world attacks. Because they are authorized, pen tests are a form of **ethical hacking**.

Unlike a **vulnerability assessment**, which identifies weaknesses, a pen test attempts to **exploit** weaknesses to understand potential consequences if a system is compromised.

Example: a financial company simulates an attack against its banking app to determine whether weaknesses could allow customer data theft or illegal fund transfers. Findings (like misconfigurations) can be fixed to strengthen security.

**Note:** Organizations regulated by **PCI DSS**, **HIPAA**, or **GDPR** may be required to routinely perform penetration testing to maintain compliance.

---

## Learning from varied perspectives (teams)

Pen tests are performed by testers skilled in areas like programming and network architecture. Organizations can take different approaches depending on objectives:

- **Red team tests**: simulate attacks to identify vulnerabilities in systems, networks, or applications
- **Blue team tests**: focus on defense and incident response to validate existing security systems
- **Purple team tests**: collaborative exercises that combine red + blue efforts to improve security posture

Red team tests are often run by independent testers hired to evaluate internal systems, though some organizations also have in-house pen testing experts.

Before attacking, testers must decide how much access and information they need.

---

## Penetration testing strategies (knowledge levels)

Three common strategies:

### Open-box testing

The tester has privileged access similar to an internal developer (system architecture, data flow, network diagrams).

Also called: **internal**, **full knowledge**, **white-box**, **clear-box** testing.

### Closed-box testing

The tester has little to no internal access—closer to a real malicious attacker.

Also called: **external**, **black-box**, **zero knowledge** testing.

Closed-box testing often produces the most realistic simulations of real-world attacks, but all approaches provide valuable insight into how an attacker might get in and what they could access.

### Partial knowledge testing

The tester has limited access/knowledge (for example, like a customer service representative).

Also called: **gray-box** testing.

---

## Becoming a penetration tester

Pen testers are in-demand. Skills that support pen testing include:

- network and application security
- operating systems experience (e.g., Linux)
- vulnerability analysis and threat modeling
- detection and response tools
- programming languages (e.g., Python and Bash)
- communication skills

Programming skills help because pen testing often targets software and IT systems. With practice, security professionals at many levels can grow into pen testing roles.

---

## Bug bounty programs

Organizations may run **bug bounty** programs that pay rewards to freelance testers for finding and reporting vulnerabilities.

Bug bounties can help newer security professionals gain experience.

**Pro tip:** **HackerOne** is a community of ethical hackers where you can find active bug bounties.

---

## Key takeaways

- Pen testing simulates real attacks to better understand security weaknesses.
- Unlike assessments, pen tests attempt to exploit weaknesses to measure impact.
- Red, blue, and purple team exercises offer different perspectives.
- Open/closed/partial knowledge strategies (white/black/gray box) determine how much internal context the tester has.
- Pen testing skills overlap with many core cybersecurity skills and can be developed over time.

