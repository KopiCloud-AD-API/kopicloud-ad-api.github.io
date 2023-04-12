---
title: KopiCloud AD API Setup Configuration File
description: KopiCloud AD API Setup Configuration File
date: 2023-04-12
---

# KopiCloud AD API Setup Configuration File
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

KopiCloud AD API Setup configuration file parameters.

----

## Sample Setup File

The Setup File can be used to automate the setup and configuration of KopiCloud AD API.

Create a new file, using the example below:

```
Dark Mode = yes
DNS Server #1 = 192.168.50.200
DNS Server #2 = 192.168.50.201
DNS Zone = kopicloud.local
Service Account User = ApiSvc
Service Account Password = MySup3rP@ssw0rd
Service Account Domain = kopicloud.local
License Code = A13V-A13V-A13V-A13V
```

----

## Setup File Parameters

Below is the list of parameters:

- `Dark Mode` = Set the GUI of the Config Tool to Dark Mode (Yes) or Light Mode (No)

- `DNS Server #1` = principal DNS server

- `DNS Server #2` = secondary DNS server

- `DNS Zone` = DNS Zone

-  `Service Account User` = Service Account Username

- `Service Account Password` = Service Account Password

- `Service Account Domain` = Service Account AD Domain

- `License Code` = KopiCloud AD API License Code
