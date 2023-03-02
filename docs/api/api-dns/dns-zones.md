---
title: DNS Zones API Methods
description: Manage Microsoft DNS Zones with KopiCloud AD API
date: 2023-03-02
---

# Manage DNS Zones with KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS Zones using the KopiCloud AD API.

----

## List All DNS Zones
<span class="btn-get">GET</span> /api/DnsZones/All

**Parameters**

| Name              | Type    | Description                          | Mandatory |
| ----------------- | ------- | ------------------------------------ | --------- |
| IgnoreSystemZones | boolean | Ignore System Zones (Default = true) | Yes       |
| Auth-Token        | string  | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "distinguishedName": "string",
      "zoneName": "string",
      "zoneType": "string",
      "type": "string"
    }
  ]
}
```

----

## List All DNS CNAME Records in a DNS Zone
<span class="btn-get">GET</span> /api/DnsCNameRecord/{ZoneName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| ZoneName   | string | DNS Zone Name                        | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**
```
{
  "output": "string",
  "result": [
    {
      "distinguishedName": "string",
      "zoneName": "string",
      "zoneType": "string",
      "type": "string"
    }
  ]
}
```

----

## Check If DNS Zone Exists
<span class="btn-get">GET</span> /api/DnsZones/{ZoneName}/Exists

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| ZoneName   | string | DNS Zone Name                        | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```


