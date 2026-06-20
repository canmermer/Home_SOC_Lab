Home-SOC-Lab

⚠️ Disclaimer This project is built strictly for educational purposes. All attack simulations are performed exclusively against virtual machines I own and control, inside a fully isolated network with no external connectivity. The tools and techniques demonstrated here reflect real-world adversary behavior and are documented solely to develop and showcase defensive security skills. Reproducing any of these techniques against systems you do not own or have explicit written permission to test is illegal and unethical.



Ubuntu Server 24.04 — SIEM — 192.168.56.10 Wazuh 4.14.5 (Indexer, Manager, Filebeat, Dashboard)



Windows 11 — Victim Endpoint — 192.168.56.20 Wazuh Agent 4.14.5, Sysmon



Kali Linux — Attacker — 192.168.56.30 nmap, Hydra, Medusa



Stack



SIEM: Wazuh 4.14.5



Endpoint telemetry: Sysmon



Hypervisor: Oracle VirtualBox



Attack tools: nmap, Hydra, Medusa



Framework: MITRE ATT\&CK



Scenario 01 — Reconnaissance \& SSH Brute Force



MITRE ATT\&CK: T1046 — Network Service Discovery | T1110 — Brute Force



Goal: Simulate an attacker discovering open ports on a defended Windows 11 host and following up with an automated credential attack against the exposed SSH service — then observe how the SIEM captures both phases.



Condition: Windows Firewall enabled throughout.



Phase 1 — Network Reconnaissance: nmap full-port scan from Kali to map the attack surface.



Phase 2 — SSH Brute Force: Hydra (primary) and Medusa (fallback).

