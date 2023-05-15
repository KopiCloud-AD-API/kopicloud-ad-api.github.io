---
title: DNS with Terraform
description: Manage Microsoft DNS with Terraform
date: 2023-05-15
---

# DNS with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS Records and DNS Zones using the KopiCloud AD Terraform Provider.

----

## DNS Terraform Resources

The provider includes **Terraform Resources** to manipulate DNS Records and DNS Zones:


- ```ad_kopicloud_dns_a_record``` - Create and remove DNS A Records

- ```ad_kopicloud_dns_aaaa_record``` - Create and remove DNS AAAA Records

- ```ad_kopicloud_dns_cname_record``` - Create and remove DNS CNAME Records

- ```ad_kopicloud_dns_lookup_zone``` - Create and remove DNS Loopkup Zones

- ```ad_kopicloud_dns_reverse_lookup_zone``` - Create and remove DNS Reverse Loopkup Zones

----

## DNS Terraform Data Sources

The provider includes **Terraform Data Sources** to list existing DNS Records and DNS Zones:

- ```ad_kopicloud_dns_a_records_list``` - List DNS A Records

- ```ad_kopicloud_dns_aaaa_records_list``` - List DNS AAAA Records

- ```ad_kopicloud_dns_cname_records_list``` - List DNS CNAME Records

- ```ad_kopicloud_dns_zone_list``` - List All DNS Zones

- ```ad_kopicloud_dns_lookup_zone_list``` - List DNS Loopkup Zones

- ```ad_kopicloud_dns_reverse_lookup_zone_list``` - List DNS Reverse Loopkup Zones

