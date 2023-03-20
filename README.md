<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 Create File Shares
- Step 2 Set Permissions
- Step 3 Attempt to access file shares
- Step 4 Create Security Groups

<h2>Actions and Observations</h2>

<p>
Create File Share Folders
</p>
<img src="https://i.imgur.com/7i0gn52.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Created new folders named Read-Access, Write-Access, and No-Access.
</p>
<br />

<p>
Set Permissions
</p>
<img src="https://i.imgur.com/qMt79Jm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click the Sharing tab.
</p>
<br />

<p>
<img src="https://i.imgur.com/dUDcZCf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Choose users to give access to the folder (Jane Doe) and set their permission level (Read only).
</p>
<br />

<p>
<img src="https://i.imgur.com/lEs4W8E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Attempt to access File Shares.
</p>
<br />

<p>
<img src="https://i.imgur.com/J3lD1Lb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Clicked on No-Access folder to check permissions. Windows will not allow access to the folder. Permissions are working correctly here.
</p>
<br />

<p>
<img src="https://i.imgur.com/O8QNeHt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After clicking Read-Access folder and trying not create a folder (write) this notification popped up. Permissions set to only read and not write or create folders/documents. The permissions are working correctly.
</p>
<br />

<p>
<img src="https://i.imgur.com/uTsSgyu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Clicked on the Write-Access folder. Created a text file and named it test. The permissions are working correctly for this folder. This folder has read & write permissions.
</p>

<p>
Create a Security Group
</p>
<img src="https://i.imgur.com/ZwcMMrk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new organizational unit in the Active Directory Domain.
</p>
<br />

<p>
<img src="https://i.imgur.com/VUIOtuK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name it _SECURITY_GROUPS.
</p>

<p>
<img src="https://i.imgur.com/p8OCvXp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new group within _SECURITY_GROUPS.

<p>
<img src="https://i.imgur.com/R6mXFyk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name the group ACCOUNTANTS, set the group type to security.
</p>
