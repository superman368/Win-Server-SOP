# SOP for Setting Up a Windows Server

**[MITT]**  
**[Winnipeg Big Street]**  
**[111-222-333]**

**Version:** 1.0  
**Written by:** [Ling Yang]  
**Approved by:** [Felix]  
**Date:** [01/01/2035]  

---

## Purpose
This SOP description is the step-by-step process for setting up a Windows Server to ensure high quality in deployment. It is intended for student for server management and deployment.

---

## Application
This document applies to Netword and System Administrator involved in setting up Windows Server environments.

---

## Definitions
- **Windows Server**: A Microsoft OS designed for server use.  
- **AD DS**: Active Directory Domain Services, a directory service for Windows networks.  
- **IP Address**: IP for network identification.  
- **DNS**: Domain Name System, responsible for resolving domain names to IP addresses.

---

## Procedure Steps

### **Step 1: Download Windows Server 2022 ISO**
1.1: Go to: https://www.microsoft.com/en-us/evalcenter \
1.1: Select “Download ISO”
### **Step 2: Creating the Virtual Machine (VM) in VMWare Workstation Pro**
1. In VMware Workstation “Home” tab, click “Create a New Virtual Machine”
2. If “Microsoft Windows” and “Windows Server 2022” are not selected, please change them so they do, then click “Next”
3. BEFORE selecting finish, click “Customize Hardware…”  
   - Memory: 4 GB
   - Processors: 1 processor * 2 cores
   - Hard Disk 1: 60 GB ; Notes: NVMe
   - Network Adapter: NAT
4. Review your new configurations and if everything is as it should be, click “Finish”.
### **Step 3: Initial install and configuration of Windows Server**
1. You will now see a new vm tab. Click “Power on the virtual machine".
2. Log in using the Administrator account.
3. Set up the network configuration:
   - Assign a static IP address.
   - Configure the DNS settings.
4. Once you have completed your Windows Server installation, the aspect ratio isn’t optimal, as other virtual tools are missing.
### **Step 4: Promote the Server to a Domain Controller**
1. Open the Server Manager dashboard.
2. Click **"Add roles and features"** and follow the wizard:
   - Select **"Active Directory Domain Services" (AD DS)** and install.
3. After installation, promote the server to a domain controller:
   - Open the AD DS setup wizard.
   - Choose to create a new domain in a new forest or add to an existing domain.
   - Configure domain name and NetBIOS name.
4. Complete the wizard and restart the server.
### **Step 5: Install and Configure Additional Roles**
1. Use Server Manager to add necessary roles, such as:
   - **DHCP** for automatic IP address assignment.
2. Follow role-specific configurations based on organizational needs.

---

## Resources
- [Microsoft Documentation: Windows Server Installation Guide](https://docs.microsoft.com/en-us/windows-server/)  
