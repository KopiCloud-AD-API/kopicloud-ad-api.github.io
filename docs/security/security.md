---
title: Security
description: KopiCloud AD API Security
date: 2023-03-22
---

# Security
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Security is a very important topic when we deploy an API that manipulate Active Directory data and DNS records.

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

When you use KopiCloud AD API based on the permissions in your AD account, you will limited to execute specific actions:

| Action Name              | Action Description                                  |
| ------------------------ | --------------------------------------------------- |
| Login                    | Login to the KopiCloud AD API Management Console    |
| Create Tokens            | Create authentication tokens and manage own tokens  |
| Manage Tokens            | Enable, Disable or Delete ANY authentication tokens |
| Call API Methods for AD  | Only execute API AD Methods                         |
| Call API Methods for DNS | Only execute API DNS Methods                        |
| Call ALL API Methods     | Execute ALL API Methods                             |
| No API Methods Execution | Cannot Execute ANY API Methods                      |
| View Security Log        | Review the Security Log                             |
| No Security Log          | Cannot Access the Security Log                      |

-----

## Restricted Access to Domain Administrators

To login into the **KopiCloud AD API Management Console**, the machine needs to be joined to AD and your AD domain account must be member of the AD Domain Admins group.

The default domain admin group can be different, based on your environment:

| Environment Type                                   | Group Name                       |
| -------------------------------------------------- | -------------------------------- |
| Microsoft Active Directory Implementations         | **Domain Admins**                |
| AWS Managed Microsoft AD Directory                 | **AWS Delegated Administrators** |
| GCP Managed Service for Microsoft Active Directory | **Cloud Service Administrators** |
| Azure Active Directory Domain Services (AADDS)     | **AAD DC Administrators**        |

> Note: Members of AD Groups listed above Login, Create Tokens, Manage Tokens, Call ALL API Methods, and Review Security Log.

----

## Default API AD Groups

We defined a few security groups, with specific permissions. 

| Group Name                  | Use                    | Actions Allowed                                                              |
| --------------------------- | ---------------------- |----------------------------------------------------------------------------- |
| APIADAuthenticationGroup    | Access AD API Methods  | Login, Create tokens, Call API Methods for AD, No Security Logs              | 
| APIDNSAuthenticationGroup   | Access DNS API Methods | Login, Create tokens, Call API Methods for DNS, No Security Logs             | 
| APIAdminGroup               | Admin Access           | Login, Create Tokens, Manage Tokens, Call ALL API Methods, View Security Log | 
| APISecurityGroup            | Security Team Access   | Login, Manage Tokens, No API Method Execution, View Security Logs            | 
| APITokenAuthenticationGroup | Create Token           | Login, Create Tokens, No API Method Execution, No Security Logs              | 

To use these groups, check [this link](../settings/security.md).

