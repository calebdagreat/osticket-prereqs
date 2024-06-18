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

- Create a Windows 10 Virtual Machine (VM) w/ 2 Virtual CPUs in Azure
- Access VM through Remote Desktop Protocol (RDP)
- Install / Enable Internet Information Services (IIS)
- Download and Install PHP Manager for IIS
- Download and Install Rewrite Module
- Create Directory C:\PHP
- Download PHP 7.3.8 and unzip contents into C:\PHP
- Download and Install "VC_redist.x86.exe", and "MySQL_5.5.62"
- Complete configurations in MySQL, and Open IIS as Admin
- Register PHP , Reload IIS
- Download and Install osTicket v1.15.8
  (Details Below)

<h2>Installation Steps</h2>

<p>
<img width="760" alt="Screenshot 2024-06-10 at 10 51 44 PM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/3b1889c0-2782-454a-b4b6-43e00d9b38e1">
  
</p>
<p>
  
- Create a Windows 10 Virtual Machine (VM) w/ 2 Virtual CPUs in Azure
</p>
<br />

<p>
<img width="700" alt="Screenshot 2024-06-11 at 8 03 53 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/4f0d66d5-cc7a-48c6-97ac-be3223f68c8d">

</p>
<p>
  
- Access VM through Remote Desktop Protocol (RDP)
- Install / Enable Internet Information Services (IIS)
</p>
<br />

<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 21 22 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/3edeb362-b507-40ca-8e9f-a07b9e17336d">
<img width="600" alt="Screenshot 2024-06-11 at 8 21 52 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/e222995d-ab50-4db3-8789-c8caa4627fd6">


</p>
<p>
  
- Download and Install PHP Manager for IIS
- Download and Install Rewrite Module
</p>
<br />
<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 18 25 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/f38aa960-6031-4d2f-92f1-b6a9f73bfd38">
<img width="600" alt="Screenshot 2024-06-11 at 8 24 15 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/013bc019-9e01-4164-bdb0-c0ea3d965d9c">

</p>
<p>
  
- Create Directory C:\PHP
- Download PHP 7.3.8 and unzip contents into C:\PHP
</p>
<br />

<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 26 09 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/2dacb093-bffd-4aa6-a7da-c466679afd27">
<img width="600" alt="Screenshot 2024-06-11 at 8 26 42 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/ab2435e7-434e-4c01-a6be-c50a05d1b527">

</p>
<p>
- Download and Install "VC_redist.x86.exe", and "MySQL_5.5.62"
</p>
<br />

<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 33 48 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/c986a9cb-7641-4b77-898e-b8a1431f1d38">
</p>
<p>
  
- Extract and copy "upload" folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename "upload" to "osTicket"

</p>
<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 43 23 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/cf4c8bc6-dd06-4c5a-a256-e2067aba63aa">

</p>
<p>
  
- Reload IIS (Open IIS, Stop and Start the server)
- Go to sites -> Default -> osTicket
    (on the right, click "Browse *:80")
</p>
<br />

<p><img width="600" alt="Screenshot 2024-06-11 at 8 44 55 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/3a004bc6-8a67-4908-92c8-50d407418e39">

</p>
<p>
  
Note that some extensions are not enabled
- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Enable three extensions, "php_imap.dll", "php_intl.dll", "php_opcache.dll"
- Refresh the osTicket site in your browser and observe the changes.
</p>
<br />
<p>

<img width="602" alt="Screenshot 2024-06-11 at 8 51 16 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/6c6eb366-25b4-4bbe-aa5d-4934d561bb80">


</p>
<p>
  
- Rename: ost-config.php
- Assign Permissions: ost-config.php
- Continue Setting up osTicket in browser
- Download and Install HeidiSQL (screenshot only for this step)
</p>
<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 52 47 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/13c29eb7-312c-4034-b0e9-495c89af2e93">

</p>
<p>
  
- Continue Setting up osticket in browser
- Enter MySQL Database name, Username and Password
- Click "Install Now!"
  
</p>
<br />

<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 53 18 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/2e66a72d-97bb-4b33-b14e-6ec4f0e602ea">

</p>
<p>
  
- This should bring us to the Congratulations screen if it is installed, hopefully with no errors.
</p>
<br />
<p>
<img width="600" alt="Screenshot 2024-06-11 at 8 55 25 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/9b67d076-2dfa-4882-8a33-e25c51a4b17a">
<img width="600" alt="Screenshot 2024-06-11 at 8 55 49 AM" src="https://github.com/calebdagreat/osticket-prereqs/assets/171304036/a3b20592-2a90-4c0c-accd-9a062ae3d099">
</p>
<p>
  
- Clean up (Delete: C:\inetpub\wwwroot\osTicket\setup)
- Set Permissions to "Read" only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Access help desk login page.
- INSTALLATION COMPLETE!
</p>
