# What is OWASP? (and the OWASP Top 10)

**OWASP** is a nonprofit foundation focused on improving software security. It’s an open platform where security professionals share information, tools, and events centered on securing the web.

---

## The OWASP Top 10

One of OWASP’s most valuable resources is the **OWASP Top 10**, a list published since 2003 to raise awareness of the web’s most targeted vulnerabilities.

Key points:

- The Top 10 mainly applies to **new or custom-made software**.
- Many large organizations reference it during development to avoid common security mistakes.
- It’s updated every few years as technologies evolve; rankings reflect how often issues are found and the risk they present.
- Auditors may use it as a reference point when checking for regulatory compliance.

This differs from the **CVE** list, which is often used to identify improvements to **existing** programs.

---

## Common vulnerabilities (frequent Top 10 categories)

### Broken access control

Access controls limit what users can do in a web application. Failures can lead to unauthorized disclosure, modification, or destruction of information, and can allow unauthorized access to business applications.

Example: a blog allows comments but should not allow a visitor to delete the article.

### Cryptographic failures

Organizations must protect sensitive information using effective encryption. Privacy laws (e.g., **GDPR**) require strong protections for data like **PII**. Weak or missing encryption/hashing (e.g., using **MD5**) increases breach risk.

### Injection

**Injection** occurs when malicious code is inserted into a vulnerable application. The app may appear normal while doing unintended actions. Injection can provide a backdoor into an information system—commonly through vulnerable login forms that allow attackers to modify or steal credentials.

### Insecure design

Applications should be designed to be resilient to attack. **Insecure design** covers missing or poorly implemented security controls that should have been built in during development (increasing risk from threats like injection or malware).

### Security misconfiguration

Misconfiguration happens when security settings are not properly set or maintained. In interconnected environments, mistakes often occur when systems aren’t set up or audited correctly.

Example: deploying a server using default settings that don’t align with the organization’s security objectives.

### Vulnerable and outdated components

Modern software often uses open-source libraries. If applications rely on components with known vulnerabilities—or components that are no longer maintained—threat actors are more likely to exploit them.

### Identification and authentication failures

When applications fail to properly identify users and enforce what they’re authorized to do, serious security issues can result.

Example: a home Wi‑Fi router relies on a login form to restrict access; if this fails, attackers can invade privacy.

### Software and data integrity failures

These failures occur when updates or patches are not adequately reviewed before implementation. Attackers may exploit this to deliver malicious software, causing downstream effects like a **supply chain attack**.

Example: the **SolarWinds cyber attack (2020)** involved malicious code injected into software updates that were unknowingly released to customers.

### Security logging and monitoring failures

Organizations need logs and monitoring to trace events (like login attempts) and respond effectively. Insufficient monitoring and incident response makes detection and remediation harder.

### Server-side request forgery (SSRF)

Web applications send requests to servers to validate identity, fetch the right data, and return it to the user. **SSRF** occurs when attackers manipulate server behavior to read or update other resources on the server, typically by exploiting a vulnerable application that can carry malicious requests to internal targets.

---

## Key takeaways

Staying informed about cybersecurity trends helps defenders prepare for evolving risks. OWASP’s **Top 10** is a practical resource for learning and tracking common web application vulnerabilities.

