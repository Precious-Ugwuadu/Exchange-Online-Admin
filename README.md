# Exchange-Online-Admin
<p align="center">
<img width="817" height="371" alt="image" src="https://github.com/user-attachments/assets/23d01c92-e3d7-44ff-89d5-dea607781ff0" />

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

  👤 HOW TO CREATE A SINGLE USER
✅ Steps:
Sign in to Microsoft 365 Admin Center with your Global Admin or User Admin account.

In the left-hand menu, click Users > Active users.

<img width="1316" height="651" alt="image" src="https://github.com/user-attachments/assets/c43a45d8-a65b-45d0-8653-4c15082f110c" />

Click “Add a user”.

<img width="1092" height="572" alt="image" src="https://github.com/user-attachments/assets/345c831b-6d0e-4e71-a6e5-a5c6ef3f3270" />

Fill in user details: First name, last name, Username (e.g., jane.doe@yourdomain.com)

<img width="990" height="578" alt="image" src="https://github.com/user-attachments/assets/d826ad5f-82cd-4603-862b-17f7f031a18e" />

Assign product license: Choose the Microsoft 365 license (e.g., Microsoft 365 Business Standard, E3).

<img width="942" height="577" alt="image" src="https://github.com/user-attachments/assets/27abf5e3-cbf9-4734-95df-9c219842258b" />

<img width="1049" height="579" alt="image" src="https://github.com/user-attachments/assets/33c97834-6279-484f-ba9e-a01eccc54da2" />

Set password: Auto-generate or manually create a password.

Option to require password change on first sign-in.

Optional settings: Assign roles (e.g., User, Global admin)

<img width="1167" height="569" alt="image" src="https://github.com/user-attachments/assets/aa1b4d32-34dd-4a0d-a5c3-299da039c7b2" />

Set usage location (e.g., Canada)

Click “Finish adding” to create the user.

<img width="1164" height="618" alt="image" src="https://github.com/user-attachments/assets/abf605ac-549e-4c9b-bdb5-b6a4e1a296e0" />

<img width="927" height="610" alt="image" src="https://github.com/user-attachments/assets/5672391d-7a20-47c5-a67c-82e4799e1672" />

Copy/save the login credentials or send them via email.

👥 To Create Multiple Users at Once (Bulk Upload):

✅ Steps: In Admin Center

<img width="1138" height="639" alt="image" src="https://github.com/user-attachments/assets/0257a6be-b1c7-490e-9867-c9939bbf780a" />

go to Users > Active users.

<img width="1254" height="622" alt="image" src="https://github.com/user-attachments/assets/7922283d-5fbf-43e7-9d68-a7c738e31475" />

Click “Add multiple users” (next to “Add a user”).

<img width="1281" height="632" alt="image" src="https://github.com/user-attachments/assets/b38abe05-db2a-49f5-ba5e-07de76dd150a" />

<img width="1311" height="616" alt="image" src="https://github.com/user-attachments/assets/79b0bc3a-825c-4a70-9e3b-c55e23ac7fb6" />

Download the CSV template provided.

<img width="1270" height="632" alt="image" src="https://github.com/user-attachments/assets/18d9e93f-2e5e-4ec9-997d-4932df82d02d" />

Fill in user info in the CSV:

Username, First Name, Last Name, Display Name, Job Title, etc.

Make sure to follow the format exactly as given.

Upload the filled-in CSV file.

Assign licenses in bulk to the users.

<img width="1052" height="627" alt="image" src="https://github.com/user-attachments/assets/e315ad6a-b3cb-44fe-95bf-f4bc6266ef6b" />

Set default password preferences for all new users.

<img width="1220" height="625" alt="image" src="https://github.com/user-attachments/assets/b410c408-7f90-4c31-b669-15fe82316bd8" />

Click “Next” > “Finish adding”.

<img width="1332" height="617" alt="image" src="https://github.com/user-attachments/assets/5684c203-766c-4380-9724-2f5d9e393f0d" />

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

  <img width="1258" height="639" alt="image" src="https://github.com/user-attachments/assets/0ca04d9c-065d-4991-88b5-81a7502d1fb4" />

- In the Exchange Admin Center (EAC), you can now manage mailboxes, groups, policies, etc.
   Shared mailboxes are ideal when multiple people need to access one mailbox. A company can create a shared mailbox for their website or a department to help when someone wants to contact them or make an inquiry, and the people who have access to this mailbox can see it. Lots of firms use shared mailboxes
- Make sure licenses (e.g., Microsoft 365 E3/E5) are assigned to users so they can access Exchange Online.

b.  CREATE A SHARED MAILBOXES.

Go to Teams & groups > Shared mailboxes.

Click Add a shared mailbox.

Provide a name and email address.

Assign members to access it.


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
