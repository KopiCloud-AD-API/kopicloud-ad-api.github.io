---
title: AD User API Methods
description: Describing all API methods of AD Users
date: 2023-05-15
---

# Manage AD Users with the KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage AD Users in Microsoft Active Directory using the KopiCloud AD API

----

## Show AD User Details

<span class="btn-get">GET</span> /api/ADUser/{UserName}/Details

**Parameters**

| Name               | Type    | Description                          | Mandatory |
| ------------------ | ------- | ------------------------------------ | --------- |
| Username           | string  | AD User Name                         | Yes       |
| ShowFields         | string  | Recursive Search                     | No        |
| Auth-Token         | string  | Bearer or Basic Authentication Token | Yes       |


**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Check If AD User Exist

<span class="btn-get">GET</span> /api/ADUser/{UserName}/Exists

**Parameters**

| Name               | Type     | Description                          | Mandatory |
| ------------------ | ------   | ------------------------------------ | --------- |
| Username           | string   | AD User Name                         | Yes       |
| Auth-Token         | string   | Bearer or Basic Authentication Token | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": true
}
```

----

## Show AD User Last Logon

<span class="btn-get">GET</span> /api/ADUser/{UserName}/LastLogon

**Parameters**

| Name               | Type     | Description                          | Mandatory |
| ------------------ | ------   | ------------------------------------ | --------- |
| Username           | string   | AD User Name                         | Yes       |
| Auth-Token         | string   | Bearer or Basic Authentication Token | Yes       |


**Return Schema**

```
{
  "output": "string",
  "result": "2023-03-24T18:01:26.340Z"
}
```

----

## List AD Users Inside an OU

<span class="btn-get">GET</span> /api/ADUser/ListUsers

**Parameters**

| Name               | Type     | Description                                                                                                        | Mandatory |
| ------------------ | ------   | ------------------------------------------------------------------------------------------------------------------ | --------- |
| OUPath             | string   | Organization Unit DN Path                                                                                          | No        |
| ShowFields         | string   | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Recursive          | boolean  | Recursive Search (Default = true)                                                                                 | Yes       |
| Auth-Token         | string   | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "username": "string",
      "firstName": "string",
      "lastName": "string",
      "displayName": "string",
      "description": "string",
      "emailAddress": "string",
      "department": "string",
      "office": "string",
      "company": "string",
      "samUsername": "string",
      "initials": "string",
      "ouPath": "string",
      "changePasswordNextLogon": true,
      "passwordNeverExpired": true,
      "jobTitle": "string",
      "manager": "string",
      "streetAddress": "string",
      "streetPoBox": "string",
      "city": "string",
      "state": "string",
      "postalCode": "string",
      "country": "string",
      "officePhone": "string",
      "homePhone": "string",
      "mobilePhone": "string",
      "profilePath": "string",
      "profileLogonScript": "string",
      "homeFolderPath": "string",
      "homeFolderDrive": "string",
      "homeFolderDirectory": "string",
      "rdsProfilePath": "string",
      "rdsHomeFolderPath": "string",
      "rdsHomeFolderDrive": "string",
      "rdsConnectDrive": true,
      "rdsAllowLogon": true,
      "_IncludeAllProperties": true,
      "_ShowFields": [
        "string"
      ]
    }
  ]
}
```

----

## List All AD Users

<span class="btn-get">GET</span> /api/ADUser/ListUsers/All

**Parameters**

