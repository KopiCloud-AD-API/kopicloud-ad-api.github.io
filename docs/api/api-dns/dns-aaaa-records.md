---
title: DNS AAAA Records API Methods
description: Manage Microsof DNS AAAA Records with KopiCloud AD API
---

# Manage DNS AAAA Records with KopiCloud AD API
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS AAAA Records using the KopiCloud AD API:

----

## GET /api/DnsAAAARecord/All
List All DNS AAAA Records in All Zones

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

## GET /api/DnsAAAARecord/{ZoneName}
List All DNS AAAA Records in a DNS Zone

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

## GET /api/DnsAAAARecord/HostName/{DNS_HostName}
List All DNS AAAA Records that match with DNS Hostname

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

## GET /api/DnsAAAARecord/IPv6Address/{IPv6_Address}

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

## GET /api/DnsAAAARecord
Get DNS AAAA Record that match with DNS Hostname and IPv6 Address

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

## POST /api/DnsAAAARecord
Create a DNS AAAA Records

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

## DELETE /api/DnsAAAARecord
Delete a DNS A Record

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
