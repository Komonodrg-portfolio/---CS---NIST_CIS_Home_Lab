### [Home](https://github.com/Komonodrg-portfolio)  | [Cybersecurity](https://github.com/Komonodrg-portfolio/Cybersecurity) | [Networking](https://github.com/Komonodrg-portfolio/Networking) | [Data Science (AI)](https://github.com/Komonodrg-portfolio/AI) | [Media Creation](https://github.com/Komonodrg-portfolio/MediaCreation) | [Mission](https://github.com/Komonodrg-portfolio/Mission/)

---
---

# 🛡️ Implementing NIST & CIS Cybersecurity Frameworks in Home Lab

## 📌 Goals
This project documents the implementation of **cybersecurity fundamentals** from the **NIST Cybersecurity Framework (CSF)** and the **CIS Critical Security Controls (CIS v8)** into a **home lab / home network**.  

The goal is to build a **practical, security-first environment** that mirrors enterprise practices, while showcasing hands-on skills in:  
- Network security  
- Endpoint hardening  
- Logging and monitoring  
- Vulnerability management  
- Identity and access controls  

---
## 🧰 Tools & Technologies

| Tool       | Purpose                              |
|------------|--------------------------------------|
| Proxmox VE     | TVirtualization platform for lab environment         |
| Wazuh | Open-source SIEM & XDR platform         |
| Suricata / Zeek    | IDS/IPS for network monitoring          |
| OpenVAS (Greenbone)  | Vulnerability scanning                      |
| Ansible / Bash scripts   | Configuration automation          |
| Linux & Windows hosts  |  Endpoints for applying hardening guides  | 

---
## 📊 NIST CSF + CIS Controls Mapping Lab Framework

| NIST CSF Function | Related CIS Controls (v8) | Purpose | Home Lab Implementation |
|-------------------|---------------------------|---------|--------------------------|
| **Identify** | CSC 1 & 2: Inventory of Assets | Understand assets, systems, and risks | - Asset inventory of Proxmox VMs and physical hosts<br>- Network diagram & VLANs in pfSense<br>- Software tracked within Wazuh |
| **Protect** | CSC 4: Secure Configurations<br>CSC 5 & 6: Account/Access Control | Safeguards to secure systems and data | - CIS benchmarks applied to Linux & Windows<br>- pfSense hardened with firewall rules & VLAN segmentation<br>- RBAC in Proxmox and Wazuh<br>- MFA and strong password policies |
| **Detect** | CSC 8: Audit Log Management<br>CSC 12 & 13: Network Monitoring & Defense | Spot anomalies and potential incidents | - Wazuh SIEM/XDR (log analysis, FIM, vuln detection)<br>- Suricata IDS integrated with pfSense<br>- Continuous monitoring dashboards |
| **Respond** | CSC 17: Incident Response Management | Contain and mitigate incidents | - Wazuh active responses (block IPs, stop processes)<br>- Incident playbooks (manual + automated)<br>- pfSense alerts & firewall event logging |
| **Recover** | CSC 16: Application Security<br>CSC 18: Penetration Testing | Restore services, validate controls, and improve | - Proxmox VM snapshots & backups<br>- Recovery testing of critical systems<br>- OpenVAS scans + remediation<br>- Kali Linux VM for controlled penetration testing |

## 🔧 Setup Instructions
