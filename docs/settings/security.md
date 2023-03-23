---
title: Configuring Security Access
description: Security Access to KopiCloud AD API
date: 2023-03-23
---

# Configuring Security Access
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

By default, AD security groups access is disabled.

This article explains how to use AD security groups to provide access to specific features of KopiCloud AD API. For details, check the Security section.

----

## APIAuthenticationGroup

The **APIAuthenticationGroup** group is used to **Call ALL API Methods** and provide the following permissions: **Login, Create and Manage OWN Tokens, Call ALL API Methods, No Event Logs Access**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example, **KopiCloud-API-Authentication**, and add users that will consume all API methods to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default, is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APIAuthenticationGroup": "KopiCloud-API-Authentication"
```

> Security Group Disabled

```
"APIAuthenticationGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

----

## APIADAuthenticationGroup

The **APIADAuthenticationGroup** group is used to **Call AD API Methods** and provide the following permissions: **Login, Create and Manage OWN Tokens, Call API Methods for AD, No Event Logs Access**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example, **KopiCloud-API-AD-Authentication**, and add users that will consume the AD API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default, is C:\KopiCloud-AD-API).

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

The **APIDNSAuthenticationGroup** group is used to **Call DNS API Methods** and provide the following permissions: **Login, Create and Manage OWN Tokens, Call API Methods for DNS, No Event Logs Access**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example, **KopiCloud-API-DNS-Authentication**, and add users that will consume the DNS API to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default, is C:\KopiCloud-AD-API).

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

The **APIAdminGroup** group is used for **Admin Access** to provide the following permissions: **Login, Create and Manage ALL Tokens, Call ALL API Methods, View Event Logs**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example, **KopiCloud-API-Admin-Access**, and add the administrator users to manage the API.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default, is C:\KopiCloud-AD-API).

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

## APISecurityGroup

The **APISecurityGroup** group is used for the **Information Security Team Access** and provides the following permissions: **Login, Create and Manage ALL Tokens, No API Method Execution, View Event Logs**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example, **KopiCloud-API-Security-Access**, and add users from your Information Security Team to it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default, is C:\KopiCloud-AD-API).

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

The **APITokenAuthenticationGroup** group is used for **Token Authentication** and provides the following permissions: **Login, Create and Manage ALL Tokens, No API Method Execution, No Event Logs Access**.   

To use this group, create an Active Directory Security Group in your Active Directory, for example, **KopiCloud-API-Token-Authentication**, and add users to manage authentication tokens.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default, is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APITokenAuthenticationGroup": "KopiCloud-API-Token-Authentication"
```

> Security Group Disabled

```
"APITokenAuthenticationGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.

---

## APILogAccessGroup

The **APILogAccessGroup** group is used for **Troubleshooting or API Debugging** and provides the following permissions: **Login, View Event Logs, No API Method Execution**. 

To use this group, create an Active Directory Security Group in your Active Directory, for example: **KopiCloud-API-Log-Access**,  and add users needing to access the Event Log for troubleshooting or developers that need to debug applications.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default, is C:\KopiCloud-AD-API).

Set the status of the Security Group using the information below:

> Security Group Enabled

```
"APILogAccessGroup": "KopiCloud-API-Log-Access"
```

> Security Group Disabled

```
"APILogAccessGroup": ""
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.
