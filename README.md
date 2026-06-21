<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket — Ticket Lifecycle: Intake Through Resolution</h1>

<p align="center">
This lab demonstrates the full lifecycle of a help desk ticket — from end-user submission through triage, escalation, and resolution — using the open-source ticketing system <b>osTicket</b>.
</p>

---

<h2>🖥️ Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines / Compute)
- Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)
- osTicket v1.15.8

<h2>🪟 Operating Systems Used</h2>

- Windows 11 Pro, version 25H2 (Azure VM)

<h2>🔄 Ticket Lifecycle Stages</h2>

| Stage | Description |
|---|---|
| **1. Intake** | End user submits a ticket via the support portal |
| **2. Assignment & Communication** | Agent reviews, triages, and sets priority/SLA |
| **3. Working the Issue** | Agent investigates, escalates, and documents progress |
| **4. Resolution** | Issue is resolved, ticket is closed and archived |

<h2>🔗 Lab Access URLs</h2>

| Portal | URL |
|---|---|
| **Admin / Agent Login** | `http://localhost/osTicket/scp/login.php` |
| **End-User Portal** | `http://localhost/osTicket` |

---

<h2>⚙️ Pre-Lab Setup (Admin Panel)</h2>

Before creating tickets, complete the following administrative configuration:

1. Navigate to **Admin Panel → Departments**
2. **Delete** the **Maintenance** department (do not archive — delete permanently)
3. Locate the **SysAdmins** department → set it to **"Top Level Department"**

> 💡 Setting SysAdmins as a Top Level Department restricts ticket visibility — only agents explicitly granted access can view tickets assigned to that department. This is intentional for the permission-restriction exercise in Scenario 1.

---

<h2>📂 Scenario 1 — Entire Mobile/Online Banking System Is Down</h2>
<p><b>Severity: A &nbsp;|&nbsp; SLA: 1 Hour, 24/7 &nbsp;|&nbsp; Priority: Emergency</b></p>

<h3>Stage 1 — Intake</h3>
<p>
<img src="https://i.imgur.com/wbqlkDs.png" height="80%" width="80%" alt="Karen submits banking outage ticket"/>
</p>
<p>
End user <b>Karen</b> navigates to the osTicket portal at <code>http://localhost/osTicket</code> and submits a new ticket. She selects <b>Help Topic: Report a Problem / Business Critical Outage</b> and describes the issue: <em>"When I returned from lunch, I discovered that the entire mobile app seems to be down. I tried logging in multiple times but couldn't access my account, and none of my tellers can log in either. This is completely blocking all our branch operations, and we need immediate assistance."</em>
</p>
<br />

<h3>Stage 2 — Assignment & Initial Triage (Permission Block Demonstration)</h3>
<p>
<img src="https://i.imgur.com/Ri5F0Hl.png" height="80%" width="80%" alt="John views ticket with default settings and limited access"/>
</p>
<p>
Agent <b>John Doe</b> logs into the staff panel and opens the newly created ticket. He observes its default properties upon intake:<br /><br />
&nbsp;&nbsp;• <b>Priority:</b> Normal<br />
&nbsp;&nbsp;• <b>Department:</b> Support<br />
&nbsp;&nbsp;• <b>SLA Plan:</b> Default SLA<br />
&nbsp;&nbsp;• <b>Assigned To:</b> Unassigned<br /><br />
John posts an internal note confirming he is testing access with <b>"Read Only"</b> permissions, then attempts to update the ticket with the correct critical settings — <b>SLA: Sev-A</b> and <b>Department: SysAdmins</b>. After saving and logging back in, the ticket completely disappears from his view. Because SysAdmins is a Top Level Department and John only has default access, he is now locked out of the ticket entirely.
</p>
<br />

<h3>Stage 3 — Permission Grant & Advanced Triage</h3>
<p>
<img src="https://i.imgur.com/KdQB8Xz.png" height="80%" width="80%" alt="Admin grants John All Access permissions"/>
</p>
<p>
An <b>Admin</b> logs into the Admin Panel, navigates to <b>Agents → John Doe → Access</b>, and upgrades his role to <b>"All Access"</b>. John logs out and back in. With visibility restored, John immediately performs a full triage:<br /><br />
&nbsp;&nbsp;• Updates <b>Priority</b> to <b>Emergency</b><br />
&nbsp;&nbsp;• Calls <b>Karen</b> to confirm all teller systems are down<br />
&nbsp;&nbsp;• Sets <b>SLA Plan</b> to <b>Sev-A (1 hour, 24/7)</b><br />
&nbsp;&nbsp;• Changes <b>Help Topic</b> to <b>Business Critical Outage</b><br />
&nbsp;&nbsp;• Posts an internal note: <em>"Entire business system is offline."</em><br />
&nbsp;&nbsp;• Assigns the ticket to <b>Jane Doe</b> and transfers the department to <b>SysAdmins</b><br />
&nbsp;&nbsp;• Posts a public reply to Karen acknowledging the escalation<br /><br />
John logs out after completing triage.
</p>
<br />

