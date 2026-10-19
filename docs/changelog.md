# Changelog 

- Installed Windows Server 2025 Evaluation Edition on a desktop computer.
- Configured an IP reservation for the server via DHCP.
- Installed Active Directory Domain Services and promoted the server to a domain controller.
  - Created test user accounts, groups, and organizational units.
  - Successfully joined client virtual machines to the domain.
  - Successfully configured and applied a group policy to enforce a specific wallpaper on domain joined devices. 
  



## 10/11/2026
- Preparing for SCCM. Installed following prerequisites:
  -  Extended the Active Directory schema and created a "System Management" container. Assigned full control to the computer account.
  -  RDC library
  - Microsoft SQL Server
  - .NET 3.5  
  - BITS for IIS
  - Microsoft ODBC driver for SQL
  - ADK with Windows PE Add-on
 
- Installed configuration manager using the setup wizard.
  - Site database configured on SQL server.
  - Configuration Manager console installed.
 
## 10/19/2026
- Configured Windows Time Service
  - Domain controller configured to synchronize from time.windows.com (Microsoft's NTP Server).
  - Domian joined devices to synchronize from domain controller.
    
    
