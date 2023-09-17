---
title: DNS Lookup Zones with Terraform
description: Manage Microsoft DNS Lookup Zones with Terraform
date: 2023-05-15
---

# DNS Lookup Zones
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage Microsoft DNS Lookup Zones using the KopiCloud AD Terraform Provider.

----

## Resources

### Create a DNS Lookup Zone

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

**Schema**

Required:

- ```zone_name``` (String) DNS Zone Name

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single DNS Zone (see below for nested schema)

----

## Data Sources

### List All DNS Lookup Zones

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

**Schema**

Optional:

- ```zone_name``` (String) DNS Zone Name

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single DNS Zone (see below for nested schema)

----

## Nested Schema for Result

Read-Only:

- ```distinguished_name``` (String) DNS Distinguished Name
- ```type``` (String) DNS Type, possible values are ```ForwardDNSZone``` or ```ReverseDNSZone```
- ```zone_name``` (String) DNS Zone Name
- ```zone_type``` (String) DNS Zone Type, possible values are ```Primary```, ```Secondary``` or ```Stub Zone```

----

## Notes

Running this resource with ```terraform apply``` will create a DNS Lookup Zone in the Microsoft DNS and running ```terraform destroy``` will remove the DNS Lookup Zone from the DNS.

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-zones)
