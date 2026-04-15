# Glossary — Networks and network security (Course 3)

Alphabetical list of **terms and definitions** from **Course 3** (Modules 1–3 and related readings/videos).

---

**2FA (two-factor authentication)** — A form of MFA that uses exactly two verification factors.

**Active packet sniffing** — A type of attack where data packets are manipulated in transit.

**Address Resolution Protocol (ARP)** — Used to determine the MAC address of the next router or device to traverse.

**Advanced Encryption Standard (AES)** — A widely used encryption standard; WPA2/WPA3 wireless security relies on AES in course materials.

**Attack surface** — The total set of exposed services, interfaces, and entry points that could be attacked; expanding cloud service usage can increase attack surface and complexity.

**Azure Network Watcher** — A network monitoring and diagnostic service/tool referenced as a network protocol analyzer option in the course.

**Backdoor** — A hidden access method that bypasses normal access controls, sometimes left for troubleshooting or installed by attackers for persistence.

**Baseline configuration (baseline image)** — A documented set of specifications within a system that is used as a basis for future builds, releases, and updates.

**Baseline** — A fixed reference configuration that can be used to compare and detect changes (configuration drift).

**Baselining** — Establishing a baseline configuration so changes can be measured against a known-good reference.

**Bandwidth** — The maximum data transmission capacity over a network, measured by bits per second.

**Bluetooth** — Used for wireless communication with nearby physical devices.

**Botnet** — A collection of computers infected by malware that are under the control of a single threat actor (a “bot-herder”).

**Brute force attack** — A trial-and-error attack used to guess private information (commonly passwords).

**CAPTCHA** — “Completely Automated Public Turing test to tell Computers and Humans Apart”; a test used to distinguish humans from bots and reduce automated brute forcing.

**Classful addressing** — Legacy IPv4 addressing scheme grouping addresses into fixed classes (Class A–E); largely replaced by classless approaches as the internet grew.

**Classless Inter-Domain Routing (CIDR)** — A flexible method of representing IP networks using address + prefix length (for example `198.51.100.0/24`) to support modern subnetting and routing.

**Cloud computing** — The practice of using remote servers, applications, and network services that are hosted on the internet instead of on local physical devices.

**Cloud-based firewalls** — Software firewalls that are hosted by the cloud service provider.

**Cloud hardware security module (CloudHSM)** — A cloud device/service that provides secure storage for cryptographic keys and performs cryptographic operations.

**Cloud network** — A collection of servers or computers that stores resources and data in remote data centers that can be accessed via the internet.

**Configuration drift** — Changes from a known-good baseline over time that can introduce security or reliability issues.

**Controlled zone** — A protected internal network area that sits between untrusted external networks and sensitive internal assets (often implemented with subnets, routing, and firewalls).

**Counter Mode Cipher Block Chain Message Authentication Code Protocol (CCMP)** — A WPA2-related protocol that provides encapsulation and ensures message authentication and integrity.

**Cryptographic erasure (crypto-shredding)** — Destroying encryption keys so encrypted data becomes unreadable/undecryptable in practice.

**Cryptography** — Using encryption and secure key management to provide confidentiality and integrity protections for data.

**Data packet** — A basic unit of information that travels from one device to another within a network.

**Deep packet inspection (DPI)** — Inspection that examines packet contents beyond basic headers; commonly associated with NGFW capabilities.

**Demilitarized zone (DMZ)** — A perimeter network segment that hosts public-facing services (web, DNS, mail, proxies) between the internet and the internal network.

**Denial of service (DoS) attack** — An attack that targets a network or server and floods it with network traffic.

**Dictionary attack** — A password-guessing attack that uses lists of common passwords and/or previously breached credentials.

**Distributed denial of service (DDoS) attack** — A type of denial of service attack that uses multiple devices or servers located in different locations to flood the target network with unwanted traffic.

**Domain Name System (DNS)** — A protocol that translates internet domain names into IP addresses.

**Dynamic Host Configuration Protocol (DHCP)** — An application-layer protocol used to automatically assign network settings such as IP address, DNS server, and default gateway information to client devices.

