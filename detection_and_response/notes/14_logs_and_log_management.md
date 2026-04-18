# Logs and log management

Data sources such as devices generate data as **events**. A **log** is a **record of events** that occur within an organization’s systems.

Logs contain **log entries**; each entry typically describes **one** event on a device or system.

---

## Why logs matter

Historically, logs were used mainly for **troubleshooting**—for example, **error logs** explain unexpected failures and support **root cause** analysis.

Today, most computing devices produce logs that support **much more** than troubleshooting, including **security monitoring** and **incident investigation**.

Security teams often access logs through **logging receivers** such as **SIEM** tools, which **consolidate** logs into a **central** place.

**Log analysis** is the process of **examining** logs to find **events of interest**. Logs help answer investigative questions—the **five W’s**: **who**, **what**, **when**, **where**, and **why** (where applicable).

---

## Types of logs

Log types depend on the **data source**. Common categories:

| Type | Source / focus | Examples |
|------|----------------|----------|
| **Network** | Network devices | Firewalls, routers, switches |
| **System** | Operating systems | Chrome OS, Windows, Linux, macOS |
| **Application** | Software applications | Events inside an app (e.g., a mobile app) |
| **Security** | Security products / features | Antivirus, IDS; may include security-relevant events such as **file deletion** |
| **Authentication** | Identity events | Successful (or failed) logins to a system |

---

## What logs usually contain

Logs commonly include elements such as **date**, **time**, **location** (system or component), **action**, and **who** performed the action (user or process).

**Example (authentication):**

```text
Login Event [05:45:15] User1 Authenticated successfully
```

### Verbose logging

**Verbose logging** records **extra** detail beyond the default. Example of the same event with more context:

```text
Login Event [2022/11/16 05:45:15.892673] auth_performer.cc:470 User1 Authenticated successfully from device1 (192.168.1.2)
```

Verbose logs help investigations but increase **volume** and **sensitivity**—balance is important.

---

## Log management

Many devices generate logs; volume can become **unmanageable** without a plan.

**Log management** is the process of **collecting**, **storing**, **analyzing**, and **disposing of** log data.

### What to log

The most important decision is **what** to log. Requirements vary by organization and by what you need to prove or detect.

- Tune sources so logs contain **useful** signal; avoid needless **verbosity** where it does not help.  
- **Personally identifiable information (PII)**—such as phone numbers, email addresses, and names—may need **special handling** and in some jurisdictions **must not** be logged (or must be minimized/transformed).

### Overlogging

Logging **everything** is a common mistake. Drawbacks include:

- Higher **storage** and **maintenance** cost (especially with SIEM licensing/storage models)  
- Extra **load** on systems and **noise** that makes **search** and **triage** harder  

**Rule of thumb:** just because something *can* be logged does not mean it *should* be.

---

## Log retention

Regulations and contracts often dictate **how long** logs must be kept. Examples of frameworks or sectors that influence retention (this course cites):

- **Public sector** — e.g., **FISMA** (Federal Information Security Modernization Act)  
- **Healthcare** — e.g., **HIPAA** (Health Insurance Portability and Accountability Act of 1996)  
- **Financial services** — e.g., **PCI DSS**, **GLBA** (Gramm-Leach-Bliley Act), **SOX** (Sarbanes-Oxley Act of 2002)  

Retention rules belong in a **log management policy** and should align with **legal** and **risk** review.

---

## Log protection (integrity)

Attackers may **alter** or **delete** logs to hide activity or mislead investigators.

**Centralized log servers** (forwarding logs to a **dedicated** system instead of keeping them only on the compromised host) add a **barrier**: it is harder for an attacker on one machine to reach or tamper with all evidence copies.

Combine centralization with **access controls**, **immutability** or **WORM** storage where appropriate, and **monitoring** of the logging infrastructure itself.

---

## Key takeaways

- **Logs** are structured **records of events**; they underpin **SIEM**, **detection**, and **incident analysis**.  
- Know major **log types** (network, system, application, security, authentication) and typical **fields**.  
- **Log management** covers collection through disposal; avoid **overlogging** and mishandling **PII**.  
- **Retention** is often **compliance-driven**; **protect** logs to preserve **integrity** against tampering.
