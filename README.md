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
