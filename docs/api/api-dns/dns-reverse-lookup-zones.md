---
title: DNS Reverse Lookup Zones API Methods
description: Manage Microsoft DNS Reverse Lookup Zones with KopiCloud AD API
date: 2023-03-02
---

# Manage DNS Reverse Lookup Zones with KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS Reverse Lookup Zones using the KopiCloud AD API.

----

## List All DNS Reverse Lookup Zones
<span class="btn-get">GET</span> /api/DnsReverseLookupZone/All

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

## Get Dns Reverse Lookup Zone by NetworkID Or Zone Name
<span class="btn-get">GET</span> /api/DnsReverseLookupZone/{NetworkIDOrZoneName}

**Parameters**

| Name                | Type    | Description                                                             | Mandatory |
| ------------------- | ------- | ----------------------------------------------------------------------- | --------- |
| NetworkIDOrZoneName | string  | Network ID (ex. 10.20.30.0/24) or Zone Name (ex. 30.20.10.in-addr.arpa) | Yes       |
| IgnoreSystemZones   | boolean | Ignore System Zones (Default = true)                                    | Yes       |
| Auth-Token          | string  | Bearer or Basic Authentication Token                                    | Yes       |

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

## Create a DNS Reverse Lookup Zone
<span class="btn-post">POST</span> /api/DnsReverseLookupZone/{NetworkID}

**Parameters**

| Name       | Type   | Description                                                     | Mandatory |
| ---------- | ------ | --------------------------------------------------------------- | --------- |
| NetworkID  | string | DNS Reverse Lookup NetworkID to Create. Format: 192.168.50.0/24 | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token                            | Yes       |

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

## Remove a DNS Reverse Lookup Zone
<span class="btn-delete">DELETE</span> /api/DnsReverseLookupZone/{NetworkIDOrZoneName}

**Parameters**

| Name                | Type   | Description                          | Mandatory |
| ------------------- | ------ | ------------------------------------ | --------- |
| NetworkIDOrZoneName | string | NetworkID Zone Name to Remove        | Yes       |
| Auth-Token          | string | Bearer or Basic Authentication Token | Yes       |

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


