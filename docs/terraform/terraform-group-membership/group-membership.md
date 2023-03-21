---
title: AD Group Membership with Terraform
description: Manage AD Group Membership with Terraform
---

# Manage Microsoft AD Group Membership using the KopiCloud AD Terraform Provider
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft AD Group Membership using the KopiCloud AD Terraform Provider:

----

## List of All AD Users with Group Membership

AD Users with Group Membership:

```
data "kopicloud_active_directory_user_list" "all" {}
```

Returns All Active Directory Users with Group Membership:

```
output "OUTPUT_active_directory_user_list_all" {
description = "Return all AD User Group Membership"
value = data.kopicloud_active_directory_user_list.all
}

```

----

## Check If a User Is a Member of an Active Directory Group

If the AD User is a member with Group Membership:

```
data "kopicloud_active_directory_member" "active_user" {}
```

Returns User of Active Directory with Group Membership:

```
output "OUTPUT_active_directory_member_active_user" {
description = "Return all AD User Group Membership"
value = data.kopicloud_active_directory_member.active_user
}

```

----

## Check If a User Is a Member of an Active Directory Group and return the AD Group

AD Group Membership of an Active Member:

```
data "kopicloud_active_directory" "groupname" {}
```

Returns Active Directory User Group Membership:

```
output "OUTPUT_kopicloud_active_directory_groupname" {
description = "Return all AD User Group Membership"
value = data.kopicloud_active_directory.groupname
}

```

----

## Create an Active Directory User to an Active Directory Group

Add an AD User in a Group Membership:

```
data "_kopicloud_active_directory_user_add" "groupname" {}
```

Returns Details of Active Directory User in Group:

```
output "OUTPUT_active_directory_user_add_groupname" {
description = "Return AD User with Group"
value = data.kopicloud_active_directory_user_add.groupname
}

```

----

## Remove an Active Directory User from an Active Directory Group Membership

Remove an AD User from AD Group: 

```
data "kopicloud_active_directory_user_" "delete" {}
```

Returns Object of removed AD User:

```
output "OUTPUT_active_directory_user_delete" {
description = "Return AD User with Group"
value = data.kopicloud_active_directory_user.delete
}

```