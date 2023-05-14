---
title: DNS CNAME Records API Methods
description: Manage Microsoft DNS CNAME Records with KopiCloud AD API
date: 2023-05-15
---

# Manage DNS CNAME Records with KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS CNAME Records using the KopiCloud AD API.

----

## List All DNS CNAME Records in All Zones
<span class="btn-get">GET</span> /api/DnsCNameRecord/All

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**
```
{
  "output": "string",
  "result": [
    {
      "name": "string",
      "type": "string",
      "data": "string",
      "zone": "string",
      "timestamp": "string"
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
      "name": "string",
      "type": "string",
      "data": "string",
      "zone": "string",
      "timestamp": "string"
    }
  ]
}
```

----

## List All DNS CNAME Records that match with DNS Hostname
<span class="btn-get">GET</span> /api/DnsCNameRecord/HostName/{DNS_HostName}

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName | string | DNS Host Name                        | Yes       |
| Auth-Token   | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "name": "string",
      "type": "string",
      "data": "string",
      "zone": "string",
      "timestamp": "string"
    }
  ]
}
```

----

## List All DNS CNAME Records that match with DNS HostName Alias
<span class="btn-get">GET</span> /api/DnsCNameRecord/HostNameAlias/{DNS_HostName_Alias}

**Parameters**

| Name               | Type   | Description                          | Mandatory |
| ------------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName_Alias | string | DNS Host Name Alias                  | Yes       |
| Auth-Token         | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "name": "string",
      "type": "string",
      "data": "string",
      "zone": "string",
      "timestamp": "string"
    }
  ]
}
```

----

## Get DNS CNAME Record that match with DNS HostName and Alias
<span class="btn-get">GET</span> /api/DnsCNameRecord

**Parameters**

| Name               | Type   | Description                          | Mandatory |
| ------------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName       | string | DNS Host Name                        | Yes       |
| DNS_HostName_Alias | string | DNS Host Name Alias                  | Yes       |
| ZoneName           | string | DNS Zone Name                        | Yes       |
| Auth-Token         | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "name": "string",
      "type": "string",
      "data": "string",
      "zone": "string",
      "timestamp": "string"
    }
  ]
}
```

----

## Create a DNS CNAME Records
<span class="btn-post">POST</span> /api/DnsCNameRecord

**Parameters**

| Name               | Type   | Description                          | Mandatory |
| ------------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName       | string | DNS Host Name                        | Yes       |
| DNS_HostName_Alias | string | DNS Host Name Alias                  | Yes       |
| ZoneName           | string | DNS Zone Name                        | Yes       |
| Auth-Token         | string | Bearer or Basic Authentication Token | Yes       |


**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "name": "string",
      "type": "string",
      "data": "string",
      "zone": "string",
      "timestamp": "string"
    }
  ]
}
```

----

## Delete a DNS CNAME Record
<span class="btn-delete">DELETE</span> /api/DnsCNameRecord

**Parameters**

| Name               | Type   | Description                          | Mandatory |
| ------------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName       | string | DNS Host Name                        | Yes       |
| DNS_HostName_Alias | string | DNS Host Name Alias                  | Yes       |
| ZoneName           | string | DNS Zone Name                        | Yes       |
| Auth-Token         | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "name": "string",
      "type": "string",
      "data": "string",
      "zone": "string",
      "timestamp": "string"
    }
  ]
}
```