<h3>Stage 4 — Resolution</h3>
<p>
<img src="https://i.imgur.com/beMfRBY.png" height="80%" width="80%" alt="Jane resolves the banking outage ticket"/>
</p>
<p>
<b>Jane Doe</b> logs in and works the ticket to completion. Her investigation reveals that the online banking backend server was accidentally restarted during business hours due to a configuration change. Jane posts a reply informing the team she is checking settings and attempting a restart. After the restart succeeds, she posts a follow-up confirming the banking system is back online. Jane contacts <b>Karen</b> directly to verify full functionality across all teller stations. Once confirmed, she changes the ticket status to <b>Resolved</b> and closes it for archival. The ticket now shows: <b>Status: Resolved | Closed By: Jane Doe | SLA: Sev-A</b>.
</p>
<br />

---

<h2>📂 Scenario 2 — Adobe Reader Not Working for Accounting Department</h2>
<p><b>Severity: B &nbsp;|&nbsp; SLA: 4 Hours, 24/7 &nbsp;|&nbsp; Priority: High</b></p>

<h3>Stage 1 — Intake</h3>
<p>
<img src="https://i.imgur.com/Dp0HNEV.png" height="80%" width="80%" alt="Ken submits Adobe Reader ticket"/>
</p>
<p>
End user <b>Ken</b> navigates to the osTicket portal and opens a new ticket. He selects <b>Help Topic: Report a Problem / Personal Computer Issues</b> and submits the following: <em>"Some people in the accounting department can't use Adobe Reader."</em> The issue summary reads: <b>"Adobe Reader not working."</b>
</p>
<br />

<h3>Stage 2 — Assignment & Communication</h3>
<p>
<img src="https://i.imgur.com/1cjdLvt.png" height="80%" width="80%" alt="John triages Adobe Reader ticket and posts update"/>
</p>
<p>
Agent <b>John Doe</b> opens the ticket and reviews its default properties. He updates the ticket with the following:<br /><br />
&nbsp;&nbsp;• <b>Priority:</b> High<br />
&nbsp;&nbsp;• <b>SLA Plan:</b> Sev-B (4 hours, 24/7) — escalated due to an active internal audit requiring Adobe Reader access<br />
&nbsp;&nbsp;• <b>Department:</b> Support<br /><br />
John calls <b>Ken</b> for additional details and posts the following reply in the ticket thread: <em>"Called Ken to get more details on the incident. 10 out of 12 people cannot even open Adobe Reader — very important because an internal audit is currently happening. When double-clicking the icon, it just hangs and nothing happens. Going to investigate what has changed recently."</em>
</p>
<br />

<h3>Stage 3 — Working the Issue</h3>
<p>
<img src="https://i.imgur.com/r1nfvjF.png" height="80%" width="80%" alt="John documents root cause and fix in ticket thread"/>
</p>
<p>
John contacts <b>Josh</b> from the Desktop Admins group. Together they identify that the issue was caused by a new Adobe Reader package that was pushed out overnight. The fix is either to: (1) wait approximately 1 hour for the corrected package to auto-deploy, or (2) have end users manually install the new package directly from the <b>Software Catalog</b>. John documents the root cause and both resolution paths in the ticket thread, and posts a status update to the accounting department keeping them informed while the fix is being applied.
</p>
<br />

<h3>Stage 4 — Resolution</h3>
<p>
<img src="https://i.imgur.com/slSasUg.png" height="80%" width="80%" alt="John closes Adobe Reader ticket after resolution confirmed"/>
</p>
<p>
<b>Ken</b> confirms that the Software Catalog installation worked and that all affected users in the accounting department are back up and running. John updates the ticket thread with a full resolution summary: <em>"Root cause analysis complete. Solution successfully delivered."</em> He changes the ticket status to <b>Closed</b> and submits the closure. The ticket is archived with complete documentation of the issue, triage steps, root cause, and resolution.
</p>
<br />
