# Azure VM + osTicket Help Desk Deployment

## 📌 Project Overview

This project demonstrates the deployment of a fully functional help desk ticketing system using Microsoft Azure. A Windows-based virtual machine was configured with IIS, PHP, and MySQL to host osTicket, an open-source support ticketing system.

The goal of this lab was to simulate a real-world IT support environment, including system setup, web server configuration, database integration, and ticket lifecycle management.

---

## 🏗️ Architecture Overview

**Environment Components:**
- Microsoft Azure Virtual Machine (Windows 10)
- Internet Information Services (IIS)
- PHP 7.3
- MySQL 5.5
- osTicket v1.15.8

---

## ⚙️ Skills Demonstrated

- Azure Virtual Machine deployment and configuration
- Windows Server remote administration (RDP)
- IIS web server installation and configuration
- PHP integration with IIS
- MySQL database setup and management
- Web application deployment
- File system permissions and security configuration
- Troubleshooting missing PHP extensions
- IT help desk workflow simulation (ticket lifecycle, SLAs, escalation)

---

## 🚀 Implementation Steps

### 1. Azure Virtual Machine Setup
- Created a Windows 10 VM in Microsoft Azure
- Configured Remote Desktop access

### 2. Web Server Configuration (IIS)
- Installed IIS with CGI support
- Enabled required application development features
- Installed PHP Manager and URL Rewrite Module
- Registered PHP with IIS

### 3. PHP & MySQL Installation
- Installed PHP 7.3 and configured `C:\PHP`
- Installed Visual C++ Redistributable
- Installed MySQL Server 5.5 and configured root credentials

### 4. osTicket Deployment
- Extracted osTicket files into IIS root directory
- Renamed and configured application folder
- Enabled required PHP extensions:
  - `php_imap.dll`
  - `php_intl.dll`
  - `php_opcache.dll`

### 5. Database Configuration
- Created `osTicket` database using HeidiSQL
- Connected application to MySQL backend

### 6. Final Configuration
- Completed web-based osTicket setup wizard
- Configured system settings and admin account
- Removed setup directory for security
- Set proper file permissions on configuration files

---

## 🎫 Ticket Lifecycle Simulation

This lab included hands-on simulation of real-world IT support workflows.

### Example Scenarios:

#### 🔴 Sev-A Incident (Critical Outage)
- Issue: Entire mobile/online banking system down
- Priority: Sev-A (1-hour SLA, 24/7 support)
- Routed to: SysAdmins department
- Outcome: Ticket escalated and access controlled based on role permissions
<img width="958" height="944" alt="osticket1 1" src="https://github.com/user-attachments/assets/fc2fdac8-6b4c-472a-b33a-67ac638374d2" />
<img width="965" height="782" alt="osticket1 2" src="https://github.com/user-attachments/assets/a97cc93d-b4a0-4987-8072-74faea81f65c" />


#### 🟡 Sev-B Service Request
- Issue: Adobe upgrade failure in Accounting department
- Priority: Sev-B (4-hour SLA)
- Routed to: Support team
- Outcome: Resolved within SLA timeframe

#### 🟠 Hardware Failure Case
- Issue: CFO laptop not powering on
- Priority: Sev-B
- Outcome: Diagnosed and resolved via support workflow

---

## 🔐 Security Considerations

- Removed setup directory after installation
- Restricted access to configuration file (`ost-config.php`)
- Applied correct NTFS permissions for web application security
- Avoided storing plaintext credentials in production environments

---

## 📚 Key Learnings

- Multi-tier application architecture (Web Server + Application + Database)
- Importance of proper service configuration and dependency management
- Real-world help desk workflows and ticket prioritization
- SLA-based incident management and escalation procedures
- Role-based access control in IT systems

---

## 🧠 Improvements & Next Steps

- Automate deployment using PowerShell or Terraform
- Implement Azure Active Directory integration
- Upgrade to a Linux-based production environment
- Add email piping for automated ticket creation
- Introduce monitoring and logging (e.g., Azure Monitor)

---

## 📸 Screenshots

> Add screenshots here to demonstrate your setup:

- Azure VM dashboard
- IIS configuration
- osTicket login page
- Ticket lifecycle examples
- SLA assignment view

---

## 📌 Author Notes

This project was built as part of a hands-on IT support and systems administration lab to simulate real-world help desk environments and infrastructure configuration.
