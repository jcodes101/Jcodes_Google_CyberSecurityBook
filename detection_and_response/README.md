# Detection & Response — Course notes index

Google Cybersecurity Certificate — **Detection and Response** notes. Use this folder as a reference for incident response lifecycles, incident response team structures (CSIRT/SOC), and core detection tooling.

## How this folder is organized

| Location | Purpose |
|----------|---------|
| [glossary/GLOSSARY.md](glossary/GLOSSARY.md) | A–Z master term list for Course 6 (IR, CSIRT/SOC/SOAR, events/incidents, IDS/IPS/HIDS/NIDS, logs/SIEM/SPL, Suricata, YARA-L, and more) |
| [notes/01_nist_ir_lifecycle_csirt_soc_detection_tools.md](notes/01_nist_ir_lifecycle_csirt_soc_detection_tools.md) | NIST Incident Response Lifecycle, CSIRT/SOC roles, IDS/IPS/EDR, SIEM advantages and process |
| [notes/02_course6_module1_terms_and_definitions.md](notes/02_course6_module1_terms_and_definitions.md) | Quick glossary: CSIRT/SOC, IDS/IPS/EDR/SIEM/SOAR, events/incidents, detection outcomes, IR documentation |
| [notes/03_network_monitoring_baselines_and_tools.md](notes/03_network_monitoring_baselines_and_tools.md) | Network monitoring basics: baselines, what to monitor (flows/payloads/time), C2, SOC vs NOC, monitoring tools |
| [notes/04_packets_protocol_analyzers_and_pcaps.md](notes/04_packets_protocol_analyzers_and_pcaps.md) | Packets (header/payload/footer), packet sniffers, promiscuous/monitor mode, p-cap analysis, common p-cap formats |
| [notes/05_ip_headers_and_wireshark_display_filters.md](notes/05_ip_headers_and_wireshark_display_filters.md) | Internet Protocol basics (IPv4 vs IPv6 headers) + Wireshark display filter operators and common filter patterns |
| [notes/06_tcpdump_capture_filter_interpret.md](notes/06_tcpdump_capture_filter_interpret.md) | tcpdump CLI: syntax, sudo/interfaces, -w/-r/-v/-c/-n, filter expressions, reading output |
| [notes/07_methods_of_detection_hunting_intelligence_deception.md](notes/07_methods_of_detection_hunting_intelligence_deception.md) | Beyond IDS/SIEM: threat hunting, threat intelligence (feeds, TIP), cyber deception and honeypots |
| [notes/08_cicd_automation_threat_detection_iocs.md](notes/08_cicd_automation_threat_detection_iocs.md) | CI/CD security: automated monitoring, pipeline IoCs, logging/SIEM/alerting, vulnerability scanning |
| [notes/09_indicators_of_compromise_attack_pyramid_of_pain.md](notes/09_indicators_of_compromise_attack_pyramid_of_pain.md) | IoC vs IoA, Pyramid of Pain (hashes through TTPs), detection value |
| [notes/10_documentation_benefits_and_best_practices.md](notes/10_documentation_benefits_and_best_practices.md) | Why document (transparency, standardization, clarity), chain of custody, IR plans, writing tips |
| [notes/11_triage_process_receive_priority_analyze.md](notes/11_triage_process_receive_priority_analyze.md) | Alert triage: receive/assess, assign priority (impact, recoverability), collect/analyze, benefits |
| [notes/12_business_continuity_planning_bcp_sites.md](notes/12_business_continuity_planning_bcp_sites.md) | BCP vs DR, ransomware/continuity, resilience, hot/warm/cold sites |
| [notes/13_post_incident_activity_lessons_learned_final_report.md](notes/13_post_incident_activity_lessons_learned_final_report.md) | Post-incident phase: lessons learned/post-mortem, recommendations, final report (5 W’s, audience) |
| [notes/14_logs_and_log_management.md](notes/14_logs_and_log_management.md) | Logs, log types, log analysis, verbose logging, log management, retention, PII, overlogging, log protection |
| [notes/15_log_formats_json_syslog_xml_csv_cef.md](notes/15_log_formats_json_syslog_xml_csv_cef.md) | Reading logs: JSON, Syslog (PRI/header/message), XML, CSV, CEF + syslog prefix |
| [notes/16_hids_nids_and_ids_detection_techniques.md](notes/16_hids_nids_and_ids_detection_techniques.md) | HIDS vs NIDS, multi-layer detection, signature vs anomaly analysis (pros/cons) |
| [notes/17_introduction_to_suricata.md](notes/17_introduction_to_suricata.md) | Suricata IDS/IPS/NSM, rule structure, rule order, suricata.yaml, eve.json vs fast.log |
| [notes/18_siem_collect_aggregate_log_ingestion_forwarders.md](notes/18_siem_collect_aggregate_log_ingestion_forwarders.md) | SIEM three-step refresher; log ingestion, SIEM copy vs source, log forwarders (native vs third-party) |
| [notes/19_siem_search_splunk_spl_chronicle_udm_raw.md](notes/19_siem_search_splunk_spl_chronicle_udm_raw.md) | SIEM search: Splunk SPL (pipes, wildcards, phrases); Chronicle UDM vs Raw Log, procedural filtering |

## Suggested study order

1. Skim **[GLOSSARY](glossary/GLOSSARY.md)** and **02** until you can recall key terms quickly.  
2. Read **01** end-to-end once for the big picture.  
3. Read **09** to distinguish **IoCs** vs **IoAs** and to learn the **Pyramid of Pain** (pairs with **07** and **08**).  
4. Read **07** for complementary detection methods (threat hunting, intelligence, deception) after you understand the Detection and Analysis phase.  
5. Read **08** if you work with or assess **CI/CD** pipelines (IoCs, baselining, SIEM, alerts).  
6. Read **03** and **04** before network-traffic investigations or packet-capture labs.  
7. Read **05** before Wireshark filtering activities.  
8. Read **06** for command-line capture with tcpdump (pairs well with **04** p-cap formats).  
9. Read **10** for documentation benefits and analyst writing practices (supports playbooks, reports, and IR plans).  
10. Read **11** for the **triage** workflow (receive → priority → analyze/escalate).  
11. Read **12** for **business continuity** (BCP), BCP vs disaster recovery, and **hot/warm/cold** sites.  
12. Read **13** for **post-incident** work: lessons learned, recommendations, and the **final report**.  
13. Read **14** for **logs** and **log management** (pairs with **01** SIEM material and investigations).  
14. Read **15** to interpret **JSON, Syslog, XML, CSV, and CEF** log lines.  
15. Read **16** for **HIDS vs NIDS** and **signature vs anomaly** IDS detection (pairs with **01** and **09**).  
16. Read **17** for **Suricata**: modes, rules, `suricata.yaml`, and **eve.json** vs **fast.log** (pairs with **04**–**06** and **15**).  
17. Read **18** for **SIEM** data collection: **log ingestion**, **forwarders**, and how central copies support investigations (pairs with **01** and **14**).  
18. Read **19** for **SIEM search** patterns: **Splunk SPL** and **Chronicle** (**UDM** vs **Raw Log**).  
19. Revisit the **NIST lifecycle** section (01) before incident response scenario questions.

