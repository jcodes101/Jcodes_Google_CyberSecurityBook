# Networks and network security — Course notes index

Google Cybersecurity Certificate — material on **network infrastructure**, **devices**, **firewalls**, **VPNs**, **security zones** and **segmentation**, **subnetting/CIDR**, the **network (IP) layer**, **cloud networking (CSP/SDN)**, **TCP/IP vs OSI**, **proxies**, and a **Course 3 glossary**.

## Contents

| Location | Purpose |
|----------|---------|
| [notes/17_brute_force_attacks_testing_environments_and_prevention.md](notes/17_brute_force_attacks_testing_environments_and_prevention.md) | **Brute force** and **dictionary** attacks; **VMs** and **sandboxes**; prevention (**hashing/salting**, **MFA/2FA**, **CAPTCHA**) |
| [notes/18_cloud_security_considerations_shared_responsibility_and_hardening.md](notes/18_cloud_security_considerations_shared_responsibility_and_hardening.md) | **Cloud security**: **IAM**, configuration, attack surface, visibility; **shared responsibility**; hardening (hypervisors, baselines, cryptography) |
| [notes/05_common_ports_quick_reference.md](notes/05_common_ports_quick_reference.md) | **Common ports** quick reference (**25 SMTP**, **445 SMB**, **443 HTTPS**, etc.) |
| [notes/03_cloud_computing_and_sdn.md](notes/03_cloud_computing_and_sdn.md) | **CSPs**, **SaaS / IaaS / PaaS**, **hybrid + multi-cloud**, **SDN** benefits (**reliability / cost / scalability**) |
| [notes/16_denial_of_service_dos_ddos_and_common_attacks.md](notes/16_denial_of_service_dos_ddos_and_common_attacks.md) | **DoS/DDoS** fundamentals and common attacks (**SYN flood**, **ICMP flood**, **ping of death**) |
| [notes/10_firewalls_types_stateful_stateless_and_ngfw.md](notes/10_firewalls_types_stateful_stateless_and_ngfw.md) | **Firewalls**: hardware/software/cloud (**FaaS**), **port filtering**, **stateful** vs **stateless**, **NGFW** |
| [glossary/GLOSSARY.md](glossary/GLOSSARY.md) | **Glossary** — Course 3 terms and definitions (**A–Z**) |
| [notes/15_network_interception_backdoors_and_protocol_analyzers_tcpdump.md](notes/15_network_interception_backdoors_and_protocol_analyzers_tcpdump.md) | **Interception** and **backdoor** attacks; protocol analyzers (**tcpdump**) and what captures show |
| [notes/08_nat_dhcp_arp_and_email_protocols.md](notes/08_nat_dhcp_arp_and_email_protocols.md) | **NAT**, **DHCP**, **ARP**, **Telnet/SSH**, and **POP3/IMAP/SMTP** with key ports |
| [notes/06_network_layer_ipv4_ipv6_packets.md](notes/06_network_layer_ipv4_ipv6_packets.md) | **Network layer** ops, **IPv4** packet (**header + data**, **13** header fields), **routing tables**, **IPv6** vs **IPv4** |
| [notes/07_overview_of_network_protocols.md](notes/07_overview_of_network_protocols.md) | **Network protocols** overview: **communication**, **management**, **security**; **TCP/UDP**, **DNS**, **HTTP/HTTPS**, **SNMP**, **ICMP**, **SFTP** |
| [notes/01_network_devices_and_lan_architecture.md](notes/01_network_devices_and_lan_architecture.md) | **Network vs devices**, packets, **firewalls**, **servers**, **hubs/switches**, **routers**, **modems**, **WAPs**, **client–server**, **diagrams** for analysts |
| [notes/14_proxies_vpn_types_sd_wan_wireguard_and_ipsec.md](notes/14_proxies_vpn_types_sd_wan_wireguard_and_ipsec.md) | **Proxies** (forward/reverse), **remote** vs **site-to-site VPN**, **SD-WAN**, **WireGuard** vs **IPsec** |
| [notes/12_security_zones_dmz_and_network_segmentation.md](notes/12_security_zones_dmz_and_network_segmentation.md) | **Security zones**: **uncontrolled/controlled**, **DMZ**, **restricted**, **segmentation** |
| [notes/13_subnetting_and_cidr.md](notes/13_subnetting_and_cidr.md) | **Subnetting** and **CIDR** notation (**/** prefix), classful vs classless (overview) |
| [notes/04_tcpip_model_and_osi_comparison.md](notes/04_tcpip_model_and_osi_comparison.md) | **TCP/IP 4-layer model** + how it compares to the **OSI 7-layer model** |
| [notes/11_vpn_encapsulation_encryption_and_privacy.md](notes/11_vpn_encapsulation_encryption_and_privacy.md) | **VPN** basics: **encapsulation**, encryption in transit, privacy on public networks |
| [notes/02_lan_connection_diagram_emojis.md](notes/02_lan_connection_diagram_emojis.md) | **Visual LAN flow** (emoji diagram) — how traffic moves from internet to devices |
| [notes/09_introduction_to_wireless_security_protocols.md](notes/09_introduction_to_wireless_security_protocols.md) | **Wireless security**: Wi‑Fi / **IEEE 802.11**, **WEP → WPA → WPA2 → WPA3**, **TKIP / CCMP / AES**, **SAE** |

## Suggested order

1. Read **01** for definitions and roles of each device type.  
2. Use **02** as a quick **mental map** of a typical LAN (home/small office style, per course).
3. Read **03** for **cloud service models**, **hybrid/multi-cloud**, and **SDN** concepts.  
4. Read **04** for **TCP/IP layers**, protocols, and **OSI comparison**.  
5. Read **06** for **IP routing**, **IPv4 header fields**, and **IPv4 vs IPv6**.  
6. Read **07** for the core **protocol categories** and how common protocols fit into the **TCP/IP model**.  
7. Read **08** for **NAT**, **DHCP/ARP**, and core **mail/remote access protocols**.  
8. Read **09** for **Wi‑Fi security protocols** (WEP/WPA/WPA2/WPA3) and why the newer ones matter.  
9. Read **10** for **firewall** types and **stateful vs stateless** vs **NGFW**.  
10. Read **12** for **security zones**, **DMZ**, and **segmentation**.  
11. Read **13** for **subnetting** and **CIDR** basics.  
12. Read **11** for **VPN** encapsulation/encryption concepts.  
13. Read **14** for **proxies**, **VPN deployment types**, **SD-WAN**, and **WireGuard vs IPsec**.  
14. Read **15** for **interception/backdoors** and the basics of **protocol analyzers** (tcpdump).  
15. Read **16** for **DoS/DDoS** patterns and common attacks (SYN flood, ICMP flood, ping of death).  
16. Read **17** for brute force patterns plus safe testing with **VMs/sandboxes** and prevention controls.  
17. Read **18** for **cloud security** considerations, shared responsibility, and hardening techniques.  
18. Keep **05** open as a **ports cheat sheet** while you study application-layer services.
