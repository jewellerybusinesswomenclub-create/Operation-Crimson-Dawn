Operation Crimson Dawn: APT Investigation with Wazuh
Laboratory evidence repository for CIP-A107: Advanced Persistent Threat Investigation, Cyber Kill Chain Analysis and Threat Intelligence with Wazuh.
Analyst: Olaronke Olajide (2026/EHIT/17106)
Date: 27 October 2026
Overview
A simulated multi-stage attack by a fictional hacktivist group (Crimson Dawn) was investigated with the Wazuh SIEM. All activity used synthetic data in an isolated laboratory. No real systems or data were involved.
Environment
Wazuh Manager, Indexer and Dashboard on an Ubuntu VM (icdfa-ubutu) in VirtualBox
The same VM acted as the monitored web server (agent ID 001, ubuntu-web-server)
Designated simulated C2 address: 203.0.113.10 (reserved documentation address, not routable)
Repository contents
Code
Activities covered
Phase
Activity
ATT&CK
1
Failed SSH logins for an invalid user; local nmap scan
T1595, T1110
2
Test script in /tmp with a cron entry; file integrity monitoring
T1036, T1053.003
3
SMB administrative share attempt against the Windows endpoint (simulated)
T1021.002
4
Synthetic file staged and archived to staged.zip; C2 connection represented by a ping and a log message
T1560.001, T1041
5
Custom Wazuh rule for the C2 address; vulnerability detection review
T1041
Custom detection rule
Xml
Configuration was validated with /var/ossec/bin/wazuh-analysisd -t.
Evidence status
The report labels each finding as Observed, Executed, Simulated or Expected. Lateral movement and data transfer were simulated and are not presented as confirmed incidents.
Safety note
No credentials, keys or real data are stored in this repository. All indicators are laboratory values.
