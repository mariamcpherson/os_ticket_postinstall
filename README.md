# os_ticket_postinstall

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Create Roles
- Set Departments  
- Set Teams
- Set Agents
- Create End Users
- Configure SLA
- Set Help Topics

<h2>Configuration Steps</h2>

<p>
This tutorial picks up where we left off in the previous section where we created a Windows 10 Virtual Machine in Azure and followed all the prerequisit and installation steps for osTicket. We will be creating Roles, Departments, Teams, Agents, Users, SLAs and Help Topics in our osTicket system.
</p>

<p>
In order to access osTicket as an administrator, browse to the following URL: http://localhost/osTicket/scp/index.php
</p>
<p>
You will be prompted to enter a Username and Password. These are the values we entered during the initial osTicket Installation setup.
</p>
<br />

<p>
Once you've entered your credentials, you should see the index page. 
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/ee4267ee-3e5f-4634-99c4-3438dc06a90c"/>
</p>

<p>
At the top of the Dashboard you can toggle between Admin Panel and User Panel. In this case we'll be setting up the Ticket System as an Admin.
</p>
<br />

<p>
- Roles:
</p>

<p>
The first thing we'll create is a Role with access to all the features in the ticketing system, that is, a role that can basically do anything in the system. We'll name this role "Supreme Admin."
</p>

<p>
On the Agents tab → Roles → Add New Role.
</p>


<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/a2f845c9-21ea-4fb6-9478-2783aa6f5a05"/>
</p>


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
