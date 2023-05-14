---
title: Configuring Service Account
description: KopiCloud AD API Service Account
date: 2023-05-15
---

# Configuring KopiCloud AD API Service Account
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

This article explains how to configure the Service Account in the settings file.

These settings are critical to execute all API methods and Terraform resources related with the Active Directory.

Service Account settings are managed by the file C**:\KopiCloud-AD-API\appsettings.json**.

----

## Config Settings

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (C:\KopiCloud-AD-API).

Update the settings listed below to configure the API Server:

```
"DNSZone": "kopicloud.local",
"DNSServer1": "192.168.20.200",
"DNSServer2": "192.168.20.201",
"ADDomainName": "kopicloud.local",
"ADServiceUser": "apisvc",
"ADServicePassword": "K0p1Cl0udS3rv1c3",
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

