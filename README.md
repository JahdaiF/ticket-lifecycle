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
2. <b>My Action:</b> I logged in as the agent ("John") to triage the ticket. Since this affected all customers, I manually upgraded the ticket to a <b>Sev-A SLA (1 hour response, 24/7)</b>. 
3. <b>The Pivot:</b> I reassigned the ticket to the **Online Banking Department**. 
4. <b>Key Learning:</b> This tested my **RBAC (Role-Based Access Control)** settings. As soon as I moved the ticket to a department I wasn't part of, I lost access to the record, exactly how a secure financial environment should function.

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
