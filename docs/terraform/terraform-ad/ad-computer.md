---
title: AD Computers with Terraform
description: Manage AD Computers with Terraform
date: 2023-03-25
---

# AD Computers with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Computers in Microsoft Active Directory using the KopiCloud AD API Terraform Provider

----

## List of All AD Computers

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

## List of All AD Computers Inside an AD OU

List All Computers Inside an OU:

```
data "kopicloud_computer_list" "test" {
  ou_path = "OU=Domain Controllers,DC=kopicloud,DC=local"
}
```

Returns All Computers Inside an OU:

```
output "OUTPUT_all_computers_list_inside_ou" {
  description = "All Existing Computers Inside an OU"
  value       = data.kopicloud_computer_list.test
}
```

----

## Register (Create) AD Computer

Use the optional **ou_path** parameter to store the computer inside a specific OU, if not it will be stored in the Computers OU.

Create New Computer:

```
resource "kopicloud_computer" "test" {
  ad_computer_name = "KOPISSRV1"
  description      = "Test Server"
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

## Update AD Computer Description

Update a Computer:

```
resource "kopicloud_computer" "test" {
  ad_computer_name = "KOPISRV1"
  description      = "DevOps Server"
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

## Clean Up Inactive AD Computers for More Than XX Days

Clean Up Inactive AD Computers:

```
resource "kopicloud_computer_cleanup" "test" {
  ou_path = "OU=Computers,DC=kopicloud,DC=local"
  days    = 90
}
```

Return Clean-Up Computers:

```
output "OUTPUT_list_cleanup_computer" {
  description = "List of Clean Up Inactive AD Computers"
  value       = resource.kopicloud_computer_cleanup.test
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-computers)
