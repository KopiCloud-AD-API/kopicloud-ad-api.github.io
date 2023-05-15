---
title: DNS Zones with Terraform
description: Manage Microsof DNS Zones with Terraform
date: 2023-05-15
---

# DNS Zones
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS Zones using the KopiCloud AD Terraform Provider.

----

## Data Sources

### List All DNS Zones

List All DNS Zones (Reverse Lookup Zones and Lookup Zones):

```
data "kopicloud_dns_zone_list" "test_all" {}
```

Returns the List of All DNS Zones:

```
output "dns_all_zone_list" {
  description = "List of All DNS Zones"
  value       = data.kopicloud_dns_zone_list.test_all
}
```

----

**Schema**

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Object) List of DNS Zones (see below for nested schema)

----

## Nested Schema for Result

Read-Only:

- ```distinguished_name``` (String) DNS Distinguished Name
- ```type``` (String) DNS Type, possible values are ForwardDNSZone or ReverseDNSZone
- ```zone_name``` (String) DNS Zone Name
- ```zone_type``` (String) DNS Zone Type, possible values are Primary, Secondary or Stub Zone

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-zones)