**Encryption** — The process of transforming readable data into ciphertext that is unreadable without the encryption key.

**Encapsulation (VPN)** — Wrapping protected payload traffic inside outer packets so it can traverse a network while keeping inner data confidential.

**Encapsulation** — A process performed by a VPN service that protects your data by wrapping sensitive data in other data packets.

**FedRAMP** — A U.S. program that provides a list/standardization for vetted cloud service providers for federal use (course reference).

**File Transfer Protocol (FTP)** — Used to transfer files from one device to another over a network.

**Firewall** — A network security device that monitors traffic and allows or blocks it based on configured rules aligned with security policy.

**Firewall as a Service (FaaS)** — A cloud-hosted firewall offering where a CSP provides firewall capabilities and centralized policy management.

**Forward proxy** — A server that regulates and restricts a person’s access to the internet.

**Forward proxy server** — A server that regulates and restricts a person’s access to the internet.

**Hashing** — A one-way function that converts data into a unique value used for integrity checking (commonly used for password storage).

**Hardware** — The physical components of a computer.

**Hub** — A network device that broadcasts information to every device on the network.

**Hypertext Transfer Protocol (HTTP)** — An application-layer protocol that provides a method of communication between clients and website servers.

**Hypertext Transfer Protocol Secure (HTTPS)** — A secure version of HTTP that uses SSL/TLS encryption to protect communication between clients and website servers.

**Hypervisor** — A virtualization layer that abstracts host hardware for operating environments; CSPs commonly manage type 1 hypervisors in cloud infrastructures.

**IAM (identity and access management)** — Processes and technologies used to manage digital identities and authorize how users can access and use resources.

**ICMP flood** — See **Internet Control Message Protocol (ICMP) flood**.

**IEEE 802.11** — A family of wireless networking standards that Wi‑Fi is based on.

**Internet Control Message Protocol (ICMP)** — An internet protocol used by devices to report transmission errors and network status information.

**Internet Control Message Protocol (ICMP) flood** — A type of DoS attack performed by an attacker repeatedly sending ICMP request packets to a network server.

**Internet Message Access Protocol (IMAP)** — An email protocol for retrieving mail while keeping messages on the server, enabling multi-device synchronization.

**Internet Protocol (IP)** — A set of standards used for routing and addressing data packets as they travel between devices on a network.

**Internet Protocol (IP) address** — A unique string of characters that identifies the location of a device on the internet.

**IP network prefix** — The `/number` suffix in CIDR notation that defines the network portion of an address (for example `/24`).

**IP spoofing** — A network attack performed when an attacker changes the source IP of a data packet to impersonate an authorized system and gain access to a network.

**IPsec** — A suite of protocols commonly used to encrypt and authenticate network traffic; frequently used for site-to-site VPN tunnels.

**Key management** — Practices and tools for securely storing, rotating, and controlling access to encryption keys.

**LAN (Local Area Network)** — A network that spans small areas like an office building, a school, or a home.

**libpcap** — An open-source packet capture library used by tools such as tcpdump.

**MAC address (Media Access Control address)** — A unique alphanumeric identifier that is assigned to each physical device on a network.

**ManageEngine OpManager** — A network monitoring tool referenced as a network protocol analyzer option in the course.

**MFA (multi-factor authentication)** — Authentication requiring two or more verification factors (e.g., password + biometrics or OTP).

**Modem** — A device that connects your router to the internet and brings internet access to the LAN.

**Network** — A group of connected devices.

**Network Address Translation (NAT)** — A process that maps private IP addresses to a public IP address (and back for return traffic), usually at a router or firewall.

**Network log analysis** — The process of examining network logs to identify events of interest.

**Network protocol** — A set of rules used by devices on a network to describe the order of delivery and the structure of data.

**Network protocols** — A set of rules used by two or more devices on a network to describe the order of delivery of data and the structure of data.

**Network segmentation** — Dividing a network into separate segments/zones with distinct access rules to reduce blast radius and improve security.

**Network virtual appliance (NVA)** — A virtualized form of a network security function (for example a firewall) delivered as software.

