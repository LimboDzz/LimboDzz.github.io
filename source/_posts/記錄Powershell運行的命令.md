---
title: 記錄Powershell運行的命令
date: 2021-05-24 16:48:43
tags:
  - cmd
  - P&S
---

## Solution

`$ Start-Transcript C:\Users\DZZ\Downloads\log.txt`

`$ Stop-Transcript`

Sample content in log.txt

```
**********************
Windows PowerShell transcript start
Start time: 20210524162644
Username: DESKTOP-IAH5EDT\DZZ
RunAs User: DESKTOP-IAH5EDT\DZZ
Configuration Name:
Machine: DESKTOP-IAH5EDT (Microsoft Windows NT 10.0.19042.0)
Host Application: C:\windows\system32\WindowsPowerShell\v1.0\powershell.exe
Process ID: 8680
PSVersion: 5.1.19041.906
PSEdition: Desktop
PSCompatibleVersions: 1.0, 2.0, 3.0, 4.0, 5.0, 5.1.19041.906
BuildVersion: 10.0.19041.906
CLRVersion: 4.0.30319.42000
WSManStackVersion: 3.0
PSRemotingProtocolVersion: 2.3
SerializationVersion: 1.1.0.1
**********************
Transcript started, output file is C:\Users\DZZ\Downloads\log.txt
PS C:\Users\DZZ> nrm ls

PS C:\Users\DZZ> npm /h

PS C:\Users\DZZ> npm help

PS C:\Users\DZZ> npm whoami

PS C:\Users\DZZ> npm v

PS C:\Users\DZZ> npm -v

PS C:\Users\DZZ> npm -whoami

PS C:\Users\DZZ> Stop-Transcript
**********************
Windows PowerShell transcript end
End time: 20210524162817
**********************
```

## References

1. <https://blog.csdn.net/sdyu_peter/article/details/80791949>
