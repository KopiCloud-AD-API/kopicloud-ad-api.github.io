---
title: Managing Token Authentication
description: Managing KopiCloud AD API Token Authentication
---

# Managing KopiCloud AD API Token Authentication
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

By default, **Token Authentication** is enabled.

How to Check the Status, Enable, or Disable KopiCloud AD API Token Authentication.

----

## Check Status

If **Token Authentication** is enabled, every call to the API will require a token.

Check the status of the Token Authentication, in the footer of the **KopiCloud AD API Management Website**:

![Token Authentication Status](https://help.kopicloud-ad-api.com/assets/docs/token_authentication_status.png)

----

## Settings

If you run **KopiCloud AD API** in a test environment, maybe you want to disable it.

Open the **appsettings.json** file located on the root of the KopiCloud AD API folder (by default is C:\KopiCloud-AD-API).

Set the status of the Token Authentication with the information below:

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