**Next-generation firewall (NGFW)** — An advanced firewall that typically combines stateful inspection with deeper inspection and modern threat prevention features (often application-aware).

**On-path attack** — An attack where a malicious actor places themselves in the middle of an authorized connection and intercepts or alters data in transit.

**One-time password (OTP)** — A temporary code used as an authentication factor (commonly for 2FA/MFA).

**Operating system (OS)** — The interface between computer hardware and the user.

**Open systems interconnection (OSI) model** — A standardized concept that describes the seven layers computers use to communicate and send data over the network.

**Packet analyzer** — A tool used to capture and analyze network traffic (often used interchangeably with packet sniffer/protocol analyzer).

**Packet sniffer** — A tool used to capture and inspect packets traveling across a network.

**Packet sniffing** — The practice of capturing and inspecting data packets across a network.

**Passive packet sniffing** — A type of attack where a malicious actor connects to a network hub and looks at all traffic on the network.

**Password policy** — Organizational rules for password complexity, rotation, reuse, and login attempt limits/lockouts.

**Patch update** — A software and operating system update that addresses security vulnerabilities within a program or product.

**Penetration testing (pen test)** — A simulated attack that helps identify vulnerabilities in systems, networks, websites, applications, and processes.

**Ping of death** — A type of DoS attack caused when a hacker pings a system by sending it an oversized ICMP packet that is bigger than 64KB (course framing).

**Port** — A software-based location that organizes the sending and receiving of data between devices on a network.

**Port filtering** — A firewall function that blocks or allows certain port numbers to limit unwanted communication.

**Post Office Protocol version 3 (POP3)** — An email retrieval protocol that downloads messages from a mail server to a local device.

**Private IP address** — An IP address intended for internal network use, not globally routable on the public internet.

**Proxy server** — A server that fulfills the requests of its clients by forwarding them to other servers.

**Public IP address** — A globally routable IP address used for communication over the public internet.

**reCAPTCHA** — A free CAPTCHA service from Google that helps protect websites from bots and malicious automation.

**Remote access VPN** — A VPN that connects an individual endpoint to a VPN gateway/server over the internet.

**Replay attack** — A network attack performed when a malicious actor intercepts a data packet in transit and delays it or repeats it at another time.

**Restricted zone** — A highly protected network segment for confidential assets, accessible only to privileged users/systems.

**Reverse proxy** — A server that regulates and restricts the Internet's access to an internal server.

**Reverse proxy server** — A server that regulates and restricts the Internet's access to an internal server.

**Router** — A network device that connects multiple networks together.

**Salting** — Adding random characters to passwords before hashing to increase hash complexity and reduce cracking effectiveness.

**Sandbox** — A testing environment that allows software to execute separately from production systems/networks for patch testing, vulnerability discovery, and suspicious file analysis.

**Secure File Transfer Protocol (SFTP)** — A secure protocol used to transfer files from one device to another over a network, typically using SSH over TCP port 22.

**Secure Shell (SSH)** — A secure protocol commonly used for encrypted remote access and for securing services such as SFTP.

**Security zone** — A network segment with defined trust boundaries and controls (often implemented with segmentation and firewalls).

**Security hardening** — The process of strengthening a system to reduce its vulnerabilities and attack surface.

**Shared responsibility model** — A cloud security principle where the CSP secures the underlying infrastructure, while the customer secures their data, configurations, and workloads they run in the cloud.

**Security information and event management (SIEM)** — An application that collects and analyzes log data to monitor critical activities for an organization.

**Simple Mail Transfer Protocol (SMTP)** — A protocol used to send and route email between systems.

**Simple Network Management Protocol (SNMP)** — A network protocol used for monitoring and managing devices on a network.

**Simultaneous Authentication of Equals (SAE)** — A password-authenticated key agreement used by WPA3 to strengthen Wi‑Fi authentication.

**Site-to-site VPN** — A VPN that connects entire networks/sites (for example branch offices) over encrypted tunnels.

**Smurf attack** — A network attack performed when an attacker sniffs an authorized user’s IP address and floods it with ICMP packets.

**Software-defined wide area network (SD-WAN)** — A virtual WAN approach to connect users and sites across distances with modern, centrally managed networking and security integration.

