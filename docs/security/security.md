---
title: Security Overview
description: KopiCloud AD API Security
date: 2023-03-23
---

# Security Overview
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Security is critical when we deploy an API that manipulates Active Directory data and DNS records.

----

## Token Authentication

**KopiCloud AD API** uses tokens to authenticate to the API instead of usernames and passwords. 

Please refer to the following documentation for details:

- [Generate Token](../authentication/token-authentication.md)
- [Manage Tokens](../authentication/manage-tokens.md)
- [API Swagger Authentication](../authentication/swagger-authentication.md)
- [Terraform Authentication](../authentication/terraform-authentication.md)

----

## API Actions

When you use KopiCloud AD API based on the permissions in your AD account, you will be limited to executing specific actions:

| Action Name              | Action Description                              |
| ------------------------ | ----------------------------------------------- |
| Login                    | Login to the KopiCloud AD API Management Portal |
| Create Tokens            | Create authentication tokens                    |
| Manage Tokens            | Enable or Disable authentication tokens         |
| Delete Tokens            | Delete authentication tokens                    |
| Call API Methods for AD  | Only execute API AD Methods                     |
| Call API Methods for DNS | Only execute API DNS Methods                    |
| Call ALL API Methods     | Execute ALL API Methods                         |
| No API Methods Execution | Cannot Execute ANY API Methods                  |
| View Event Logs          | View the Event Logs                             |
| No Event Log Access      | Cannot Access the Event Logs                    |

-----

## Restricted Access to Domain Administrators

To login into the **KopiCloud AD API Management Portal**, the machine must be joined to AD, and your AD domain account must be a member of the **AD Domain Admins** group.

The default domain admin group can be different based on your environment:

| Environment Type                                   | Group Name                       |
| -------------------------------------------------- | -------------------------------- |
| Microsoft Active Directory Implementations         | **Domain Admins**                |
| AWS Managed Microsoft AD Directory                 | **AWS Delegated Administrators** |
| GCP Managed Service for Microsoft Active Directory | **Cloud Service Administrators** |
| Azure Active Directory Domain Services (AADDS)     | **AAD DC Administrators**        |

> Note: Members of AD Groups listed above Login, Create and Manage ALL Tokens, Delete Tokens, Call ALL API Methods, and View Event Log.

----

## Default API AD Groups

By default, We defined a list security groups, with specific permissions. 

| Group Name                  | Use                  | Actions Allowed                                                              |
| --------------------------- | -------------------- |----------------------------------------------------------------------------- |
| APIAuthenticationGroup      | Call ALL API Methods | Login, Create tokens, Call ALL API Methods, No Event Logs                    | 
| APIADAuthenticationGroup    | Call AD API Methods  | Login, Create tokens, Call API Methods for AD, No Event Logs                 | 
| APIDNSAuthenticationGroup   | Call DNS API Methods | Login, Create tokens, Call API Methods for DNS, No Event Logs                | 
| APIAdminGroup               | Admin Access         | Login, Create, Manage & Delete Tokens, Call ALL API Methods, View Event Logs | 
| APISecurityGroup            | Security Team Access | Login, Create, Manage & Delete Tokens, View Event Logs, No API Method Calls  | 
| APITokenAuthenticationGroup | Manage Tokens        | Login, Create Tokens, Manage Token, No API Method Calls, No Event Logs       | 
| APILogAccessGroup           | View Event Logs      | Login, View Event Logs, No Token Management, No API Method Calls             | 

To use these groups, check [this link](../settings/security.md).
