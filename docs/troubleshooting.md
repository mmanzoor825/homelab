# Issue #1: Configuration Manager - 10/11/2026

Configuration Manager console unable to connect to the site database. Logs show that there is an issue connecting
to the SQL server. 
- Confirmed that ports 1433 and 4022 are open for SQL Server connection.
```powershell
PS > Get-Content -tail 8 C:\Program Files\Microsoft Configuration Manager\logs\SMSProv.log

Set SQL Machine DC-02.homelab.com from registry~  $$<SMS Provider><10-11-2026 19:47:42.281+240><thread=9660 (0x25BC)>
*** *** Unknown SQL Error!  $$<SMS Provider><10-11-2026 19:47:42.284+240><thread=9660 (0x25BC)>
*** Failed to connect to the SQL Server, connection type: SMS ACCESS.  $$<SMS Provider><10-11-2026 19:47:42.285+240><thread=9660 (0x25BC)>
Failed to get sql connection  $$<SMS Provider><10-11-2026 19:47:42.285+240><thread=9660 (0x25BC)>
~*~*~F:\dbs\sh\cmgm\0926_074307\cmd\18\src\SiteServer\SDK_Provider\SMSProv\sspclassmanager.cpp(677) : Failed to get active site server information.~*~*~  $$<SMS Provider><10-11-2026 19:47:42.286+240><thread=9660 (0x25BC)>
~*~*~Failed to get active site server information. ~*~*~  $$<SMS Provider><10-11-2026 19:47:42.286+240><thread=9660 (0x25BC)>
Found IClassManger: Opal SMS CSsp Provider Extension Implementation.~  $$<SMS Provider><10-11-2026 19:47:42.287+240><thread=9660 (0x25BC)>
CExtUserContext::LeaveThread : Releasing IWbemContextPtr=-409915808~  $$<SMS Provider><10-11-2026 19:47:42.288+240><thread=9660 (0x25BC)>
```