| Name       | Type    | Description                                                                                   | Mandatory |
| ---------- | ------- | --------------------------------------------------------------------------------------------- | --------- |
| ShowFields | string  | Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token | string  | Bearer or Basic Authentication Token                                                          | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": [
    {
      "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "username": "string",
      "firstName": "string",
      "lastName": "string",
      "displayName": "string",
      "description": "string",
      "emailAddress": "string",
      "department": "string",
      "office": "string",
      "company": "string",
      "samUsername": "string",
      "initials": "string",
      "ouPath": "string",
      "changePasswordNextLogon": true,
      "passwordNeverExpired": true,
      "jobTitle": "string",
      "manager": "string",
      "streetAddress": "string",
      "streetPoBox": "string",
      "city": "string",
      "state": "string",
      "postalCode": "string",
      "country": "string",
      "officePhone": "string",
      "homePhone": "string",
      "mobilePhone": "string",
      "profilePath": "string",
      "profileLogonScript": "string",
      "homeFolderPath": "string",
      "homeFolderDrive": "string",
      "homeFolderDirectory": "string",
      "rdsProfilePath": "string",
      "rdsHomeFolderPath": "string",
      "rdsHomeFolderDrive": "string",
      "rdsConnectDrive": true,
      "rdsAllowLogon": true,
      "_IncludeAllProperties": true,
      "_ShowFields": [
        "string"
      ]
    }
  ]
}
```

----

## Create AD User

<span class="btn-post">POST</span> /api/ADUser/{UserName}

**Parameters**

| Name                    | Type    | Description                                                                                                        | Mandatory |
| ----------------------- | ------- | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username                | string  | AD User Name                                                                                                       | Yes       |
| Password                | string  | User Password                                                                                                      | No        |
| FirstName               | string  | AD User First Name                                                                                                 | No        |
| Initials                | string  | AD User Initials                                                                                                   | No        |
| LastName                | string  | AD User LastName                                                                                                   | No        |
| DisplayName             | string  | User DisplayName                                                                                                   | No        |
| Description             | string  | User Description                                                                                                   | No        |
| EmailAddress            | string  | User Email Address                                                                                                 | No        |
| Department              | string  | User Department                                                                                                    | No        |
| Office                  | string  | User Office                                                                                                        | No        |
| Company                 | string  | User Company                                                                                                       | No        |
| OUPath                  | string  | Organization Unit DN Path                                                                                          | No        |
| ChangePasswordNextLogon | boolean | User Must Change Password at Next Logon (Default = true)                                                           | No        |
| PasswordNeverExpired    | boolean | Password never expire. (Default = false)                                                                           | No        |
| JobTitle                | string  | AD User Job Title                                                                                                  | No        |
| Manager                 | string  | AD User Manager                                                                                                    | No        |
| Street                  | string  | AD User Street                                                                                                     | No        |
| POBox                   | string  | AD User Po Box                                                                                                     | No        |
| City                    | string  | AD User City                                                                                                       | No        |
| State                   | string  | AD User State                                                                                                      | No        |
| ZipCode                 | string  | AD User Zip Code                                                                                                   | No        |
| Country                 | string  | AD User Country                                                                                                    | No        |
| OfficePhone             | string  | AD User Office Phone                                                                                               | No        |
| HomePhone               | string  | AD User Home Phone                                                                                                 | No        |
| MobilePhone             | string  | AD User Mobile Phone                                                                                               | No        |
| ProfilePath             | string  | AD User Profile Path                                                                                               | No        |
| ProfileLogonScript      | string  | AD User Profile Logon Script                                                                                       | No        |
| HomeFolderPath          | string  | AD User Home Folder Path                                                                                           | No        |
| HomeFolderDrive         | string  | AD User Home Folde rDrive                                                                                          | No        |
| HomeFolderDirectory     | string  | AD User Home Folder Directory                                                                                      | No        |
| RdsProfilePath          | string  | AD User Rds Profile Path                                                                                           | No        |
| RdsHomeFolderPath       | string  | AD User Rds Home Folder Path                                                                                       | No        |
| RdsHomeFolderDrive      | string  | AD User Rds Home Folder Drive                                                                                      | No        |
| RdsConnectDrive         | boolean | AD User Rds Connect Drive (Default = false)                                                                        | No        |
| RdsAllowLogon           | string  | AD User Allow RDS Logon (Default = true)                                                                           | No        |
| ShowFields              | string  | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token              | string  | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Update AD User

<span class="btn-put">PUT</span> /api/ADUser/{UserName}

**Parameters**

| Name                    | Type    | Description                                                                                                        | Mandatory |
| ----------------------- | ------- | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username                | string  | AD User Name                                                                                                       | Yes       |
| Password                | string  | User Password                                                                                                      | No        |
| FirstName               | string  | AD User First Name                                                                                                 | No        |
| Initials                | string  | AD User Initials                                                                                                   | No        |
| LastName                | string  | AD User LastName                                                                                                   | No        |
| DisplayName             | string  | User DisplayName                                                                                                   | No        |
| Description             | string  | User Description                                                                                                   | No        |
| EmailAddress            | string  | User Email Address                                                                                                 | No        |
| Department              | string  | User Department                                                                                                    | No        |
| Office                  | string  | User Office                                                                                                        | No        |
| Company                 | string  | User Company                                                                                                       | No        |
| OUPath                  | string  | Organization Unit DN Path                                                                                          | No        |
| ChangePasswordNextLogon | boolean | User Must Change Password at Next Logon (Default = true)                                                           | No        |
| PasswordNeverExpired    | boolean | Password never expire. (Default = false)                                                                           | No        |
| JobTitle                | string  | AD User Job Title                                                                                                  | No        |
| Manager                 | string  | AD User Manager                                                                                                    | No        |
| Street                  | string  | AD User Street                                                                                                     | No        |
| POBox                   | string  | AD User Po Box                                                                                                     | No        |
| City                    | string  | AD User City                                                                                                       | No        |
| State                   | string  | AD User State                                                                                                      | No        |
| ZipCode                 | string  | AD User Zip Code                                                                                                   | No        |
| Country                 | string  | AD User Country                                                                                                    | No        |
| OfficePhone             | string  | AD User Office Phone                                                                                               | No        |
| HomePhone               | string  | AD User Home Phone                                                                                                 | No        |
| MobilePhone             | string  | AD User Mobile Phone                                                                                               | No        |
| ProfilePath             | string  | AD User Profile Path                                                                                               | No        |
| ProfileLogonScript      | string  | AD User Profile Logon Script                                                                                       | No        |
| HomeFolderPath          | string  | AD User Home Folder Path                                                                                           | No        |
| HomeFolderDrive         | string  | AD User Home Folde rDrive                                                                                          | No        |
| HomeFolderDirectory     | string  | AD User Home Folder Directory                                                                                      | No        |
| RdsProfilePath          | string  | AD User Rds Profile Path                                                                                           | No        |
| RdsHomeFolderPath       | string  | AD User Rds Home Folder Path                                                                                       | No        |
| RdsHomeFolderDrive      | string  | AD User Rds Home Folder Drive                                                                                      | No        |
| RdsConnectDrive         | boolean | AD User Rds Connect Drive (Default = false)                                                                        | No        |
| RdsAllowLogon           | string  | AD User Allow RDS Logon (Default = true)                                                                           | No        |
| ShowFields              | string  | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token              | string  | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Disable AD User

<span class="btn-put">PUT</span> /api/ADUser/{UserName}/Disable

**Parameters**

| Name        | Type   | Description                                                                                                        | Mandatory |
| ----------- | ------ | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username    | string | AD User Name                                                                                                       | Yes       |
| ShowFields  | string | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token  | string | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Enable AD User

<span class="btn-put">PUT</span> /api/ADUser/{UserName}/Enable

**Parameters**

| Name       | Type   | Description                                                                                                        | Mandatory |
| ---------- | ------ | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username   | string | AD User Name                                                                                                       | Yes       |
| ShowFields | string | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token | string | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Rename AD User

<span class="btn-put">PUT</span> /api/ADUser/{UserName}/Rename/{NewUserName}

**Parameters**

| Name           | Type    | Description                                                                                                        | Mandatory |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username       | string  | AD User Name                                                                                                       | Yes       |
| NewUsername    | string  | New AD User Name                                                                                                   | No        |
| ShowFields     | string  | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token     | string  | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Reset AD User Password

<span class="btn-put">PUT</span> /api/ADUser/{UserName}/ResetPassword

**Parameters**

| Name           | Type    | Description                                                                                                        | Mandatory |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username       | string  | AD User Name                                                                                                       | Yes       |
| newPassword    | string  | New User Password                                                                                                  | No        |
| ChangePassword | boolean | Force User to Change Password on Next Login (Default = false)                                                      | No        |
| ShowFields     | string  | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token     | string  | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Unlock AD User

<span class="btn-put">PUT</span> /api/ADUser/{UserName}/Unlock

**Parameters**

| Name       | Type   | Description                                                                                                        | Mandatory |
| ---------- | ------ | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username   | string | AD User Name                                                                                                       | Yes       |
| ShowFields | string | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token | string | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```

