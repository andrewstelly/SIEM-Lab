# SIEM Honeypot Lab

## Description  
I set up Azure Sentinel (SIEM) and connected it to a live virtual machine acting as a honeypot. I observed real-time brute-force RDP attacks from around the world. A custom PowerShell script collected geolocation data of attackers and plotted it on the Azure Sentinel Map.

---

## Languages and Utilities Used
- **PowerShell**  
- **Azure**

## Environments Used
- **Windows 10**

---

## Program Walkthrough

<p align="center">
Create a virtual machine through Microsoft Azure with an open firewall  
<br/>
<img src="./images/Part1.png" width="80%" alt="Azure VM Setup"/>
<br/><br/>
  
<p align="center">
After creating the VM, disable the firewall and ensure ICMP Echo requests work (pingable)  
<br/>
<img src="./images/Part2.png" width="80%" alt="Firewall Disabled"/>
<br/><br/>

<p align="center">
Run a PowerShell script to log geolocation data of login attempts  
<br/>
<img src="./images/Part3.png" width="80%" alt="PowerShell Script"/>
<br/><br/>

<p align="center">
Verify logs are being written correctly  
<br/>
<img src="./images/Part4.png" width="80%" alt="Log Output"/>
<br/><br/>

<p align="center">
Observe attempts in the Windows Event Log (Security log)  
<br/>
<img src="./images/Part 5.png" width="80%" alt="Security Log"/>
<br/><br/>

<p align="center">
View usernames being targeted, most often 'administrator'  
<br/>
<img src="./images/Part 6.png" width="80%" alt="Username Enumeration"/>
<br/><br/>

<p align="center">
Use Azure Monitor to capture failed login attempts  
<br/>
<img src="./images/Part 7.png" width="80%" alt="Azure Log Analytics"/>
<br/><br/>

<p align="center">
Visualize attacker geolocation data in Microsoft Sentinel  
<br/>
<img src="./images/Part 8.png" width="80%" alt="Sentinel Visualization"/>
<br/><br/>

<p align="center">
Final attack map showing global brute-force RDP attempts  
<br/>
<img src="./images/Part 9.png" width="80%" alt="Final Sentinel Map"/>
</p>
