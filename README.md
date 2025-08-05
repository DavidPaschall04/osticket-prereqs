<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When installing "MySQL", Make sure the setup type is "Typical" and the Configuration type is "Standard Configuration". Once you make it past those settings, set the username and password to "root" and you will be done configuring MySQL.
</p>
<br />
