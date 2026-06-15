# Active-Directory-Lab
This is an Active Directory Lab created by [Josh Madakor](https://www.youtube.com/watch?v=MHsI8hJmggI&amp;t=373s). This lab is what I will be using to get a hands-on experience with Active Directory.

# Active Directory Diagram
<img width="1777" height="1062" alt="Diagram" src="https://github.com/user-attachments/assets/41f4dd3c-c4b2-4d00-a781-c824f28d7ce9" />

This is the diagram. The two operating systems that are used are Windows Server 2019 and Windows 10.

# Network Setup

Once Windows Server 2019 is installed. You need to first identify which network is the external and internal.

<img width="1219" height="633" alt="Screenshot 2026-06-13 182121" src="https://github.com/user-attachments/assets/fa4609b8-0f97-4e54-9142-1e1b98e89e2a" />

Now that you have identified which adapter is which, you now must set up the internal network like the diagram had shown.

<img width="1016" height="740" alt="image" src="https://github.com/user-attachments/assets/8517bdb0-6357-4bb4-81fb-7731b2b9bb10" />

# Adding Domain
Now that your network has been configured. Install the Domain Services role on your server.

<img width="387" height="136" alt="Screenshot 2026-06-13 183434" src="https://github.com/user-attachments/assets/2884c7f9-16b4-4ee1-b930-e7a882989de9" />

After it has been installed you now need to deploy it.  

You will know if it has been installed if the user is now MYDOMAIN\administrator
<img width="1192" height="708" alt="Screenshot 2026-06-14 162035" src="https://github.com/user-attachments/assets/26407357-a382-40b7-a126-948186c6aa28" />

# Creating Admin Account
Now that you have added a domain you must create and admin account instead of the default account.

Locate the Active Directory Users and Computers.

<img width="345" height="390" alt="Screenshot 2026-06-14 162353" src="https://github.com/user-attachments/assets/22bc2b90-fd96-49a5-ae2f-6df7d0ce8951" />

Once found, right-click (yourdomain).com and create an organization unit naming that admin or any naming convention you prefer for this lab.

<img width="1581" height="784" alt="Screenshot 2026-06-14 162605" src="https://github.com/user-attachments/assets/07343fd1-8492-4e87-b00a-f59ca5679af2" />

After that has been created, right-click the OU and create a new user.

<img width="645" height="585" alt="Screenshot 2026-06-14 162721" src="https://github.com/user-attachments/assets/cbd7d3b5-a851-482b-a89f-d3eec4c34dfa" />

You will notice that the user is not admin. Right-click the user and go into properties, click "Member of" then click add and title the object to your preference, check the name, and then click "okay". 

<img width="1292" height="954" alt="Screenshot 2026-06-14 163408" src="https://github.com/user-attachments/assets/07426117-1664-47ec-b047-44b536c638bb" />

Sign out of your account and then log in to "other user" and log in with the credentials you have set your admin account as.

<img width="1313" height="863" alt="Screenshot 2026-06-14 163829" src="https://github.com/user-attachments/assets/1c8525b8-9ef1-4643-805a-4cdf91f540d5" />

# RAS/NAT Installation

The purpose of installing RAS/NAT is to allow the Windows 10 Client to connect to the public facing internet using one IP address without having exhaust the address pool in the network.

What you need to do, is to install remote access through the "Add Roles and Features" and then click the role services, "Routing" and "DirectAccess and VPN". 

<img width="934" height="570" alt="Screenshot 2026-06-14 180801" src="https://github.com/user-attachments/assets/de2c3236-7358-4294-bb8b-3c55ef98e20b" />

Proceed, to Tools then Routing and Remote Access

Right-click DC and then click NAT, and then select the DHCP and then click Finish.

<img width="1598" height="674" alt="Screenshot 2026-06-14 184343" src="https://github.com/user-attachments/assets/65e6a383-adb6-4355-a35e-8199f6ad4e3d" />

<img width="1720" height="782" alt="Screenshot 2026-06-14 184533" src="https://github.com/user-attachments/assets/d67a9327-0bbb-4e05-8db3-9dff856eeaae" />

# DHCP Server Install and Scope

To add the DHCP server. Like adding Remote Access, click the DHCP Server and install.

<img width="843" height="410" alt="image" src="https://github.com/user-attachments/assets/a3c21cfa-4896-4aef-985d-b457d24fbd28" />

Once installed, you must configure your scope by going through tools, clicking DHCP, righ-clicking IPv4 and then create a new scope based on the scope in the diagram.

<img width="1591" height="882" alt="Screenshot 2026-06-14 190110" src="https://github.com/user-attachments/assets/3e764f7a-6f08-4fbc-91bb-56849e4c4b59" />

# Create Users through Powershell

Now it's time to create users.

Using this link [Link](https://github.com/joshmadakor1/AD_PS/archive/master.zip). This is the script helps you automate user creation, instead of having to manually fill out a user individually.

This ZIP file contains the powershell script and the random user generated names that will be created once the script has been ran. 

Extract the file and make sure to add your name to the names.txt and then proceed to open Powershell ISE and run as administrator, open file, and click "1_CREATE_USERS"

<img width="1774" height="781" alt="Screenshot 2026-06-14 194717" src="https://github.com/user-attachments/assets/673590f7-adf0-4d1d-b217-da12aca3548d" />

<img width="1309" height="652" alt="Screenshot 2026-06-14 194552" src="https://github.com/user-attachments/assets/f39dbb36-22f8-488e-b9d4-47ad9088a3a1" />

In order for the script to run, first you type Set-ExecutionPolicy Unrestriced, then make sure you run it from the directory you have placed it in. 

<img width="697" height="101" alt="Screenshot 2026-06-14 200733" src="https://github.com/user-attachments/assets/3dcd4d5d-29d9-46b6-89f5-a881c0a69e6b" />

<img width="707" height="220" alt="Screenshot 2026-06-14 195321" src="https://github.com/user-attachments/assets/fffeb95a-67c9-472f-ac9e-981e03f94b81" />

Once that has ran until you have created as many users as you want. Make sure to verify by going back to the Active Directory and clicking on "_USERS"

<img width="1693" height="829" alt="Screenshot 2026-06-14 201240" src="https://github.com/user-attachments/assets/ae07014e-4ee3-45c9-a062-38b868b8ac78" />

















