#Network-File-Shares-and-Permissions
<p align="center">
<img src="https://i.imgur.com/AeiqMDZ.png" alt="Traffic Examination"/>
</p>

<h1>Network File Shares and Permission Configuration</h1>

This lab walks through the process of sharing resources across a network by creating directories and setting specific permissions to grant or restrict read/write access for users and groups. <br />

<h2>Tools and Environment Used</h2>

- Microsoft Azure (VMs including Domain Controller and Client)
- Remote Desktop Protocol (RDP)
- Shared File Resources over Network

<h2>Operating System</h2>

- Windows 10</b> (version 21H2)

<h2>Requirements</h2>

- A Virtual Machine functioning as a Domain Controller with Active Directory Domain Services (AD DS) installed
- A separate Virtual Machine acting as a Client system

<h2>Step-by-Step Instructions</h2>

<p>
<img src="https://i.imgur.com/IX7eI1M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Start by logging into the DC-1 machine using the domain administrator credentials (mydomain.com\ken_admin). On the Client-1 machine, log in using a standard user account (mydomain\<someuser>). On DC-1’s C:\ drive, create four new directories named: read-access, write-access, no-access, and accounting.
</p>
<br />

<p>
<img src="https://i.imgur.com/YpWvuuh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, on DC-1, adjust sharing and permission settings for each folder:
- For the "read-access" folder, provide Read access to the Domain Users group.
- For "write-access", grant Read/Write permissions to Domain Users.
- For "no-access", only Domain Admins should have Read/Write rights.
- Skip permissions for the "accounting" folder at this point.
</p>
<br />

<p>
<img src="https://i.imgur.com/mJLXlBj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Uuy43Na.pngg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, on the Client-1 VM, access File Explorer and enter \\dc-1 in the address bar to browse available shares. Try accessing each folder:
- You’ll be able to open "read-access" and view files, but not make changes.
- "write-access" will allow full modification privileges.
- Access to "no-access" will be blocked for non-admin users.
</p>
<br />

<p>
<img src="https://i.imgur.com/xsdCaQp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On DC-1, open Active Directory Users and Computers (ADUC) and create a new Organizational Unit named _GROUPS. Inside this OU, set up a security group called ACCOUNTANTS.
</p>
<br />

<p>
<img src="https://i.imgur.com/cZo9Poi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Still in ADUC, add domain users to the ACCOUNTANTS group by right-clicking it, selecting Properties, switching to the Members tab, and choosing the users to include. Then return to the "accounting" folder and assign the ACCOUNTANTS group Read/Write access.
</p>
<br />

<p>
<img src="https://i.imgur.com/HzkNmDO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Restart the Client-1 virtual machine and log in with a user who is part of the ACCOUNTANTS group. Open File Explorer, type \\dc-1, and attempt to access the accounting folder. Access should now be granted thanks to the new group permissions.
</p>
<br />
