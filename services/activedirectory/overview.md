# Overview
Active Directoy Domain Services allow centralized
identity access and management on the network. The domain 
consists of one domain controller and a few virtual machines
that serve as domain-joined clients. Group Policy Objects (GPOs)
are also configured to apply setting across domain-joined devices.

- Domain Name: homelab.com
- Domain Controller: DC-02, 192.168.1.2
- DNS Server: DC-02,192.168.1.2

```powershell
PS > Get-ADDomainController

ComputerObjectDN           : CN=DC-02,OU=Domain Controllers,DC=homelab,DC=com
DefaultPartition           : DC=homelab,DC=com
Domain                     : homelab.com
Enabled                    : True
Forest                     : homelab.com
HostName                   : DC-02.homelab.com
InvocationId               : f5c8674a-db7c-471f-9d96-3b04c2035e64
IPv4Address                : 192.168.1.2
IPv6Address                : fdd1:45f1:d6e4:0:5681:890c:9b85:3107
IsGlobalCatalog            : True
IsReadOnly                 : False
LdapPort                   : 389
Name                       : DC-02
NTDSSettingsObjectDN       : CN=NTDS Settings,CN=DC-02,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,
                             DC=homelab,DC=com
OperatingSystem            : Windows Server 2025 Standard Evaluation
OperatingSystemHotfix      :
OperatingSystemServicePack :
OperatingSystemVersion     : 10.0 (26100)
OperationMasterRoles       : {SchemaMaster, DomainNamingMaster, PDCEmulator, RIDMaster...}
Partitions                 : {DC=ForestDnsZones,DC=homelab,DC=com, DC=DomainDnsZones,DC=homelab,DC=com,
                             CN=Schema,CN=Configuration,DC=homelab,DC=com, CN=Configuration,DC=homelab,DC=com...}
ServerObjectDN             : CN=DC-02,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=homelab,DC=com
ServerObjectGuid           : 69363b74-dc71-4ce4-af28-134580c11734
Site                       : Default-First-Site-Name
SslPort                    : 636
```
