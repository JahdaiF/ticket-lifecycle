<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
This tutorial outlines the entire lifecycle of a support ticket, from the moment an end user reports an issue to its final resolution by the IT team. We will simulate a professional environment by creating tickets as users and then switching roles to manage, escalate, and resolve them as help desk agents.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Support Scenario 1:</h2>



### Support Scenario 1: Critical Banking System Outage

1. **The Intake (End User):** Our first simulation begins with **Karen (Karen@gmail.com)** reporting a high-priority issue. She submits a ticket through the portal stating that the "Entire mobile/online banking system is down."



2. **The Agent Review (John):** Logging in as **John**, we first perform a review of the ticket. At this stage, we observe the default details—specifically the Priority and SLA—assigned by the system based on the Help Topic Karen selected.

3. **The Escalation:** To ensure the issue is handled within the proper timeframe, John manually upgrades the ticket to a **Sev-A (1 hour, 24/7)** SLA and reassigns it to the **Online Banking** department. 

4. **Permission Check:** A key observation in this step is the system's "disappearing" act: once the ticket is moved to a department where John lacks membership, he can no longer access the record. 

5. **Resolution:** **Jane** (the SysAdmin) then steps in to resolve the outage and close the ticket.

---

### Support Scenario 2: Routine Software Request

1. **The Submission:** **Ken (Ken@gmail.com)** submits a request regarding the accounting department’s need for an **Adobe upgrade**, noting that the current installation is non-functional.

2. **The Workflow:** John identifies this as a standard software support task. He classifies the ticket under a **Sev-B (4 hours, 24/7)** SLA and assigns it to the **Support** department. 

3. **Resolution:** Because this falls within his area of responsibility, John manages the communication and works the ticket until it is successfully closed.

---

### Support Scenario 3: Executive Hardware Support

1. **The Incident:** **Karen** returns to the portal to report a hardware failure: the **CFO's laptop** will no longer power on. 

2. **The Triage:** John reviews the ticket and applies a **Sev-B** SLA. Even though the user is an executive, the hardware repair falls under standard support procedures. 

3. **Resolution:** John retains ownership of the ticket, performs the necessary coordination, and documents the resolution.

---

### Advanced Analysis: Testing Security Boundaries

To truly understand **Role-Based Access Control (RBAC)**, we performed a deliberate escalation of all active tickets. By moving tickets into the **SysAdmins** department, we confirmed that standard agents lose all visibility and modification rights.

**Restoring Access:**
1. We transitioned to the **Admin Panel** to modify our agent profile.
2. We granted our account **"View Only"** access to the SysAdmins department.
3. Upon returning to the **Agent Panel**, we observed that while we could now "see" the escalated tickets, we were still prohibited from making any changes to them. 



---

### Professional Summary

This lab serves as a blueprint for how modern IT departments manage the influx of support requests. By utilizing **Service Level Agreements (SLAs)** and **Departmental Routing**, we ensure that critical outages are prioritized over routine software updates.

#### The "Ticket Everything" Principle
In a professional setting, "drive-by" requests—where a user catches you in the hallway—can derail productivity and leave no audit trail. This lab emphasizes the importance of documentation; if a task isn't recorded in a ticket, it doesn't exist in the eyes of management. Tickets provide the data necessary to justify team growth and identify failing hardware trends.

#### Building Technical Intuition
Mastery of these platforms comes through repetition. By cycling through these scenarios multiple times, we build the "technical pillars" and professional muscle memory required to manage a help desk with confidence and precision.
