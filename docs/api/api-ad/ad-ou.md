---
title: AD Organization Unit (OU) API Methods
description: Describing all API methods of AD Organization Units (OUs)
date: 2023-05-15
---

# Manage AD OUs with the KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage AD Organization Units (OUs) in Microsoft Active Directory using the KopiCloud AD API

----

## List All AD OUs

<span class="btn-get">GET</span> /api/OU/All

**Parameters**

| Name           | Type    | Description                                                                      | Mandatory |
| -------------- | ------- | -------------------------------------------------------------------------------- | --------- |
| ListContainers | boolean | List All AD Containers, Including Hidden and System Containers (Default = value) | No        |
| Auth-Token     | string  | Bearer or Basic Authentication Token                                             | Yes       |

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

## Get AD OU Details using the GUID

<span class="btn-get">GET</span> /api/OU/Guid/Details

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUGuid     | string | Organization Unit Guid               | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

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

## Get AD OU Details using the OU Path

<span class="btn-get">GET</span> /api/OU/Path/Details

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath     | string | Organization Unit DN Path            | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

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

## Check If the AD OU Exists

<span class="btn-get">GET</span> /api/OU/Path/Exists

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath     | string | Organization Unit DN Path            | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## Create an AD OU

<span class="btn-post">POST</span> /api/OU

**Parameters**

| Name              | Type    | Description                                                           | Mandatory |
| ----------------- | ------- | --------------------------------------------------------------------- | --------- |
| OUName            | string  | Organization Unit Name                                                | Yes       |
| OUDestinationPath | string  | Destination Organization Unit DN Path (Parent)                        | Yes       |
| OUDescription     | string  | Organization Unit Description                                         | No        |
| IsProtected       | boolean | Protect Organization Unit from Accidental Deletion (Default = value)  | No        |
| Auth-Token        | string  | Bearer or Basic Authentication Token                                  | Yes       |

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

## Update an AD OU

<span class="btn-put">PUT</span> /api/OU

**Parameters**

| Name          | Type    | Description                                                           | Mandatory |
| ------------- | ------- | --------------------------------------------------------------------- | --------- |
| OUPath        | string  | Organization Unit DN Path                                             | Yes       |
| OUDescription | string  | Organization Unit Description                                         | No        |
| IsProtected   | boolean | Protect Organization Unit from Accidental Deletion (Default = value)  | No        |
| Auth-Token    | string  | Bearer or Basic Authentication Token                                  | Yes       |

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

## Move an AD OU

<span class="btn-put">PUT</span> /api/OU/Move

**Parameters**

| Name              | Type   | Description                                      | Mandatory |
| ----------------- | ------ | ------------------------------------------------ | --------- |
| OUPath            | string | Organization Unit DN Path                        | Yes       |
| OUDestinationPath | string | Destination Organization DN Path (New Parent OU) | Yes       |
| Auth-Token        | string | Bearer or Basic Authentication Token             | Yes       |

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

## Rename an AD OU

<span class="btn-put">PUT</span> /api/OU/Rename

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath     | string | Organization Unit DN Path            | Yes       |
| OUNewName  | string | Organization Unit New Name           | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

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

## Delete an AD OU

<span class="btn-delete">DELETE</span> /api/OU/Path/Remove

**Parameters**

| Name       | Type    | Description                                                      | Mandatory |
| ---------- | ------- | ---------------------------------------------------------------- | --------- |
| OUPath     | string  | Organization Unit DN Path                                        | Yes       |
| Force      | boolean | Force Deletion of Protected Organization Unit (Default = value)  | No        |
| Auth-Token | string  | Bearer or Basic Authentication Token                             | Yes       |

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
