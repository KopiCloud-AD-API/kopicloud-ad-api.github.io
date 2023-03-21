---
title: AD Group Membership API Methods
description: Describing all API methods of AD Group Membership 
date: 2023-03-02
---

# Manage Microsoft AD Group Membership using the KopiCloud AD API with 
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft AD Group Membership API Methods using the KopiCloud

----

## Get Active Directory Users from Group Membership

<span class="btn-get">GET</span> /api/ADUser/{Username}/Group/All

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username | string | AD User Name | Yes       |
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

## Check If a User Is a Member of an Active Directory Group

<span class="btn-get">GET</span> /api/ADUser/{Username}/Group/{GroupName}/Exists

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username | string | AD User Name | Yes       |
| GroupName | string | AD Group Name | Yes       |
| Auth-Token | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## Check If a User Is a Member of an Active Directory Group and return the AD Group

<span class="btn-get">GET</span> /api/ADUser/{Username}/Group/{GroupName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username | string | AD User Name | Yes       |
| GroupName | string | AD Group Name | Yes       |
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

## Add an Active Directory User to an Active Directory Group

<span class="btn-post">POST</span> /api/ADUser/{Username}/Group/{GroupName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username | string | AD User Name | Yes       |
| GroupName | string | AD Group Name | Yes       |
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

## Remove an Active Directory User From an Active Directory Group

<span class="btn-delete">DELETE</span> /api/ADUser/{Username}/Group/{GroupName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username | string | AD User Name | Yes       |
| GroupName | string | AD Group Name | Yes       |
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
