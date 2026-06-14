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