----

## Delete AD User

<span class="btn-delete">DELETE</span> /api/ADUser/{UserName}

**Parameters**

| Name       | Type   | Description                                                                                                        | Mandatory |
| ---------- | ------ | ------------------------------------------------------------------------------------------------------------------ | --------- |
| Username   | string | AD User Name                                                                                                       | Yes       |
| ShowFields | string | User Fields to show. Optional argument: comma-separated string with the name of the fields you want to be returned | No        |
| Auth-Token | string | Bearer or Basic Authentication Token                                                                               | Yes       |

**Return Schema**

```
{
  "output": "string",
  "result": {
    "guid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "username": "string",
    "firstName": "string",
    "lastName": "string",
    "displayName": "string",
    "description": "string",
    "emailAddress": "string",
    "department": "string",
    "office": "string",
    "company": "string",
    "samUsername": "string",
    "initials": "string",
    "ouPath": "string",
    "changePasswordNextLogon": true,
    "passwordNeverExpired": true,
    "jobTitle": "string",
    "manager": "string",
    "streetAddress": "string",
    "streetPoBox": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "officePhone": "string",
    "homePhone": "string",
    "mobilePhone": "string",
    "profilePath": "string",
    "profileLogonScript": "string",
    "homeFolderPath": "string",
    "homeFolderDrive": "string",
    "homeFolderDirectory": "string",
    "rdsProfilePath": "string",
    "rdsHomeFolderPath": "string",
    "rdsHomeFolderDrive": "string",
    "rdsConnectDrive": true,
    "rdsAllowLogon": true,
    "_IncludeAllProperties": true,
    "_ShowFields": [
      "string"
    ]
  }
}
```
