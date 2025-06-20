---
title: AD Group Membership with Terraform
description: Manage AD Group Membership with Terraform
date: 2025-05-25
---

# AD Group Membership with Terraform
Manage AD Group Membership in Microsoft Active Directory using the KopiCloud AD API Terraform Provider

----

## Resources

### Add an AD User to an AD Group
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Add an AD User to an AD Group:

```
resource "kopicloud_group_membership" "test" {
  user_name  = "guillermo"
  group_name = "KopiCloud Architects"
}
```

Returns the Group Membership of an AD User:

```
output "OUTPUT_kopicloud_group_membership" {
  description = "Added User to an AD Group"
  value       = resource.kopicloud_group_membership.test
}
```

----

**Schema**

Required:

- ```user_name``` (String) AD Username

Optional:

- ```group_name``` (String) AD Group Name

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

### Add an AD Group to an AD Group
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.2+-blueviolet.svg)](https://adapi.kopicloud.com)

Add an AD Group to an AD Group:

```
resource "kopicloud_group_membership" "test" {
  parent_group_name = "KopiCloud DevOps"
  child_group_name  = "KopiCloud Architects"
}
```

Returns the Group Membership of the AD Group:

```
output "OUTPUT_kopicloud_group_membership" {
  description = "Added User to an AD Group"
  value       = resource.kopicloud_group_membership.test
}
```

----

**Schema**

Required:

- ```parent_group_name``` (String) Parent AD Group Name

- ```child_group_name``` (String) Child AD Group Name

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

## Data Sources

### List Group Membership of AD User
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

List AD User Group Membership:

```
data "kopicloud_group_membership_list" "test" {
  user_name  = "guillermo"
}
```

Show Group Membership:

```
output "OUTPUT_active_directory_user_list_all" {
  description = "Return all AD User Group Membership"
  value = data.kopicloud_active_directory_user_list.all
}
```

----

**Schema**

Required:

- ```user_name``` (String) AD Username

Optional:

- ```group_name``` (String) AD Group Name

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

## Nested Schema for Result:

Read-Only:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```guid``` (String) AD Group GUID

- ```name``` (String) AD Group Name

- ```ou_path``` (String) AD Group OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope

- ```type``` (String) AD Group Type

----

### List Group Membership of AD Group
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.2+-blueviolet.svg)](https://adapi.kopicloud.com)

List AD User Group Membership:

```
data "kopicloud_group_membership_list" "test" {
  group_name  = "KopiCloud DevOps"
}
```

Show Group Membership:

```
output "OUTPUT_active_directory_user_list_all" {
  description = "Return all AD User Group Membership"
  value = data.kopicloud_active_directory_user_list.all
}
```

----

**Schema**

Required:

- ```group_name``` (String) AD Group Name

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

## Nested Schema for Result:

Read-Only:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```guid``` (String) AD Group GUID

- ```name``` (String) AD Group Name

- ```ou_path``` (String) AD Group OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope

- ```type``` (String) AD Group Type

----

## Notes

Running this resource with ```terraform apply `` will add or modify an AD user's group membership, and running ```terraform destroy `` will remove the AD User from the AD Group.

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-group-membership)
