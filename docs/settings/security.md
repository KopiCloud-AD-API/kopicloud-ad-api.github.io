---
title: Configuring Security Access
description: Security Access to KopiCloud AD API
date: 2023-03-22
---

# Configuring Security Access
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

By default, AD security groups access is disabled.

This article explains how to use AD security groups to provide access to specific features of KopiCloud AD API. For details, check the Security section.

----

## APIADAuthenticationGroup

The **APIADAuthenticationGroup** group is used to **Call AD API Methods** provide the folowing permissions: **Login, Create tokens, Call API Methods for AD, No Security Logs**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example: **KopiCloud-API-AD-Authentication** and add users that will consume the AD API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APIADAuthenticationGroup": "KopiCloud-API-AD-Authentication"
```

> Security Group Disabled

```
"APIADAuthenticationGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## APIDNSAuthenticationGroup

The **APIDNSAuthenticationGroup** group is used to **Call DNS API Methods** provide the folowing permissions: **Login, Create tokens, Call API Methods for DNS, No Security Logs**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example: **KopiCloud-API-DNS-Authentication** and add users that will consume the DNS API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APIDNSAuthenticationGroup": "KopiCloud-API-DNS-Authentication"
```

> Security Group Disabled

```
"APIDNSAuthenticationGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## APIAdminGroup

The **APIAdminGroup** group is used for **Admin Access** provide the folowing permissions: **Login, Create Tokens, Manage Tokens, Call ALL API Methods, View Security Log**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example: **KopiCloud-API-Admin-Access** and add users that will consume the DNS API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APIAdminGroup": "KopiCloud-API-Admin-Access"
```

> Security Group Disabled

```
"APIAdminGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## APIAdminGroup

The **APIAdminGroup** group is used for **Admin Access** provide the folowing permissions: **Login, Create Tokens, Manage Tokens, Call ALL API Methods, View Security Log**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example: **KopiCloud-API-Admin-Access** and add users that will consume the DNS API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APIAdminGroup": "KopiCloud-API-Admin-Access"
```

> Security Group Disabled

```
"APIAdminGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

---

## APISecurityGroup

The **APISecurityGroup** group is used for **Security Access** provide the folowing permissions: **Login, Manage Tokens, No API Method Execution, View Security Logs**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example: **KopiCloud-API-Security-Access** and add users that will consume the DNS API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APISecurityGroup": "KopiCloud-API-Security-Access"
```

> Security Group Disabled

```
"APISecurityGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

---

## APITokenAuthenticationGroup

The **APISecurityGroup** group is used for **Token Authentication** provide the folowing permissions: **Login, Create Tokens, No API Method Execution, No Security Logs**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example: **KopiCloud-API-Token-Authentication** and add users that will consume the DNS API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APITokenAuthenticationGroup": "KopiCloud-API-Security-Access"
```

> Security Group Disabled

```
"APITokenAuthenticationGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

