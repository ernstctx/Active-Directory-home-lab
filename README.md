<h1>Active Directory - Configured client-server network</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
Create domain controller (Win Server 2019) on Virtual Machine using Oracle VirtualBox. Domain controller boasts an internal network adapter (assigned IP address) and an external network adapter NIC (DHCP enabled). Install Active Directory on the Win Server 2019 and create a domain: <cayedomain.com> Configure NAT and routing –permits client users on private network to access the internet through the domain controller. Setup DHCP (1 Scope) on the domain controller--Range:172.16.0.100-200/Mask:255.255.255.0/Gateway:172.168.01/DNS:172.16.0.1 DHCP permits client pc joined to domain to automatically obtain IP address.
<br/> 
Run PowerShell script>automatically creates 1K users in Active Directory.
<br/>
Create/deploy client virtual machine(Windows 10) using Oracle, VirtualBox. The Win10 client machine will be connected to the private network on the WinSer2019, domain controller. Log into the client machine using one of the domain accounts created using PowerShell script.
<br />


<h2>Topics</h2>

- <b>PowerShell</b> 
- <b>Active Directory</b>
- <b>Domain Controller</b>
- <b>Routing(RAS/NAT)</b>
- <b>DHCP</b>
- <b>Organizational Unit</b>
- <b>Command LineP</b>
- <b>IP addressing</b>
- <b>Client</b>
- <b>Network segmentation</b>

<h2>Environment </h2>

- <b>Windows 10</b> 
- <b>Windows Server 2019</b> 
- <b>Oracle VirtualBox</b> 
 
<h2>Active Directory lab walk-through:</h2>

<p align="center">
Network overview: <br/>
<img src="https://i.imgur.com/0HQfj07.png" width="80%"
<br/>
<br/>
Next step: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
