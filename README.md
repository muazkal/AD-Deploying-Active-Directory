<h1>Deploying Active Directory in Azure</h1> 

<h2>Description</h2> This is part 2/3 of the Active Directory lab. In this portion, Active Directory will be installed on the domain controller, a domain admin will be created, and the client VM will be connected to the domain. <br/><br /> 

<h2>Environments and Utilities Used</h2>
- <b>Microsoft Azure</b>
- <b>Virtual Machines</b>
- <b>Remote Desktop Connection</b>
- <b>Active Directory</b>

<h2>Operating Systems Used</h2>
- <b>Windows Server</b>
- <b>Windows 10</b>


<h2>Project Walk-through:</h2> 

<h3>Log back into the domain controller VM and click "Add Roles and Features." We will now install Active Directory.</h3> 
<img src="Capture2.JPG"> 

<h3>Click "Next" until you get to the "Server Roles" tab. Once there, check <b>Active Directory Domain Services</b>.</h3> 
<img src="Capture3.JPG"> 

<h3>Now, click "Next" until you are given the option to install.</h3> 
<img src="Capture4.JPG"> 

<h3>A yellow flag should now appear at the top right of the screen. Click it and go to "Add a new forest."</h3> 
<p>You will be given the choice to choose any domain name. For this lab, I chose "mydomain.com."</p> 
<img src="Capture5.JPG"> 
<img src="Capture6.JPG"> 

<h3>Make sure to uncheck the option to create a new DNS delegation. Then, click "Next" until you are given the option to install.</h3> 
<img src="Capture7.JPG"> 

<h2>Creating two "Organizational Units" (OUs): "Employees" and "Admins."</h2> 
<h3>Now open "Active Directory Users and Computers" and create the two OUs mentioned above <b>under the new domain</b>.</h3> 
<img src="Capture8.JPG"> <img src="Capture9.JPG"> 

<h2>Adding the Windows 10 computer (which I named Client-1) to the domain</h2> <h3>Log back in to the client VM and open the "About" page in the computer settings. Then open <b>"Rename PC (advanced)"</b>.</h3> 
<p>Then click "Change."</p> 
<img src="Annotation 2025-01-16 061043.png"> 
<img src="Annotation 2025-01-16 072940.png"> 

<h3>Check "Domain" and enter the new domain name you created on the domain controller.</h3> 
<img src="Annotation 2025-01-16 073006.png"> 

<h3>A new window will open (close the settings to see it). Now the VM will restart.</h3> 
<img src="Annotation 2025-01-16 073046.png"> 

<h1>You did it 🎉!</h1> <h3>You just successfully completed part 2 of the Active Directory lab! Here's what you achieved in this portion:</h3>
  <ul> 
    <li>Installed and configured Active Directory Domain Services on the domain controller.</li> 
    <li>Created a new forest and set up a domain with a custom name.</li> 
    <li>Organized the domain structure by adding "Organizational Units" for Employees and Admins.</li> 
    <li>Connected the Windows 10 client VM to the newly created domain.</li> 
  </ul> 
    
<p> At this point, your Active Directory environment is set up and ready for user management and domain-based administration. Stay tuned for part 3, where we will explore creating user accounts, setting group policies, and managing permissions!</p>
