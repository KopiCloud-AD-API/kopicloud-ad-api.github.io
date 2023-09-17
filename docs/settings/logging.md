---
title: Configuring Windows Event Logging
description: Configuring Windows Event Logging
date: 2023-05-14
---

# Configuring Windows Event Logging
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

By default, writing events to Windows Event Viewer is **disabled**.

This article explains enabling or disabling writing events to Windows Event Viewer.

Logging settings are managed by the file **C:\KopiCloud-AD-API\appsettings.json**.

----

## DisableLogToEventViewer

The **DisableLogToEventViewer** setting manages writing events to Windows Event Viewer.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> Writing events to Windows Event Viewer Enabled

```
"DisableLogToEventViewer: false"
```

> Writing events to Windows Event Viewer Disabled

```
"DisableLogToEventViewer: true"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

