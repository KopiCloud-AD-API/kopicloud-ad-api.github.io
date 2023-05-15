---
title: AD Group API Methods
description: Describing all API methods of AD Groups 
date: 2023-05-15
---

# Manage AD Groups with the KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Groups in Microsoft Active Directory using the KopiCloud AD API

----

## List AD Groups Inside an OU

<span class="btn-get">GET</span> /api/ADGroups

**Parameters**

| Name       | Type    | Description                          | Mandatory |
| ---------- | ------- | ------------------------------------ | --------- |
| OUPath     | string  | Organization Unit DN Path            | No        |
| Recursive  | boolean | Recursive Search (Default = value)   | No        |
| Auth-Token | string  | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "name": "string",
      "scope": "Global",
      "description": "string",
      "email": "string",
      "ouPath": "string",
      "type": "string"
    }
  ]
}
```

----

## Show AD Group Details

<span class="btn-get">GET</span> /api/ADGroups/{GroupName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| GroupName  | string | AD Group Name                        | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "scope": "Global",
    "description": "string",
    "email": "string",
    "ouPath": "string",
    "type": "string"
  }
}
```

----

## Check If an AD Group Exists

<span class="btn-get">GET</span> /api/ADGroups/{GroupName}/Exists

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| GroupName  | string | AD Group Name                        | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## Get a List of All AD Groups

<span class="btn-get">GET</span> /api/ADGroups/All

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
      "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "name": "string",
      "scope": "Global",
      "description": "string",
      "email": "string",
      "ouPath": "string",
      "type": "string"
    }
  ]
}
```

----

## List All AD Distribution Groups

<span class="btn-get">GET</span> /api/ADGroups/Distribution/All

**Parameters**

| Name       | Type    | Description                          | Mandatory |
| ---------- | ------- | ------------------------------------ | --------- |
| OUPath     | string  | Organization Unit DN Path            | No        |
| Recursive  | boolean | Recursive Search (Default = value)   | No        |
| Auth-Token | string  | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "name": "string",
      "scope": "Global",
      "description": "string",
      "email": "string",
      "ouPath": "string",
      "type": "string"
    }
  ]
}
```

----

## List All AD Security Groups

<span class="btn-get">GET</span> /api/ADGroups/Security/All

**Parameters**

| Name       | Type    | Description                          | Mandatory |
| ---------- | ------- | ------------------------------------ | --------- |
| OUPath     | string  | Organization Unit DN Path            | No        |
| Recursive  | boolean | Recursive Search (Default = value)   | No        |
| Auth-Token | string  | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "name": "string",
      "scope": "Global",
      "description": "string",
      "email": "string",
      "ouPath": "string",
      "type": "string"
    }
  ]
}
```

----

## Create an AD Distribution Group

>**Note:** Optional set the OU where to create the group or create it in the default Users OU

<span class="btn-post">POST</span> /api/ADGroups/{GroupName}/Distribution

**Parameters**

| Name             | Type   | Description                          | Mandatory |
| ---------------- | ------ | ------------------------------------ | --------- |
| OUPath           | string | Organization Unit DN Path            | No        |
| GroupName        | string | AD Group Name                        | Yes       |
| GroupScope       | string | AD GroupScope                        | No        |
| GroupDescription | string | AD Group Description                 | No        |
| GroupEmail       | string | AD Group Email                       | No        |
| Auth-Token       | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "scope": "Global",
    "description": "string",
    "email": "string",
    "ouPath": "string",
    "type": "string"
  }
}
```

----
## Create an AD Security Group

>**Note:** Optional set the OU where to create the group or create it in the default Users OU

<span class="btn-post">POST</span> /api/ADGroups/{GroupName}/Security

**Parameters**

| Name             | Type   | Description                          | Mandatory |
| ---------------- | ------ | ------------------------------------ | --------- |
| OUPath           | string | Organization Unit DN Path            | No        |
| GroupName        | string | AD Group Name                        | Yes       |
| GroupScope       | string | AD GroupScope                        | No        |
| GroupDescription | string | AD Group Description                 | No        |
| GroupEmail       | string | AD Group Email                       | No        |
| Auth-Token       | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "scope": "Global",
    "description": "string",
    "email": "string",
    "ouPath": "string",
    "type": "string"
  }
}
```

----

## Rename an AD Group

<span class="btn-put">PUT</span> /api/ADGroups/{GroupName}/Rename/{NewGroupName}

**Parameters**

| Name         | Type   | Description                          | Mandatory |
| ------------ | ------ | ------------------------------------ | --------- |
| GroupName    | string | AD Group Name                        | Yes       |
| NewGroupName | string | New AD Group Name                    | Yes       |
| Auth-Token   | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "scope": "Global",
    "description": "string",
    "email": "string",
    "ouPath": "string",
    "type": "string"
  }
}
```

----

## Delete an AD Group

<span class="btn-delete">DELETE</span> /api/ADGroups/{GroupName}/Remove

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| GroupName  | string | AD Group Name                        | Yes       |
| OUPath     | string | Organization Unit DN Path            | No        |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "name": "string",
    "scope": "Global",
    "description": "string",
    "email": "string",
    "ouPath": "string",
    "type": "string"
  }
}
```
