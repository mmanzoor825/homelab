# Issue #1: Configuration Manager Console
## 10/11/2026
```text
The Configuration Manager console cannot connect to the Configuration Manager site database. Verify the following:

      •	This computer has network connectivity to the SMS Provider computer.
      •	Your user account has Remote Activation permission on the Configuration Manager site server and the SMS Provider computer.
      •	The Configuration Manager console version is supported by the site server.
      •	You are assigned to at least one role-based administration security role.
      •	You have the following WMI permissions to the Root\SMS and Root\SMS\site_<site code> namespaces: Execute Methods, Provider Write, Enable Account, and Remote Enable.
```
- Configuration Manager console unable to connect to the site database. Logs show that there is an issue connecting
to the SQL server. 
```text
C:\Program Files\Microsoft Configuration Manager\logs\SMSProv.log

Set SQL Machine DC-02.homelab.com from registry~  $$<SMS Provider><10-11-2026 19:47:42.281+240><thread=9660 (0x25BC)>
*** *** Unknown SQL Error!  $$<SMS Provider><10-11-2026 19:47:42.284+240><thread=9660 (0x25BC)>
*** Failed to connect to the SQL Server, connection type: SMS ACCESS.  $$<SMS Provider><10-11-2026 19:47:42.285+240><thread=9660 (0x25BC)>
Failed to get sql connection  $$<SMS Provider><10-11-2026 19:47:42.285+240><thread=9660 (0x25BC)>
~*~*~F:\dbs\sh\cmgm\0926_074307\cmd\18\src\SiteServer\SDK_Provider\SMSProv\sspclassmanager.cpp(677) : Failed to get active site server information.~*~*~  $$<SMS Provider><10-11-2026 19:47:42.286+240><thread=9660 (0x25BC)>
~*~*~Failed to get active site server information. ~*~*~  $$<SMS Provider><10-11-2026 19:47:42.286+240><thread=9660 (0x25BC)>
Found IClassManger: Opal SMS CSsp Provider Extension Implementation.~  $$<SMS Provider><10-11-2026 19:47:42.287+240><thread=9660 (0x25BC)>
CExtUserContext::LeaveThread : Releasing IWbemContextPtr=-409915808~  $$<SMS Provider><10-11-2026 19:47:42.288+240><thread=9660 (0x25BC)>
```

- Event Viewer displayed the following error in regard to the ODBC driver. 
```text
The system has called a custom component and that component has failed and generated an exception. This indicates a problem with the custom component. Notify the developer of this component that a failure has occurred and provide them with the information below.
Component Prog ID: 0[ODBC][C:\WINDOWS\system32\msodbcsql18.dll]
Method Name: IDispenserDriver::CreateResource
Process Name: sitecomp.exe
Exception: c0000005
Address: 0X00007FFFA7DF2C10
```
## Resolution
- There are currently some documented issues with ODBC Driver for SQL Server version 18.7.1.1. Will attempt to rollback to version 18.6.2.1
- Rollback to version 18.6.2.1 successful. Configuration manager console is able to start up without issues.
