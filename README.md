# 🖥️ Active Directory Monitoring Lab 🖥️  

## 📖 Description  
This lab demonstrates **Active Directory security monitoring** and **incident response** using **Splunk** and **SOAR automation (Shuffle)**.  

- A **Windows Server Domain Controller** and a **Windows test machine** were joined under the domain `MyDFIR.local`.  
- Authentication events were forwarded to **Splunk** on an **Ubuntu server**.  
- **Splunk dashboards** and **alerts** were configured to detect suspicious login attempts.  
- Automated **Shuffle playbooks** sent notifications to SOC analysts via **Slack** and **email**, with the option to disable compromised accounts.  

This simulates how enterprise SOCs monitor Active Directory, investigate alerts, and respond to threats in real time.  

---

## 🛠️ Languages and Utilities Used  

- PowerShell  
- Splunk  
- Shuffle (SOAR automation)  
- Slack (SOC notifications)  
- SSH (remote access)  
- Remote Desktop Client  
- Linux networking utilities (ping, curl, etc.)  

---

## 🖥️ Environments Used  

- Windows Server (Active Directory Domain Controller)  
- Windows 10 (Test Machine)  
- Ubuntu Server (Splunk)  
- Vultr Cloud Hosting  

---

## 🔄 Workflow  

**Lab Diagram and Playbook Layout:**  
![Lab Diagram](https://i.imgur.com/t0cOZeZ.jpeg)  

**Provisioning 3 servers (2 Windows, 1 Ubuntu):**  
![VM Setup](https://i.imgur.com/NtiKzxm.png)  

**Windows Test Machine (55GB):**  
![Windows Test Machine](https://i.imgur.com/ZZDNoGm.png)  

**Active Directory Server (80GB):**  
![AD Server](https://i.imgur.com/eewx2iC.png)  

**Splunk Server (Ubuntu 80GB):**  
![Splunk Server](https://i.imgur.com/eewx2iC.png)  

**Firewall Group Creation & Rules:**  
![Firewall Group](https://i.imgur.com/oO1qXt8.png)  
![Firewall Rules](https://i.imgur.com/xEYVGXc.png)  

**Remote Access (RDP/SSH):**  
![RDP](https://i.imgur.com/bc14zKk.png)  
![SSH](https://i.imgur.com/UVIlZBA.png)  

**Verifying IP addresses (`ip a` / `ipconfig`):**  
![IP Config 1](https://i.imgur.com/O4kUfQB.png)  
![IP Config 2](https://i.imgur.com/gAefKCd.png)  
![IP Config 3](https://i.imgur.com/ycDLNpH.png)  

**Installing and configuring Active Directory (promote to Domain Controller):**  
![AD Install 1](https://i.imgur.com/gfhrgWh.png)  
![AD Install 2](https://i.imgur.com/OWBlaxS.png)  
![AD Install 3](https://i.imgur.com/9Ee5cVJ.png)  
