---
title: AD Organization Units API Methods (OU)
description: Describing all API methods of AD Organization Units (OU)
date: 2023-03-23
---

# Manage Microsoft AD Organization Units using the KopiCloud AD API with
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft AD Organization Units API Methods using the KopiCloud

----

## Get a List of All Active Directory Organization Units

<span class="btn-get">GET</span> /api/OU/All

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| ListContainers | boolean | List All AD Containers, Including Hidden and System Containers| No       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "name": "string",
      "description": "string",
      "path": "string",
      "protected": true
    }
  ]
}
```

----

## Get the Active Directory Organization Unit Guid

<span class="btn-get">GET</span> /api/OU/Guid/Details

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUGuid  | string     | Organization Unit Guid    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token| Yes      |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "description": "string",
    "path": "string",
    "protected": true
  }
}
```

----

## Get the Active Directory Organization Unit Details

<span class="btn-get">GET</span> /api/OU/Path/Details

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath   | string     | Organization Unit DN Path    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token| Yes      |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "description": "string",
    "path": "string",
    "protected": true
  }
}
```

----

## Get and Check if the Active Directory Organization Unit Exists

<span class="btn-get">GET</span> /api/OU/Path/Exists

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath   | string     | Organization Unit DN Path    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token| Yes      |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## Create an Active Directory Organization Unit

<span class="btn-post">POST</span> /api/OU

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUName    | string     | Organization Unit Name    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token| Yes      |
| OUDestinationPath  | string  | Destination Organization Unit DN Path (Parent)   | Yes      |
| OUDescription  | string  | Organization Unit Description   | No      |
| IsProtected  | boolean  | Protect Organization Unit from Accidental Deletion   | No      |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "description": "string",
    "path": "string",
    "protected": true
  }
}
```

----

## Update an Active Directory Organization Unit

<span class="btn-put">PUT</span> /api/OU

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath     | string     | Organization Unit DN Path    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token      | Yes      |
| OUDescription  | string  | Organization Unit Description   | No      |
| IsProtected  | boolean  | Protect Organization Unit from Accidental Deletion   | No      |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "description": "string",
    "path": "string",
    "protected": true
  }
}
```

----

## Move an Active Directory Organization Unit

<span class="btn-put">PUT</span> /api/OU/Move

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath     | string     | Organization Unit DN Path    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token      | Yes      |
| OUDestinationPath   | string  | Destination Organization DN Path (New Parent OU)   | Yes      |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "description": "string",
    "path": "string",
    "protected": true
  }
}
```

----

## Rename an Active Directory Organization Unit

<span class="btn-put">PUT</span> /api/OU/Rename

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath     | string     | Organization Unit DN Path    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token      | Yes      |
| OUNewName    | string  | Organization Unit New Name   | Yes      |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "description": "string",
    "path": "string",
    "protected": true
  }
}
```

----

## Delete an Active Directory Organization Unit

<span class="btn-delete">DELETE</span> /api/OU/Path/Remove

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath     | string     | Organization Unit DN Path    | Yes       |
| Auth-Token  | string  | Bearer or Basic Authentication Token      | Yes      |
| Force    | boolean  | Force Deletion of Protected Organization Unit   | No      |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "description": "string",
    "path": "string",
    "protected": true
  }
}
```

----