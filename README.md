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

<h2>Lifecycle Stages</h2>

---

<h3>Scenario 1: Entire Mobile/Online Banking System Is Down (Sev-A)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/wbqlkDs.png" height="80%" width="80%" alt="Ticket Intake - Online Banking Down"/>
</p>
<p>
End user <strong>Karen</strong> navigates to the osTicket end-user portal at <code>http://localhost/osTicket</code> and submits a new ticket. She selects the Help Topic <strong>"Business Critical Outage"</strong> and describes the issue: the entire online banking system is down and customers are unable to access their accounts. This ticket is flagged as high urgency due to its broad impact on business operations.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Assignment - Online Banking Down"/>
</p>
<p>
Agent <strong>Jane</strong> (SysAdmins) logs into the Admin/Analyst portal at <code>http://localhost/osTicket/scp/login.php</code> and reviews the open ticket. The ticket is assigned <strong>Sev-A</strong> SLA (1-hour grace period, 24/7 schedule) due to its critical nature. Jane assigns the ticket to herself and the <strong>Online Banking</strong> team. An internal note is added and the user is notified that the issue is being investigated with top priority.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Working the Issue - Online Banking Down"/>
</p>
<p>
Jane works to diagnose and resolve the outage. She updates the ticket thread with progress notes and communicates with the end user throughout the process. The ticket status is updated to <strong>"Open"</strong> while the investigation is active. All actions taken are documented within the ticket to maintain a clear record of the resolution process.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Online Banking Down"/>
</p>
<p>
Once the banking system is restored, Jane updates the ticket with a resolution summary and changes the ticket status to <strong>"Resolved"</strong>. The end user Karen is notified that the issue has been fixed and service has been restored. The ticket is then closed and archived for future reference.
</p>
<br />

---

<h3>Scenario 2: Adobe Software Not Working for Accounting Department (Sev-B)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Intake - Adobe Software Issue"/>
</p>
<p>
End user <strong>Ken</strong> submits a ticket through the end-user portal reporting that Adobe software has stopped working for the entire accounting department, preventing them from completing daily reports. He selects the Help Topic <strong>"Personal Computer Issues"</strong> and provides details about the software, error messages, and affected machines.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Assignment - Adobe Software Issue"/>
</p>
<p>
Agent <strong>John</strong> (Support) picks up the ticket and assigns it <strong>Sev-B</strong> SLA (4-hour grace period, 24/7 schedule) based on the departmental impact. John responds to Ken acknowledging the issue and letting him know it is being actively worked on. The ticket is assigned to the Support department and marked as in progress.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Working the Issue - Adobe Software Issue"/>
</p>
<p>
John troubleshoots the Adobe software issue by checking license status, reinstalling the application on affected machines, and verifying network access to Adobe's licensing servers. All steps are documented in the ticket thread. John communicates updates to Ken throughout the process to keep the accounting department informed.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Adobe Software Issue"/>
</p>
<p>
After resolving the licensing conflict and restoring Adobe functionality across all accounting machines, John updates the ticket with a full resolution summary. The ticket status is changed to <strong>"Resolved"</strong> and Ken is notified. The ticket is closed with documentation of the root cause and fix for future reference.
</p>
<br />

---

<h3>Scenario 3: Password Reset Request (Sev-C)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Intake - Password Reset"/>
</p>
<p>
End user <strong>Karen</strong> submits a ticket requesting a password reset for her account. She selects the Help Topic <strong>"Password Reset"</strong> and provides her username and department information. This is a routine, low-priority request that does not impact business operations.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Assignment - Password Reset"/>
</p>
<p>
Agent <strong>John</strong> (Support) reviews the ticket and assigns it <strong>Sev-C</strong> SLA (8-hour grace period, Business Hours). Since this is a standard request, it is handled during normal business hours. John replies to Karen confirming receipt of the request and lets her know the reset will be completed shortly.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Working the Issue - Password Reset"/>
</p>
<p>
John verifies Karen's identity using standard procedures and resets her password through the appropriate system. A temporary password is generated and securely communicated to Karen with instructions to change it upon her next login. The action is logged in the ticket thread.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Password Reset"/>
</p>
<p>
Karen confirms she has successfully logged in with the new credentials. John updates the ticket status to <strong>"Resolved"</strong> and closes the ticket. The full interaction is documented, including identity verification steps and the resolution outcome, ensuring a complete audit trail for compliance purposes.
</p>
<br />
