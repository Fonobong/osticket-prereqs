<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This is a demonstration which outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Utilized</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Utilized </h2>

- Windows 10</b> (21H2) 

<h2>List of Prerequisites for osTicket</h2>

- PHP Manager for IIS
- Rewrite Module
- C++ Redistributable
- MySQL
- Item 5

<h1>Ticketing System Installation Tutorial:</h1>

<h2>Step 1. Configure Virtual Machine</h2>

<p>
<img src="https://i.imgur.com/9Z6Dagb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the home screen of Microsoft Azure, click the Virtual Machine icon and create a new virtual machine. In the Basic tab, scroll down and fill out all fields appropriately. At the bottom of the page, mark the Licensing check box, as shown in the graphic above. Failing to do so will stop the generation of any machines. When you are done configuring your machine, press the blue "Review and Create" button. You'll be taken to the Review and Create tab where you'll press the "Create" button and generate your virtual machine.  
</p>
<br />

<h2>Step 2. Log Into the Virtual Machine</h2>

<p>
<img src="https://i.imgur.com/59wmtVT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to your virtual machine and copy its public ip address. Open the remote desktop application and input the appropriate fields, including the ip you copied. When it is done initializing, you should be logged into a virtual Windows operating system.
</p>
<br />

<h2>Step 3. Extract Folder Containing osTicket Installation Files</h2>

<p>
<img src="https://i.imgur.com/0QBr437.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within the virtual machine download the contents from https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and unzip them unto your desktop, name the folder appropriately.  
</p>
<br />

<h2>Step 4. Install & Enable IIS and CGI</h2>

<p>
<img src="https://i.imgur.com/qWF45WO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on the start menu, then click on the Control Panel. In the Control Panel, go to programs and click "unintall programs". On the left side, click "Turn Windows features on or off" then scroll down to "Internet Information Systems" and click the box. After clicking it, expand the same box and find "World Wide Web Services" then expand "Application Development Features" then expand and scroll down to CGI, click the box, then press ok. The IIS will act as a web server within the virtual machine for osTicket. 
</p>
<br />

<h2>Step 5. Install the Prerequisites for osTicket</h2>

<p>
<img src="https://i.imgur.com/MIaN8yF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install the PHP Manager for IIS and Rewrite Module from the osTicket installation files. Create a folder in the Windows C: drive called PHP where you will extract the PHP 7.3.8 files (not the PHP Manager) from the original installation files into for storage, like the image above. Next, install the C++ redistributable "VC_redist" as well as MySQL. Pick standard configuration for MySQL and make sure to write down or store your credentials so they can be remembered at a later time.    
</p>
<br />

<h2>Step 6. Register PHP within IIS</h2>

<p>
<img src="https://i.imgur.com/3jV6H6c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click start, and type IIS then right click the application to run "Internet Information Systems Manager" an administrator. When it loads, click PHP Manager, click "Register new PHP version" and browse to the PHP folder on the Windows C: drive, and click "php.cgi". Open it then press ok. Next, reload the webserver by clicking the green refresh symbol on the right side.    
</p>
<br />

<h2>Step 7. Install osTicket</h2>

<p>
<img src="https://i.imgur.com/b7mA6tm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open the osticket installation files and extract the contents from the osTicketv1.15.8 folder within. Inside of the osTicket folder, move the uploud folder to the wwwroot folder which can be found by traversing from the Windows C: drive > inethub > wwwroot. Rename the uploud folder to "osTicket".      
</p>
<br />

<h2>Step 8. Load the osTicket Site from the IIS</h2>

<p>
<img src="https://i.imgur.com/MLVR4uV.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Reopen the ISS and run it as an administrator like in Step 6. Click the green refresh button on the right side. Next, click the dropdown menu in the following order: osticket-vm > Site > Default Web Site > osticket. In osTicket, click the "Browse ":80 (http)" link on the right side which should open up the webpage for osTicket like the image displays.       
</p>
<br />

