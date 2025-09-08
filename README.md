# 🚔Intrusion Detection Systems (SNORT) Lab🚔

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

**Install Snort:**  
![Snort](https://i.imgur.com/YJ0X1Gt.png)  

**With Ifconfig, make sure both machines are on the same network:**  
![Ifconfig](https://i.imgur.com/NWT39Dt.png)  

**Use a text editor to view Snort.conf if error occurs you must give rwx permisions:**  
![AD Server](https://i.imgur.com/rRFOQmb.png)
![AD Server](https://i.imgur.com/rMe01rs.png)  

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
