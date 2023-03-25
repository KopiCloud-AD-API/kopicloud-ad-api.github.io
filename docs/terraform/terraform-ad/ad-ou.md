---
title: AD Organization Units (OUs) with Terraform
description: Manage AD Organization Units (OU) with Terraform
date: 2023-03-25
---

# AD Organization Units (OUs) with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Organization Units (OUs) in Microsoft Active Directory using the KopiCloud AD API Terraform Provider

----

## List AD OUs

Get the List of AD OUs:

```
data "kopicloud_ou_list" "test" {}
```

Returns the List of OUs:

```
output "OUTPUT_list_ou" {
  description = "List of Existing OUs"
  value       = data.kopicloud_ou_list.test
}
```

## Create an AD OU

Create an AD OU:

```
resource "kopicloud_ou" "test" {
  ou_path     = "DC=kopicloud,DC=local"
  ou_name     = "kopicloud-europe"
  protected   = false
  description = "OU for KopiCloud Europe"
}
```

Returns created AD OU:

```
output "OUTPUT_created_ou" {
  description = "Created OU"
  value       = resource.kopicloud_ou.test
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-ou)
