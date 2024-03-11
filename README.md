<h1>SIEM Honeypot Lab</h1>

<h2>Description</h2>
I setup Azure Sentinel (SIEM) and connected it to a live virtual machine acting as a honey pot. I observed live attacks (RDP Brute Force) from all around the world. I used a custom PowerShell script to look up the attackers Geolocation information and plot it on the Azure Sentinel Map!
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Azure</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>

<h2>Program walkthrough:</h2>

<p align="center">
Create a virtual machine through Microsoft Azure with an open firewall <br/>
<img src="https://i.imgur.com/MLUCZP7.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
After creating the virtual machine, turn off all firewall settings and ping the machine, ensuring that echo requests are allowed  <br/>
<img src="https://i.imgur.com/5ZEd8wE.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
Use PowerShell script that collects geographic data on users that attempt to log into the virtual machine <br/>
<img src="https://i.imgur.com/vJJ0AGU.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
Run the PowerShell script. Should successfully recieve pings and they should be sent to the log file   <br/>
<img src="https://i.imgur.com/FfLoRrk.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
These pings can also be observed in the Windows Security Log  <br/>
<img src="https://i.imgur.com/Ut6h9sD.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
Within PowerShell, you can information such as the username the attackers are attempting, which in my case was most commonly administrator <br/>
<img src="https://i.imgur.com/hu1Pbta.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
After creating a Log in Azure, you can now view the failed login information of attackers pinging the VM from your Azure account   <br/>
<img src="https://i.imgur.com/zvmqUjx.png" height="80%" width="80%" alt="SIEM Steps"/>
<br/>
<br/>
Now that you are receiving the geodata of the attackers on your Azure account, you can now visualize this information through Microsoft Sentinel <br/>
<img src="https://i.imgur.com/iLI7pzw.png" height="80%" width="80%" alt="SIEM Steps"/>
<br/>
<br/>
Complete Map <br/>
<img src="https://i.imgur.com/iaqHBlb.png" height="80%" width="80%" alt="SIEM Steps"/>
<br/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
