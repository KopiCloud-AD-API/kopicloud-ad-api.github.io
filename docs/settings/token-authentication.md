---
title: Managing Token Authentication
description: Managing KopiCloud AD API Token Authentication
date: 2023-02-28
---

# Managing API Token Authentication
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

By default, **Token Authentication** is enabled.

This article explains how to Check the Status, Enable, or Disable KopiCloud AD API Token Authentication.

Token Authentication settings are managed by the file C**:\KopiCloud-AD-API\appsettings.json**.

----

## Check Status

If **Token Authentication** is enabled, every call to the API will require a token.

Check the status of the Token Authentication, in the footer of the **KopiCloud AD API Management Portal**:

![Token Authentication Status](https://help.kopicloud-ad-api.com/assets/docs/token_authentication_status.png)

----

## Config Settings

If you run **KopiCloud AD API** in a test environment, maybe you want to disable Token Authentication.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Token Authentication using the information below:

> Token Authentication Enabled

```
"DisableTokenAuthentication":false
```

> Token Authentication Disabled

```
"DisableTokenAuthentication":true
```

Save the file.

Restart the web server using the **IISReset command** or the IIS Console.
