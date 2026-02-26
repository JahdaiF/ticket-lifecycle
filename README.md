<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
The goal of this tutorial is to manage a full-service help desk environment in the cloud. I simulated the entire ticket lifecycle, from end-user reporting to final resolution, using role-based access to manage priorities and department escalations.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (RDP)
- Internet Information Services (IIS)
- osTicket (PHP/MySQL)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Real-World Support Scenarios</h2>

<h2>Support Scenario 1: Critical Banking Outage</h2>

1. <b>The Issue:</b> A user ("Karen") reported a total outage of the mobile and online banking portal.
<img width="1420" height="1118" alt="1" src="https://github.com/user-attachments/assets/ec6ec06e-0cea-4d2c-8de1-a75c6f0955e5" />
<img width="1396" height="1149" alt="2" src="https://github.com/user-attachments/assets/9b1bf2b4-28d5-4fac-85ba-32ed3c3a2005" />

2. <b>My Action:</b> I logged in as the agent ("John") to triage the ticket. Since this affected all customers, I manually upgraded the ticket to a <b>Sev-A SLA (1 hour response, 24/7)</b>.
<img width="1415" height="1178" alt="3" src="https://github.com/user-attachments/assets/12141786-abfb-4165-85f7-6403829b7b4c" />
<img width="1417" height="1167" alt="4" src="https://github.com/user-attachments/assets/09fa9b3f-ee5d-4a5b-a770-0ac4d03258e1" />
<img width="1405" height="1204" alt="5" src="https://github.com/user-attachments/assets/8987a56f-edfd-4bc8-9dbd-4332a16a40b3" />
<img width="1413" height="1164" alt="6" src="https://github.com/user-attachments/assets/61874f67-9f55-49d6-9621-dadb2b1eed0a" />
<img width="1405" height="1204" alt="7" src="https://github.com/user-attachments/assets/b6326973-6f09-4c88-8641-29faf965bcb5" />
<img width="1413" height="1184" alt="8" src="https://github.com/user-attachments/assets/312e063d-1ce2-42c6-8f7c-bbc1c91f332b" />
<img width="1424" height="1180" alt="9" src="https://github.com/user-attachments/assets/c5eb4c5c-c9e7-4d90-b56a-b01062fff95e" />

3. <b>The Pivot:</b> I reassigned the ticket to the **Online Banking Department**.
<img width="1397" height="1183" alt="10" src="https://github.com/user-attachments/assets/bf463df6-cceb-40c3-aa5d-5ea022752518" />

4. <b>Key Learning:</b> This tested my **RBAC (Role-Based Access Control)** settings. As soon as I moved the ticket to a department I wasn't part of, I lost access to the record, exactly how a secure financial environment should function.
<img width="1418" height="1189" alt="11" src="https://github.com/user-attachments/assets/a2a2a3d0-7bbf-4b28-8614-d9e254da3c23" />
<img width="1405" height="1175" alt="13" src="https://github.com/user-attachments/assets/5c1c055e-b382-4ccb-a126-40f761964c42" />
<img width="1413" height="1205" alt="14" src="https://github.com/user-attachments/assets/3ff184d9-8560-4732-b6d6-4e4753f5e0ea" />

<h2>Scenario 2: Departmental Software Request</h2>
1. <b>The Issue:</b> A user requested an Adobe upgrade for the accounting team, stating that the current version was not working properly. <br>
2. <b>My Action:</b> Since this was a routine software request, I assigned it a 4-hour SLA (Sev-B) and routed it to the Support department. <br>
3. <b>Resolution:</b> Due to having the correct permissions for the <b>Support</b> department, I handled the communication and closed the ticket once the software was verified. <br>

<h2>Scenario 3: Executive Hardware Failure</h2>
1. <b>The Issue:</b> There is a report that the CFO's laptop is no longer powering on. <br>
2. <b>Triage:</b> Even though it involved an executive, I followed standard hardware protocols. I assigned a <b>Sev-B SLA</b> and kept ownership of the ticket to coordinate the repair. <br>



### Deep Dive: Troubleshooting Security Boundaries
One of the most important parts of this lab was testing **permissions**. I intentionally tried to "break" the workflow to see how the system responded:

1. **Isolation Test:** I moved all active tickets into the **SysAdmin** department.
2. **Verification:** I confirmed that as a standard agent, I was completely locked out and could no longer see the tickets.
3. **Modification:** I went into the **Admin Panel** to give my account "View Only" access to that department. 
4. **The Result:** I could finally see the escalated tickets again, but the system correctly prevented me from editing them. This confirmed that my permission "layers" were working exactly as intended.



<h2>Summary and Key Takeaways</h2>

This lab demonstrates how a structured IT department manages a constant flow of support requests. By using <b>Service Level Agreements (SLAs)</b> and <b>Departmental Routing</b>, I was able to ensure that critical outages stayed at the top of the queue while routine software updates were scheduled appropriately.

<b> The "Ticket Everything" Principle </b>
One of the most important takeaways from this project was the necessity of documentation. In a fast-paced environment, direct requests made outside of the ticketing system can easily be forgotten and leave no record for the team. I used this lab to emphasize a "ticket everything" approach. If a task isn't recorded, it doesn't exist for reporting or management purposes. Having this data is what allows a team to identify hardware trends and justify the need for more resources.

#### Building Technical Muscle Memory
I believe technical intuition comes through repetition. By cycling through these different scenarios, from banking outages to hardware failures, I built the professional muscle memory needed to manage a help desk with confidence and precision.
