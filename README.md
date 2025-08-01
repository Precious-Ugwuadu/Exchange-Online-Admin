# Exchange-Online-Admin
<p align="center">
<img width="817" height="371" alt="image" src="https://github.com/user-attachments/assets/23d01c92-e3d7-44ff-89d5-dea607781ff0" />
/>
</p>

<h1>- Microsoft 365 Administration Lab Environment</h1>
This tutorial outlines Exchange Online and Mailbox Management, Identity & Access Management, PowerShell Automation, Security, Compliance & eDiscovery, Mailbox Migration and User Setup<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to create, work, and resolves tickets within osTicket](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft 365 Admin Center, Exchange Admin Center
- Microsoft Entra Admin Center (formerly Azure AD)
- Windows PowerShell / Azure Cloud Shell
- Microsoft Purview Compliance Portal
   

<h2>Operating Systems Used </h2>

- Windows 11</b> (21H2)

<h2>Requirements</h2>

- Microsoft 365 Developer/Education Tenant (E5 trial or developer program)
- Admin Access to Microsoft 365 portal
- Windows 10/11 PC or VM
- PowerShell v5+ / Windows Terminal
- Internet Connection
- Modern browser (Edge/Chrome)
- Microsoft 365 Apps installed (Outlook, Teams, etc. – optional but useful)
- Azure Cloud Shell (Optional) for cloud-based scripting
- User Scenarios (create 2–3 test users with roles)

<h2>1. Exchange Online and Mailbox Management </h2>

Goal: Learn to manage mailboxes, distribution groups, and email policies in Exchange Online.

Requirements:

- Microsoft 365 tenant with Exchange Online plan

- Admin account

- PowerShell access

Steps:

a.  SET UP EXCHANGE ONLINE IN YOUR MICROSOFT 365 ADMIN CENTER.

  Steps:

- Go to https://admin.microsoft.com and sign in with your Global Admin account.

  <img width="1343" height="679" alt="image" src="https://github.com/user-attachments/assets/8f7c74ed-8e1b-44a7-b217-9d34e0b55972" />

- Navigate to Admin centers > Exchange.

  <img width="1306" height="640" alt="image" src="https://github.com/user-attachments/assets/e45f254b-fbda-47ad-a8c3-72e13aa6e2ea" />

- In the Exchange Admin Center (EAC), you can now manage mailboxes, groups, policies, etc.
- Make sure licenses (e.g., Microsoft 365 E3/E5) are assigned to users so they can access Exchange Online.



b.  CREATE SHARED AND USER MAILBOXES.

Configure mailbox permissions (Full Access, Send As).

Set mailbox limits and retention policies.

Use PowerShell to automate mailbox creation.

Configure email forwarding, mailbox delegation, and rules.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.

  2. Microsoft 365 Identity & Access Management Lab
Goal: Manage users, groups, roles, and conditional access in Microsoft 365.

Requirements:

Microsoft 365 tenant with Azure AD access

Global Administrator privileges

Steps:

Create and manage users and security groups in Azure AD.

Assign and manage admin roles using Role-Based Access Control (RBAC).

Configure Conditional Access policies for sign-ins.

Set up multi-factor authentication (MFA).

Monitor sign-in activity and access logs.

3. PowerShell Automation for Microsoft 365 Administration
Goal: Automate tasks like user creation, license assignment, and reporting.

Requirements:

PowerShell 7 or Windows PowerShell

Microsoft Graph & Exchange Online modules installed

Steps:

Connect to Microsoft 365 via PowerShell:

powershell
Copy
Edit
Connect-ExchangeOnline
Connect-MgGraph
Automate:

Bulk user creation using a CSV

Assigning licenses with Set-MsolUserLicense

Creating mailboxes or distribution groups

Generate reports (e.g., inactive users, mailbox sizes)

4. Microsoft 365 Security, Compliance & eDiscovery Lab
Goal: Implement compliance policies and conduct eDiscovery.

Requirements:

Compliance center access (Microsoft 365 E3 or above)

Compliance admin role

Steps:

Enable audit logging in the Compliance Center.

Create and apply DLP (Data Loss Prevention) policies.

Set up retention policies and labels.

Configure litigation hold on mailboxes.

Perform content search and eDiscovery.

5. Microsoft 365 Mailbox Migration and User Setup Lab
Goal: Migrate users from on-premises Exchange or PST to Exchange Online.

Requirements:

Exchange Online license

Migration endpoint if from on-prem

PST files if doing import

Steps:

Prepare users in Azure AD or sync with AD Connect (if hybrid).

Use Exchange Admin Center or PowerShell for migration:

Cutover, staged, or hybrid migration for on-prem

PST import via Microsoft’s network upload tool

Assign licenses and verify mailbox health.

Redirect DNS records (MX, Autodiscover).
</p>
<br />
