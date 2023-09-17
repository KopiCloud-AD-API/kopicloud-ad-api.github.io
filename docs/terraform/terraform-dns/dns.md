---
title: DNS with Terraform
description: Manage Microsoft DNS with Terraform
date: 2023-05-15
---

# DNS with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Manage Microsoft DNS Records and DNS Zones using the KopiCloud AD Terraform Provider.

----

## DNS Terraform Resources

The provider includes **Terraform Resources** to manipulate DNS Records and DNS Zones:


- ```kopicloud_dns_a_record``` - Create and remove DNS A Records

- ```kopicloud_dns_aaaa_record``` - Create and remove DNS AAAA Records

- ```kopicloud_dns_cname_record``` - Create and remove DNS CNAME Records

- ```kopicloud_dns_lookup_zone``` - Create and remove DNS Lookup Zones

- ```kopicloud_dns_reverse_lookup_zone``` - Create and remove DNS Reverse Lookup Zones

----

## DNS Terraform Data Sources

The provider includes **Terraform Data Sources** to list existing DNS Records and DNS Zones:

- ```kopicloud_dns_a_records_list``` - List DNS A Records

- ```kopicloud_dns_aaaa_records_list``` - List DNS AAAA Records

- ```kopicloud_dns_cname_records_list``` - List DNS CNAME Records

- ```kopicloud_dns_zone_list``` - List All DNS Zones

- ```kopicloud_dns_lookup_zone_list``` - List DNS Lookup Zones

- ```kopicloud_dns_reverse_lookup_zone_list``` - List DNS Reverse Lookup Zones

