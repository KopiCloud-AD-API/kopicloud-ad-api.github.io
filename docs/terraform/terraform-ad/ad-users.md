---
title: AD Users with Terraform
description: Manage AD Users with Terraform
date: 2023-03-25
---

# AD Users with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Users in Microsoft Active Directory using the KopiCloud AD Terraform Provider

----

## List of All Computers Inside an Active Directory Organization Unit

Get All AD Users:

```
data "kopicloud_user_list" "test_all" { }
```

Returns All AD Users:

```
output "OUTPUT_kopicloud_all_users" {
  description = "All Existing AD Users"
  value       = data.kopicloud_user_list.test_all
}
```

----

## List of All AD Users Inside an Organization Unit

Get All AD Users Inside an OU:

```
data "kopicloud_user_list" "test_ou" {
  ou_path = "LDAP://CN=API Service,CN=Managed Service Accounts,DC=kopicloud,DC=local"
}
```

Returns All AD Users Inside an OU:

```
output "OUTPUT_kopicloud_all_users_ou" {
  description = "All Existing AD Users inside an OU"
  value       = data.kopicloud_user_list.test_ou
}
```

----

## List of All AD Users Showing Specific Fields

Get All AD Users Showing Specific Fields :

```
data "kopicloud_user_list" "test_filter" {
  show_fields = "firstName,lastName,displayName"
}
```

Returns all AD Users Showing Specific Fields:

```
output "kopicloud_all_users_filter" {
  description = "All Existing AD Users Showing Specific Fields"
  value       = data.kopicloud_user_list.test_filter
}
```

----

## Create an AD User

Create AD User:

```
resource "kopicloud_user" "test" {
  username      = "rsmith"
  password      = var.password
  first_name    = "Robert"
  initials      = "T"
  last_name     = "Smith"
  display_name  = "Robert T Smith"
  company       = "KopiCloud Limited"
  description   = "Marketing Director"
  department    = "Marketing"
  email_address = "robert.smith@kopicloud.net"
}
```

Returns AD User Result:

```
output "OUTPUT_new_user" {
  description = "Created User"
  value       = resource.kopicloud_user.test
  sensitive = true
}
```

----

## Reset the Password of an AD User

Reset User Password:

```
resource "kopicloud_user_password_reset" "test" {
  username     = "msmith"
  new_password = var.password
  
  change_password_next_logon = false
}
```

Reset Password Output:

```
output "OUTPUT_user_password_reset" {
  description = "User Password Result"
  value       = resource.kopicloud_user_password_reset.test.result
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-users)
