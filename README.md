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

[osTicket Installation Files](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

Azure Virtual Machine with a minimum of 2 VCPUs and 16GBs of memory


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

3.) Enter the public IP address and click connect. The program will attempt to connect to the public IP, but will need your Username and Password. Select More choices and enter your info. When prompted to verify, select Yes. Once inside the VM, allow your PC to become discoverable on your network by selecting Yes on the popup that appears.

</p>
<br />

![Step 3](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/719db6f5-aaa6-49ba-a443-8174df7833e2)

![Step 4 Turn Features on](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/cc73bc90-e007-4c23-a869-68b56b1cf284)

 
4.) Now, open up control panel and select Programs, then  click Turn Windows Features on or off.

</p>
<br />

![Step 4 1](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/d054ad68-4049-412f-ad76-fd1495811268)

 
5.) From here, we will enable install/enable Internet Information Services. Follow these steps in order: select Internet Information Services-> World Wide Web Services  -> Application Development Features-> [X]CGI -> Common HTTP Features -> [X] All sub folders
 
</p>
<br />


![Step 5 127 0 0 1](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/7cb87c16-a464-4d19-82a6-505f43a6d7ed)

6.) To test that Internet Information Services was configured correctly, open up your preferred browser and search 127.0.0.1 in the address bar. If the installation was a success, the IIS webpage should appear.


![Step 6 IIS](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/0348eafd-21b3-409f-9463-b10bb994041a)

7.) From the [link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) provided, install PHPManagerForIIS_V1.5.0.msi and continue through the installation wizard. Next, download rewrite_amd64_en-US.msi. Once again, continue to the installation wizard and accept the terms when prompted.

![Step 7](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/5360a3cf-9f26-45c9-9e4c-21304cf39650)
![Step 7 1](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/ccc78fa2-8e9c-4449-b5ab-eadcebf53c5e)



8.) Open up File Explorer and create a new folder in the C: drive named "PHP", and download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip). Locate the PHP 7.3.8 file and right click to find the Extract All option- select it and click Browse. You will unzip the PHP file into the new PHP folder, and it will slowly move the contents over. 
</p>
<br />

9.)Back in the Installation Files Google Drive, download VC_redist.x86.exe and mysql-5.5.62-win32.msi. Launch the mySQL installation and run the installer. Click these in order: Typical Setup-> Launch Configuration Wizard after Install-> Standard Configuration-> Install as Windows Service-> Click Next. Create a password, then click Next. Select Execute and wait for the settings to process; when this is complete, click Finish.

![Step 8](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/4ad7aaa0-01d9-4961-8731-ba34788fbac4)

10.) In the taskbar search box, search for Internet Information Services Manager and right click to run as an administrator. Navigate to the PHP Manager icon and double click it. Under PHP Setup, click on Register new PHP version. Click the 3 dots and search for the PHP folder within the C drive; inside the folder select the php-cgi file.

 ![Step 10](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/eab53538-eeff-4536-96c9-8fc44dcdeee2)
 
![Step 11](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/a315c917-1781-425a-aaf4-339b1cc5c03c)

11.) Put these changes in effect by restarting the server.

![Step 12](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/cdabc83a-db41-455a-af7a-dacd09cf759f)


12.) Download the osTicket zip file from the Installation Files folder and open up another File Explorer window. In this new window, click on This PC and head to the C: drive; open it and locate the inetpub folder. Within inetpub, open the wwwroot folder and copy the "upload" folder by dragging it from the osTicket file explorer window to the inetpub window. When the files are completely copied over, rename the upload folder to osTicket then restart IIS again. 

![Step 13](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/917ba40a-98ea-4ffe-849c-3f90b9e718a7)

13.) In IIS, click on the name of your VM on the left hand side, then Sites-> Default Web Site-> osTicket. Now click on Browse *:80(http).

![Step 14](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/f48bb03e-5667-4a62-a59b-73f409f1a973)




14.) The osTicket Installer homepage will be shown, meaning that our installation is almost complete! However, we can observe that a few important extensions have not been enabled. We will enable these in IIS by opening PHP Manager again and selecting "enable or disable an extension". 


![Step 15](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/03bb6c30-630c-479f-89e5-e960ef84088b)


15.) The 3 extensions we will enable are php_imap.dll, php_intl.dll, and php_opcache.dll. Select each one and right click to see the enable option. Refreshing the osTicket page should show that our changes have gone into effect, though the opcache extension will still show as offline.

![Step 16](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/168a8ea2-e578-45fe-9e43-ada72b17eaa3)

![Step 17](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/cc841609-1073-4086-a17a-f2ffb35912a4)

 
16.) In file explorer, go back to the osTicket subfolder by following this path: Windows(C:)-> inetpub-> wwwroot->osTicket. Select the "include" folder and find the file named "ost-sampleconfig.php";rename this file to "ost-config.php". Right click the re-named file and select properties, then security, then "Advanced". We will now disable inheritances by selecting "remove all inherited permissions from this object". We're going to replace the old permissions with new ones by clicking "Add" then "Select a principal" and when the text box appearss, type "Everyone". Give Everyone complete permissions now by selecting Full Control. Apply the changes by clicking Apply then OK, then OK again; the window will close when the settings are applied.  

17.) Return to the osTicket homepage on your browser and proceed with the setup process by clicking continue on the bottom of the page and filling out the settings. For now don't worry about the Database Settings as we have not connected one yet.


![Step 18](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/e67f9b59-d602-4c96-a7dd-1e40d6098f2d)

![Step 19](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/1d33dd1a-2157-4b3a-a2fc-9afefdda35c1)

![Step 20](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/ab123d9b-05d4-4bfc-9c23-852a074f83eb)



18.) We are now going to download HeidiSQL from the Installation Files and create a database connection. When HeidiSQL downloads, select the installation file and click "Next" until you reach the Install prompt and select it. The Session Manager will launch now and we will select the green Create New Session button on the bottom left. Create a new User and Password; for the sake of simplicity, root for the Username and Password1 as the password should be fine. Click Open and now click on the filter on the left side that says "Unnamed". Right click to see the options list and select "create new" then "database". Name the database "osTicket" then click Ok. Back in the osTicket signup page, fill out the database details with the newly created database name, username, and password. You can now click Install.

![Step 21](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/6685387c-2e21-4925-b23a-bd2086c9191a)

![Step 22](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/a56e86d7-8fac-47e7-8f20-f232b236f0ab)

![Step 23](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/af89025a-0ec9-4a68-909c-eb3c34023b8d)

19.) Before we test out our finished project, we have to clean it up by going back to the C:inetpub\wwwroot\osTicket path and deleting the "setup" folder inside. We must also change the permissions of the ost-config.php file; to find it again, follow this path C:\inetpub\wwwroot\osTicket\include\ ost-config.php. Right click, select properties, then security, then Advanced, then select the name Everyone. Select Edit, and remove all permissions except for Read. Click Apply then OK.

![Step 24](https://github.com/CGLuissi/osTicket-prereqs/assets/143234913/938ee49c-c24f-4d5b-aa8b-c8ca0dd6632d)


20.) The setup is now complete and you will be able to head to the Agent login page and see the results of your hard work. 

EXTRA: If you'd like to continue on and create Users and Tickets you can do so, but if you want finish up here, go back to the Azure portal and delete your Resource Group. If not deleted, you will be charged at a fixed rate hourly as long as the resource group and VM are active.











































