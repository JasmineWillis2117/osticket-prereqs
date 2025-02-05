<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine (Windows 10, 4vCPUs, 16 GiB memory)
- Remote Desktop
- Install/Enable IIS
- PHP Manager
- Rewrite Module
- VC Redist (in download folder
- MySQL
- Heidi SQL
- osTicket V1.15.8
- Links to download: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 (Installation Files)</p>
</p>
</p>
</p>
</p>
<br />
<br />


<h2>Installation Steps</h2>


<br />
<p>
1. Navigate to https://portal.azure.com and create a Resource group for your project (this will be where your project files are housed). 
</p>
<br />

<p>
<img src="https://i.imgur.com/jQJf0HL.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
2. Create the Virtual machine (Windows 10 Pro, version 22H2, allow it to create a Virtual Network (Vnet)). </p> Use the already created Resource Group, input a User name and Password (this will be used to log into your Virtual Machine). Pick the size needed for your project. <span style="color:black"><b> Note: For this project we will be using the "Standard_D4s_v3 - 4 vcpus, 16 GiB memory" (as this size vcpu will be able to navigate the resources needed to run osTicket successfully).</b></span>
</p>
<br />

<p>
<img src="https://i.imgur.com/sakkjWI.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
3. Connect via Remote Desktop using your Azure VM IP Address to connect to a Virtual Machine.</p> Install/Enable IIS is Windows with CGI, Common HTTP features and IIS Management Console.</p> Download file PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) in folder listed above.
</p>
<br />

<p>
<img src="https://i.imgur.com/cIsM6d5.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/PtFOlBO.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
<span style="color:black"><b> Note: To make sure the IIS is installed/enabled go to a browser and search for 127.0.0.1, it should look like this. </b></span>
</p>
<br /> 
<p>
<img src="https://i.imgur.com/xYVdPEi.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
4. Download and install the Rewrite Module (rewrite_amd64_en-US.msi) in folder listed above.</p> Create the directory C:\PHP (folder in C: drive)
</p>
<br />

<p>
<img src="https://i.imgur.com/XxXi8Bz.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/aeS5vEM.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
5. Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip).</p>Extract all (right click to complete this step), browse to folder C:\PHP (select this folder) and unzip/extract the contents into folder you created.</p> Below are the files being extracted from Downloads to C:\PHP and what is will look like once completed.
</p>
<br />


<p>
<img src="https://i.imgur.com/5fUqvsC.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
6. Download and install VC_redist.x86.exe and then download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) (From folder listed above)
<p>
Example of setup:
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Create and setup password
</p>
<br />

<p>
<img src="https://i.imgur.com/jU12Mtw.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
<img src="https://i.imgur.com/sMyrQMk.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/UalS5nJ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
7. Open IIS as an Admin, Register PHP from within IIS, Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img src="https://i.imgur.com/xF5DZXR.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<p>
<img src="https://i.imgur.com/kxqmtks.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/gV6hZKB.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
8. Install osTicket v1.15.8
  
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

</p>
<br />

<p>
<img src="https://i.imgur.com/N3YRtGQ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
<img src="https://i.imgur.com/8sCWHIu.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
9. Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”</p>

<span style="color:black"><b> Note: that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes</b></span>

</p>
<br />

<p>
</p> <img src="https://i.imgur.com/vI0g0Rr.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/29YQRXG.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> </p> <img src="https://i.imgur.com/47xuzM4.png" height="30%" width="30%" alt="Disk Sanitization Steps"/></p>  <img src="https://i.imgur.com/MxMukfU.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
10. Rename: ost-config.php</p>
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php</p>
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>Before
</p> <img src="https://i.imgur.com/qRZIeJ0.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p>

</p>After
<img src="https://i.imgur.com/u9rwhJp.png" height="20%" width="20%" alt="Disk Sanitization Steps"/></p>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
11. Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All</p>

Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

</p>
<br />

<p>
<img src="https://i.imgur.com/Yslaojy.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p>  <img src="https://i.imgur.com/tgVcG5S.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/70KcwXx.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
12. Download and install HeidiSQL. </p>
Open Heidi SQL</p>
Create a new session, root/Password1</p>
Connect to the session</p>
Create a database called “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/OtQlA7G.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/yXzCHLY.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/rEv0uIY.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
13. Continue Setting up osticket in the browser</p>
Congratulations, hopefully it is installed with no errors!</p>

Browse to your help desk login page: http://localhost/osTicket/scp/login.php</p>

End Users osTicket URL: http://localhost/osTicket/

</p>
<br />

<p>
<img src="https://i.imgur.com/3ynkdkB.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/KAY8XmN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/hO7VA17.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/ogr8bxM.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
14. Clean up </p>
Delete: C:\inetpub\wwwroot\osTicket\setup</p>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://i.imgur.com/Hm0TEo6.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p><img src="https://i.imgur.com/JMjJXcs.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> <img src="https://i.imgur.com/yzeWzeY.png" height="40%" width="40%" alt="Disk Sanitization Steps"/></p> 
</p>
</p>
</p>
<br />
<br />
<br />
<br />

