# Common ports quick reference (examples like 25 and 445)

## What a port number is (in one line)

A **port** identifies the **destination service/application** on a host (most commonly via **TCP** or **UDP**) so the OS knows which process should receive the traffic.

## High-signal ports to recognize

| Port | Protocol | Service | What it’s commonly used for | Security notes (why analysts care) |
|------|----------|---------|------------------------------|------------------------------------|
| 20/21 | TCP | FTP | File transfer | FTP is unencrypted by default; often replaced by SFTP/FTPS |
| 22 | TCP | SSH | Secure remote admin | Exposed SSH invites brute force; enforce keys/MFA where possible |
| 23 | TCP | Telnet | Remote admin (legacy) | Unencrypted; usually should be disabled |
| 25 | TCP | SMTP | Sending email between servers | Phishing campaigns, spam relays, mail misconfigurations |
| 53 | TCP/UDP | DNS | Name resolution | DNS tunneling, exfil, spoofing attempts; monitor query patterns |
| 67/68 | UDP | DHCP | IP assignment on local networks | Rogue DHCP can redirect traffic; impacts network access layer behavior |
| 80 | TCP | HTTP | Web (unencrypted) | Redirect to HTTPS; cleartext credentials risk |
| 110 | TCP | POP3 | Email retrieval (legacy) | Prefer encrypted variants; credential theft risk |
| 123 | UDP | NTP | Time synchronization | Time drift breaks logs/auth; NTP abuse in amplification attacks |
| 139 | TCP | NetBIOS | Legacy Windows file/printer sharing | Often disabled in modern networks; lateral movement risk |
| 143 | TCP | IMAP | Email retrieval | Prefer TLS; account takeover monitoring |
| 389 | TCP/UDP | LDAP | Directory services queries | Misconfig can expose directory info; auth-related investigations |
| 443 | TCP | HTTPS | Secure web | Certificate issues, MITM defenses; primary web app surface |
| 445 | TCP | SMB | Windows file/printer sharing | Major target for worms/ransomware; lateral movement and domain abuse |
| 3389 | TCP | RDP | Remote Desktop | Common brute-force target; restrict exposure; strong auth/monitoring |

## Notes on your examples

- **Port 25 (SMTP)**: commonly seen with **mail server** operations and investigations involving phishing/spam or misconfigured relays.
- **Port 445 (SMB)**: heavily associated with Windows file sharing and frequently shows up in **lateral movement** and **ransomware** investigations.

