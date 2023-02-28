---
title: DNS A Records with Terraform
description: Manage Microsof DNS A Records with Terraform
date: 2023-03-01
---

# DNS A Records
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS A Records using the KopiCloud AD Terraform Provider.

----

## Create a DNS A Record

Create a DNS A Record for a computer

```
resource "kopicloud_dns_a_record" "test_a" {
  hostname   = "atftestvm01"
  ip_address = "100.30.1.1"
  zone_name  = "kopicloud.local"
}
```

Output the created DNS A Record:

```
output "dns_a_record" {
  description = "Created DNS A Record"
  value       = resource.kopicloud_dns_a_record.test_a
}
```

Output the Hostname of the created DNS A Record:

```
output "dns_a_record_hostname" {
  description = "Hostname of Created DNS A Record"
  value       = resource.kopicloud_dns_a_record.test_a.hostname
}
```

----

## List All DNS A Records

List All DNS A Records:

```
data "kopicloud_dns_a_records_list" "test_a_all" {}
```

Returns All DNS A Records:

```
output "OUTPUT_dns_a_records_list_all" {
  description = "List Existing DNS A Records"
  value       = data.kopicloud_dns_a_records_list.test_a_all
}
```

----

## Filter DNS A Records with the Zone Name

Filter DNS A Records with the Zone Name:

```
data "kopicloud_dns_a_records_list" "test_a_zone_name" {
  zone_name = "kopicloud.local"
}
```

Returns all DNS A Records that matches the Zone Name:

```
output "OUTPUT_dns_a_records_list_zone_name" {
  description = "List existing DNS A Records filtered by Zone Name"
  value       = data.kopicloud_dns_a_records_list.test_a_zone_name
}
```

----

## Filter DNS A Records with an IP Address

Filter DNS A Records with an IP Address:

```
data "kopicloud_dns_a_records_list" "test_a_ip" {
  ip_address = "12.12.12.12"
}
```

Returns all DNS A Records that matches the IP Address:

```
output "OUTPUT_dns_a_records_list_ip_address" {
  description = "List existing DNS A Records filtered by IP Address"
  value       = data.kopicloud_dns_a_records_list.test_a_ip
}
```

----

## Filter DNS A Records with a Hostname

Filter DNS A Records with a Hostname:

```
data "kopicloud_dns_a_records_list" "test_a_hostname" {
  hostname = "computer75"
}
```

Returns all DNS A Records that matches the Hostname:

```
output "dns_a_records_list_hostname" {
  description = "List Existing DNS A Records"
  value       = data.kopicloud_dns_a_records_list.test_a_hostname
}
```

Returns the IP Address of the 1st DNS A Record:

```
output "dns_a_records_list_hostname_record_1_ip_address" {
  description = "Show the IP Address of the 1st DNS A Record"
  value       = data.kopicloud_dns_a_records_list.test_a_hostname.result.0.data
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-a-records)
