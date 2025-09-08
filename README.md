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
![Snort](https://i.imgur.com/Vju1f6s.png)  

**With Ifconfig, make sure both machines are on the same network:**  
![Ifconfig](https://i.imgur.com/NWT39Dt.png)  

**Use a text editor to view Snort.conf if error occurs, you must give rwx permissions:**  
![AD Server](https://i.imgur.com/rRFOQmb.png)
![AD Server](https://i.imgur.com/rMe01rs.png)  
![AD Server](https://i.imgur.com/s9mkG0u.png) 

**Using a text editor, open snort.conf and change ipvar network lan range, also view different rules towards the bottom:**  
![Splunk Server](https://i.imgur.com/VpB66FT.png)  
![Splunk Server](https://i.imgur.com/tSRqn6S.png)  

**Validate configuration:**  
![Firewall Rules](https://i.imgur.com/NfMKOdz.png)  
![Firewall Group](https://i.imgur.com/Ba5ByM5.png)  

**Start Snort:**  
![IP Config 1](https://i.imgur.com/30HCEvR.png)  

**On attacking machine use Nmap to run ip on target:**  
![AD Install 1](https://i.imgur.com/WsiDLqf.png)  

**Snorts alerts that theres a nmap scan happeing leaking informatiom:**  
![AD Install 1](https://i.imgur.com/Wmu0AOb.png)  

