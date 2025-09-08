# 🚔Snort Network Detection Lab — Nmap Detection & SOC Response (Ubuntu + Kali)

## 📖 Description  
## This lab shows how to deploy and operate Snort on an Ubuntu sensor to detect host and network scanning performed from a Kali attacker VM. The focus is on:
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

**Install Snort on the Ubuntu sensor and verify installation.:**  
![Snort](https://i.imgur.com/Vju1f6s.png)  

**Use ip a or ifconfig to confirm the sensor sees the lab network and target IPs.:**  
![Ifconfig](https://i.imgur.com/NWT39Dt.png)  

**Use a text editor to edit configuration(Snort.conf) if error occurs, give rwx permissions:**  
![AD Server](https://i.imgur.com/rRFOQmb.png)
![AD Server](https://i.imgur.com/rMe01rs.png)  
![AD Server](https://i.imgur.com/s9mkG0u.png) 

**Once in snort.conf Set HOME_NET to network IP range, and review enabled rules:**  
![Splunk Server](https://i.imgur.com/VpB66FT.png)  
![Splunk Server](https://i.imgur.com/tSRqn6S.png)  

**Validate configuration:**  
![Firewall Rules](https://i.imgur.com/NfMKOdz.png)  
![Firewall Group](https://i.imgur.com/Ba5ByM5.png)  

**Launch Snort to monitor an interface and log alerts:**  
![IP Config 1](https://i.imgur.com/30HCEvR.png)  

**From the Kali VM, run Nmap scans to generate reconnaissance telemetry:**  
![AD Install 1](https://i.imgur.com/WsiDLqf.png)  

**Observe Snort alerts a Nmap scan is happening, "leaking information", Use tcpdump -w /tmp/attack_capture.pcap host <attacker-ip> and host <target-ip> or tshark to save packet captures for analyst review:**  
![AD Install 1](https://i.imgur.com/Wmu0AOb.png)  

