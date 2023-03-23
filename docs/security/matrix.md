---
title: Welcome to KopiCloud AD API
description: Welcome to KopiCloud AD API
date: 2023-03-01
---

# KopiCloud AD API Security Group Matrix

## AD User

| API Method Type and Description   | API<br />Group | AD<br />Group | DNS<br />Group | Token<br />Group | Admin<br />Group | Security<br />Group |
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

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / List ALL Computers inside in AD                               | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / List Computers inside an AD OU                                | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Show Computer Details                                         | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Check If Computer Exists                                      | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Register Computer                                            | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Rename Computer                                               | Yes       | Yes      | No        | No          | Yes         | No             |
| PUT / Update Computer Description                                   | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Remove Computer                                            | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Remove Multiple Computer                                   | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / CleanUp Inactive AD Computers                              | Yes       | Yes      | No        | No          | Yes         | No             |

----

## AD Group

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
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

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / AD User Group Membership                                      | Yes       | Yes      | No        | No          | Yes         | No             |
| GET / Check If User is a Member of a Group                          | Yes       | Yes      | No        | No          | Yes         | No             |
| POST / Add User to Specific Group                                   | Yes       | Yes      | No        | No          | Yes         | No             |
| DELETE / Remove User from Specific Group                            | Yes       | Yes      | No        | No          | Yes         | No             |

----

## AD OU

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
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

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| List All DNS AAAA Records in All Zones                              | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS AAAA Records in a Zone                                 | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS AAAA Records that match with DNS Hostname              | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS AAAA Records that match with IPv6 Address              | Yes       | No       | Yes       | No          | Yes         | No             |
| Get DNS AAAA Records                                                | Yes       | No       | Yes       | No          | Yes         | No             |
| Create a DNS AAAA Records                                           | Yes       | No       | Yes       | No          | Yes         | No             |

----

## DNS A Record

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| Delete a DNS A Records                                              | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS A Records in All Zones                                 | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS A Records in a Zone                                    | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS A Records that match with hostname                     | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS A Records that match with IP_address                   | Yes       | No       | Yes       | No          | Yes         | No             |
| Get DNS A Record that match with Hostname and IP_address            | Yes       | No       | Yes       | No          | Yes         | No             |
| Create a DNS A Records                                              | Yes       | No       | Yes       | No          | Yes         | No             |
| Delete a DNS A Records                                              | Yes       | No       | Yes       | No          | Yes         | No             |

----

## DNS CNAME Record

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| List All DNS CNAME Records in All Zones                             | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS CNAME Records in a Zone                                | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS CNAME Records that match with hostname                 | Yes       | No       | Yes       | No          | Yes         | No             |
| List All DNS CNAME Records that match with DNS HostName Alias       | Yes       | No       | Yes       | No          | Yes         | No             |
| Get DNS CNAME Record that match with DNS HostName and Alias         | Yes       | No       | Yes       | No          | Yes         | No             |
| Create a DNS CNAME Records                                          | Yes       | No       | Yes       | No          | Yes         | No             |
| Delete a DNS CNAME Records                                          | Yes       | No       | Yes       | No          | Yes         | No             |

----

## DNS Zone

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET / Check If DNS Zone Exists                                      | Yes       | No       | Yes       | No          | Yes         | No             |
| GET / List All DNS Zones                                            | Yes       | No       | Yes       | No          | Yes         | No             |
| GET / Get DNS Zone by Name                                          | Yes       | No       | Yes       | No          | Yes         | No             |
| GET / List All DNS Lookup Zones                                     | Yes       | No       | Yes       | No          | Yes         | No             |
| POST / Create a DNS Lookup Zone                                     | Yes       | No       | Yes       | No          | Yes         | No             |
| DELETE / Delete a DNS Lookup Zone                                   | Yes       | No       | Yes       | No          | Yes         | No             |
| GET / List All DNS Reverse Lookup Zones                             | Yes       | No       | Yes       | No          | Yes         | No             |
| GET / Get Dns Reverse Lookup Zone by NetworkID or Zone Name         | Yes       | No       | Yes       | No          | Yes         | No             |
| POST / Create a DNS Reverse Lookup Zone NetworkID                   | Yes       | No       | Yes       | No          | Yes         | No             |
| DELETE / Delete a DNS Reverse Lookup Zone                           | Yes       | No       | Yes       | No          | Yes         | No             |

----

## Token Management

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| Generate JWT Bearer Token                                           | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| Generate Basic Token                                                | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| List OWN Token List                                                 | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| List ALL Token List                                                 | No        | No       | No        | Yes         | Yes         | Yes            |
| Enable/Disable OWN Token                                            | Yes       | Yes      | Yes       | Yes         | Yes         | Yes            |
| Enable/Disable ALLTokens                                            | No        | No       | No        | Yes         | Yes         | Yes            |
| Delete Token                                                        | No        | No       | No        | Yes         | Yes         | Yes            |

----

## Event Log

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| Show Event Log                                                      | No        | No       | No        | No          | Yes         | Yes            |

----

## License Management

| Method                                                              | API Group | AD Group | DNS Group | Token Group | Admin Group | Security Group |
| ------------------------------------------------------------------- | --------- | -------- | --------- | ----------- | ----------- | -------------- |
| GET /License                                                        | No        | No       | No        | No          | Yes         | Yes            |
| Post /License                                                       | No        | No       | No        | No          | Yes         | Yes            |
