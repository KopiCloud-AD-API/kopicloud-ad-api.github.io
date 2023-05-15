---
title: AD Organization Units (OUs) with Terraform
description: Manage AD Organization Units (OU) with Terraform
date: 2023-05-15
---

# AD Organization Units (OUs) with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Organization Units (OUs) in Microsoft Active Directory using the KopiCloud AD API Terraform Provider

----

## Resources

### Create an AD OU

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

**Schema**

Required:

- ```description``` (String) The Description of the AD OU

- ```ou_name``` (String) Name of the AD OU

Optional:

- ```ou_path``` (String) Path of the AD OU (Distinguished Name)

- ```protected``` (Boolean) Protect the AD OU from Accidental Deletion

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD OU (see below for nested schema)

----

## Data Sources:

### List AD OUs

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

----

**Schema**

Optional:

- ```ou_name``` (String) Name of the AD OU

- ```ou_path``` (String) Path of the AD OU (Distinguished Name)

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD OU (see below for nested schema)

----

## Nested Schema for Result:

Read-Only:

- ```description``` (String) The Description of the AD OU

- ```guid``` (String) The GUID of the AD OU

- ```name``` (String) Name of the AD OU

- ```path``` (String) Path of the AD OU (Distinguished Name)

- ```protected``` (Boolean) Protect the AD OU from Accidental Deletion

----

## Notes

Running this resource with ```terraform apply``` will create or update the AD OU and running ```terraform destroy``` will remove this AD OU from the Active Directory.

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-ou)
