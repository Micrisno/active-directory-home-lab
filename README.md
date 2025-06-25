🧪 Active Directory Home Lab with VirtualBox & PowerShell

This project simulates a real-world Windows IT environment using a local home lab. The setup includes a Windows Server 2019 domain controller and a Windows 10 client machine, running inside Oracle VirtualBox. PowerShell is used to automate user creation in Active Directory.

Inspired by [Josh Madakor's tutorial](https://www.youtube.com/watch?v=uq7zjBodZ5I), this lab provides hands-on experience with AD, networking, and system administration.

🧰 Tools & Technologies Used

- Oracle VirtualBox (free virtualization tool)
- Windows Server 2019 (180-day evaluation)
- Windows 10 (unactivated version)
- PowerShell scripting
- Active Directory Domain Services (AD DS)
- DNS / DHCP configuration (brief)
- Internal networking in VirtualBox

🏗️ Lab Architecture

| Component       | Description                            |
|----------------|----------------------------------------|
| Domain Controller | Windows Server 2019, AD DS, DNS installed |
| Client Machine  | Windows 10, joined to AD domain        |
| Network Mode    | Internal Network (VirtualBox)          |
| Domain Name     | `example.internal`     |

🔧 Setup Process (Overview)

1. **Installed Oracle VirtualBox**
2. **Created two VMs**:
   - Server 2019 (configured as Domain Controller)
   - Windows 10 (client)
3. Promoted Server 2019 to **Domain Controller** using AD DS
4. Created a custom OU in Active Directory
5. Wrote and executed a **PowerShell script** to add multiple users
6. Joined the Windows 10 VM to the domain
7. Successfully logged in as a created domain user

💻 PowerShell Script Sample

You can find the full script in `/powershell-scripts/add-users.ps1`.

```powershell
# PowerShell script to add multiple users to Active Directory
Import-Module ActiveDirectory

for ($i = 1; $i -le 10; $i++) {
    $username = "user$i"
    $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
    New-ADUser -Name $username `
               -SamAccountName $username `
               -AccountPassword $password `
               -Enabled $true `
               -Path "OU=Users,DC=ad,DC=homelab,DC=local"
}
