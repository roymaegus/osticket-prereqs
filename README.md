<p align="center">
<img src="images/osTicketBanner.png" alt="osTicketBanner" >
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

<h3>Create an Azure Virtual Machine Windows 10, 4 vCPUs</h3>
<h5>Name: Vm-osticket</h5>
<h5>Username: labuser (for example/whatever you chose)</h5>
<h5>Password: osTicketPassword1! (for example/whatever you chose)</h5>
<h5>Initialize Virtual Machine</h5>



<h2>Installation Steps</h2>
<h5>Download osTicket from the Installation Files Folder</h5>

<h5>Extract and copy “upload” folder to c:\inetpub\wwwroot</h5>
<p>
<img src="images/pic8 - dndUploadFolder.PNG" alt="dndUploadFolder" width="50%" height="50%">
</p>
<h5>Within c:\inetpub\wwwroot, Rename “upload” to “osTicket” </h5>
<p>

</p>
<br />
<p>

<h5>Reload IIS (Open IIS, Stop and Start the server) </h5>
<br />

<h2>Go to sites -> Default -> osTicket </h2>
On the right, click “Browse *:80”
<p>
<img src="images/pic9 - browse80.PNG" alt="browse80" width="50%" height="50%">
</p>
<br />


<h2>Enable extensions</h2>
<h5>Go back to IIS, sites -> Default -> osTicket </h5>
<h5>Double-click PHP Manager</h5>
<p>
<img src="images/pic4 - openISS.PNG" alt="openISS" width="50%" height="50%">
</p>

<h5>Click “Enable or disable an extension”</h5>
<p><img src="images/pic11 - enableOrDisable.PNG" alt="enableOrDisable" width="50%" height="50%"></p>
<p>- Enable: php_imap.dll</p>
<p>- Enable: php_intl.dll</p>
<p>- Enable: php_opcache.dll</p>
<p>- Refresh the osTicket site in your browse, observe the changes</p>
<p>
<img src="images/pic12 - enableFeatures.PNG" alt="enableFeatures" width="50%" height="50%">
</p>
<br />

<h5>Refresh osTicket in the browser to confirm changes to extensions</h5>
<img src="images/pic10 - osTicketInstaller.PNG" alt="osTicketInstaller" width="50%" height="50%">
<p><img src="images/pic13 - refreshedOsTicketInstaller.PNG" alt="refreshedOsTicketInstaller" width="50%" height="50%"></p>

<h2>Rename: ost-sample-config.php</h2>
<h5>- From: C:\inetpub\wwwroot\osTicket\include\ost-sample-config.php</h5>
<h5>- From: To: C:\inetpub\wwwroot\osTicket\include\ost-config.php</h5>
<h4>Open Properties for ost-config</h4>
<p>
<img src="images/pic14 - osTicketConfig.PNG" alt="osTicketConfig" width="50%" height="50%">
</p>
<br />


<h2>Assign Permissions</h2>
<h5>- Disable inheritance -> Remove All</h5>
<h5>- New Permissions -> Everyone -> All</h5>
<p>
<img src="images/pic15 - disableInheritence.PNG" alt="disableInheritence" width="50%" height="50%">
<img src="images/pic16 - everyonePermit.PNG" alt="everyonePermit" width="50%" height="50%">
<img src="images/pic17 - applyPermit.PNG" alt="applyPermit" width="50%" height="50%">
</p>

<br />


<h2>Continue Setting up osTicket in the browser (click Continue)</h2>
<p><img src="images/pic18 - fillOutInfo.PNG" alt="fillOutInfo" width="50%" height="50%"></p>
<br />


<h2>From the Installation Files, download and install HeidiSQL</h2>
<h5>- Open Heidi SQL</h5>
<h5>- Create a new session, root/Password1</h5>
<p><img src="images/pic19 - hiediNew.PNG" alt="hiediNew" width="50%" height="50%"></p>
<br />
<h5>- Click OK to connect to the session</h5>
<p><img src="images/pic20 - connectionEstablished.PNG" alt="connectionEstablished" width="50%" height="50%"></p>
<br />
<h5>- Right click and create a new database called “osTicket”</h5>
<p>
<img src="images/pic22 - newDatabase.PNG" alt="newDatabase" width="50%" height="50%">
<img src="images/pic23 - databaseCreated.PNG" alt="databaseCreated" width="50%" height="50%">
</p>
<br />


<h2>Continue Setting up osticket in the browser</h2>
<h5>- MySQL Database: osTicket</h5>
<h5>- MySQL Username: root</h5>
<h5>- MySQL Password: Password1</h5>
<h5>- Click “Install Now!”</h5>
<p>
<img src="images/pic21 - databaseDetails.PNG" alt="databaseDetails" width="50%" height="50%">
</p>
<br />


<h2>Congratulations, hopefully it is installed with no errors!</h2>
<h5>- Browse to your help desk login page: http://localhost/osTicket/scp/login.php</h5>
<p>
<img src="images/pic24 - congrats.PNG" alt="congrats" width="50%" height="50%">
</p>
<br />

<h2>Clean up steps</h2>
<h5>Delete setup folder from - c:\inetpub\wwwroot\osTicket </h5>
<img src="images/pic25 - deleteSetupFolder.PNG" alt="deleteSetupFolder" width="50%" height="50%">

<h5>Restore permissions in ost-config to read only</h5>
<img src="images/pic26 - readOnly.PNG" alt="readOnly" width="50%" height="50%">

<h5>Login to osTicket</h5>
<img src="images/pic27 - loginToOsticket.PNG" alt="loginToOsticket" width="50%" height="50%">
<img src="images/pic28 - loginSuccessful.PNG" alt="loginSuccessful" width="50%" height="50%">




