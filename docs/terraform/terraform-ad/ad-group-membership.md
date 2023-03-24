---
title: AD Group Membership with Terraform
description: Manage AD Group Membership with Terraform
date: 2023-03-21
---

# AD Group Membership with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft AD Group Membership using the KopiCloud AD Terraform Provider:

----

## List of All AD Users with Group Membership

List Group Membership for an User:

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

## Create an Active Directory User to an Active Directory Group

Add an AD User in a Group Membership:

```
resource "kopicloud_group_membership" "test" {
  user_name  = "guillermo"
  group_name = "KopiCloud Architects"
}
```

Returns Details of Active Directory User in Group:

```
output "OUTPUT_kopicloud_group_membership" {
  description = "Added User to an AD Group"
  value       = resource.kopicloud_group_membership.test
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-group-membership)
