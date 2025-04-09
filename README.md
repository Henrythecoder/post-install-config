post-install-config<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the how to configure osTicket and go over a few terms we might see in the work force.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>osTicket Admin Panel Configuration Lab</h2>

Now that we have installed osTicket and accessed the admin panel, let’s configure it.

If you haven't installed osTicket yet, please refer to my [osTicket installation lab](https://github.com/AustinmJoseph/ostiket-prereqs).

1. Log into the Admin Panel
Log in with your admin account first. Once logged in, click on the Admin Panel. You will notice many additional options appear.

---

![ade1](https://github.com/user-attachments/assets/e22a717a-dc2f-48ea-9a50-f534d89d406b)


---


2. Create Roles and Groups
   
We will begin by creating roles that define different access levels for different groups. Groups are used to assign permissions to different people.

Create a Role:

Go to Admin Panel → Manage → Roles.

Create a new role called System Admins and give them all permissions.

Create a Group:

Go to Admin Panel → Manage → Groups.

Create a group called System Admins and assign the System Admins role to this group.

---

![ade3](https://github.com/user-attachments/assets/c41bb680-bceb-48c9-986a-8fa3fd6b9c13)
![ad4](https://github.com/user-attachments/assets/6cc98b30-b670-4830-b086-dc0df5660119)
![ade5](https://github.com/user-attachments/assets/47b8450b-8560-4877-9cd9-8c5eb0fc3bb5)

---

3. Create a Department
   
Next, let's create a department for system admins.

Go to Admin Panel → Manage → Departments.

Create a new department called Sys Admins.

---

![ade6](https://github.com/user-attachments/assets/0c1dc84b-3072-4384-afee-20c2f7724dd0)
![ad7](https://github.com/user-attachments/assets/6840fa95-7f80-42b9-8d12-06dddf9d6a91)
![ad8](https://github.com/user-attachments/assets/940fddc4-9990-497c-a9f9-0ebd4fb66119)

---


4. Create a Team
   
Teams allow you to pull agents from different departments into one team.

Go to Admin Panel → Manage → Teams.

Create a team called Shield.

---

![ade7](https://github.com/user-attachments/assets/9f19c4ae-c207-4178-a89c-a958e4d97780)
![ade8](https://github.com/user-attachments/assets/c87e42ac-cfc4-4b98-b56f-99cf5bb039e9)

---

5. Adjust Ticket Registration Settings
For this lab, we want everyone to be able to register tickets.

Go to Admin Panel → Settings → Users.

Make sure the box labeled "Allow users to register tickets" is unchecked.

---

![ade9](https://github.com/user-attachments/assets/34f13566-9001-4d27-88e7-0ff7b590ffcc)

---

6. Create Agents
Now we will create a few agents (workers) to assign roles and teams.

Go to Admin Panel → Manage → Agents.

Click on Agents and add a new agent.

---

![ade10](https://github.com/user-attachments/assets/73585f74-2408-473a-b51d-d3db409b4772)

---

Agent 1:

Name: Gwen Stacy

Role: Superior Admin (full access)

Team: Shield

---

![ad13](https://github.com/user-attachments/assets/1ead547d-90fb-44b2-832a-ad5843af6f16)
![ad15](https://github.com/user-attachments/assets/dd0aab65-63cb-41d0-bb89-422769307f27)


---



Agent 2:

Name: Harry Osborn

Role: Support (view access only)

Team: Shield

Make sure to record the email addresses for these agents, as they will be required for login.

---

![ad14](https://github.com/user-attachments/assets/d130f5bb-f3f6-4cb1-8fa2-d30cf0e877dd)
![ad15](https://github.com/user-attachments/assets/02a56f11-1212-4f60-8db8-f0a79c383e6c)


---

7. Create a User
Now, let's create a user for ticket submission.

Go to the top-right corner and click on Agent Panel.

Navigate to Users and click Add New User.

Create a user with the name Norman Osborn (for this lab, we’ll create just one user).

---

![ad16](https://github.com/user-attachments/assets/a168490f-25ed-44d1-aad0-052fa1f4fe24)
![ad17](https://github.com/user-attachments/assets/051bdf79-ec01-47dc-9d3a-525df7437a87)
![ad18](https://github.com/user-attachments/assets/6677b1ec-5155-4ea0-a0b8-7bf326eeee00)

---

8. Configure SLA (Service Level Agreements)
SLAs are used to notify agents how quickly a ticket should be handled.

Go to Admin Panel → Manage → SLA.

Create the following 3 SLAs:

SEV-A: Critical – needs immediate attention

---

![ad19](https://github.com/user-attachments/assets/4bf6a3af-0049-46a3-96c0-340f7b08cd9a)

---

SEV-B: Medium priority

---

![ad20](https://github.com/user-attachments/assets/ec466a50-a665-472c-871c-aae79f130582)


---

SEV-C: Low priority

---

![ad21](https://github.com/user-attachments/assets/946898be-6f68-4d40-943c-430a01b4cce6)


---

![ad22](https://github.com/user-attachments/assets/661ab724-62f8-4500-86b9-f8889d2988c4)

---

9. Create Help Topics
Help Topics guide users when they create tickets, directing them toward the correct category.

Go to Admin Panel → Manage → Help Topics.

Create the following Help Topics:

Personal Computer (with the sub-topic Report a Problem)

Equipment Request (with the sub-topic General Inquiry)

---

![ad23](https://github.com/user-attachments/assets/50e957f9-e103-4c98-b85e-637919c7cf36)
![ad24](https://github.com/user-attachments/assets/7b083788-9014-4bf9-bd22-7d62e2f28a37)
![ad25](https://github.com/user-attachments/assets/942579f4-4845-4bf8-8e59-f0b6d3b4e950)
![ad26](https://github.com/user-attachments/assets/da320c7b-edef-4ff5-83f5-6c4182fbc472)

---


Conclusion
This lab is a prerequisite for the next lab, where we will practice using the ticketing system. Follow these steps to set up your admin panel, roles, groups, agents, and SLAs in preparation for the next Lab.



