---
title: DNS AAAA Records API Methods
description: Manage Microsoft DNS AAAA Records with KopiCloud AD API
date: 2023-05-15
---

# Manage DNS AAAA Records with KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage Microsoft DNS AAAA Records using the KopiCloud AD API.

----

## Get DNS AAAA Record that match with DNS Hostname and IPv6 Address
<span class="btn-get">GET</span> /api/DnsAAAARecord

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName | string | DNS Host Name                        | Yes       |
| IPv6_Address | string | IPv6 Address                         | Yes       |
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

## List All DNS AAAA Records in a DNS Zone
<span class="btn-get">GET</span> /api/DnsAAAARecord/{ZoneName}

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

## List All DNS AAAA Records in All Zones
<span class="btn-get">GET</span> /api/DnsAAAARecord/All

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

## List All DNS AAAA Records that match with DNS Hostname
<span class="btn-get">GET</span> /api/DnsAAAARecord/HostName/{DNS_HostName}

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

## List All DNS AAAA Records that match with IPv6 Address
<span class="btn-get">GET</span> /api/DnsAAAARecord/IPv6Address/{IPv6_Address}

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| IPv6_Address | string | IPv6 Address                         | Yes       |
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


## Create a DNS AAAA Records
<span class="btn-post">POST</span> /api/DnsAAAARecord

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName | string | DNS Host Name                        | Yes       |
| IPv6_Address | string | IPv6 Address                         | Yes       |
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

## Delete a DNS AAAA Record
<span class="btn-delete">DELETE</span> /api/DnsAAAARecord


**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| DNS_HostName | string | DNS Host Name                        | Yes       |
| IPv6_Address | string | IPv6 Address                         | Yes       |
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
