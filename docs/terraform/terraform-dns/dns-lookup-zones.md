---
title: DNS Lookup Zones with Terraform
description: Manage Microsoft DNS Lookup Zones with Terraform
date: 2023-03-01
---

# DNS Lookup Zones
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS Lookup Zones using the KopiCloud AD Terraform Provider.

----

## Create a DNS Lookup Zone

Create a DNS Lookup Zone:

```
resource "kopicloud_dns_lookup_zone" "test_lookup" {
  zone_name = "kopicloud.org"
}
```

Returns the created DNS Lookup Zone:

```
output "dns_lookup_zone" {
  description = "Created DNS Lookup Zone"
  value       = resource.kopicloud_dns_lookup_zone.test_lookup
}
```

----

## List All DNS Lookup Zones

List All DNS Lookup Zones:

```
data "kopicloud_dns_lookup_zone_list" "test_lookup_all" {}
```

Returns the List of DNS Lookup Zones:

```
output "dns_lookup_zone_list" {
  description = "List of DNS Lookup Zones"
  value       = data.kopicloud_dns_lookup_zone_list.test_lookup_all
}
```

----

## List All DNS Zones

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

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-zones)
