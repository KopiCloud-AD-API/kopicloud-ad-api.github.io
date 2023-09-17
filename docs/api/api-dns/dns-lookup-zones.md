---
title: DNS Lookup Zones API Methods
description: Manage Microsoft DNS Lookup Zones with KopiCloud AD API
date: 2023-05-15
---

# Manage DNS Lookup Zones with KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage Microsoft DNS Lookup Zones using the KopiCloud AD API.

----

## List All DNS Lookup Zones
<span class="btn-get">GET</span> /api/DnsLookupZone/All

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

## Create a DNS Lookup Zone
<span class="btn-post">POST</span> /api/DnsLookupZone/{ZoneName}

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

## Remove a DNS Lookup Zone
<span class="btn-delete">DELETE</span> /api/DnsLookupZone/{ZoneName}

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


