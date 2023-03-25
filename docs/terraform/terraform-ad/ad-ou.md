---
title: AD Organization Units (OU) with Terraform
description: Manage AD Organization Units (OU) with Terraform
date: 2023-03-25
---

# OUs (Organization Units) with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Organization Units (OUs) in Microsoft Active Directory using the KopiCloud AD API Terraform Provider

----

## Get and List of All Active Directory Organization Units

Get List OUs:

```
data "kopicloud_ou_list" "test" {}
```

Returns List of OUs:

```
output "OUTPUT_list_ou" {
  description = "List of Existing OUs"
  value       = data.kopicloud_ou_list.test
}
```

----

## Get and List of Active Directory Organization Unit Guid

Get List OU Guid:

```
data "kopicloud_ou_list" "test" {}
```

Returns List of OU Gui:

```
output "OUTPUT_list_ou" {
  description = "List of Existing OU Guid"
  value       = data.kopicloud_ou_list.test
}
```

----

## Get and List of Active Directory Organization Unit Details

Get AD OU Details:

```
data "kopicloud_ou_list" "test" {}
```

Returns List of AD OU :

```
output "OUTPUT_list_ou" {
  description = "List of Existing AD OU Details"
  value       = data.kopicloud_ou_list.test
}
```

----

## Get and Check if the Active Directory Organization Unit Exists

Get AD OU Unit Exists:

```
data "kopicloud_ou_list" "test" {}
```

Returns of AD OU Exists:

```
output "OUTPUT_list_ou" {
  description = "List of Existing AD OU"
  value       = data.kopicloud_ou_list.test
}
```

----

## Create an Active Directory Organization Unit

Create an OU:

```
resource "kopicloud_ou" "test" {
  ou_path     = "DC=kopicloud,DC=local"
  ou_name     = "kopicloud-europe"
  protected   = false
  description = "OU for KopiCloud Europe"
}
```

Returns created AD:

```
output "OUTPUT_created_ou" {
  description = "Created OU"
  value       = resource.kopicloud_ou.test
}

```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-ou)
