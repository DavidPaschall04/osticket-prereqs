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
