# Cloud security considerations, shared responsibility, and hardening

## Why cloud security is different (and sometimes harder)

Organizations use cloud services for easier and faster deployment, cost savings, and scalability. But cloud introduces unique security considerations:

- **IAM and role configuration** mistakes can over-privilege users.
- The ecosystem is complex; each service requires precise **configuration** for security and compliance.
- Many services can increase the **attack surface** and complexity.
- Visibility/monitoring changes (flow logs/packet mirroring exist, but you don’t get the same access as on-prem).
- CSPs ship frequent updates; customers must adapt processes (“things change fast”).

---

## Identity and access management (IAM)

**Identity access management (IAM)** is a collection of processes and technologies used to manage digital identities and authorize how users can use resources.

Cloud risk pattern called out in the course:

- **Loose/misconfigured user roles** can allow unauthorized users to perform critical operations.

---

## Configuration risk (especially during migrations)

Cloud environments require careful configuration to maintain:

- Security
- Compliance
- Correct access boundaries

During migrations, every migrated process and service must be configured properly. Misconfiguration is a frequent source of cloud security incidents.

---

## Attack surface

Cloud providers offer many services at low cost. Each additional service may introduce:

- More potential vulnerabilities
- More operational complexity

Important nuance from the course:

- Multiple services do not necessarily increase entry points if network design is correct, but they do increase the need for appropriate controls and monitoring.
- CSPs often default to secure options and undergo more scrutiny than many on-prem environments, but customers still have responsibilities.

---

## Zero-day attacks

A **zero-day attack** exploits a vulnerability that was previously unknown.

Course emphasis:

- CSPs may learn about and respond to zero-days quickly.
- CSPs can patch hypervisors and migrate workloads to other VMs to reduce customer impact.
- Customers can also patch at the operating system level (where responsible).

---

## Visibility and tracking (on-prem vs cloud)

On-prem:

- Administrators can sniff/inspect packets crossing networks.

Cloud:

- Visibility is often provided through mechanisms like **flow logs** and **packet mirroring**.
- CSPs secure their own infrastructure and generally do not permit customers to monitor traffic *on the CSP’s servers* the same way as on-prem.
- CSP third-party audits can help verify security posture and clarify whether issues originate from on-prem or cloud configurations.

---

## Shared responsibility model

The **shared responsibility model** is a core cloud security principle that defines “who is responsible for what.”

- **CSP responsibility**: security *of* the cloud infrastructure (physical data centers, hypervisors, host operating systems).
- **Customer responsibility**: security *in* the cloud for what they run/store (assets, processes, and especially application/service configuration).

Common failure mode:

- Customers assume the CSP is securing items that are actually the customer’s responsibility (like app config and access settings).

---

## Cloud security hardening (course list)

Common techniques and tools mentioned:

- **IAM**
- **Hypervisors** (understanding responsibilities and risks)
- **Baselining**
- **Cryptography**
- **Cryptographic erasure** (crypto-shredding)
- **Key management**

## Cloud security hardening techniques (practical checklist)

This is a broader, “useful in real jobs” checklist that builds on the course list.

### Identity and access hardening

- **Least privilege / role hygiene**: keep roles minimal, remove unused permissions, use separate admin roles.
- **MFA / 2FA** for privileged access and sensitive systems.
- Prefer short-lived credentials/tokens where supported and rotate secrets regularly.

### Configuration and change hardening

- Maintain **baseline configurations (baseline images)** for systems so builds/updates start from a known-good reference.
- Monitor and remediate **configuration drift** vs the baseline.
- Apply **patch updates** quickly for OS and applications, especially for internet-exposed services.

### Logging, visibility, and detection hardening

- Centralize logs and perform **network log analysis** to identify events of interest.
- Use **SIEM** tooling to collect/correlate logs and alert on critical activity.
- In cloud, enable and review provider telemetry (e.g., flow logs) as available.

### Network and perimeter hardening

- Minimize exposed services, restrict inbound/outbound paths, and use segmentation where appropriate.
- Use firewalls/WAFs and tighten access by IP, port, and identity where possible.

### Data protection and key hardening

- Encrypt sensitive data (in transit and at rest) and implement strong **key management**.
- Use hardware-backed key protection where available (e.g., **TPM**, **CloudHSM**).
- For secure deletion in cloud, use **cryptographic erasure** when appropriate.

### Vulnerability discovery and validation

- Use vulnerability scanning and **penetration testing (pen tests)** to find gaps in systems, networks, apps, and processes.
- Use **VMs** and **sandboxes** to test suspicious files and patches more safely.

### OS and file-permission hardening

- Harden operating system defaults (services, accounts, configs).
- Watch for risky permissions (example: **world-writable files**) that allow unintended modification.

### Hypervisors

A **hypervisor** abstracts host hardware from operating environments.

- **Type 1 hypervisor**: runs on host hardware (example: VMware ESXi).
- **Type 2 hypervisor**: runs on host OS software (example: VirtualBox).

Course emphasis:

- CSPs commonly use type 1 hypervisors and manage them (patching, availability).
- Vulnerabilities or misconfigurations can lead to **VM escape**.
- Customers rarely manage hypervisors directly in public cloud.

### Baselining

**Baselining** is establishing a fixed reference configuration for the cloud environment so changes can be compared against a known-good state.

Examples of baseline-related practices mentioned:

- Restrict access to the admin portal
- Enable password management
- Enable file encryption
- Enable threat detection services for databases (example mentioned: SQL)

Good baselines improve both **security** and **performance** by making drift easier to detect.

### Cryptography in the cloud

**Cryptography** is used to secure data processed and stored in the cloud.

- Uses encryption + secure key management to support **confidentiality** and **integrity**.
- Modern encryption relies primarily on keeping the **key** secret, not the algorithm.

### Cryptographic erasure (crypto-shredding)

**Cryptographic erasure** is destroying the encryption keys used to decrypt data, making encrypted data effectively unreadable.

- Also called **crypto-shredding** in the course.
- When destroying cloud data, traditional physical destruction methods don’t apply the same way, so key destruction becomes a practical control.
- All copies of the key must be destroyed to prevent future decryption.

### Key management (protecting encryption keys)

Modern encryption depends on keeping keys secure.

Measures and tools mentioned:

- **Trusted Platform Module (TPM)**: a chip that can securely store secrets such as certificates and encryption keys.
- **Cloud hardware security module (CloudHSM)**: a cloud device/service that stores keys and performs cryptographic operations like encryption/decryption.

Course note on customer-managed keys:

- Many CSPs allow customers to provide their own encryption keys (service-dependent).
- If customers provide keys, the customer is responsible for protecting them; the CSP’s ability to help is limited if keys are lost or compromised.

Course note on audits/compliance:

- Customers can request audits and security reports from CSPs.
- For federal contractors, the course references **FedRAMP** as a source of verified CSPs.

---

## Key takeaways

- Cloud security requires strong IAM, careful configuration, and continuous attention to change.
- The shared responsibility model clarifies what the CSP secures vs what the customer must secure.
- Hardening techniques include IAM, baselines, understanding hypervisor risk, cryptography, cryptographic erasure, and key management.
