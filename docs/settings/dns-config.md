---
title: DNS Configuration
description: DNS Configuration
date: 2023-03-23
---

# Configuring DNS Settings
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

This article explains how to configure DNS settings. These settings are **critical** for the API to work correctly.

The wrong DNS settings can cause failures in authentication to the **KopiCloud AD API Portal** and malfunctioning API.

DNS settings are managed by the file C**:\KopiCloud-AD-API\appsettings.json**.

> Note: the API auto-failover the DNS in case of a failure of the principal DNS to the secondary DNS.

----

## Check Status

Open the file C**:\KopiCloud-AD-API\appsettings.json** and check DNS Settings:

Search for the following settings: "DNSZone", "DNSServer1" and "DNSServer2".

![Troubleshooting DNS Settings](https://adapihelp.kopicloud.com/assets/docs/troubleshooting_dns_settings.png)

Check the values are valid.

----

## DNSZone

The **DNSZone** is used to set the DNS Zone managed using the API and Terraform.


Set the status of the DNSZone using the information below:

```
"DNSZone": "kopicloud.local"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## DNSServer1

The **DNSServer1** is used to set the DNS Server #1 or Principal DNS. This DNS server is required to manage DNS using the API and Terraform.


Set the status of the DNSServer1 to your DNS using the information below:

```
"DNSServer1": "192.168.50.200"
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## DNSServer2

The **DNSServer2** is used to set the DNS Server #2 or the Secondary DNS. This DNS server is **Optional** and used to manage DNS using the API and Terraform, in case of failure of the Principal DNS.


Set the status of the DNSServer2 to your DNS using the information below:

```
"DNSServer2": "192.168.50.201"
```

> Note: if you want to use one DNS Server enter "DNSServer2": "" or the same value for both DNSServer1 and DNSServer2.

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.
