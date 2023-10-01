# Windows-Active-Directory-and-VM-User-Management-Project


```markdown
## Setting Up Active Directory in Windows Server

In this section, we'll guide you through the process of setting up an Active Directory domain in a Windows Server environment. Active Directory is a crucial component for centralized user management, authentication, and access control.

### Step 1: Install Windows Server

Install Windows Server on a dedicated machine, ensuring it meets the system requirements. You can use the following PowerShell command to install the Active Directory Domain Services (AD DS) role:

```powershell
Install-WindowsFeature -Name AD-Domain-Services -IncludeManagementTools
```

### Step 2: Promote the Server to a Domain Controller

Promote the Windows Server to a domain controller by running the following PowerShell command:

```powershell
Install-ADDSForest -DomainName yourdomain.local -DomainMode 7 -ForestMode 7 -InstallDns
```

Replace `yourdomain.local` with your preferred domain name and adjust the domain and forest modes as needed.

### Step 3: Configure Active Directory

After promotion, configure Active Directory, including creating organizational units (OUs), adding users, and setting group policies according to your organization's requirements.

### Step 4: Add Users in Windows 10

Now, let's add Windows 10 machines to the domain and create user accounts:

1. Install Windows 10 in a virtual machine (VM) environment.

2. In Windows 10, navigate to "Settings" > "Accounts" > "Access work or school."

3. Click "Connect" and follow the prompts to join the Windows 10 machine to the Active Directory domain.

4. Once joined, log in to the Windows 10 machine with domain administrator credentials.

5. In Active Directory Users and Computers (ADUC), create user accounts for Windows 10 users in specific OUs.

6. On the Windows 10 machine, use the newly created user accounts to log in, and they will have access to resources based on group policies and permissions.

Your Windows Server is now serving as an Active Directory domain controller, and Windows 10 machines are connected to the domain, allowing you to manage users and resources centrally.
```
