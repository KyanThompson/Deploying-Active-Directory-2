# Deploying-Active-Directory-2
# Deploying-Active-Directory# Preparing-Ad-infrastructure<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>
- Turn On Remote Desktop on Client-1:
Log into Client-1 as jane_admin, then go to System Properties and make sure domain users are allowed to use Remote Desktop.

- Create New User Accounts in AD:
On DC-1, sign in as jane_admin and open PowerShell. Run a script to create several user accounts in the _EMPLOYEES OU.

- Double-Check the New Accounts:
Open Active Directory Users and Computers and look in the _EMPLOYEES OU to confirm that the new accounts were created successfully.

- Test Remote Desktop Login:
Try logging into Client-1 with one of the new standard user accounts to make sure Remote Desktop is working as expected.

<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/user-attachments/assets/2cc7ae30-5712-400b-8791-6a84a45e924b)![image](https://github.com/user-attachments/assets/fbf36b15-29cc-4b52-8901-ac5ac1f2d162)
![image](https://github.com/user-attachments/assets/b8537608-7a0f-4ec2-833e-12c95ca2e4c9)![image](https://github.com/user-attachments/assets/19f5326e-d53d-40f1-b138-d61ef1db16a0)

Steps to Set Up Remote Desktop for Standard Users on Client-1

1. Log into Client-1 as an Admin:
Sign in to Client-1 using the domain admin account mydomain.com\jane_admin.

2. Turn On Remote Desktop for Domain Users:
Go to the System Properties on Client-1, find the Remote Desktop settings, and allow domain users to connect.

3. Add More Users:
On DC-1, log in as jane_admin. Open PowerShell ISE with admin rights and run a script that creates several new user accounts.

4. Check New Users in ADUC:
After running the script, open Active Directory Users and Computers and make sure the new users were added to the _EMPLOYEES OU.

5. Test Remote Desktop Login:
Try logging into Client-1 using one of the new user accounts you created. Use the password from the script and check that the user can connect with Remote Desktop.

