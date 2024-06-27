<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
<img src="images/osTicketBanner.PNG" alt="dndUploadFolder" width="50%" height="50%">
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

- Virtual Machine of Windows 10
- Microsoft Remote Desktop
- IIS (Internet Information Service)


<h2>Installation Steps</h2>
<h4>Step 1 -  Download osTicket from the Installation Files Folder</h4>

<h4>Step 2 - Extract and copy “upload” folder to c:\inetpub\wwwroot</h4>
<p>
<img src="images/pic8 - dndUploadFolder.PNG" alt="dndUploadFolder" width="50%" height="50%">
</p>
<h4>Step 3 - Within c:\inetpub\wwwroot, Rename “upload” to “osTicket” ---> 8</h4>
<p>

</p>
<br />
<p>

<h4>Reload IIS (Open IIS, Stop and Start the server) --->?</h4>
<br />

<h2>Go to sites -> Default -> osTicket --->9</h2>
On the right, click “Browse *:80”
<p>
<img src="images/pic9 - browse80.PNG" alt="browse80" width="50%" height="50%">
</p>
<br />


<h2>Enable extensions</h2>
<h4>Go back to IIS, sites -> Default -> osTicket --->4</h4>
<h4>Double-click PHP Manager ---></h4>
<p>
<img src="images/pic4 - openISS.PNG" alt="openISS" width="50%" height="50%">
</p>

<h4>Click “Enable or disable an extension”--->11,12</h4>
<p><img src="images/pic11 - enableOrDisable.PNG" alt="enableOrDisable" width="50%" height="50%"></p>
<p>- Enable: php_imap.dll</p>
<p>- Enable: php_intl.dll</p>
<p>- Enable: php_opcache.dll</p>
<p>- Refresh the osTicket site in your browse, observe the changes</p>
<p>
<img src="images/pic12 - enableFeatures.PNG" alt="enableFeatures" width="50%" height="50%">
</p>
<br />

<h4>Refresh osTicket in the browser to confirm changes to extensions</h4>
<img src="images/pic10 - osTicketInstaller.PNG" alt="osTicketInstaller" width="50%" height="50%">
<p><img src="images/pic13 - refreshedOsTicketInstaller.PNG" alt="refreshedOsTicketInstaller" width="50%" height="50%"></p>

<h2>Rename: ost-sample-config.php--->14</h2>
<h4>- From: C:\inetpub\wwwroot\osTicket\include\ost-sample-config.php---></h4>
<h4>- From: To: C:\inetpub\wwwroot\osTicket\include\ost-config.php---></h4>
<h4>Open Properties for ost-config</h4>
<p>
<img src="images/pic14 - osTicketConfig.PNG" alt="osTicketConfig" width="50%" height="50%">
</p>
<br />


<h2>Assign Permissions</h2>
<h4>- Disable inheritance -> Remove All---></h4>
<h4>- New Permissions -> Everyone -> All---></h4>
<p>
<img src="images/pic15 - disableInheritence.PNG" alt="disableInheritence" width="50%" height="50%">
<img src="images/pic16 - everyonePermit.PNG" alt="everyonePermit" width="50%" height="50%">
<img src="images/pic17 - applyPermit.PNG" alt="applyPermit" width="50%" height="50%">
</p>

<br />


<h2>Continue Setting up osTicket in the browser (click Continue)--->18</h2>
<p><img src="images/pic18 - fillOutInfo.PNG" alt="fillOutInfo" width="50%" height="50%"></p>
<br />


<h2>From the Installation Files, download and install HeidiSQL---></h2>
<h4>- Open Heidi SQL</h4>
<h4>- Create a new session, root/Password1---></h4>
<p><img src="images/pic19 - hiediNew.PNG" alt="hiediNew" width="50%" height="50%"></p>
<br />
<h4>- Click OK to connect to the session--->20</h4>
<p><img src="images/pic20 - connectionEstablished.PNG" alt="connectionEstablished" width="50%" height="50%"></p>
<br />
<h4>- Right click and create a new database called “osTicket”--->22, 23</h4>
<p>
<img src="images/pic22 - newDatabase.PNG" alt="newDatabase" width="50%" height="50%">
<img src="images/pic23 - databaseCreated.PNG" alt="databaseCreated" width="50%" height="50%">
</p>
<br />


<h2>Continue Setting up osticket in the browser---21></h2>
<h4>- MySQL Database: osTicket</h4>
<h4>- MySQL Username: root---></h4>
<h4>- MySQL Password: Password1---></h4>
<h4>- Click “Install Now!”---></h4>
<p>
<img src="images/pic21 - databaseDetails.PNG" alt="databaseDetails" width="50%" height="50%">
</p>
<br />


<h2>Congratulations, hopefully it is installed with no errors!--->24</h2>
<h4>- Browse to your help desk login page: http://localhost/osTicket/scp/login.php</h4>
<p>
<img src="images/pic24 - congrats.PNG" alt="congrats" width="50%" height="50%">
</p>
<br />

<h2>Clean up steps</h2>
<h4>Delete setup folder from - c:\inetpub\wwwroot\osTicket </h4>
<img src="images/pic25 - deleteSetupFolder.PNG" alt="deleteSetupFolder" width="50%" height="50%">

<h4>Restore permissions in ost-config to read only</h4>
<img src="images/pic26 - readOnly.PNG" alt="readOnly" width="50%" height="50%">

<h4>Login to osTicket</h4>
<img src="images/pic27 - loginToOsticket.PNG" alt="loginToOsticket" width="50%" height="50%">
<img src="images/pic28 - loginSuccessful.PNG" alt="loginSuccessful" width="50%" height="50%">




