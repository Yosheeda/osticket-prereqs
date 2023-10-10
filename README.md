# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Virtual Machine in Azure
- Install Web Platform Installer
- Install osTicket v1.15.8
- Install HeidiSQL



<h2>PreRequisite Steps</h2>
<p>
  <h2>Part 1 (Create Virtual Machine in Azure)</h2>
  <h3 align="center">CREATE A RESOURCE GROUP</h3>
  </p>
  
  
<img src="https://i.imgur.com/RsDyeSr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here we're in the initial window for Resource Groups where we proceed by clicking the "+ Create" button near the top left. 
</p>
<br />

<p>
<img src="https://imgur.com/DuFSVmE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once inside, I adjust the Resource Group settings as I see fit for this project. I then click the "Review = create" button at the bottom to get to the last step and create the Resource Group.
</p>
<br />

<p>
<img src="https://imgur.com/dSyvK12.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Once we see "Validation Passed" up top then we are set to "Create" our Resource Group.
</p>
<br />


 <h3 align="center">CREATE WINDOWS VIRTUAL MACHINE</h3>
  </p>
<img src="https://imgur.com/GIphPNL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once inside the Virtual Machines tab, we click the "+ Create" button and then click the "Azure virtual machine" that pops up under said menu.  
</p>
<br />

<p>
<img src="https://imgur.com/ZmDO4wP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/0L0mir6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Here in the "Basics" tab we are simply setting up base settings for our VM such as the type of Image we want, Region, security, size, and the administrator account so we can access the VM. We now click the "Review + create" button at the bottom to finish up creating our VM.
</p>
<br />

<p>
<img src="https://imgur.com/L7ywLmC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we see "Validation passed", we click "create" and will officially have our Windows VM.
</p>
<br />



<h2>Installation Steps</h2>
<p>
<img src="https://i.imgur.com/LDuI7xG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Plug in to your Virtual Machine via Remote Desktop
</p>
<br />

<p>
<img src="https://i.imgur.com/Lep0NOA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install / Enable IIS in Windows
</p>
<br />

<p>
<img src="https://i.imgur.com/PlErCcd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and Install PHP Manager for IIS
</p>
<br />

<p>
<img src="https://i.imgur.com/9QHHRml.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install the rewite module.
</p>
<br />

<p>
<img src="https://i.imgur.com/paM884d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download C++ redistributable
</p>
<br />


<p>
<img src="https://i.imgur.com/03MgAfC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download MySQL Server 5.5
</p>
<br />

 <h3 align="center">INSTALL osTicket v.1.15.8</h3>

<p>
<img src="https://i.imgur.com/XiFPqQ0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/n4SwVnh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
 Once we have donwloaded osTicket from the lab installation files we extract and copy "osTicket" folder to c:\inetpub\wwwroot 
</p>
<br />


<h3 align="center">Opening osTicket for the first time
</h3>

<p>
<img src="https://i.imgur.com/k8q5urI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to sites -> Default -> osTicket
</p>
<br />


<p>

</p>
<p>
On the right, click “Browse *:80”.
</p>
<br />


<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled
</h3>
<p>
<img src="https://i.imgur.com/wE7Jy3O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GPfxlGz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/CoV1L4s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>     
</p>
<p>
Go back to IIS, sites -> Default -> osTicket

  Double-click PHP Manager

</p>
<br />


<p>
<img src="https://i.imgur.com/kn7Siv7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click “Enable or disable an extension”
  
Enable: php_imap.dll
  
Enable: php_intl.dll

Enable: php_opcache.dll

</p>
<br />

<h3 align="center">Refresh the osTicket site in your browser, observe the changes
</h3>
<p>
<img src="https://i.imgur.com/cON6bBE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<h3 align="center">Rename########
</h3>
<p>
<img src="https://i.imgur.com/fiIdl2c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<h3 align="center">Assign Permissions: ost-config.php
</h3>
</p>
<br />

<p>
<img src="https://i.imgur.com/ZEXIQXZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Disable inheritance -> Remove All:
</p>
<br />

<p>
<img src="https://i.imgur.com/IFzgnxr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Au864kD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
New Permissions -> Everyone -> All
</p>
<br />

<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
</p>
<p>
	<img src="https://i.imgur.com/rvMvlNC.png" height="75%" width="100%" alt="continue osTicket setup"/>
	


<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/AEg0b2P.png" height="75%" width="100%" alt="download HeidiSQL"/>
</p>
<p>
:
</p>
<p>
	<img src="https://i.imgur.com/9t51ApR.png" height="75%" width="100%" alt="create sessions"/>
</p>
Create a new session, root/Password1.

Connect to the session:

<p>

</p>
<p>
	<img src="https://i.imgur.com/vXzmQqg.png" height="75%" width="100%" alt="create database"/>
</p>
Create a database called “osTicket”:
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />

</p>
<p>
	<img src="https://i.imgur.com/akDyber.png" height="75%" width="100%" alt="setting up osTicket cont'd"/>
</p>
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>

<p>
	<img src="https://i.imgur.com/J5omRoE.png" height="75%" width="100%" alt="installation complete"/>
</p>
<p>Click “Install Now!”</p>
<p>Bazinga! We have installed osTicket</hp>
<p>
<br />
<br />
<h3 align="center">Clean up</h3>
<br />
<p>
	
</p>
<p>
	<img src="https://i.imgur.com/eg0ZPG3.png" height="75%" width="100%" alt="clean up"/>
</p>
Delete: C:\inetpub\wwwroot\osTicket\setup:
<p>

</p>
<p>
	<img src="https://i.imgur.com/n6k46XL.png" height="75%" width="100%" alt="permissions"/>
</p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/n4qSgi3.png" height="75%" width="100%" alt="admin panel"/>
</p>
<br />
<br />
<p>
	That wraps up this tutorial for installing osTicket. 
</p>
<p>
	Now you can practice running your own help desk.
</p>
