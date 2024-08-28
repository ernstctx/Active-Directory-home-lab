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
Next step: Visit virtualbox.org to download VirtualBox<br/>
<img src="https://i.imgur.com/dmSDtJU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
Next step:download WinSer 2019 ISO
<img src="https://i.imgur.com/e7z8IKT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Deploy a Virtual Machine:  <br/>
<img src="https://i.imgur.com/MbFvDLR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
Oracle VirtualBox^Create 1st Microsoft 2019 VM|Ram 2G=2048 MB, 4 core processor, /net adapater 1 NAT /net adapter 2 internal /Standard desktop experience(GUI)
<br />
<br />
Configure NIC: <br/> 
<img src="https://i.imgur.com/XaTLTJ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
configure NIC^righ+click Network/change adapter option/right+click>rename NIC and specify between gateway and internal NIC. Internal NIC IP:169.254.196.79 <internal >[assign IP address to internal adapter>IPv4 Properties>IP:172.16.0.1/Sub Mask:255.255.255.0/Def Gateway: [blank]] [DNS Server:172.0.0.1]
<br />
<br />
Configure network adapters and label(identify) inner and outer NIC:  <br/>
<img src="https://i.imgur.com/rh0BVN0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create domain: Organization Unit  <br/>
>Right+click Network icon on desktop/
<br />
>Install Active Directory^Server Manager dashboard/add roles and features/server location/select server/Active directory Domain Services^
<br />
>Active Directory Domain Services Configuration Wizard>add new forest>create domain>name domain. >[mydomainname.com] rename domain once PC reboots
<br />
Log into created domain
<img src="https://i.imgur.com/HPMFKVr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create Organizational Unit | domain admins:  <br/>
<img src="https://i.imgur.com/R2dSLH9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Organizational Unit | Admins:  <br/> 
Organizational Unit>Admin account/[  ]>select [mydomainname.com]>right+click>New>Organizational Unit>[_admin]/right+click>New user>create new user
<img src="https://i.imgur.com/IUjE2SE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
*Naming convention ex. A_ ECayemitte(indicate admin acct for DC/domain0
>Set up Admin account
>in Domain Admin>right click properties>add|domain admin
<img src="https://i.imgur.com/MtX4zf6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Network MAP>install RAS/NAT(Remote access servr/Network address translation) in domain controller>add roles & features>routing 
<img src="https://i.imgur.com/xbBN08c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> 
Next
<img src="https://i.imgur.com/NQEi0IW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br />
Next
<img src="https://i.imgur.com/A4HeUWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Next
<img src="https://i.imgur.com/A4HeUWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
*RAS/NAT allows joined client1 to remain on private network and 
allowed to access the internet through the domain controller*
<img src="https://i.imgur.com/rDb6SFI.png" height="80%" width="80%" alt="Disk Sanitization Steps">
<br />
<br />
>domain controller/Server Manager Dashboard/add roles and features/Roles^Remote access>routing>^/^ /install
<img src="https://i.imgur.com/MPZOQoP.png" height="80%" width="80%" alt="Disk Sanitization Steps">
<br />
<br />
Configure 
<img src="https://i.imgur.com/MPZOQoP.png" height="80%" width="80%" alt="Disk Sanitization Steps"> 
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
