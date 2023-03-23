---
title: Welcome to KopiCloud AD API
description: Welcome to KopiCloud AD API
date: 2023-03-01
---

# KopiCloud AD API Security Group Matrix

## AD User

| <div style="width:200px">API Method</div> | <div style="width:50px">API<br />Group</div> | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| _________________________________ | ___ | ___ | ___ | ___ | ___ | ___ |
| --------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / List of ALL Users           | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / List of Users Inside an OU  | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Get User Details            | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Get User Details By Guid    | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Check If User Exist         | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Get Last Logon              | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Create New User            | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Update User                 | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Update User by Guid         | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Reset User Password         | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Enable User                 | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Disable User                | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Unlock User                 | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Rename User                 | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Delete User              | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Delete User by Guid      | Yes       | Yes      | No        | No          | Yes         | No             |

----

## AD Computer

| API Method                             | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ---------------------------------------| --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / List ALL Computers               | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / List Computers inside an AD OU   | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Show Computer Details            | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Check If Computer Exists         | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Register Computer               | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Rename Computer                  | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Update Computer Description      | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Remove Computer               | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Remove Multiple Computer      | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / CleanUp Inactive AD Computers | Yes       | Yes      | No        | No          | Yes         | No             |

----

## AD Group

| API Method                | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / List ALl Groups                                               | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / List Groups Inside OU                                         | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / List All Distribution Groups                                  | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / List All Security Groups                                      | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Show Group Details                                            | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Group Exists                                                  | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Create Security Group                                        | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Create Distribution Group                                    | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Rename Group                                                  | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Delete Group                                               | Yes       | Yes      | No        | No          | Yes         | No             |

----

## AD Group Membership

| API Method                | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / AD User Group Membership                                      | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Check If User is a Member of a Group                          | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Add User to Specific Group                                   | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Remove User from Specific Group                            | Yes       | Yes      | No        | No          | Yes         | No             |

----

## AD OU

| API Method                | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / List All AD OUs                                               | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / AD OU Details by OUPath                                       | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / AD OU Details by Guid                                         | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / AD OU Exists                                                  | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Create AD OU                                                 | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Rename AD OU                                                  | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Update AD OU                                                  | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Move AD OU                                                    | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Delete AD OU                                               | Yes       | Yes      | No        | No          | Yes         | No             |

----

## DNS AAAA Record

Manage DNS AAAA records.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------- | --- | -- | --- | -- | --- | -- |
| List All DNS AAAA Records | Yes | No | Yes | No | Yes | No |
| Create a DNS AAAA Records | Yes | No | Yes | No | Yes | No |
| Delete a DNS AAAA Records | Yes | No | Yes | No | Yes | No |

----

## DNS A Record

Manage DNS A records.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ---------------------- | --- | -- | --- | -- | --- | -- |
| List All DNS A Records | Yes | No | Yes | No | Yes | No |
| Create a DNS A Records | Yes | No | Yes | No | Yes | No |
| Delete a DNS A Records | Yes | No | Yes | No | Yes | No |

----

## DNS CNAME Record

Manage DNS CNAME records.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| -------------------------- | --- | -- | --- | -- | --- | -- |
| List All DNS CNAME Records | Yes | No | Yes | No | Yes | No |
| Create a DNS CNAME Records | Yes | No | Yes | No | Yes | No |
| Delete a DNS CNAME Records | Yes | No | Yes | No | Yes | No |

----

## DNS Zone

Manage DNS zones.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------------------------------------| --------- | -------- | --------- | ----------- | ----------- | -------------- |
| Check If DNS Zone Exists                              | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS Zones                                    | Yes       | No       | Yes       | No          | Yes         | No             |
| Get DNS Zone by Name                                  | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS Lookup Zones                             | Yes       | No       | Yes       | No          | Yes         | No             |
| Create a DNS Lookup Zone                              | Yes       | No       | Yes       | No          | Yes         | No             |
| Delete a DNS Lookup Zone                              | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS Reverse Lookup Zones                     | Yes       | No       | Yes       | No          | Yes         | No             |
| Get DNS Reverse Lookup Zone by NetworkID or Zone Name | Yes       | No       | Yes       | No          | Yes         | No             |
| Create a DNS Reverse Lookup Zone NetworkID            | Yes       | No       | Yes       | No          | Yes         | No             |
| Delete a DNS Reverse Lookup Zone                      | Yes       | No       | Yes       | No          | Yes         | No             |

----

## Token Management

Create, list, enable, disable and delete authentication tokens.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| --------------------------| --------- | -------- | --------- | ----------- | ----------- | -------------- |
| Generate JWT Bearer Token | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| Generate Basic Token      | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| List OWN Tokens           | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| List ALL Tokens           | No        | No       | No        | Yes         | Yes         | Yes            |
| Enable/Disable OWN Tokens | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| Enable/Disable ALL Tokens | No        | No       | No        | Yes         | Yes         | Yes            |
| Delete Token              | No        | No       | No        | Yes         | Yes         | Yes            |

----

## Event Log

Review the KopiCloud AD API Event Log.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| -------------- | -- | -- | -- | -- | --- | --- |
| Show Event Log | No | No | No | No | Yes | Yes |

----

## License Management

Configure the KopiCloud AD API License.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
| ------------- | -- | -- | -- | -- | --- | --- |
| Read License  | No | No | No | No | Yes | Yes |
| Write License | No | No | No | No | Yes | Yes |
