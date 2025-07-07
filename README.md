# osTicket-Instillation-lab
# osTicket Installation Lab

## Course Information
- **Course**: [Your Course Name/Code]
- **Institution**: [Your Institution]
- **Semester**: [Current Semester/Year]
- **Assessment Type**: Practical Lab Assignment

## Project Overview
This project demonstrates the complete installation and configuration of osTicket, an open-source help desk ticketing system, on a Windows 10 virtual machine hosted in Microsoft Azure. The lab covers server setup, web server configuration, database installation, and application deployment.

## Learning Objectives
- Deploy and configure Azure Virtual Machines
- Install and configure Internet Information Services (IIS) with CGI
- Set up PHP runtime environment
- Install and configure MySQL database
- Deploy and configure osTicket help desk system
- Implement basic security configurations

## Technologies Used
- **Cloud Platform**: Microsoft Azure
- **Operating System**: Windows 10
- **Web Server**: Internet Information Services (IIS)
- **Runtime**: PHP 7.3.8
- **Database**: MySQL 5.5.62
- **Application**: osTicket v1.15.8
- **Database Management**: HeidiSQL

## Infrastructure Setup

### Azure Virtual Machine Specifications
- **Name**: osticket-vm
- **OS**: Windows 10
- **vCPUs**: 4
- **Access**: Remote Desktop Protocol (RDP)
- **Credentials**: 
  - Username: labuser
  - Password: osTicketPassword1!

## Installation Process

### Phase 1: Environment Preparation
1. **Azure VM Creation**
   - Deployed Windows 10 VM with 4 vCPUs
   - Configured RDP access
   - Established secure connection

2. **Prerequisites Download**
   - Downloaded osTicket-Installation-Files.zip
   - Extracted to desktop for organized access

### Phase 2: Web Server Configuration
1. **IIS Installation & Configuration**
   - Enabled Internet Information Services
   - Activated CGI support under Application Development Features
   - Configured for PHP integration

2. **PHP Environment Setup**
   - Installed PHP Manager for IIS
   - Installed URL Rewrite Module
   - Created C:\PHP directory
   - Extracted PHP 7.3.8 runtime
   - Installed Visual C++ Redistributable
   - Registered PHP with IIS

### Phase 3: Database Setup
1. **MySQL Installation**
   - Installed MySQL 5.5.62
   - Configured with Standard Setup
   - Set root credentials (root/root)
   - Launched Configuration Wizard

2. **Database Management**
   - Installed HeidiSQL for database administration
   - Created osTicket database
   - Configured connection parameters

### Phase 4: osTicket Deployment
1. **Application Installation**
   - Extracted osTicket v1.15.8
   - Deployed to IIS web directory (C:\inetpub\wwwroot)
   - Renamed upload folder to osTicket

2. **PHP Extensions Configuration**
   - Enabled php_imap.dll
   - Enabled php_intl.dll
   - Enabled php_opcache.dll

3. **File Permissions & Security**
   - Renamed ost-sampleconfig.php to ost-config.php
   - Configured file permissions for installation
   - Implemented security cleanup post-installation

## Access Points

### Administrator Access
- **Help Desk Login**: http://localhost/osTicket/scp/login.php
- **Purpose**: Staff and admin ticket management

### End User Access
- **Ticket Portal**: http://localhost/osTicket/
- **Purpose**: Customer ticket submission and tracking

## Security Implementations

### Post-Installation Cleanup
1. **File Removal**
   - Deleted installation setup directory
   - Removed temporary configuration files

2. **Permission Hardening**
   - Set ost-config.php to read-only
   - Removed excessive permissions
   - Disabled inheritance on sensitive files

## Project Structure
