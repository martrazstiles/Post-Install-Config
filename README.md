<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Installation Setup</h1>
This guide covers the steps to configure osTicket after installation, setting it up for efficient help desk management.<br />

<h2>Tools and Platforms Used</h2>

- Microsoft Azure (Virtual Machines/Compute Services)
- Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)

<h2>Operating System Utilized</h2>

- Windows 10</b> (version 21H2)

<h2>Setup Process</h2>

<p>
<img src="https://i.imgur.com/sx170cG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Awesome! With osTicket installed successfully, it's time to carry out administrative configuration tasks. We'll begin by setting up user roles to help manage permissions and access across the platform.
</p>
<br />

<p>
<img src="https://i.imgur.com/DAhGSan.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To define roles in osTicket, head to the Admin Panel, navigate to Agents, then choose Roles. Click "Add new role" and input a name like "Supreme Admin". This role will include full system access, so make sure to enable every available permission before saving.
</p>
<br />

<p>
<img src="https://i.imgur.com/KzFVjJQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, select "Departments" under the Agents section. You’ll use this area to assign agents to specific departments. Create one called "System Administrators" to house all Supreme Admin-level users. Additional features like SLA policies, department managers, and email settings can be configured here to fine-tune your support workflow.
</p>
<br />

<p>
<img src="https://i.imgur.com/ob4MEma.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To manage agent collaboration, go to Admin Panel -> Agents -> Teams. Teams allow multiple agents from various departments to work together. Set up a team titled "Level II Support" and assign the relevant agents accordingly.
</p>
<br />

<p>
<img src="https://i.imgur.com/TcRrhwN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To make ticket submission open to all, navigate to Admin Panel -> Settings -> User Settings. Disable the "Require registration and login to create tickets" option so users can submit tickets without needing an account.
</p>
<br />

<p>
<img src="https://i.imgur.com/dwAhP3I.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To add new agents (staff), go to Admin Panel -> Agents -> Add New. Complete the necessary information such as name, email address, assigned role, and department to create their profile and assign permissions.
</p>
<br />

<p>
<img src="https://i.imgur.com/aYLnu3z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To register users (clients), go to the Agent Panel -> Users -> Add New. Add individuals like Ryu and Ken by entering their names and email addresses. This enables them to submit and track their support tickets.
</p>
<br />

<p>
<img src="https://i.imgur.com/YXWfwh8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For ticket categorization, navigate to Admin Panel -> Manage -> Help Topics. Help topics assist users in selecting the right category when creating tickets, streamlining the ticket routing process.

</p>
<br />
