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
Now, let's assign permissions to this new role we have created. And, remember, we want this Admin to be able to have "full control" of the Ticketing System. 
</p>
<p>
On the Permission tabs, under Tickets, check all options.
</p>
  
<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/70bff473-ae92-45b8-815e-9954f8c5c018"/>
</p>


<p>
Under the Tasks and Knowledgebase tabs, check all options as well.
</p>


<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/65fbb1c7-8263-43bd-8b1c-fd973d60d0fe"/>
</p>



<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/f866a0e0-7fa5-4119-9c7f-f0d37828e4b0"/>
</p>
<br />


<p>
- Departments:
</p>

<p>
Let's create a New Department named "System Administrators." Agents tab → Departments → Add New Department
</p>


<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/4dc6e080-5f50-4397-986c-b4b38920dbb1"/>
</p>
<br />

<p>
- Teams:
</p>

<p>
Now, let's create a team. This would allow us to assign different agents to that particular team with different accesses and permissions to different features, and to assign tickets to a whole team. 
</p>
<p>
In this tutorial, I created a team named "Level II Support." Agents tab → Teams → Add New Team
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/ee9996f7-83a4-4801-b16e-95aec8550795"/>
</p>
<br />


<p>
*Before we proceed to create Agents, we need to determine who can create new tickets in our system, for the sake of this tutorial, we'll allow anyone to create tickets with registration required.
</p>

<p>
Settings → Users → Authentication → Settings
</p>
<p>
We will check "Require registration and login to create tickets", and select "Public Access"
</p>


<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/295351ba-e7e2-43ad-b86e-f35b8c26daf3"/>
</p>
<br />


<p>
- Agents:
</p>

<p>
Next, we will be creating Agents that will work under a specific Department/Team. I used made up names and random values as with the rest of the tutorial. 
</p>

<p>
Agents → Add New Agents
</p>


<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/19047a95-7610-4380-8241-fbe876091533"/>
</p>

<p>
Click on "Set Password" in order to assign credentials to the agent. 
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/72ab65e5-e1d1-4eef-a76a-67f5c6a5b350"/>
</p>


<p>
On the Access tab, you can assign the Primary Department each Agent will be under, and the type of access.
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/d2fbace9-8311-48c5-a5bf-1721d28f494e"/>
</p>
<br />


<p>
- Configure Service Level Agreement (SLA):
</p>

<p>
In this section, different types of SLAs can be configured, according to the severity of the issue for which the ticket was created, and the target time in which the Help Desk Administrator expects them to be resolved.
</p>

<p>
Manage → SLA → Add New SLA 
</p>

<p>
In this tutorial, we will create 3 different types of SLAs for three different levels of severity:
</p>
<p>
Severity A SLA. This would correspond to tickets created for urgent or severe issues that would significantly impact the end user's business. For this reason the schedule to resolve tickets within this SLA would be 24/7, and the grace period would be only 1 hour. 
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/6ea79e36-0f9a-4345-9ab2-1f6b4936c8bd"/>
</p>


<p>
Severity B SLA. This would correspond to tickets created for less urgent tickets and the Administrator expects to be worked on around the clock, but with a longer grace period of 4 hours.
</p>

<p>
<img src="https://github.com/mariamcpherson/os_ticket_postinstall/assets/139581822/6ec2165d-13e2-4da9-8b5f-c04308356154"/>
</p>

<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>





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
