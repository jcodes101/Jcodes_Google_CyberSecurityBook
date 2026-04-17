# IAM, access control models, and core security principles

Security is not just a collection of processes and technologies—it’s ensuring they create a secure environment that supports a defense strategy. Two fundamental principles help limit access to organizational resources:

- **Principle of least privilege**: users get only the minimum access and authorization needed to complete a task or function
- **Separation of duties** (also called **segregation of duties**): users should not have authorization levels that would allow them to misuse a system

These principles support each other. Least privilege limits how much access one person gets, while separation of duties divides responsibilities so no single person has too much control.

---

## Least privilege + separation of duties (example)

- Least privilege: someone who approves IT purchases should not be able to approve purchases for every department.
- Separation of duties: the person who approves purchases should be different from the person who inputs new purchases.

---

## IAM (identity and access management)

Regulatory pressure has increased expectations that organizations prevent threats. **Identity and access management (IAM)** is a collection of processes and technologies used to manage digital identities.

Previously you learned the **AAA** framework (authentication, authorization, accounting). **IAM** and **AAA** systems are both designed to:

- authenticate users
- determine access privileges
- track activities within a system

Neither IAM nor AAA is usually a single tool; each is a collection of security controls that ensure the right user is granted access to the right resources **at the right time** and **for the right reasons**—based on organizational policy.

**Note:** A “user” can be a person, a device, or software.

---

## Authenticating users

Authentication is proving a user is who they claim to be. Common factor categories:

- **Knowledge**: something you know
- **Ownership**: something you have
- **Characteristic**: something you are

Login credentials are the most common proof, but organizations also use controls like:

- **SSO** (single sign-on): combines multiple logins into one
- **MFA** (multi-factor authentication): requires two or more proofs to access a system/network

**Pro tip:** “something you know, something you have, something you are.”

---

## User provisioning (and deprovisioning)

Back-end systems must verify a user’s identity information is accurate. **User provisioning** is the process of creating and maintaining a user’s digital identity.

Example: a college creates an account for a new instructor and configures it to access instructor-only resources.

Security analysts often help provision users and access privileges.

**Pro tip:** Analysts may also **deprovision** users—removing access rights when users should no longer have them.

---

## Granting authorization (access control models)

After authentication, the system must authorize access to the right resources. Three common authorization frameworks are:

- **Mandatory access control (MAC)**
- **Discretionary access control (DAC)**
- **Role-based access control (RBAC)**

### Mandatory Access Control (MAC)

**MAC** is the strictest model. Access is granted on a strict need-to-know basis and is typically assigned manually by a central authority (e.g., a system administrator). It’s common in law enforcement, military, and government settings where access is requested through a chain of command.

MAC is also called **non-discretionary control** because access is not at the data owner’s discretion.

### Discretionary Access Control (DAC)

**DAC** is used when the **data owner** decides appropriate access levels.

Example: the owner of a Google Drive folder shares **editor**, **viewer**, or **commenter** access.

### Role-Based Access Control (RBAC)

**RBAC** determines authorization based on a user’s **role** in an organization.

Example: a marketing user has access to analytics but not network administration.

---

## Access control technologies (how it works in practice)

Users often experience authentication and authorization as a seamless workflow because access control technologies are integrated.

These tools provide:

- speed and automation for administrators to monitor/modify access rights
- fewer errors and reduced risk

Organizations may build custom access control systems, but it can be expensive in time and resources. Many instead license third-party suites.

A typical IAM/AAA setup includes:

- a **user directory**
- tools to **manage** that directory
- an **authorization** system
- an **auditing** system

Security depends on configuring these technologies to support a secure environment—not just collecting tools.

---

## Key takeaways

- Least privilege and separation of duties are foundational access-limiting principles.
- **IAM** and **AAA** are common frameworks to implement these principles.
- Analysts often support IAM/AAA work such as provisioning and deprovisioning.
- IAM/AAA aims to ensure the right user gets the right resources at the right time for the right reasons.

