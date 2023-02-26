---
title: DNS Reverse Lookup Zones
description: Manage Microsof DNS Reverse Lookup Zones with Terraform
---

# DNS Reverse Lookup Zones

Manage Microsoft DNS Reverse Lookup Zones in AD DNS using the KopiCloud AD Terraform Provider:

[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

----

## Create a DNS Reverse Lookup Zone

Create a DNS Reverse Lookup Zone:

```
resource "kopicloud_dns_reverse_lookup_zone" "test_reverse" {
  network_id = "192.168.55.0/24"
}
```

Returns the created DNS Reverse Lookup Zone:

```
output "dns_reverse_zone" {
  description = "Created DNS Reverse Lookup Zone"
  value       = resource.kopicloud_dns_reverse_lookup_zone.test_reverse
}
```

----

## List All DNS Reverse Lookup Zones

List All DNS Reverse Lookup Zones:

```
data "kopicloud_dns_reverse_lookup_zone_list" "test_reverse_all" {}
```


Returns the List of DNS Reverse Lookup Zones:

```
output "dns_reverse_lookup_zone_list" {
  description = "List of DNS Reverse Lookup Zones"
  value       = data.kopicloud_dns_reverse_lookup_zone_list.test_reverse_all
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
