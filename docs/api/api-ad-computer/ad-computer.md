---
title: AD Computer API Methods
description: Describing all API methods of AD Computer
date: 2023-03-24
---

# Manage Microsoft AD Computer using the KopiCloud AD API with
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Computers in Microsoft AD using the KopiCloud AD API

----

## Get a List of All Computer Inside an Active Directory Organization Unit

<span class="btn-get">GET</span> /api/Computers

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| OUPath   | string     | Organization Unit DN Path    | No       |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| Recursive  | boolean | Recursive Search    | No      |


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

## Get and Show AD Computer Details (Operating System, Description, DNS Name, Creation Date)

<span class="btn-get">GET</span> /api/Computers/{ADComputersName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| ADComputerName   | string | AD Computer Name   | Yes      |


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

## Get and Check If AD Computer Exists with Optional Search Inside Specific OUs

<span class="btn-get">GET</span> /api/Computers/{ADComputersName}/Exists

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| ADComputerName   | string | AD Computer Name   | Yes      |


**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## Get a List of All Computers in Active Directory

<span class="btn-get">GET</span> /api/Computers/All

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |


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

## Create and Register Active Directory Computer Inside an Optional OU

<span class="btn-post">POST</span> /api/Computers/{ADComputerName}/Register

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| ADComputerName   | string | AD Computer Name   | Yes      |
| ADComputerDescription   | string | AD Computer Description (Optional)   | No      |
| OUPath   | string | Organization Unit DN Path   | No      |



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

## Rename an Active Directory Computer

<span class="btn-put">PUT</span> /api/Computers/{ADComputerName}/Rename/{NewADComputerName}

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| ADComputerName   | string | AD Computer Name   | Yes      |
| NewADComputerName    | string | New AD Computer Name   | Yes      |



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

## Update Active Directory Computer Description

<span class="btn-put">PUT</span> /api/Computers/{ADComputerName}/Update

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| ADComputerName   | string | AD Computer Name   | Yes      |
| ComputerDescription    | string | AD Computer Description | No      |



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

## Remove Active Directory Computer Inside an Optional OU

<span class="btn-delete">DELETE</span> /api/Computers/{ADComputerName}/Remove

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| ADComputerName   | string | AD Computer Name   | Yes      |



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

## CleanUp Inactive Active Directory Computers for More Than XX Days

<span class="btn-delete">DELETE</span> /api/Computers/Cleanup

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| OUPath   | string | Organization Unit DN Path   | No      |
| Days   | integer | Number of Inactive Days  | No      |
| Recursive   | boolean | Recursive Search  | No      |



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

## Remove Multiple AD Computers Using WildCard Inside an Optional OU

<span class="btn-delete">DELETE</span> /api/Computers/Remove

**Parameters**

| Name       | Type   | Description                          | Mandatory |
| ---------- | ------ | ------------------------------------ | --------- |
| Auth-Token  | string | Bearer or Basic Authentication Token   | Yes      |
| OUPath   | string | Organization Unit DN Path   | No      |
| WildCard   | integer | Wild Card for AD Computer Name  | No      |
| Recursive   | boolean | Recursive Search  | No      |



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