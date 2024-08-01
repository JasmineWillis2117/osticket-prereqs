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
- Links to download: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 (Installation Files)
  

<h2>Installation Steps</h2>


- VC Redist
- MySQL
- Heidi SQL
- osTicket V1.15.8


<br />
<p>
1. Navigate to https://portal.azure.com, from there create a Resource group for your project (this will be where your project files are housed). 
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
2. Create the Virtual machine (Windows 10 Pro, version 22H2, allow it to create a Virtual Network (Vnet)). Use the already created Resource Group, input a User name and Password (this will be used to log into your Virtual Machine). Pick the size needed for your project. <span style="color:black"><b> Note: For this project we will be using the "Standard_D4s_v3 - 4 vcpus, 16 GiB memory" (as this size vcpu will be able to navigate the resources needed to run osTicket successfully).</b></span>
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
3. Connect via Remote Desktop using your Azure VM IP Address to connect to a Virtual Machine. Install/Enable IIS is Windows with CGI, Common HTTP features and IIS Management Console. Download file PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) in folder listed above.
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
4. Download and install the Rewrite Module (rewrite_amd64_en-US.msi) in folder listed above and create the directory C:\PHP (folder in C: drive)
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
5. Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip), Extract all (right click to complete this step), browse to folder C:\PHP (select this folder) and unzip/extract the contents into folder you created. Below are the files being extracted from Downloads to C:\PHP and what is will look like once completed.
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
6. (From folder listed above) Download and install VC_redist.x86.exe and then download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Example of setup:
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Setup password
</p>
<br />

<p>
<img src="https://i.imgur.com/jU12Mtw.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
</p>
<img src="https://i.imgur.com/sMyrQMk.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
</p>
<br />
<br />
<br />
<br />
