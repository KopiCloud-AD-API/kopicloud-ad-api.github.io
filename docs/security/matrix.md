---
title: Welcome to KopiCloud AD API
description: Welcome to KopiCloud AD API
date: 2023-03-01
---

# KopiCloud AD API Security Groups Matrix

The tables above explain the permissions based on your AD Group Membership

-----

## AD User

List, Create, Rename, Update and Delete AD Users.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| --------------------------------- | --------- | -------- | --------- | ----------- | -------------- |
| List of ALL Users           | Yes       | Yes      | No        | Yes         | No             |
| List of Users Inside an OU  | Yes       | Yes      | No        | Yes         | No             |
| Get User Details            | Yes       | Yes      | No        | Yes         | No             |
| Get User Details By Guid    | Yes       | Yes      | No        | Yes         | No             |
| Check If User Exist         | Yes       | Yes      | No        | Yes         | No             |
| Get AD Last Logon              | Yes       | Yes      | No        | Yes         | No             |
| POST / Create New User            | Yes       | Yes      | No        | Yes         | No             |
| PUT / Update User                 | Yes       | Yes      | No        | Yes         | No             |
| PUT / Update User by Guid         | Yes       | Yes      | No        | Yes         | No             |
| PUT / Reset User Password         | Yes       | Yes      | No        | Yes         | No             |
| PUT / Enable User                 | Yes       | Yes      | No        | Yes         | No             |
| PUT / Disable User                | Yes       | Yes      | No        | Yes         | No             |
| PUT / Unlock User                 | Yes       | Yes      | No        | Yes         | No             |
| PUT / Rename User                 | Yes       | Yes      | No        | Yes         | No             |
| DELETE / Delete User              | Yes       | Yes      | No        | Yes         | No             |
| DELETE / Delete User by Guid      | Yes       | Yes      | No        | Yes         | No             |

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

List, Create, Rename, Update and Delete AD Groups.

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

List, Create, Rename, Update and Delete AD OUs.

| API Method            | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| --------------------- | --------- | -------- | --------- | ----------- | -------------- |
| List All AD OUs       | Yes       | Yes      | No        | Yes         | No             |
| Show AD OU Details    | Yes       | Yes      | No        | Yes         | No             |
| Check if AD OU Exists | Yes       | Yes      | No        | Yes         | No             |
| Create AD OU          | Yes       | Yes      | No        | Yes         | No             |
| Rename AD OU          | Yes       | Yes      | No        | Yes         | No             |
| Update AD OU          | Yes       | Yes      | No        | Yes         | No             |
| Move AD OU            | Yes       | Yes      | No        | Yes         | No             |
| Delete AD OU          | Yes       | Yes      | No        | Yes         | No             |

----

## DNS AAAA Record

List, Create and Delete DNS AAAA records (IP v6).

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------- | --- | -- | --- | --- | -- |
| List All DNS AAAA Records | Yes | No | Yes | Yes | No |
| Create a DNS AAAA Records | Yes | No | Yes | Yes | No |
| Delete a DNS AAAA Records | Yes | No | Yes | Yes | No |

----

## DNS A Record

List, Create and Delete DNS A records (IP v4).

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ---------------------- | --- | -- | --- | --- | -- |
| List All DNS A Records | Yes | No | Yes | Yes | No |
| Create a DNS A Records | Yes | No | Yes | Yes | No |
| Delete a DNS A Records | Yes | No | Yes | Yes | No |

----

## DNS CNAME Record

List, Create and Delete DNS CNAME records.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| -------------------------- | --- | -- | --- | --- | -- |
| List All DNS CNAME Records | Yes | No | Yes | Yes | No |
| Create a DNS CNAME Records | Yes | No | Yes | Yes | No |
| Delete a DNS CNAME Records | Yes | No | Yes | Yes | No |

----

## DNS Zone

List, Create and Delete DNS zones.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------------------------------------| --------- | -------- | --------- | ----------- | -------------- |
| Check If DNS Zone Exists                              | Yes       | No       | Yes       | Yes         | No             |
| List All DNS Zones                                    | Yes       | No       | Yes       | Yes         | No             |
| Get DNS Zone by Name                                  | Yes       | No       | Yes       | Yes         | No             |
| List All DNS Lookup Zones                             | Yes       | No       | Yes       | Yes         | No             |
| Create a DNS Lookup Zone                              | Yes       | No       | Yes       | Yes         | No             |
| Delete a DNS Lookup Zone                              | Yes       | No       | Yes       | Yes         | No             |
| List All DNS Reverse Lookup Zones                     | Yes       | No       | Yes       | Yes         | No             |
| Get DNS Reverse Lookup Zone by NetworkID or Zone Name | Yes       | No       | Yes       | Yes         | No             |
| Create a DNS Reverse Lookup Zone NetworkID            | Yes       | No       | Yes       | Yes         | No             |
| Delete a DNS Reverse Lookup Zone                      | Yes       | No       | Yes       | Yes         | No             |

----

## Token Management

Create, list, enable, disable and delete authentication tokens.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| --------------------------| ----| ----| ----| ----| --- |
| Generate JWT Bearer Token | Yes | Yes | Yes | Yes | Yes |
| Generate Basic Token      | Yes | Yes | Yes | Yes | Yes |
| List OWN Tokens           | Yes | Yes | Yes | Yes | Yes |
| List ALL Tokens           | No  | No  | No  | Yes | Yes |
| Enable/Disable OWN Tokens | Yes | Yes | Yes | Yes | Yes |
| Enable/Disable ALL Tokens | No  | No  | No  | Yes | Yes |
| Delete Token              | No  | No  | No  | Yes | Yes |

----

## Event Log

Review the KopiCloud AD API Event Log.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| -------------- | -- | -- | -- | --- | --- |
| Show Event Log | No | No | No | Yes | Yes |

----

## License Management

Configure the KopiCloud AD API License.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ------------- | -- | -- | -- | --- | --- |
| Read License  | No | No | No | Yes | Yes |
| Write License | No | No | No | Yes | Yes |
