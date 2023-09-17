---
title: Installing the KopiCloud AD API
description: Installing the KopiCloud AD API
date: 2023-05-15
---

# Installing the KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Installing and configuring the KopiCloud AD API on your server

----

## Requirements

KopiCloud AD API needs a **Service Account** to manage the Active Directory. 

Create an Active Directory user, for example, "KopiCloudAPISvC" with a complex password and set the "Password never expires" setting.

Add the Service Account username to the default **Domain Administrators** Active Directory group.

The default domain admin group can be different based on your environment:

| Environment Type                                   | Group Name                       |
| -------------------------------------------------- | -------------------------------- |
| Microsoft Active Directory Implementations         | **Domain Admins**                |
| AWS Managed Microsoft AD Directory                 | **AWS Delegated Administrators** |
| GCP Managed Service for Microsoft Active Directory | **Cloud Service Administrators** |
| Azure Active Directory Domain Services (AADDS)     | **AAD DC Administrators**        |

**IMPORTANT:** You cannot login to the **KopiCloud AD API Portal** with your Service Account for security reasons.

----

## Installing KopiCloud AD API

The process of the installing the API requires three steps:

1) Install the API by running the Setup scripts and installing the API in one of your servers, deploy a VM using our Terraform scripts, or deploy the API from the Marketplace of your cloud provider.

2) After the machine is deployed, join the machine to the Active Directory you want to manage and restart the machine.

3) Log into the API machine with a domain administrator account, and run the [**KopiCloudConfig.exe**](setup-config-tool.md) configuration tool.
