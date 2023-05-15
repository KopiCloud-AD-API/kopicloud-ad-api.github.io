---
title: AD Groups with Terraform
description: Manage AD Groups with Terraform
date: 2023-05-15
---

# AD Groups with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Groups in Microsoft Active Directory using the KopiCloud AD API Terraform Provider

----

## Resources

### Create an AD Distribution Group

Create a Global Distribution Group:

```
resource "kopicloud_distribution_group" "test_distribution_global" {
  name        = "kopicloud-europe-distribution-group"
  scope       = "Global"
  description = "This is a very cool Global distribution group"
  email       = "europe.distribution@kopicloud.com"
  ou_path     = "CN=Users,DC=kopicloud,DC=local"
}
```

Returns Created Global Distribution Group:

```
output "OUTPUT_global_distribution_group" {
  description = "Created Global Distribution Group"
  value       = resource.kopicloud_distribution_group.test_distribution_global
}
```

**Schema**

Required:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```name``` (String) AD Group Name

Optional:

- ```ou_path``` (String) OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope, possible values are Global, Universal or Domain_Local. Default is Global

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

Create a Universal Distribution Group:

```
resource "kopicloud_distribution_group" "test_distribution_universal" {
  name        = "kopicloud-america-distribution-group"
  scope       = "Universal"
  description = "This is a very cool Universal distribution group"
  email       = "america.distribution@kopicloud.com"
  ou_path     = "CN=Users,DC=kopicloud,DC=local"
}
```

Returns Created Universal Distribution Group:

```
output "OUTPUT_universal_distribution_group" {
  description = "Created Universal Distribution Group"
  value       = resource.kopicloud_distribution_group.test_distribution_universal
}
```

**Schema**

Required:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```name``` (String) AD Group Name

Optional:

- ```ou_path``` (String) OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope, possible values are Global, Universal or Domain_Local. Default is Global

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

Create a Domain Local Distribution Group:

```
resource "kopicloud_distribution_group" "test_distribution_domain_local" {
  name        = "kopicloud-asia-distribution-group"
  scope       = "Domain_Local"
  description = "This is a very cool Domain Local distribution group"
  email       = "asia.distribution@kopicloud.com"
  ou_path     = "CN=Users,DC=kopicloud,DC=local"
}
```

Returns Created Domain Local Distribution Group:

```
output "OUTPUT_domain_local_distribution_group" {
  description = "Created Domain Local Distribution Group"
  value       = resource.kopicloud_distribution_group.test_distribution_domain_local
}
```

**Schema**

Required:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```name``` (String) AD Group Name

Optional:

- ```ou_path``` (String) OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope, possible values are Global, Universal or Domain_Local. Default is Global

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

### Create an AD Security Group:

Create a Global Security Group

```
resource "kopicloud_security_group" "test_security_global" {
  name        = "kopicloud-europe-security-group"
  scope       = "Global"
  description = "This is a very cool Global security group"
  email       = "europe.security@kopicloud.com"
  ou_path     = "CN=Users,DC=kopicloud,DC=local"
}
```

Returns Created Global Security Group:

```
output "OUTPUT_global_security_group" {
  description = "Created Global Security Group"
  value       = resource.kopicloud_security_group.test_security_global
}
```

**Schema**

Required:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```name``` (String) AD Group Name

Optional:

- ```ou_path``` (String) OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope, possible values are Global, Universal or Domain_Local. Default is Global

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

Create a Universal Security Group:

```
resource "kopicloud_security_group" "test_security_universal" {
  name        = "kopicloud-america-security-group"
  scope       = "Universal"
  description = "This is a very cool Universal security group"
  email       = "america.security@kopicloud.com"
  ou_path     = "CN=Users,DC=kopicloud,DC=local"
}
```

Returns Created Universal Security Group:

```
output "OUTPUT_universal_security_group" {
  description = "Created Universal Security Group"
  value       = resource.kopicloud_security_group.test_security_universal
}
```

**Schema**

Required:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```name``` (String) AD Group Name

Optional:

- ```ou_path``` (String) OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope, possible values are Global, Universal or Domain_Local. Default is Global

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

Create a Domain Local Security Group:

```
resource "kopicloud_security_group" "test_security_domain_local" {
  name        = "kopicloud-asia-security-group"
  scope       = "Domain_Local"
  description = "This is a very cool Domain Local security group"
  email       = "asia.security@kopicloud.com"
  ou_path     = "CN=Users,DC=kopicloud,DC=local"
}
```

Returns Created Domain Local Security Group:

```
output "OUTPUT_domain_local_security_group" {
  description = "Created Domain Local Security Group"
  value       = resource.kopicloud_security_group.test_security_domain_local
}
```

**Schema**

Required:

- ```description``` (String) AD Group Description

- ```email``` (String) AD Group Email Address

- ```name``` (String) AD Group Name

Optional:

- ```ou_path``` (String) OU Path (Distinguished Name)

- ```scope``` (String) AD Group Scope, possible values are Global, Universal or Domain_Local. Default is Global

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

## Data Sources

### List All AD Groups

Get All AD Groups List:

```
data "kopicloud_security_group_list" "test_all" { }
```

Returns All AD Groups List:

```
output "OUTPUT_security_kopicloud_all_groups" {
  description = "All AD Groups List"
  value       = data.kopicloud_security_group_list.test_all
}
```

**Schema**

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

### List AD Distribution Groups

Get the List of Distribution Groups:

```
data "kopicloud_distribution_group_list" "test_distribution" { }
```

Returns the List of Distribution Groups:

```
output "OUTPUT_kopicloud_distribution_groups_list" {
  description = "All Existing Distribution Groups"
  value       = data.kopicloud_distribution_group_list.test_distribution
}
```

**Schema**

Read-Only:

- ```id``` (String) The ID of this Resource

- ```result``` (List of Objects) Single AD Group (see below for nested schema)

----

### List AD Security Groups

Get the List of Security Groups:

```
data "kopicloud_security_group_list" "test_security" { }
```

Returns the List of Security Groups:

```
output "OUTPUT_kopicloud_security_groups_list" {
  description = "All Existing Security Groups"
  value       = data.kopicloud_security_group_list.test_security
}
```

**Schema**

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

Running this resource with ```terraform apply``` will create or update the AD group and running ```terraform destroy``` will remove this AD Group from the Active Directory.

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-groups)
