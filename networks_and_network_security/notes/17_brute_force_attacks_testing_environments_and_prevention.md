# Brute force attacks, testing environments (VMs/sandboxes), and prevention

## Brute force attacks (password guessing)

A **brute force attack** is a trial-and-error process of discovering private information (commonly **passwords**).

### Common types

- **Simple brute force attack**: guessing login credentials by trying many username/password combinations until one works.
- **Dictionary attack**: trying a list of common passwords and stolen credentials from prior breaches (historically literal dictionary words, before complex password rules became common).

Brute force can be manual, but attackers often use tools to automate the process.

---

## Assessing vulnerabilities (before incidents)

Organizations can test their networks or web applications to assess vulnerabilities and simulate incidents.

Two common safe-testing approaches are:

- **Virtual machines (VMs)**
- **Sandbox environments**

---

## Virtual machines (VMs)

**Virtual machines (VMs)** are software versions of physical computers.

Why analysts use VMs:

- Run suspicious code in an **isolated environment** to reduce the chance of impacting the host system.
- Investigate potentially infected machines in a constrained setup.
- Revert to a previous **snapshot/state** to repeat tests.
- Delete and restore from a clean/pristine image after malware testing.

Important caveat:

- There is still a small risk of **VM escape**, where malicious code breaks isolation and reaches the host or other VMs.

---

## Sandbox environments

A **sandbox** is a testing environment that allows executing software separate from your normal environment/network.

Common uses:

- Test patches
- Identify/address bugs
- Detect cybersecurity vulnerabilities
- Evaluate suspicious files/software
- Simulate attack scenarios

Sandboxes can be:

- Stand-alone physical computers disconnected from networks, or
- Software/cloud-based (often more cost/time efficient)

Important caveat:

- Some malware can detect VMs/sandboxes and behave benignly during analysis to avoid detection.

---

## Prevention measures (against brute force and related attacks)

### Salting and hashing

- **Hashing** converts data into a unique value used to check integrity; it’s a **one-way** function (not decryptable back to the original).
- **Salting** adds random characters to passwords before hashing, increasing hash complexity and making password cracking harder.

### MFA / 2FA

- **MFA** requires two or more verification methods (factors) to access a system.
- **2FA** is MFA using exactly two factors.
- Example factors mentioned: password, biometrics, one-time password (OTP) sent to phone/email.

### CAPTCHA / reCAPTCHA

- **CAPTCHA**: a challenge designed to distinguish humans from automated software, reducing automated brute force attempts.
- **reCAPTCHA**: Google’s CAPTCHA service commonly used to protect websites from bots and malicious automation.

### Password policies

Organizations standardize password practices such as:

- Complexity requirements
- Rotation frequency
- Reuse rules
- Lockout/attempt limits (suspension after too many attempts)

## Key takeaways

- Brute force attacks include simple guessing and dictionary-based guessing.
- Analysts use VMs and sandboxes to test suspicious files and simulate attacks more safely.
- Common prevention measures: salting/hashing, MFA/2FA, CAPTCHA/reCAPTCHA, and strong password policies.
