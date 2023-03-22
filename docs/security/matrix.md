---
title: Welcome to KopiCloud AD API
description: Welcome to KopiCloud AD API
date: 2023-03-01
---

# KopiCloud AD API Security Group Matrix

| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| AD User             | Get list of users                     | Yes      | No        | Yes         | No             | No          |
|                     | Check If User Exist                   | Yes      | No        | Yes         | No             | No          |
|                     | Reset User Password                   | Yes      | No        | Yes         | No             | No          |
|                     | Create New User                       | Yes      | No        | Yes         | No             | No          | 
|                     | Delete Existing User                  | Yes      | No        | Yes         | No             | No          | 
|                     | Add User to Specific Group            | Yes      | No        | Yes         | No             | No          | 
|                     | Remove User from Specific Group       | No       | No        | Yes         | No             | No          | 
|                     | Get List of groups membership of User | No       | No        | Yes         | No             | No          | 


| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| AD Group Membership | xx                                    | Yes      | No        | Yes         | Yes            | No          |
|                     | Check If User is a Member of a Group  | Yes      | No        | Yes         | No             | No          | 

| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| AD Group            | xx                                    | Yes      | No        | Yes         | Yes            | No          |


| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| AD OU               | List OUs                              | Yes      | No        | Yes         | Yes            | No          |
|                     | Show OU Details                       | Yes      | No        | Yes         | Yes            | No          |
|                     | Check If OU Exists                    | Yes      | No        | Yes         | Yes            | No          |
|                     | Create OU                             | Yes      | No        | Yes         | Yes            | No          |
|                     | Update OU                             | Yes      | No        | Yes         | Yes            | No          |
|                     | Move OU                               | Yes      | No        | Yes         | Yes            | No          |
|                     | Rename OU                             | Yes      | No        | Yes         | Yes            | No          |
|                     | Delete OU                             | Yes      | No        | Yes         | Yes            | No          |

| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| AD Computer         | List Computers                        | Yes      | No        | Yes         | Yes            | No          |
|                     | Show Computer Details                 | Yes      | No        | Yes         | Yes            | No          |
|                     | Check If Computer Exists              | Yes      | No        | Yes         | Yes            | No          |
|                     | Register Computer                     | Yes      | No        | Yes         | Yes            | No          |
|                     | Rename Computer                       | Yes      | No        | Yes         | Yes            | No          |
|                     | Update Computer                       | Yes      | No        | Yes         | Yes            | No          |
|                     | Rename OU                             | Yes      | No        | Yes         | Yes            | No          |
|                     | Delete OU                             | Yes      | No        | Yes         | Yes            | No          |
|                     | Clean Up Inactive Computers           | Yes      | No        | Yes         | Yes            | No          |
|                     | Remove Multiple Computers             | Yes      | No        | Yes         | Yes            | No          |

| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| DNS Record          | List A Records                        | No       | Yes       | Yes         | No             | No          | 
|                     | Add A Record                          | No       | Yes       | Yes         | No             | No          | 
|                     | Delete A Record                       | No       | Yes       | Yes         | No             | No          |
|                     | List AAAA Record                      | No       | Yes       | Yes         | No             | No          |
|                     | Add AAAA Record                       | No       | Yes       | Yes         | No             | No          | 
|                     | Delete AAAA Record                    | No       | Yes       | Yes         | No             | No          | 
|                     | List CNAME Record                     | No       | Yes       | Yes         | No             | No          |
|                     | Add CNAME Record                      | No       | Yes       | Yes         | No             | No          | 
|                     | Delete CNAME Record                   | No       | Yes       | Yes         | No             | No          | 

| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| DNS Zone            | List DNS Zones                        | No       | Yes       | Yes         | No             | No          | 
|                     | Check If DNS Zone Exists              | No       | Yes       | Yes         | No             | No          | 
|                     | List DNS Lookup Zone                  | No       | Yes       | Yes         | No             | No          | 
|                     | Create DNS Lookup Zone                | No       | Yes       | Yes         | No             | No          | 
|                     | Delete DNS Lookup Zone                | No       | Yes       | Yes         | No             | No          | 
|                     | List DNS Reverse Lookup Zone          | No       | Yes       | Yes         | No             | No          | 
|                     | Create DNS Reverse Lookup Zone        | No       | Yes       | Yes         | No             | No          | 
|                     | Delete DNS Reverse Lookup Zone        | No       | Yes       | Yes         | No             | No          | 

| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| Token               | Generate JWT Bearer Token             | Yes      | Yes       | Yes         | No             | Yes         | 
|                     | Generate Basic Token                  | Yes      | Yes       | Yes         | No             | Yes         |
|                     | Token List                            | Yes      | Yes       | Yes         | Yes            | Yes         |
|                     | Enable/Disable/Delete OWN Token       | Yes      | Yes       | Yes         | Yes            | Yes         |
|                     | Enable/Disable/Delete ALL Tokens      | No       | No        | Yes         | Yes            | No          |

| Module              | Method                                | AD Group | DNS Group | Admin Group | Security Group | Token Group |
| ------------------- | ------------------------------------- | -------- | --------- | ----------- | -------------- | ----------- |
| Log                 | View Event Log                        | No       | No        | Yes         | Yes            | No          |
