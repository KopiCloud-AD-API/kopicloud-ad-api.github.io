---
title: Enable/Disable API Sections
description: Enable/Disable API Sections
date: 2024-05-20
---

# Enable/Disable (Show/Hide) API Sections
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.1+-blueviolet.svg)](https://adapi.kopicloud.com)

By default, all API sections are **enabled**, but you may need to disable sections for application or security reasons.

This article explains enabling or disabling some specific KopiCloud AD API sections.

API Section settings are managed by the file **C:\KopiCloud-AD-API\appsettings.json**.

This is the list of API settings that you can enable/disable:

- APIEnableAD
- APIEnableADComputer
- APIEnableADGroup
- APIEnableADGroupMembership
- APIEnableADUser
- APIEnableADOu
- APIEnableDns
- APIEnableDnsA
- APIEnableDnsAAAA
- APIEnableDnsCNAME
- APIEnableDnsZones

----

## Enable ALL AD Sections

The **APIEnableAD** setting manages **ALL Active Directory** sections. 

When you enable/disable this section, you will see/hide the **AD Computer**, **AD Users**, **AD Organization Units (OU)**, **AD Groups**, and **AD Group Membership** sections.

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

## Enable the AD Computer Section

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

## Enable the AD Group Section

The **APIEnableADGroup** setting manages the **AD Groups** section. 

When you enable/disable this section, you will see/hide the **AD Groups** section.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> AD Groups Section Enabled

```
"APIEnableADGroup: true"
```

> AD Groups Section Disabled

```
"APIEnableADGroup: false"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## Enable the AD Group Membership Section

The **APIEnableADGroupMembership** setting manages the **AD Group Membership** section. 

When you enable/disable this section, you will see/hide the **AD Group Membership** section.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> AD Group Membership Section Enabled

```
"APIEnableADGroupMembership: true"
```

> AD Group Membership Section Disabled

```
"APIEnableADGroupMembership: false"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## Enable the AD User Section

The **APIEnableADUser** setting manages the **AD Users** section. 

When you enable/disable this section, you will see/hide the **AD Users** section.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> AD Users Section Enabled

```
"APIEnableADUser: true"
```

> AD Users Section Disabled

```
"APIEnableADUser: false"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## Enable the AD OU Section

The **APIEnableOu** setting manages the **AD Organization Units (OU)** section. 

When you enable/disable this section, you will see/hide the **AD Organization Units (OU)** section.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> AD Organization Units (OU) Section Enabled

```
"APIEnableADOu: true"
```

> AD Organization Units (OU) Section Disabled

```
"APIEnableADOu: false"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## Enable ALL DNS Sections

The **APIEnableDNS** setting manages **ALL DNS** sections. 

When you enable/disable this section, you will see/hide the **DNS A Records**, **DNS AAAA Records**, **DNS CNAME Records**, **DNS Zones**, **DNS Lookup Zones**, and **DNS Reverse Lookup Zones** sections.

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

----

## Enable DNS A Records Section

The **APIEnableDnsA** setting manages the **DNS A Records** section. 

When you enable/disable this section, you will see/hide the **DNS A Records** sections.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> DNS A Records Section Enabled

```
"APIEnableDnsA: true"
```

> DNS A Records Section Disabled

```
"APIEnableDnsA: false"
```

----

## Enable DNS AAAA Records Section

The **APIEnableDnsAAAA** setting manages the **DNS AAAA Records** section. 

When you enable/disable this section, you will see/hide the **DNS AAAA Records** sections.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> DNS AAAA Records Section Enabled

```
"APIEnableDnsAAAA: true"
```

> DNS AAAA Records Section Disabled

```
"APIEnableDnsAAAA: false"
```

----

## Enable DNS CNAME Records Section

The **APIEnableDnsCNAME** setting manages the **DNS CNAME Records** section. 

When you enable/disable this section, you will see/hide the **DNS CNAME Records** sections.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> DNS CNAME Records Section Enabled

```
"APIEnableDnsCNAME: true"
```

> DNS CNAME Records Section Disabled

```
"APIEnableDnsCNAME: false"
```

----

## Enable DNS Zones Section

The **APIEnableDnsZones** setting manages the **DNS Zones**, **DNS Lookup Zones**, and **DNS Reverse Lookup Zones** sections. 

When you enable/disable this section, you will see/hide the **DNS Zones**, **DNS Lookup Zones**, and **DNS Reverse Lookup Zones** sections.

Open the **appsettings.json** file located at the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

> DNS Zones Sections Enabled

```
"APIEnableDnsZones: true"
```

> DNS Zones Sections Disabled

```
"APIEnableDnsZones: false"
```
