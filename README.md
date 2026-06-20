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
As an end user, navigate to the osTicket portal at <code>http://localhost/osTicket</code> and submit a new ticket with the issue: <strong>"Entire mobile/online banking system is down."</strong> This represents a critical outage affecting all customers. Log out and log back in as Help Desk Agent <strong>John</strong> at <code>http://localhost/osTicket/scp/login.php</code> to begin working the ticket.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/Ri5F0Hl.png height="80%" width="80%" alt="Ticket Assignment - Online Banking Down"/>
</p>
<p>
As agent <strong>John</strong>, observe the ticket's default properties — Priority, Department, SLA, and Assigned To. Then set the following properties on the ticket:<br /><br />
- <strong>SLA:</strong> Sev-A (1 hour, 24/7)<br />
- <strong>Department:</strong> Online Banking (SysAdmins)<br /><br />
After saving, attempt to view or change the ticket again as John. Because SysAdmins is a top-level department and John does not have access to change anything because its view pnly, the ticket is <strong></strong> from his agent panel.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Working the Issue - Online Banking Down"/>
</p>
<p>
Log in as <strong>Jane</strong> (SysAdmins department). Jane has full access to the escalated ticket and works it to completion. She investigates the banking system outage, documents all troubleshooting steps in the ticket thread, and communicates updates to the end user throughout the process. The ticket status remains <strong>"Open"</strong> while the investigation is active.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Online Banking Down"/>
</p>
<p>
Once the banking system is restored, Jane updates the ticket with a resolution summary and changes the ticket status to <strong>"Resolved"</strong>. The end user is notified that the issue has been fixed and service has been restored. The ticket is then closed and archived for future reference.
</p>
<br />

---

<h3>Scenario 2: Adobe Software Not Working for Accounting Department (Sev-B)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Intake - Adobe Software Issue"/>
</p>
<p>
As an end user, navigate to <code>http://localhost/osTicket</code> and submit a new ticket with the issue: <strong>"Accounting department needs Adobe upgrade — broken."</strong> This affects an entire department and must be treated as a high-priority request. Log back in as agent <strong>John</strong> to begin working the ticket.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Assignment - Adobe Software Issue"/>
</p>
<p>
As agent <strong>John</strong>, observe the ticket's default properties — Priority, Department, SLA, and Assigned To. Then set the following properties:<br /><br />
- <strong>SLA:</strong> Sev-B (4 hours, 24/7)<br />
- <strong>Department:</strong> Support<br /><br />
John acknowledges the issue and notifies the end user that it is being actively worked on.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Working the Issue - Adobe Software Issue"/>
</p>
<p>
John troubleshoots the Adobe software issue by checking license status, reinstalling the application on affected machines, and verifying network access to Adobe's licensing servers. All steps are documented in the ticket thread. John communicates updates to the end user throughout the process to keep the accounting department informed.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Adobe Software Issue"/>
</p>
<p>
After resolving the licensing conflict and restoring Adobe functionality across all accounting machines, John updates the ticket with a full resolution summary. The ticket status is changed to <strong>"Resolved"</strong> and the end user is notified. The ticket is closed with documentation of the root cause and fix for future reference.
</p>
<br />

---

<h3>Scenario 3: Password Reset Request (Sev-C)</h3>

<h4>Stage 1: Intake</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Intake - Password Reset"/>
</p>
<p>
As an end user, navigate to <code>http://localhost/osTicket</code> and submit a new ticket requesting a password reset. Select the Help Topic <strong>"Password Reset"</strong> and provide the username and department information. This is a routine, low-priority request that does not impact business operations. Log back in as agent <strong>John</strong> to work the ticket.
</p>
<br />

<h4>Stage 2: Assignment and Communication</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Ticket Assignment - Password Reset"/>
</p>
<p>
As agent <strong>John</strong>, observe the ticket's default properties — Priority, Department, SLA, and Assigned To. Then set the following properties:<br /><br />
- <strong>SLA:</strong> Sev-C (8 hours, Business Hours)<br />
- <strong>Department:</strong> Support<br /><br />
John replies to the end user confirming receipt of the request and lets them know the reset will be completed shortly.
</p>
<br />

<h4>Stage 3: Working the Issue</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Working the Issue - Password Reset"/>
</p>
<p>
John verifies the end user's identity using standard procedures and resets the password through the appropriate system. A temporary password is generated and securely communicated with instructions to change it upon next login. The action is logged in the ticket thread.
</p>
<br />

<h4>Stage 4: Resolution</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Resolution - Password Reset"/>
</p>
<p>
The end user confirms they have successfully logged in with the new credentials. John updates the ticket status to <strong>"Resolved"</strong> and closes the ticket. The full interaction is documented, including identity verification steps and the resolution outcome, ensuring a complete audit trail for compliance purposes.
</p>
<br />
