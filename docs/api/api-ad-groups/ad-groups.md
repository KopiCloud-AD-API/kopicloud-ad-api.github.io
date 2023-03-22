---
title: AD Groups API Methods
description: Describing all API methods of AD Groups 
date: 2023-03-22
---

# Manage Microsoft AD Groups using the KopiCloud AD API with 
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft AD Groups API Methods using the KopiCloud

----

## Get a List of Active Directory Groups Inside an OU (Review)

<span class="btn-get">GET</span> /api/ADGroups


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath | string | Organization Unit DN Path| No       |
| Recursive | boolean | Recursive Search| No       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |

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

## Get an AD Group Details (Name, Description, Path, Type and Scope)

<span class="btn-get">GET</span> /api/ADGroups/{GroupName}


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| GroupName  | string | AD Group Name| Yes       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |

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

## Get and Check if the Active Directory Organization Unit Exists

<span class="btn-get">GET</span> /api/ADGroups/{GroupName}/Exists


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| GroupName  | string | AD Group Name| Yes       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## Get a List of All Active Directory Groups

<span class="btn-get">GET</span> /api/ADGroups/All


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |

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

## Get a List of Active Directory Distribution Groups

<span class="btn-get">GET</span> /api/ADGroups/Distribution/All


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath | string | Organization Unit DN Path| No       |
| Recursive | boolean | Recursive Search| No       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |

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

## Get a List of Active Directory Security Groups

<span class="btn-get">GET</span> /api/ADGroups/Security/All


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath | string | Organization Unit DN Path| No       |
| Recursive | boolean | Recursive Search| No       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |

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

## Create an Active Directory Distribution Group, Optional Set the OU to Create it or Create in the Default Users OU

<span class="btn-post">POST</span> /api/ADGroups/{GroupName}/Distribution


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath | string | Organization Unit DN Path| No       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |
| GroupName | string | AD Group Name  | Yes   |
| GroupScope | string | AD GroupScope| No      |
| GroupDescription  | string | AD Group Description| No      |
| GroupEmail  | string | AD Group Email| No      |

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
## Create an Active Directory Security Group, Optional Set the OU to Create it or Create in the Default Users OU

<span class="btn-post">POST</span> /api/ADGroups/{GroupName}/Security


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath | string | Organization Unit DN Path| No       |
| Auth-Token  | string | Bearer or Basic Authentication Token| Yes      |
| GroupName | string | AD Group Name  | Yes   |
| GroupScope | string | AD GroupScope| No      |
| GroupDescription  | string | AD Group Description| No      |
| GroupEmail  | string | AD Group Email| No      |

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

## Rename an Active Directory Group, Optional Set the OU to Create it or Create in the Default Users OU

<span class="btn-put">PUT</span> /api/ADGroups/{GroupName}/Rename/{NewGroupName}


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath | string | Organization Unit DN Path| Yes       |
| NewGroupName  | string | Bearer or Basic Authentication Token| Yes      |
| GroupName | string | AD Group Name  | Yes   |

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

## Delete an Active Directory Group, Optional Set the OU to Create it or Create in the Default Users OU

<span class="btn-delete">DELETE</span> /api/ADGroups/{GroupName}/Remove


**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath | string | Organization Unit DN Path| No       |
| Auth-Token   | string | Bearer or Basic Authentication Token| Yes      |
| GroupName | string | AD Group Name  | Yes   |

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

