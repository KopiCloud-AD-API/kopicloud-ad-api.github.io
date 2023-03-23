---
title: AD Computers with Terraform
description: Manage AD Computers with Terraform
date: 2023-03-24

---

# AD Computers with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Computers in Microsoft AD using the KopiCloud AD API Terraform Provider:

----

## List of All Computer Inside an Active Directory Organization Unit

List All Computers Inside an OU:

```
data "kopicloud_computer_list" "test" {
  ou_path = "OU=Domain Controllers,DC=kopicloud,DC=local"
}
```

Returns All Computers Inside an OU:

```
output "OUTPUT_all_computers_list_inside_ou" {
  description = "Existing All Computers Inside an OU"
  value       = data.kopicloud_computer_list.test
}
```

----

## Show AD Computer Details (Operating System, Description, DNS Name, Creation Date)

List All Computers:

```
data "kopicloud_computer_list" "test_all" {}
```

Returns All Computers:

```
output "OUTPUT_all_computers_list" {
  description = "List ALL Existing Computers"
  value       = data.kopicloud_computer_list.test_all
}
```

----

## Check If AD Computer Exists with Optional Search Inside Specific OUs

List All Computers:

```
data "kopicloud_computer_list" "test" {
  ou_path = "OU=Domain Controllers,DC=kopicloud,DC=local"
}
```

Returns All Computers Inside an OU:

```
output "OUTPUT_all_computers_list_inside_ou" {
  description = "Existing All Computers Inside an OU"
  value       = data.kopicloud_computer_list.test
}
```

----

## Get a List of All Computers in Active Directory

List All Computers:

```
data "kopicloud_computer_list" "test_all" {}
```

Returns All Computers:

```
output "OUTPUT_all_computers_list" {
  description = "List ALL Existing Computers"
  value       = data.kopicloud_computer_list.test_all
}
```

----

## Create and Register Active Directory Computer Inside an Optional OU

Create New Computer:

```
resource "kopicloud_computer" "test" {
  ad_computer_name = "BIG-MAC"
  ou_path          = "OU=kopicloud-europe,DC=kopicloud,DC=local"    
}
```

Return Created Computer:

```
output "OUTPUT_new_computer" {
  description = "Created Computer"
  value       = resource.kopicloud_computer.test
}
```

----

## Rename an Active Directory Computer

Rename a Computer:

```
resource "kopicloud_computer" "test" {
  ad_computer_name = "BIG-MAC"
  ou_path          = "OU=kopicloud-europe,DC=kopicloud,DC=local"    
}
```

Return Renamed Computer:

```
output "OUTPUT_new_computer" {
  description = "Created Computer"
  value       = resource.kopicloud_computer.test
}
```

----

## Update Active Directory Computer Description

Update a Computer:

```
resource "kopicloud_computer" "test" {
  ad_computer_name = "BIG-MAC"
  ou_path          = "OU=kopicloud-europe,DC=kopicloud,DC=local"    
}
```

Return Updated Computer:

```
output "OUTPUT_new_computer" {
  description = "Created Computer"
  value       = resource.kopicloud_computer.test
}
```

----

## Remove Active Directory Computer Inside an Optional OU

Remove a Computer:

```
resource "kopicloud_computer" "test" {
  ad_computer_name = "BIG-MAC"
  ou_path          = "OU=kopicloud-europe,DC=kopicloud,DC=local"    
}
```

Return Removed Computer:

```
output "OUTPUT_new_computer" {
  description = "Created Computer"
  value       = resource.kopicloud_computer.test
}
```

----

## CleanUp Inactive Active Directory Computers for More Than XX Days

Clean Up Inactive AD Computers:

```
resource "kopicloud_computer_cleanup" "test" {
  ou_path = "OU=Domain Controllers,DC=kopicloud,DC=local"
  days    = 90
}
```

Return Clean Up Computers:

```
output "OUTPUT_list_cleanup_computer" {
  description = "List of Clean Up Inactive AD Computers"
  value       = resource.kopicloud_computer_cleanup.test
}
```

----

## Remove Multiple AD Computers Using WildCard Inside an Optional OU

Remove Computers:

```
resource "kopicloud_computer" "test" {
  ad_computer_name = "BIG-MAC"
  ou_path          = "OU=kopicloud-europe,DC=kopicloud,DC=local"    
}
```

Return Removed Computers:

```
output "OUTPUT_new_computer" {
  description = "Created Computer"
  value       = resource.kopicloud_computer.test
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-computers)
