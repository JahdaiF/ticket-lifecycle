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

2. <b>My Action:</b> I logged in as the agent ("John") to triage the ticket. I updated the priority level to <b>Emergency</b> and updated the <b>Help Topic</b> to <b>Report a Problem/Business Critical Outage</b>. Since this affected all customers, I manually upgraded the ticket to a <b>Sev-A SLA (1 hour response, 24/7)</b>.
<img width="1415" height="1178" alt="3" src="https://github.com/user-attachments/assets/12141786-abfb-4165-85f7-6403829b7b4c" />

<img width="1417" height="1167" alt="4" src="https://github.com/user-attachments/assets/09fa9b3f-ee5d-4a5b-a770-0ac4d03258e1" />

<img width="1550" height="1248" alt="1" src="https://github.com/user-attachments/assets/62ef20aa-eaf5-4603-97de-e1ff00c71d1d" />
<img width="1550" height="1252" alt="2" src="https://github.com/user-attachments/assets/f8a9cb6a-d2e8-45fe-b8ea-88f9e8485524" />
<img width="1553" height="1258" alt="3" src="https://github.com/user-attachments/assets/f3c5fc09-ddf9-46f4-9781-ea49b682c1c3" />
<img width="1555" height="1249" alt="4" src="https://github.com/user-attachments/assets/1f7946fd-04f2-40e2-ba8c-b12e08ba0066" />
<img width="1558" height="1239" alt="5" src="https://github.com/user-attachments/assets/61e6c031-1df3-4681-a35d-78db909c61e5" />
<img width="1555" height="1253" alt="6" src="https://github.com/user-attachments/assets/5d7f20da-af36-4c32-9586-6879823f5c0b" />

3. <b>The Pivot:</b> I reassigned the ticket to the **SysAdmins Department** and to <b>Jane Doe</b>.
<img width="1557" height="1252" alt="7" src="https://github.com/user-attachments/assets/8a17bd32-5aad-47e3-896a-aec7b4835d90" />
<img width="1552" height="1258" alt="8" src="https://github.com/user-attachments/assets/b0e7465d-e373-4b30-a5f8-63264533699f" />
<img width="1549" height="1249" alt="9" src="https://github.com/user-attachments/assets/6709c5ee-7eb7-4420-98d0-a9bef87d3cf1" />
<img width="1554" height="1263" alt="10" src="https://github.com/user-attachments/assets/2f2dd614-45c8-4d8d-be1c-71d4e07e6a6f" />
<img width="1552" height="1253" alt="11" src="https://github.com/user-attachments/assets/cf09edbe-7928-400d-a476-a7874a4a4565" />
<img width="1555" height="1270" alt="12" src="https://github.com/user-attachments/assets/bf7514b9-c704-458c-9ed5-3f04951b2746" />


4. <b>Key Learning:</b> This tested my **RBAC (Role-Based Access Control)** settings. As soon as I moved the ticket to a department I wasn't part of, I lost access to the record, exactly how a secure financial environment should function.
<img width="1554" height="1260" alt="13" src="https://github.com/user-attachments/assets/45dd6191-6bc1-4a0b-aec3-83975a14c309" />

5. <b>Resolve ticket</b>
<img width="1549" height="1245" alt="16" src="https://github.com/user-attachments/assets/502a17a6-41d1-428b-a96b-b71e412464e3" />
<img width="1557" height="1364" alt="18" src="https://github.com/user-attachments/assets/deb95f8c-00dd-4b50-b827-5fc411ca8bea" />
<img width="1553" height="1362" alt="19" src="https://github.com/user-attachments/assets/d7cb757c-b280-4407-bcb4-8c6b000a8e10" />
<img width="1551" height="1370" alt="20" src="https://github.com/user-attachments/assets/0032e0ff-ddaf-4822-b972-47a44ba68a15" />


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