**SolarWinds NetFlow Traffic Analyzer** — A network monitoring/analysis tool referenced as a network protocol analyzer option in the course.

**Speed** — The rate at which a device sends and receives data, measured by bits per second.

**SSL/TLS** — Encryption protocols used to protect data in transit, such as traffic sent over HTTPS.

**Stateful firewall** — A firewall that tracks session/connection state and can enforce rules based on observed traffic behavior.

**Stateful** — A class of firewall that keeps track of information passing through it and proactively filters out threats.

**Stateless firewall** — A firewall that enforces primarily static rules without maintaining connection state.

**Stateless** — A class of firewall that operates based on predefined rules and that does not keep track of information from data packets.

**Subnetting** — The subdivision of a network into logical groups called subnets.

**Synchronize (SYN) flood attack** — A type of DoS attack that simulates a TCP/IP connection and floods a server with SYN packets.

**Switch** — A device that makes connections between specific devices on a network by sending and receiving data between them.

**TCP/IP model** — A framework used to visualize how data is organized and transmitted across a network.

**tcpdump** — A lightweight command-line network protocol analyzer that captures and prints packet details (timestamp, IPs, ports) and uses libpcap.

**Telnet** — An application-layer remote access protocol that sends data in clear text and typically uses TCP port 23.

**Temporal Key Integrity Protocol (TKIP)** — A protocol introduced with WPA to address weaknesses in WEP’s encryption usage.

**TPM (Trusted Platform Module)** — A computer chip that can securely store passwords, certificates, and encryption keys.

**Transmission Control Protocol (TCP)** — An internet communication protocol that allows two devices to form a connection and stream data.

**Transmission control protocol (TCP) 3-way handshake** — A three-step process used to establish an authenticated connection between two devices on a network.

**Type 1 hypervisor** — A hypervisor that runs directly on host hardware (example: VMware ESXi).

**Type 2 hypervisor** — A hypervisor that runs on top of a host operating system (example: VirtualBox).

**Uncontrolled zone** — Networks outside organizational control (commonly the internet).

**User Datagram Protocol (UDP)** — A connectionless protocol that does not establish a connection between devices before transmissions.

**Virtual machine (VM)** — A software version of a physical computer used to run code in an isolated environment; supports snapshots and safe testing but still carries some isolation-escape risk.

**Virtual Private Network (VPN)** — A network security service that changes your public IP address and masks your virtual location so that you can keep your data private when you are using a public network like the internet.

**VM escape** — An exploit where malicious code escapes virtualization/sandbox boundaries to access the host system or other VMs.

**WEP (Wired Equivalent Privacy)** — A legacy wireless security protocol (introduced in 1999) now considered high risk.

**Wi‑Fi** — A set of standards that define communication for wireless LANs, based on IEEE 802.11.

**Wi‑Fi Alliance** — The industry group that manages Wi‑Fi branding and certification; formerly the Wireless Ethernet Compatibility Alliance (WECA).

**Wi‑Fi Protected Access (WPA)** — A wireless security protocol introduced in 2003 to replace WEP and improve wireless security; uses TKIP and integrity checks.

**Wi‑Fi Protected Access 2 (WPA2)** — A Wi‑Fi security protocol introduced in 2004 that uses AES and CCMP; long considered the standard for Wi‑Fi security.

**Wi‑Fi Protected Access 3 (WPA3)** — A Wi‑Fi security protocol introduced in 2018 that improves authentication and encryption and uses SAE.

**Wireshark** — A widely used GUI packet analyzer referenced as a network protocol analyzer option in the course.

**WireGuard** — A high-speed VPN protocol with advanced encryption, designed to be simpler to set up and maintain than many legacy VPN approaches (course framing).

**Wireless Ethernet Compatibility Alliance (WECA)** — The former name of the organization now called the Wi‑Fi Alliance.

**Wide Area Network (WAN)** — A network that spans a large geographic area like a city, state, or country.

**World-writable file** — A file that can be altered by anyone in the world.

**Zero-day attack** — An exploit that was previously unknown (before a fix is widely available).
