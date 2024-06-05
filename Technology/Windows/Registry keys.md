---
label: Registry Keys
---

==- Disable Bing searches
Location: HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Search

Key: BingSearchEnabled, DWORD 32-bit, 0

File:
```
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Search]
"BingSearchEnabled"=dword:00000000
```
===

==- Set Windows to use UTC instead of localtime
Location: HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation

Key: RealTimeIsUniversal, DWORD 32-bit, 1

File:
```
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation]
"RealTimeIsUniversal"=dword:00000001
```
===