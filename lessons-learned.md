🧠 Lessons Learned – Active Directory Home Lab Project

Completing this lab project provided valuable, hands-on experience with real-world IT concepts and technical skills. Below is a summary of key takeaways and personal insights gained throughout the setup process.

 🖥️ Virtualization & Lab Design
- Learned how to set up multiple virtual machines using Oracle VirtualBox.
- Gained practical experience configuring VM resources and network adapters for isolated lab environments.
- Understood the use of **Internal Network mode** to allow VM-to-VM communication while keeping the lab isolated from the host machine.

🛡️ Active Directory Domain Services (AD DS)
- Successfully installed and configured Active Directory on a Windows Server 2019 machine.
- Understood the concept of domain controllers, forests, domains, and organizational units (OUs).
- Practiced promoting a Windows Server to a domain controller with a custom domain (`mydomain.com`).

💻 PowerShell Scripting
- Gained experience writing and running PowerShell scripts to automate user creation in Active Directory.
- Learned how to use `New-ADUser`, `ConvertTo-SecureString`, and loop logic to generate multiple users efficiently.
- Realized the importance of automation in managing large-scale environments.

🔗 Domain Join & Network Troubleshooting
- Understood how DNS plays a role in joining a client machine to a domain.
- Practiced configuring a client’s network settings to point to the domain controller’s IP address.
- Resolved common domain join issues (e.g., connectivity, DNS mismatch).

🔍 Validation & Testing
- Used tools like `whoami`, `ping`, and Windows login prompts to validate successful domain integration.
- Confirmed that domain users could log in to the client machine.
- Validated the AD user creation through the ADUC console and PowerShell output.

🧠 General IT and Cybersecurity Insights
- This lab reinforced core IT administration concepts such as domain management, directory services, and user provisioning.
- Improved confidence in setting up isolated test environments, which are essential for safe cybersecurity experimentation.
- Strengthened foundational skills that align with the CompTIA Security+ and Google Cybersecurity Certificate competencies.

🚀 Next Steps (For the future)
- Explore group policies (GPOs) to manage client behavior from the domain controller.
- Implement login auditing via Event Viewer.
- Simulate basic cyber attack scenarios (e.g., failed login attempts, brute force) in a safe environment.
- Try integrating a Kali Linux VM to practice basic red team activities against the Windows environment.
