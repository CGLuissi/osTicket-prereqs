<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

osTicket Installation Files

Azure Virtual Machine with a minimum of 2 VCPUs and 16GBs of memory

Heidi SQL

<h2>Installation Steps</h2>


1.) To begin our project, head to the Microsoft Azure portal and create a new virtual machine. Create a new Resource Group, and name both the resource group and virtual machine anything you'd like. For the VM, use these settings- Image: Windows 10 Pro version 22H2, Size: 2-4 VCPUs with 16GiB memory. Create a username and password, and remember these for the next step. Confirm you have an eligible Windows 10/11 license and continue by clicking review/create.  
</p>
<br />

![Step 1- Public IP](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/04bb75e9-1773-4a63-871a-90e3f25f4e51)

2.) Once our resources have been created, click on our VM and take note of the public IP address. We will be connecting to our VM through Remote Desktop Connection and will need the public IP as well as the Username and Password from the previous step.  
 </p>
<br />

![Step 2- RDP](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/d27ff12c-ce33-4ac8-8f5e-16e716bd5725)

![STEP 2 RDP alt](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/10826ddb-dc02-4e58-b666-4f0e9bfea6d5)

3.) Enter the public IP address and click connect. The program will attempt to connect to the public IP, but will need your Username and Password. Select More choices and enter your info. When prompted to verify, select Yes. 

</p>
<br />

![Step 3](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/719db6f5-aaa6-49ba-a443-8174df7833e2)

![Step 4 Turn Features on](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/cc73bc90-e007-4c23-a869-68b56b1cf284)

 
4.) Inside the VM, allow your PC to become discoverable on your network by selecting Yes on the popup that appears. Now, open up control panel and select Programs, then  click Turn Windows Features on or off.

</p>
<br />

![Step 4 1](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/d054ad68-4049-412f-ad76-fd1495811268)

 
5.) From here, we will enable install/enable Internet Information Services. Follow these steps in order: select Internet Information Services-> World Wide Web Services  -> Application Development Features-> [X]CGI -> Common HTTP Features -> [X] All sub folders
 
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
