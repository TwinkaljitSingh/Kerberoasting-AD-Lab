# Kerberoasting-AD-Lab

## Author: Twinkaljit Singh  
## Project: Mega Hacking Final Project: Kerberoasting Attack & Mitigation  


### Project Summary  
This repository contains a complete **Active Directory Kerberoasting Lab** built using Windows Server 2022 and Windows 10.  
The project demonstrates:

- Kerberos ticket extraction using **Rubeus**
- Offline password cracking using **Hashcat**
- Privilege escalation using cracked service account password
- Successful **Domain Admin compromise**
- Hardening & Mitigation techniques implemented
- Re-testing proves **attack fails after mitigation**

This repo includes **Lab Creation Guide**, **Attack Report**, **Mitigation Report**, and **screenshots** to reproduce this environment.



### Repository Structure

Kerberoasting-AD-Lab/
├── LabGuide.pdf
├── AttackReport.pdf
├── MitigationReport.pdf
├── screenshots/
├── wordlists/
└── README.md



### Tools & Technologies

| Component           |      Role                      |
|---------------------|--------------------------------|
| Windows Server 2022 | Domain Controller + DNS        |
| Windows 10          | Workstation (Attacker machine) |
| Active Directory    | Kerberos Authentication        |
| Rubeus              | Extract TGS tickets            |
| Hashcat             | Offline cracking               |
| VMware              | Virtualization platform        |


### How to Reproduce

1. Build AD lab using **LabGuide.pdf**
2. Run Kerberoasting attack using **AttackReport.pdf**
3. Crack service ticket hash using Hashcat
4. Escalate privileges using cracked password
5. Apply mitigations from **MitigationReport.pdf**
6. Run attack again -> attack blocked 


### Mitigation Implemented

- Strong password for service account
- Removed Domain Admin rights (least privilege)
- Enabled password rotation
- Optional: Disable RC4 -> Force AES
- Monitoring Kerberos TGS events (Event ID 4769)



### Before vs After Impact

| Stage                 | Result                                 |
|-----------------------|----------------------------------------|
| **Before Mitigation** | Attack SUCCESS: Domain Admin acquired  |
| **After Mitigation**  | Attack FAILED: Hash not cracked        |



### Disclaimer  
This project is for **education & internal lab use only.**  
Do NOT perform Kerberoasting on systems without permission.



### Status: Complete  
Project successfully executed, mitigated & validated.
