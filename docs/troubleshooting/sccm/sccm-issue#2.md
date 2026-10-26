# Issue #2: Client Push Install
## 10/26/2026

Issue: SCCM client not downloading on client device. The following is from a client-side log file
```text
C:\windows\ccmsetup\logs\ccmsetup.log

<![LOG[[CCMHTTP] ERROR: URL=http://DC-02.homelab.com/CCM_Client, Port=80, Options=1248, Code=0, Text=CCM_E_BAD_HTTP_STATUS_CODE]LOG]!><time="05:04:46.310+240" date="10-26-2026" component="ccmsetup" context="" type="1" thread="4296" file="ccmhttperror.cpp:306">
<![LOG[[CCMHTTP] ERROR INFO: StatusCode=500 StatusText=Internal Server Error]LOG]!><time="05:04:46.310+240" date="10-26-2026" component="ccmsetup" context="" type="1" thread="4296" file="ccmhttperror.cpp:317">
<![LOG[GetDirectoryList failed with a non-recoverable failure, 0x87d0027e]LOG]!><time="05:04:46.311+240" date="10-26-2026" component="ccmsetup" context="" type="3" thread="4296" file="httphelper.cpp:958">
<![LOG[Failed to get directory list from 'http://DC-02.homelab.com/CCM_Client'. Error 0x87d0027e]LOG]!><time="05:04:46.311+240" date="10-26-2026" component="ccmsetup" context="" type="3" thread="4296" file="httphelper.cpp:985">
<![LOG[Failed to correctly receive a WEBDAV HTTP request.. (StatusCode at WinHttpQueryHeaders: 500) and StatusText: 'Internal Server Error' ]LOG]!><time="05:04:46.311+240" date="10-26-2026" component="ccmsetup" context="" type="3" thread="4296" file="state.h:69">
<![LOG[Failed to check url http://DC-02.homelab.com/CCM_Client/ccmsetup.cab. Error 0x80004005]LOG]!><time="05:04:46.311+240" date="10-26-2026" component="ccmsetup" context="" type="3" thread="4296" file="httphelper.cpp:1345">
<![LOG[Accessing the URL 'http://DC-02.homelab.com/CCM_Client/ccmsetup.cab' failed with 80004005]LOG]!><time="05:04:46.311+240" date="10-26-2026" component="ccmsetup" context="" type="2" thread="4296" file="ccmsetup.cpp:11265">
```
