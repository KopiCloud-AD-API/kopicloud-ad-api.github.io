---
title: KopiCloud AD API Security Groups Matrix
description: KopiCloud AD API Security Groups Matrix
date: 2023-03-23
---

# KopiCloud AD API Security Groups Matrix

Review the permissions listed below based on your AD Group Membership.

-----

## AD User

List, Create, Rename, Update and Delete AD Users.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ---------------------- | --- | --- | -- | --- | -- |
| List AD User           | Yes | Yes | No | Yes | No |
| Get AD User Details    | Yes | Yes | No | Yes | No |
| Check If AD User Exist | Yes | Yes | No | Yes | No |
| Get AD User Last Logon | Yes | Yes | No | Yes | No |
| Create New AD User     | Yes | Yes | No | Yes | No |
| Update AD User         | Yes | Yes | No | Yes | No |
| Reset AD User Password | Yes | Yes | No | Yes | No |
| Enable AD User         | Yes | Yes | No | Yes | No |
| Disable AD User        | Yes | Yes | No | Yes | No |
| Unlock AD User         | Yes | Yes | No | Yes | No |
| Rename AD User         | Yes | Yes | No | Yes | No |
| Delete AD User         | Yes | Yes | No | Yes | No |

----

## AD Computer

List, Create, Rename, Update and Delete AD Computers.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ------------------------------ | --- | --- | -- | --- | -- |
| List ALL AD Computers          | Yes | Yes | No | Yes | No |
| Show AD Computer Details       | Yes | Yes | No | Yes | No |
| Check If AD Computer Exists    | Yes | Yes | No | Yes | No |
| Register AD Computer           | Yes | Yes | No | Yes | No |
| Rename AD Computer             | Yes | Yes | No | Yes | No |
| Update AD Computer Description | Yes | Yes | No | Yes | No |
| Remove AD Computer             | Yes | Yes | No | Yes | No |
| Remove Multiple AD Computers   | Yes | Yes | No | Yes | No |
| Clean Up Inactive AD Computers | Yes | Yes | No | Yes | No |

----

## AD Group

List, Create, Rename, Update and Delete AD Groups.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ---------------------------- | --- | --- | -- | --- | -- |
| List AD Groups               | Yes | Yes | No | Yes | No |
| List AD Distribution Groups  | Yes | Yes | No | Yes | No |
| List AD Security Groups      | Yes | Yes | No | Yes | No |
| Show AD Group Details        | Yes | Yes | No | Yes | No |
| Check if AD Group Exists     | Yes | Yes | No | Yes | No |
| Create AD Security Group     | Yes | Yes | No | Yes | No |
| Create AD Distribution Group | Yes | Yes | No | Yes | No |
| Rename AD Group              | Yes | Yes | No | Yes | No |
| Delete AD Group              | Yes | Yes | No | Yes | No |

----

## AD Group Membership

Manage AD Group Membership of AD Users.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| ---------------------------------- | --- | --- | -- | --- | -- |
| Check AD User Group Membership     | Yes | Yes | No | Yes | No |
| Add AD User to Specific AD Group   | Yes | Yes | No | Yes | No |
| Remove AD User from Specific Group | Yes | Yes | No | Yes | No |

----

## AD OU

List, Create, Rename, Update and Delete AD OUs.

| API Method | API<br />Group | AD<br />Group | DNS<br />Group | Admin<br />Group | Security<br />Group |
| --------------------- | --- | --- | -- | --- | -- |
| List All AD OUs       | Yes | Yes | No | Yes | No |
| Show AD OU Details    | Yes | Yes | No | Yes | No |
| Check if AD OU Exists | Yes | Yes | No | Yes | No |
| Create AD OU          | Yes | Yes | No | Yes | No |
| Rename AD OU          | Yes | Yes | No | Yes | No |
| Update AD OU          | Yes | Yes | No | Yes | No |
| Move AD OU            | Yes | Yes | No | Yes | No |
| Delete AD OU          | Yes | Yes | No | Yes | No |

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
