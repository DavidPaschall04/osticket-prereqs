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

- Install / Enable IIS in Windows With CGI
- Install PHP manager, Rewrite Module, VC_reist
- Install MySQL and setup your username and password
- Register PHP within IIS
- Install OsTicket
  

<h2>Installation Steps</h2>

<p>
<img width="1164" height="656" alt="Screenshot 2025-08-01 121216" src="https://github.com/user-attachments/assets/c55bc009-84d4-4ac0-a4de-cfcb0331782e" />

</p>
<p>
To install and enable IIS, you have to Open your Control Panel, locate "World Wide Web Services" on the Control Panel, then navigate to Application/Windows Features, and check off the box labeled Internet Information Services.
</p>
<br />

<p>
<img width="758" height="592" alt="Screenshot 2025-08-05 140124" src="https://github.com/user-attachments/assets/f770ad1b-d045-4ccf-97b7-e8a1ab21aeef" />

</p>
<p>
Next, Install the PHP Manager and Rewrite Module from https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD . After installing both programs, create a Directory in your C drive called "PHP", then unzip the "PHP 7.3.8" file into the PHP directory. Once you unzip the file, go back into the OsTicket Installation Files and install VC_Redist.
</p>
<br />

<p>
<img width="1163" height="513" alt="Screenshot 2025-08-05 161916" src="https://github.com/user-attachments/assets/fb7096c3-f226-420b-b1aa-6a1baedb9894" />

</p>
<p>
When installing "MySQL", Make sure the setup type is "Typical" and the Configuration type is "Standard Configuration". Once you make it past those settings, set the username and password to "root" and you will be done configuring MySQL.
</p>
<br />

<p>
<img width="656" height="572" alt="Screenshot 2025-08-05 180120" src="https://github.com/user-attachments/assets/8fb6b6be-7d3b-4e1b-bffb-0593d3e1d9ae" />

<img width="607" height="612" alt="Screenshot 2025-08-05 180455" src="https://github.com/user-attachments/assets/53b2fd3d-c8dc-4421-84d5-75272e3e634b" />

</p>
<p>
Registering PHP with IIS: open Internet Information Services as admin on your computer and register PHP, Stop and Start the IIS server once PHP is Registered.
</p>
<br />

<p>
<img width="623" height="582" alt="Screenshot 2025-08-07 105038" src="https://github.com/user-attachments/assets/bc5fd6f4-bae0-4a77-92d8-62d9db0b139f" />



</p>
<p>
Install osTicket: From the "osTicket-installation-Files" folder, unzip "osTicket-v1.15.8.zip" and copy the upload folder into "c\inetpub\wwwroot" (files -> C drive -> inetpub -> wwwroot) Within "c:\inetpub\wwwroot", Rename "upload" to "osTicket". Once thats finished, Reload IIS the same way done in the previous step.
<p></p>
  <img width="805" height="637" alt="Screenshot 2025-08-07 105221" src="https://github.com/user-attachments/assets/6ffd01f3-8367-46b9-bf34-26e1cd407a23" />
   
   To open the osTicket browser site, locate "sites" in IIS, then click default -> osTicket and on the right side, click "Brows *.80". By default, some extentions for OsTicket will be disabled, to Enable these extentions, go back to IIS, navigate to sites -> Default -> osTicket. then double click the PHP Manager and click on "Enable or disable an extention" use the filter to locate and enable the following extentions:
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll

</p>
<br />

<p>
<img width="612" height="589" alt="Screenshot 2025-08-07 104412" src="https://github.com/user-attachments/assets/37c78f80-a152-4935-af5a-d79b49aac958" />


</p>
<p>
After all the extentions are enabled, refresh the osTicket site in your browser, and you can see the changes made. Next, in your folders, Find "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" and rename it to "C:\inetpub\wwwroot\osTicket\include\ost-config.php" (MAKE SURE IT IS TYPED CORRECTLY)
and assign ost-config.php permissions 
<p>
  <img width="1155" height="545" alt="Screenshot 2025-08-07 104802" src="https://github.com/user-attachments/assets/6667e88c-544e-4ad8-bd2f-1f82cfea0e28" />

  (Right click the file, go to properties -> security -> advanced -> Disable inheritance -> Remove all, Then select "Add", Select a principal -> set permissions to full control. Confirm everything by selecting "apply", and then "OK"
</p>
<br />

<p>
<img width="850" height="558" alt="Screenshot 2025-08-07 110908" src="https://github.com/user-attachments/assets/eb6fa7d6-eb04-4708-bc0e-a64ccc123b25" />


</p>
<p>
Installing osTicket, Final: In the osTicket browser site, Continue setting up by Naming the Help Desk and Adding an Email, Once finsihed, go back into the “osTicket-Installation-Files” folder and install HeidiSQL. Open Hidi SQL, Create a new session (press new, username root, password root, press open) Create a database called "osTicket" (right click "Unnamed" -> Create new -> Database -> name it "osTicket". Once youve completed setting up HeidiSQL, You can continue setting up osTicket in the browser, (MySQL Database -> osTicket, Username/password -> root, then click "Install Now!" 
</p>
<img width="761" height="351" alt="image" src="https://github.com/user-attachments/assets/f2b77817-8c16-4a4d-9e1a-76ab5582ac5f" />

</p>
After installing osTicket, you have finished the prereqs and installation manual.
<br />
