# Automation for finding threats in CI/CD pipelines

**CI/CD pipelines** help ship software faster, but they can also introduce risk. If an attacker compromises a pipeline, they might inject code, steal sensitive data, or disrupt releases. **Ongoing monitoring** that **automatically** surfaces unusual pipeline activity is therefore critical.

Strong CI/CD security goes beyond **collecting logs**. Monitoring tools can **automatically** spot unusual behavior in **builds**, **code**, or **deployment** steps that may indicate threats. When those signals appear, security teams can respond quickly and limit damage. **Automated threat detection** is a central goal of robust CI/CD security.

---

## Common indicators of compromise (IoCs) in CI/CD

Knowing typical CI/CD IoCs helps you monitor effectively and catch incidents sooner.

### Unauthorized code changes

- Changes from people who should not be committing  
- Changes at unusual times or from unexpected locations  
- Suspicious changes: obfuscated code, very large deletions without justification, or violations of coding standards  

### Suspicious deployment patterns

- Deployments to unusual or unapproved targets (e.g., production directly from a developer branch)  
- Deployments at unexpected times or far more often than normal (outside planned release windows)  
- Deployments triggered by unexpected users or automation accounts that should not release to production  

### Compromised dependencies

- **CVEs** reported in dependencies during automated checks  
- Sudden addition of unexpected dependencies to build configuration  
- Pulling dependencies from unofficial or untrusted sources  

### Unusual pipeline execution

- Steps that usually succeed start **failing**  
- Pipelines taking **much longer** without a clear operational reason  
- Changes to **step order** or behavior without approved configuration changes  

### Secrets exposure attempts

- Logs showing attempts to access **secrets** from unapproved parts of the pipeline  
- **Secrets hardcoded** in code changes (ideally blocked earlier; monitoring can still catch mistakes)  

---

## Proactive security through IoC-focused monitoring

Continuous pipeline monitoring—with **automated anomaly detection** and IoC detection—supports a more **proactive** security posture. Benefits include:

- **Faster incident response**: Early IoCs help teams react before attackers reach their goals.  
- **Reduced blast radius**: Quicker response limits how long attackers can operate in the pipeline.  
- **Better threat knowledge**: IoC review improves understanding of how CI/CD is targeted, which feeds future hardening and **threat hunting**.  

---

## Using automation to find anomalies and IoCs

### Comprehensive logging and auditing

**Detailed logs** are the foundation of monitoring. Tools analyze logs for unusual activity and potential IoCs.

**Pipeline execution logs**  
Specialized tools often use **automated baselining**: they learn from **normal**, successful runs to profile expected behavior (e.g., typical **duration** per stage, usual **success/failure** rates). Ongoing comparison to that baseline can flag anomalies—long-running steps, unexpected errors, or **changes in step order**—as potential IoCs for follow-up.

**Code commit logs**  
Track changes tied to pipeline runs. Watch for wrong authors, off-hours commits, or suspicious diffs (large deletions, confusing changes).

**Access logs**  
Establish who usually accesses CI/CD. Unusual logins (new regions, failed-then-success patterns, attempts to change sensitive pipeline settings) are strong IoC signals.

**Deployment logs**  
Baseline deployment frequency and patterns. Odd timing or unexpected targets can be IoCs.

### Security information and event management (SIEM) integration

Sending CI/CD logs to a **SIEM** helps **scale** anomaly and IoC detection. SIEMs commonly:

- **Detect anomalies** using analytics and machine learning on pipeline log data.  
- **Alert on known IoCs** via rules, for example:  
  - Malicious **file hashes** in build artifacts (known CI/CD-related threats)  
  - CI/CD infrastructure communicating with **known malicious C2** (using threat intelligence)  
  - Attempts to access **secrets** outside approved pipeline steps  

### Real-time alerting and notifications

Automation should notify teams quickly. Useful alert categories include:

- **Unusual build failures** (especially repeated failures after benign-looking changes)  
- **Suspicious code changes** flagged by analysis (size, author, content anomalies)  
- **Secret exposure** attempts detected by security tooling  
- **Unusual network traffic** from CI/CD systems, especially egress to unknown or suspicious destinations  

### Performance monitoring (IoAs leading to IoCs)

**Performance monitoring** is often used for reliability, but it can also surface **indicators of attack (IoAs)**—for example sudden slowdowns or resource exhaustion on CI/CD servers—that warrant deeper investigation and may reveal IoCs.

### Continuous vulnerability scanning

Regular scans of CI/CD **infrastructure**, **plugins**, and **containers** surface **CVEs** and misconfigurations. These findings act as risk signals and potential precursors to compromise; **patching** reduces pipeline attack surface.

---

## Key takeaways

- **Automation** in CI/CD monitoring helps find **anomalies** and **IoCs** so teams can **respond quickly** and **limit damage**.  
- Common IoC themes: **unauthorized or suspicious code**, **bad deployment patterns**, **bad dependencies**, **broken or slow pipelines**, and **secrets issues**.  
- **Logging** (pipeline, commits, access, deployments) plus **baselining**, **SIEM**, **alerting**, **performance clues**, and **vulnerability scanning** work together.  
- Building security into CI/CD supports **confident, resilient** delivery of features and fixes while protecting the organization and its customers.
