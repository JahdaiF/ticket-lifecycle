<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
The goal of this tutorial is to manage a full-service help desk environment in the cloud. I simulated the entire ticket lifecycle—from end-user reporting to final resolution—using role-based access to manage priorities and department escalations.<br />

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

* **The Issue:** A user ("Karen") reported a total outage of the mobile and online banking portal. 
* **My Action:** I logged in as the agent ("John") to triage the ticket. Since this affected all customers, I manually upgraded the ticket to a **Sev-A SLA (1 hour response, 24/7)**. 
* **The Pivot:** I reassigned the ticket to the **Online Banking Department**. 
* **Key Learning:** This tested my **RBAC (Role-Based Access Control)** settings. As soon as I moved the ticket to a department I wasn't part of, I lost visibility of the record—exactly how a secure financial environment should function.

<h2>Scenario 2: Departmental Software Request</h2>
* **The Issue:** A user requested an Adobe upgrade for the accounting team, noting the current version was non-functional.
* **My Action:** I classified this as a standard software task under a **Sev-B SLA (4-hour window)** and assigned it to the Support department.
* **Resolution:** Since I had the correct permissions for the "Support" department, I handled the communication and closed the ticket once the software was verified.

<h2>Scenario 3: Executive Hardware Failure</h2>
* **The Issue:** A report that the CFO's laptop would no longer power on.
* **Triage:** Even though it involved an executive, I followed standard hardware protocols. I assigned a **Sev-B SLA** and kept ownership of the ticket to coordinate the repair.



### Deep Dive: Troubleshooting Security Boundaries
One of the most important parts of this lab was testing **permissions**. I intentionally tried to "break" the workflow to see how the system responded:

1. **Isolation Test:** I moved all active tickets into the **SysAdmin** department.
2. **Verification:** I confirmed that as a standard agent, I was completely locked out and could no longer see the tickets.
3. **Modification:** I went into the **Admin Panel** to give my account "View Only" access to that department. 
4. **The Result:** I could finally see the escalated tickets again, but the system correctly prevented me from editing them. This confirmed that my permission "layers" were working exactly as intended.



###  Final Takeaway
Building this lab taught me that **documentation is the audit trail.** If it isn't in the ticket, it didn't happen. By using SLAs and automated routing, I learned how to prevent "drive-by" requests from derailing a team's productivity and how to ensure critical outages (like a bank going offline) always get eyes on them first.
