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

- Create a Resource Group
- Create an Azure Virtual Machine operating on Windows with 2-4 Virtual CPU's
- Have Remote Desktop
- Install/Enable IIS in created virtual machine
- Have all files that will be needed to help us run OSticket

<h2>Installation Steps</h2>

![20240318_230117 (1)](https://github.com/tylermartin12368/osticket-prereqs/assets/161632103/981c9ace-8b10-4039-a90e-6a192eda83af)
</p>
<p>
In our created Azure Virtual Machine we will need to Install/Enable IIS. This can be done by opening up Control Panel and going to Programs. Once in we can go to Turn Windows feature on and off and locate Internet Information Services (IIS) and check the box to turn it on. Other things within Internet Information Services will need to be checked including all boxes in the Common HTTP Features and in Application Development Features the CGI will need to also be turned on. When done it will start installing IIS. We can check to make sure this worked by going to a web browser and type 127.0.0.1 and when searched it will pop up Internet Information Services.  
</p>
<br />

![20240318_234637](https://github.com/tylermartin12368/osticket-prereqs/assets/161632103/07553459-b933-41d6-be30-c097af495c9a)
</p>
<p>
In order to get OSticket to function, we will need to install a bunch of different files like PHP Manager for IIS and Rewrite Module. All these files play a role in making OSticket run correctly. Once we have all the files needed, then we can open up IIS as an Admin and register PHP in IIS. This will then finally allow us to start downloading OSticket and once installed we can restart IIS and it should appear. In IIS go to Sites, Default Web Site, then OSticket folder. On the right of IIS in the Manage Folder area their should be a Browse 80 that can be clicked on and that will open up OSticket Installer on your web browser. Before we begin setting up the rest of OSticket through the broweser, a few extensions within IIS will need to be enabled, so certain features will be able to run in OSticket. The extensions that need to be enabled are located in PHP Extensions and they are called php_imap.dll, php_intl.dll, and php_opcache.dll. Go back to the browser with OSticket and refresh the site and that will enable the features that we want enabled. All that will be left is to go to File Explorer and Rename ost-sampleconfig.php to ost-config.php and let everyone have access to that file.  
</p>
<br />

![20240318_235648](https://github.com/tylermartin12368/osticket-prereqs/assets/161632103/8f9a88c8-1830-4092-b499-86d92c9e54cb)
</p>
<p>
OSticket can now be finished setting up through the web browser. A name will need to be created for the Helpdesk, a default email that will receive all emails from customers, and an Admin User that we can use to create Agents and Users. After getting through those sections, then you will get to the Database Settings. This is where HeidiSQL will need to be installed. IT will allow us to connect to the SQL Server and set up a database in HeidiSQL that OSticket will use. Once all the information has been put in, then we can click on "Install Now" which will finish up the installation of OSticket.   
</p>
<br />
