---
title: Enable/Disable API Sections
description: Enable/Disable API Sections
date: 2024-05-18
---

# Enable/Disable (Show/Hide) API Sections
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.1+-blueviolet.svg)](https://adapi.kopicloud.com)

By default, all API sections are **enabled**, but you may need to disable sections for security reasons.

This article explains enabling or disabling some specific KopiCloud AD API sections.

API Section settings are managed by the file **C:\KopiCloud-AD-API\appsettings.json**.

This is the list of API settings that you can enable/disable:

- APIEnableAD
- APIEnableADComputer
- APIEnableADGroup
- APIEnableADGroupMembership
- APIEnableADUser
- APIEnableADOu
- APIEnableDNS
- APIEnableDnsA
- APIEnableDnsAAAA
- APIEnableDnsCNAME
- APIEnableDnsZones

----

## APIEnableAD

The **APIEnableAD** setting manages **ALL Active Directory** sections. 

When you enable/disable this section, you will see/hide the **AD Computer**, **AD OU**, **AD User**, **AD Group**, and **ADGroupMembership** sections.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> AD Sections Enabled

```
"APIEnableAD: true"
```

> AD Sections Disabled

```
"APIEnableAD: false"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## APIEnableADComputer

The **APIEnableADComputer** setting manages the **AD Computer** section. 

When you enable/disable this section, you will see/hide the **AD Computer** section.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> AD Computer Section Enabled

```
"APIEnableADComputer: true"
```

> AD Computer Section Disabled

```
"APIEnableADComputer: false"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## APIEnableDNS

The **APIEnableDNS** setting manages **ALL DNS** sections. 

When you enable/disable this section, you will see/hide the **APIEnableDnsA**, **APIEnableDnsAAAA**, **APIEnableDnsCNAME**, and **APIEnableDnsZones** sections.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> DNS Sections Enabled

```
"APIEnableDNS: true"
```

> DNS Sections Disabled

```
"APIEnableDNS: false"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.
