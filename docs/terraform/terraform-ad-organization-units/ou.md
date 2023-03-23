---
title: AD Organization Units (OU) with Terraform
description: Manage AD Organization Units (OU) with Terraform
date: 2023-03-23
---

# OUs (Organization Units) with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft AD Organization Units using the KopiCloud AD Terraform Provider:

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

## Update an Active Directory Organization Unit

Update an OU:

```
resource "kopicloud_ou" "test" {
  ou_path     = "DC=kopicloud,DC=local"
  ou_name     = "kopicloud-europe"
  ou_new_name = "kopicloud-europe-new
  protected   = false
  description = "OU for KopiCloud Europe"
}
```

Returns updated AD:

```
output "OUTPUT_created_ou" {
  description = "Created OU"
  value       = resource.kopicloud_ou.test
}

```

----

## Move an Active Directory Organization Unit

Move an OU:

```
resource "kopicloud_ou" "test" {
  ou_path     = "DC=kopicloud,DC=local"
  ou_name     = "kopicloud-europe"
  OU_destination_path = "kopicloud-europe-path
  protected   = false
  description = "OU for KopiCloud Europe"
}
```

Returns moved OU:

```
output "OUTPUT_created_ou" {
  description = "Created OU"
  value       = resource.kopicloud_ou.test
}

```

----

## Rename an Active Directory Organization Unit

Rename an OU:

```
resource "kopicloud_ou" "test" {
  ou_path     = "DC=kopicloud,DC=local"
  ou_name     = "kopicloud-europe"
  ou_new_name = "kopicloud-europe-new
  protected   = false
  description = "OU for KopiCloud Europe"
}
```

Returns Renamed OU:

```
output "OUTPUT_created_ou" {
  description = "Created OU"
  value       = resource.kopicloud_ou.test
}

```

----

## Delete an Active Directory Organization Unit

Delete an OU:

```
resource "kopicloud_ou" "test" {
  ou_path     = "DC=kopicloud,DC=local"
  ou_name     = "kopicloud-europe"
  force = "true"
  protected   = false
  description = "OU for KopiCloud Europe"
}
```

Returns Deleted OU:

```
output "OUTPUT_created_ou" {
  description = "Created OU"
  value       = resource.kopicloud_ou.test
}

```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-ou)