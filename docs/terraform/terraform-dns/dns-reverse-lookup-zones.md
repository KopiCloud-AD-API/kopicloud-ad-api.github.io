---
title: DNS Reverse Lookup Zones
description: Manage Microsoft DNS Reverse Lookup Zones with Terraform
date: 2023-05-15
---

# DNS Reverse Lookup Zones
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage Microsoft DNS Reverse Lookup Zones using the KopiCloud AD Terraform Provider.

----

## Resouces

### Create a DNS Reverse Lookup Zone

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

**Schema**

Required:

- ```network_id``` (String) Network ID (example: 10.20.30.0/24)

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single DNS Zone (see below for nested schema)

----

## Data Sources

### List DNS Reverse Lookup Zones

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

**Schema**

Optional:

- ```network_id``` (String) Network ID (example: 10.20.30.0/24) or Zone Name (example: 30.20.10.in-addr.arpa)

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

Running this resource with ```terraform apply``` will create a DNS Reverse Lookup Zone in the Microsoft DNS and running ```terraform destroy``` will remove the DNS Reverse Lookup Zone from the DNS.

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-zones)
