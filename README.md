<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> (25H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<br />

---

<h3>📋 Pre‑Lab Setup (Admin Panel)</h3>

Before creating tickets, perform the following administrative tasks:

1. Navigate to the **Admin Panel** → **Departments**.
2. **Delete** the <strong>Maintenance</strong> department (do not archive it).
3. Locate the <strong>SysAdmins</strong> department and change its setting to <strong>"Top Level Department"</strong>. This restricts visibility so that only agents explicitly granted access can view tickets assigned to this department.

> **Access URLs for this lab:**  
> - **Admin / Agent Login:** `http://localhost/osTicket/scp/login.php`  
> - **End‑User Portal:** `http://localhost/osTicket`

---

<h3>Scenario 1: Entire Mobile/Online Banking System Is Down (Sev‑A)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/wbqlkDs.png" height="80%" width="80%" alt="Ticket Intake - Online Banking Down"/>
</p>
<p>
As an end user, navigate to the osTicket portal at <code>http://localhost/osTicket</code> and submit a new ticket with the issue: <strong>"Entire mobile/online banking system is down."</strong> This represents a critical outage affecting all customers.
</p>
<br />

<h4>Stage 2: Assignment & Initial Triage (Permission Block)</h4>
<p>
<img src="https://i.imgur.com/Ri5F0Hl.png" height="80%" width="80%" alt="Ticket Assignment - Online Banking Down"/>
</p>
<p>
Log in as Help Desk Agent <strong>John</strong> at <code>http://localhost/osTicket/scp/login.php</code>. Open the new ticket and observe its default properties:<br /><br />
- <strong>Priority:</strong> Normal<br />
- <strong>Department:</strong> Support<br />
- <strong>SLA:</strong> Default SLA<br />
- <strong>Assigned To:</strong> Unassigned<br /><br />
John attempts to update the ticket with the correct critical settings:<br /><br />
- <strong>SLA:</strong> Sev-A (1 hour, 24/7)<br />
- <strong>Department:</strong> Online Banking (SysAdmins)<br /><br />
After saving, John logs out and logs back in. Because SysAdmins is a Top‑Level Department and John only has default view‑only access, the ticket is now completely hidden from his agent panel. He cannot see or modify any tickets assigned to that department.
</p>
<br />

<h4>Stage 3: Permission Grant & Advanced Triage</h4>
<p>
<img src="https://i.imgur.com/KdQB8Xz.png" height="80%" width="80%" alt="Working the Issue - Online Banking Down"/>
</p>
<p>
To resolve the permission block, an <strong>Admin</strong> logs into the Admin Panel and navigates to <strong>Agents → John Doe → Access</strong>, granting John <strong>"All Access"</strong> permissions. John logs out and back in.<br /><br />
Now able to view the ticket, John immediately:<br />
- Updates the <strong>Priority</strong> to <strong>Emergency</strong>.<br />
- Calls the end user (Karen) to confirm that all teller systems are indeed down.<br />
- Sets the <strong>SLA Plan</strong> to <strong>Sev-A</strong>.<br />
- Changes the <strong>Help Topic</strong> to <strong>Business Critical Outage</strong> with an internal note: <em>"Entire business system is offline."</em><br />
- Posts a public reply escalating the issue to the SysAdmin department after completing his triage.<br />
- Assigns the ticket to <strong>Jane Doe</strong> and assigns the department to <strong>SysAdmins</strong>.<br /><br />
logs out as john.
</p>
<br />

<h4>Stage 4: Resolution (as Jane)</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Online Banking Down"/>
</p>
<p>
log  in as jane and works the ticket to completion. She investigates and discovers that the online banking system backend server was accidentally restarted during business hours due to a configuration issue. Jane posts a reply stating that she will check the settings and attempt a restart. After successfully restarting the server, she posts another reply confirming that online banking appears to be back up. Jane contacts Karen directly to confirm full functionality. Once confirmed, Jane updates the ticket status to <strong>"Resolved"</strong>, notifies the end user, and closes the ticket for archival.
</p>
<br />

---

<h3>Scenario 2: Adobe Software Not Working for Accounting Department (Sev‑B)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Intake - Adobe Software Issue"/>
</p>
<p>
As an end user, submit a new ticket with the issue: <strong>"Accounting department needs Adobe upgrade — broken."</strong> This affects an entire department and requires prompt attention.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Assignment - Adobe Software Issue"/>
</p>
<p>
Log in as agent <strong>John</strong>. Observe the ticket's default properties, then set the following:<br /><br />
- <strong>SLA:</strong> Sev-B (4 hours, 24/7)<br />
- <strong>Department:</strong> Support<br /><br />
John acknowledges the issue and notifies the end user that work has begun.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Working the Issue - Adobe Software Issue"/>
</p>
<p>
John troubleshoots by checking license status, reinstalling the application, and verifying network access to Adobe's licensing servers. All steps are documented in the ticket thread, and John posts regular updates to the accounting department.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Adobe Software Issue"/>
</p>
<p>
After resolving the licensing conflict and restoring Adobe functionality, John updates the ticket with a full resolution summary, changes the status to <strong>"Resolved"</strong>, and closes the ticket.
</p>
<br />

---

<h3>Scenario 3: CFO’s Laptop Will No Longer Turn On (Sev‑B)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Intake - CFO Laptop"/>
</p>
<p>
As an end user, submit a new ticket with the issue: <strong>"CFO’s laptop will no longer turn on."</strong> This is a high‑visibility executive request that must be prioritized.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Assignment - CFO Laptop"/>
</p>
<p>
Log in as agent <strong>John</strong>. Observe the default properties, then set:<br /><br />
- <strong>SLA:</strong> Sev-B (4 hours, 24/7)<br />
- <strong>Department:</strong> Support<br /><br />
John replies to confirm receipt and assures the CFO that a technician will investigate immediately.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/KdQB8Xz.png" height="80%" width="80%" alt="Working the Issue - CFO Laptop"/>
</p>
<p>
John checks the power adapter, battery, and motherboard. He swaps the laptop with a loaner device to restore the CFO’s productivity while the original unit is diagnosed. All actions are logged in the ticket thread.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - CFO Laptop"/>
</p>
<p>
The laptop is repaired (or replaced), and the CFO confirms it is fully operational. John changes the status to <strong>"Resolved"</strong>, documents the fix, and closes the ticket.
</p>
<br />

---

<p>
<strong>Technical Skill Pillar:</strong> Mastering osTicket's permission model, SLA management, and ticketing workflows is a foundational skill for any IT support professional. The more you practice, the more natural these processes become. Good luck!
</p>
<br />
