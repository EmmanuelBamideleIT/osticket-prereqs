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

- Windows OS
- Internet Information Services
- MySQL Database
- PHP
- PHP Manager for IIS 
- Rewrite Module
- Visual C++ Redistributable package
- HeidiSQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/1BQfNdO.png" height="80%" width="80%" "/>
</p>
<p>
Enabling IIS with CGI and Common HTTP Features, and installing IIS Management Console

Install IIS with CGI and Common HTTP Features: Enable CGI and Common HTTP Features in the World Wide Web Services -> Application Development Features section during the installation process.

Install IIS Management Console: Enable the IIS Management Console in the Internet Information Services -> Web Management Tools section during the installation process.
</p>
<br />

<p>
<img src="https://imgur.com/DRcGJ2k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install PHP Manager for IIS: Install the PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the installation files.

Download and install the Rewrite Module: Install the Rewrite Module (rewrite_amd64_en-US.msi) from the installation files.

Create the directory C:\PHP: Create a directory named "C:\PHP" on your system.

Download and unzip PHP 7.3.8: Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the installation files. Unzip the contents of the file into the "C:\PHP" directory.

Install VC_redist.x86.exe: Download and install VC_redist.x86.exe from the installation files.</p>
<br />

<p>
<img src="https://imgur.com/6nZK5JM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install MySQL 5.5.62: Install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the installation files. Choose the typical setup option, launch the configuration wizard, select the standard configuration, and set the password as "Password1".

Configure osTicket in IIS: Open IIS as an administrator. Register PHP from within IIS. Stop and start the IIS server.

Install osTicket: Download osTicket from the installation files folder. Extract the contents of the "upload" folder to "c:\inetpub\wwwroot" and rename it to "osTicket". Reload IIS.

Enable PHP extensions: Open IIS, go to sites -> Default -> osTicket, and double-click PHP Manager. Enable the following extensions: php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osTicket site in your browser to observe the changes.

Configure ost-config.php: Rename "ost-sampleconfig.php" to "ost-config.php" in the "C:\inetpub\wwwroot\osTicket\include" directory.

Set permissions for ost-config.php: Disable inheritance for "ost-config.php" and assign new permissions to the file, granting access to Everyone with full control.

Complete osTicket setup: Continue setting up osTicket in the browser, providing the required information such as helpdesk name and default email address for receiving customer emails.

Install HeidiSQL: Download and install HeidiSQL from the installation files. Open HeidiSQL and create a new session using the root user and "Password1" as the password. Connect to the session and create a database called "osTicket".

Continue osTicket setup: Provide the MySQL database name, username (root), and password (Password1) during the osTicket setup process. Click "Install Now!"

Congratulations! Verify the installation by browsing to the help desk login page (http://localhost/osTicket/scp/login.php). The end users' osTicket URL is http://localhost/osTicket/.

Clean-up: Delete the "C:\inetpub\wwwroot\osTicket\setup" folder and set the permissions of "C:\inetpub\wwwroot\osTicket\include\ost-config.php" to "Read-only".</p>
<br />
