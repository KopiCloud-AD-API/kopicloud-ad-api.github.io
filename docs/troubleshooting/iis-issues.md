---
title: Troubleshooting IIS Issues
description: Troubleshooting IIS Issues
date: 2023-04-09
---

# Troubleshooting IIS Issues
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

This article explains how to troubleshoot Internet Information Services (IIS) errors.

----

# IIS HTTP Error 500.19 - Internal Server Error

Detailed Error Information:
Module: IIS Web Core
Notification: Unknown
Handler: Not yet determined
Error Code: 0x8007000d
Config File: \\?\C:\KopiCloud-AD-API\web.config

**Explanation:**

This error is caused by a lack of permission or by a physical path that doesn't match the path for the virtual directory.

**Solution #1:**

Add the local user IIS_IUSRS and the AD Domain Service Account user (for example apisvc) to the NTFS permissions of the folder **C:\KopiCloud-AD-API**.


**Solution #2:

There is a reference in the web.config of the IIS to a missing component.

Make a copy of your file **C:\KopiCloud-AD-API\web.config** and replace it with the code below:

```
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <system.webServer>
    <security>
      <requestFiltering removeServerHeader="true" />
    </security>
    <httpProtocol>
      <customHeaders>
        <add name="X-Content-Type-Options" value="nosniff" />
        <remove name="X-Powered-By" />
        <remove name="Server" />
      </customHeaders>
    </httpProtocol>
    <handlers>
      <add name="aspNetCore" path="*" verb="*" modules="AspNetCoreModuleV2" resourceType="Unspecified" />
    </handlers>
    <aspNetCore processPath=".\KopiCloud.AD.API.Core.exe" stdoutLogEnabled="false" stdoutLogFile=".\logs\stdout" hostingModel="inprocess" />
  </system.webServer>
</configuration>
```

----


