---
title: DNS A Records API Methods
description: Manage Microsoft DNS A Records with KopiCloud AD API
date: 2023-05-15
---

# Manage DNS A Records with KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage Microsoft DNS A Records using the KopiCloud AD API.

----

## Get DNS A Record that match with DNS Hostname and IP Address
<span class="btn-get">GET</span> /api/DnsARecord

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName | string | DNS Host Name                        | Yes       |
| IP_Address   | string | IP Address                           | Yes       |
| ZoneName     | string | DNS Zone Name                        | Yes       |
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

## List All DNS A Records in a DNS Zone
<span class="btn-get">GET</span> /api/DnsARecord/{ZoneName}

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

## List All DNS A Records in All Zones
<span class="btn-get">GET</span> /api/DnsARecord/All

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

## List All DNS A Records that match with DNS Hostname
<span class="btn-get">GET</span> /api/DnsARecord/HostName/{DNS_HostName}

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

## List All DNS A Records that match with IP Address
<span class="btn-get">GET</span> /api/DnsARecord/IPAddress/{IP_Address}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| IP_Address | string | IP Address                           | Yes       |
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


## Create a DNS A Records
<span class="btn-post">POST</span> /api/DnsARecord

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName | string | DNS Host Name                        | Yes       |
| IP_Address   | string | IP Address                           | Yes       |
| ZoneName     | string | DNS Zone Name                        | Yes       |
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

## Delete a DNS A Record
<span class="btn-delete">DELETE</span> /api/DnsARecord

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName | string | DNS Host Name                        | Yes       |
| IP_Address   | string | IP Address                           | Yes       |
| ZoneName     | string | DNS Zone Name                        | Yes       |
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
