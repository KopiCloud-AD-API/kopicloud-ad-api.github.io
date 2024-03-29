---
title: AD Computer API Methods
description: Describing all API methods of AD Computers
date: 2023-05-15
---

# Manage AD Computers with the KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage AD Computers in Microsoft Active Directory using the KopiCloud AD API

----

## List All AD Computers Inside an AD OU

<span class="btn-get">GET</span> /api/Computers

**Parameters**

| Name               | Type    | Description                          | Mandatory |
| ------------------ | ------- | ------------------------------------ | --------- |
| OUPath             | string  | Organization Unit DN Path            | No        |
| Recursive          | boolean | Recursive Search                     | No        |
| Auth-Token         | string  | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "sid": "string",
      "computerName": "string",
      "operatingSystem": "string",
      "description": "string",
      "dnsName": "string",
      "path": "string",
      "created": "string"
    }
  ]
}
```

----

## Show AD Computer Details

<span class="btn-get">GET</span> /api/Computers/{ADComputersName}

**Parameters**

| Name              | Type      | Description                          | Mandatory  |
| ----------------- | --------- | ------------------------------------ | ---------- |
| ADComputerName    | string    | AD Computer Name                     | Yes        |
| Auth-Token        | string    | Bearer or Basic Authentication Token | Yes        |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "sid": "string",
    "computerName": "string",
    "operatingSystem": "string",
    "description": "string",
    "dnsName": "string",
    "path": "string",
    "created": "string"
  }
}
```

----

## Check If AD Computer Exists

<span class="btn-get">GET</span> /api/Computers/{ADComputersName}/Exists

**Parameters**

| Name              | Type      | Description                          | Mandatory  |
| ----------------- | --------- | ------------------------------------ | ---------- |
| ADComputerName    | string    | AD Computer Name                     | Yes        |
| Auth-Token        | string    | Bearer or Basic Authentication Token | Yes        |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## List All AD Computers

<span class="btn-get">GET</span> /api/Computers/All

**Parameters**

| Name              | Type      | Description                          | Mandatory  |
| ----------------- | --------- | ------------------------------------ | ---------- |
| Auth-Token        | string    | Bearer or Basic Authentication Token | Yes        |


**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "sid": "string",
      "computerName": "string",
      "operatingSystem": "string",
      "description": "string",
      "dnsName": "string",
      "path": "string",
      "created": "string"
    }
  ]
}
```

----

## Register (Create) an AD Computer

<span class="btn-post">POST</span> /api/Computers/{ADComputerName}/Register

**Parameters**

| Name                    | Type      | Description                          | Mandatory  |
| ----------------------- | --------- | ------------------------------------ | ---------- |
| ADComputerName          | string    | AD Computer Name                     | Yes        |
| ADComputerDescription   | string    | AD Computer Description (Optional)   | No         |
| OUPath                  | string    | Organization Unit DN Path            | No         |
| Auth-Token              | string    | Bearer or Basic Authentication Token | Yes        |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "sid": "string",
    "computerName": "string",
    "operatingSystem": "string",
    "description": "string",
    "dnsName": "string",
    "path": "string",
    "created": "string"
  }
}
```

----

## Rename an AD Computer

<span class="btn-put">PUT</span> /api/Computers/{ADComputerName}/Rename/{NewADComputerName}

**Parameters**

| Name                    | Type      | Description                          | Mandatory  |
| ------------------------| --------- | ------------------------------------ | ---------- |
| ADComputerName          | string    | AD Computer Name                     | Yes        |
| NewADComputerName       | string    | New AD Computer Name                 | Yes        |
| Auth-Token              | string    | Bearer or Basic Authentication Token | Yes        |


**Return Schema**

```
{
  "output": "string",
  "result": {
    "sid": "string",
    "computerName": "string",
    "operatingSystem": "string",
    "description": "string",
    "dnsName": "string",
    "path": "string",
    "created": "string"
  }
}
```

----

## Update the AD Computer Description

<span class="btn-put">PUT</span> /api/Computers/{ADComputerName}/Update

**Parameters**

| Name                    | Type      | Description                          | Mandatory  |
| ----------------------- | --------- | ------------------------------------ | ---------- |
| ADComputerName          | string    | AD Computer Name                     | Yes        |
| ComputerDescription     | string    | AD Computer Description              | No         |
| Auth-Token              | string    | Bearer or Basic Authentication Token | Yes        |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "sid": "string",
    "computerName": "string",
    "operatingSystem": "string",
    "description": "string",
    "dnsName": "string",
    "path": "string",
    "created": "string"
  }
}
```

----

## Remove an AD Computer

<span class="btn-delete">DELETE</span> /api/Computers/{ADComputerName}/Remove

**Parameters**

| Name                    | Type      | Description                          | Mandatory  |
| ----------------------- | --------- | ------------------------------------ | ---------- |
| ADComputerName          | string    | AD Computer Name                     | Yes        |
| Auth-Token              | string    | Bearer or Basic Authentication Token | Yes        |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "sid": "string",
    "computerName": "string",
    "operatingSystem": "string",
    "description": "string",
    "dnsName": "string",
    "path": "string",
    "created": "string"
  }
}
```

----

## Remove Multiple AD Computers Using Wildcard

<span class="btn-delete">DELETE</span> /api/Computers/Remove

**Parameters**

| Name                    | Type      | Description                          | Mandatory  |
| ----------------------- | --------- | ------------------------------------ | ---------- |
| OUPath                  | string    | Organization Unit DN Path            | No         |
| WildCard                | integer   | Wild Card for AD Computer Name       | No         |
| Recursive               | boolean   | Recursive Search (Default = value)   | No         |
| Auth-Token              | string    | Bearer or Basic Authentication Token | Yes        |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "sid": "string",
      "computerName": "string",
      "operatingSystem": "string",
      "description": "string",
      "dnsName": "string",
      "path": "string",
      "created": "string"
    }
  ]
}
```
