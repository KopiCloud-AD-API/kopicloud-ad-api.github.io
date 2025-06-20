---
title: AD Group Membership API Methods
description: Describing all API methods of AD Group Membership
date: 2025-05-25
---

# Manage AD Group Membership with the KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage AD Group Membership in Microsoft Active Directory using the KopiCloud AD API

----

## Check If a User Is a Member of an AD Group and return the AD Group

<span class="btn-get">GET</span> /api/ADUser/{Username}/Group/{GroupName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username   | string | AD User Name                         | Yes       |
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

## Check If an AD User Is a Member of an AD Group

<span class="btn-get">GET</span> /api/ADUser/{Username}/Group/{GroupName}/Exists

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username   | string | AD User Name                         | Yes       |
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

## Get AD User Group Membership

<span class="btn-get">GET</span> /api/ADUser/{Username}/Group/All

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username   | string | AD User Name                         | Yes       |
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

## Add an AD User to an AD Group

<span class="btn-post">POST</span> /api/ADUser/{Username}/Group/{GroupName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username   | string | AD User Name                         | Yes       |
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

## Remove an AD User from an AD Group

<span class="btn-delete">DELETE</span> /api/ADUser/{Username}/Group/{GroupName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Username   | string | AD User Name                         | Yes       |
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

## Add an AD Group to an AD Group [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.2+-blueviolet.svg)](https://adapi.kopicloud.com)

<span class="btn-post">POST</span> /api/ADGroup/{ParentGroupName}/Group/{ChildGroupName}

**Parameters**

| Name            | Type   | Description                          | Mandatory |
| --------------- | ------ | ------------------------------------ | --------- |
| ParentGroupName | string | Parent AD Group Name                 | Yes       |
| ChildGroupName  | string | Child AD Group Name                  | Yes       |
| Auth-Token      | string | Bearer or Basic Authentication Token | Yes       |

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

## Remove an AD Group Name from an AD Group Name [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.2+-blueviolet.svg)](https://adapi.kopicloud.com)

<span class="btn-delete">DELETE</span> /api/ADGroup/{ParentGroupName}/Group/{ChildGroupName}

**Parameters**

| Name            | Type   | Description                          | Mandatory |
| --------------- | ------ | ------------------------------------ | --------- |
| ParentGroupName | string | Parent AD Group Name                 | Yes       |
| ChildGroupName  | string | Child AD Group Name                  | Yes       |
| Auth-Token      | string | Bearer or Basic Authentication Token | Yes       |

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

## Check If an AD Group Is a Member of an AD Group [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.2+-blueviolet.svg)](https://adapi.kopicloud.com)

<span class="btn-get">GET</span> /api/ADGroup/{ParentGroupName}/Group/{ChildGroupName}/Exists

**Parameters**

| Name            | Type   | Description                          | Mandatory |
| --------------- | ------ | ------------------------------------ | --------- |
| ParentGroupName | string | Parent AD Group Name                 | Yes       |
| ChildGroupName  | string | Child AD Group Name                  | Yes       |
| Auth-Token      | string | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----
