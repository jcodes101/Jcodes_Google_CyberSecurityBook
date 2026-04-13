# Security principles (OWASP)

In daily work—**log analysis**, **SIEM** dashboards, **vulnerability scanners**, and more—you apply these ideas whether or not you name them.

---

## OWASP principles (earlier introduction)

| Principle | Meaning |
|-----------|---------|
| **Minimize attack surface area** | **Attack surface** = all places a threat actor **could** attack (features, ports, accounts, APIs). Shrink what is exposed. |
| **Principle of least privilege** | Users get the **minimum** access needed for **everyday** tasks—no more. |
| **Defense in depth** | Use **multiple layers** of **different** controls so one failure does not collapse security. |
| **Separation of duties** | Sensitive actions need **more than one person**, each still following **least privilege**. |
| **Keep security simple** | Avoid **unnecessary** complexity—complex systems are **harder** to secure and operate safely. |
| **Fix security issues correctly** | On incident: find **root cause**, **contain** impact, find **vulnerabilities**, **test** fixes so **remediation** actually worked. |

---

## Additional OWASP security principles

### Establish secure defaults

The **best security state** of an application should be its **default** state. It should take **extra steps** to become **less** secure—not the other way around.

### Fail securely

When a control **fails** or **stops**, it should land in the **safest** posture. **Example:** a **firewall** failure should **block** traffic (deny-by-default), not **open** everything.

### Don’t trust services

Partners and vendors have **their own** policies and exposure. **Do not assume** their systems are safe. **Example:** an airline uses a vendor for **loyalty points**—**verify** balances before showing them to customers.

### Avoid security by obscurity

**Do not rely** on **secrecy** alone (hidden URLs, “private” code) for safety. Per OWASP (e.g., **Mobile Top 10**, 2016 framing): security should rest on **password policy**, **defense in depth**, **transaction limits**, **network design**, **fraud/audit** controls—not only on **hidden source code**.

---

## Key takeaway

These principles support **safer development** and **operations** and **reduce** risk to the organization and its users. As an analyst, you reinforce them through **monitoring**, **access reviews**, and **clear** incident handling.

---

## Related notes

- Control **categories** and **types** (preventative, detective, etc.): [07_control_categories_matrix.md](07_control_categories_matrix.md)  
- Frameworks and **CIA**: [04_frameworks_controls_and_cia_triad.md](04_frameworks_controls_and_cia_triad.md)
