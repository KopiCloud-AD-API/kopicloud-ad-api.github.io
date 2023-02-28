---
title: DNS AAAA Records with Terraform
description: Manage Microsof DNS AAAA Records with Terraform
date: 2023-03-01
---

# DNS AAAA Records
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS AAAA Records in AD DNS using the KopiCloud AD Terraform Provider:

----

## Create DNS AAAA Records

Create a DNS AAAA Record for a computer:

```
resource "kopicloud_dns_aaaa_record" "test_aaaa" {
  hostname     = "computer75v6"
  ipv6_address = "2340:0023:AABA:0A01:0055:5054:9ABC:ABB0"
  zone_name    = "kopicloud.local"
}
```


Output the created DNS AAAA Record:

```
output "dns_aaaa_record" {
  description = "Created DNS AAAA Record"
  value       = resource.kopicloud_dns_aaaa_record.test_aaaa
}
```


Output the Hostname of the created DNS AAAA Record:

```
output "dns_aaaa_record_hostname" {
  description = "Hostname of Created DNS AAAA Record"
  value       = resource.kopicloud_dns_aaaa_record.test_aaaa.hostname
}
```

----

## List ALL DNS AAAA Records


List All DNS AAAA Records:

```
data "kopicloud_dns_aaaa_records_list" "test_aaaa_all" {}
```


Returns All DNS AAAA Records:

```
output "OUTPUT_dns_aaaa_records_list_all" {
  description = "List ALL existing DNS AAAA Records"
  value       = data.kopicloud_dns_aaaa_records_list.test_aaaa_all
}
```

----


## List DNS AAAA Records filtered by Zone Name


Filter DNS AAAA Records with the Zone Name:

```
data "kopicloud_dns_aaaa_records_list" "test_aaaa_zone_name" {
  zone_name = "kopicloud.local"
}
```


Returns all DNS AAAA Records that matches the Zone Name:

```
output "OUTPUT_dns_aaaa_records_list_zone_name" {
  description = "List existing DNS AAAA Records filtered by Zone Name"
  value       = data.kopicloud_dns_aaaa_records_list.test_aaaa_zone_name
}
```

----

## List DNS AAAA Records filtered by Hostname

Filter DNS AAAA Records with an IPv6 Address:

```
data "kopicloud_dns_aaaa_records_list" "test_aaaa_ip" {
  ipv6_address = "2001:db8:3333:4444:5555:6666:7777:8888"
}
```


Returns all DNS AAAA Records that matches the IPv6 Address:

```
output "OUTPUT_dns_aaaa_records_list_ip_address" {
  description = "List existing DNS AAAA Records filtered by IPv6 Address"
  value       = data.kopicloud_dns_aaaa_records_list.test_aaaa_ip
}
```

----

## List DNS AAAA Records filtered by Alias

Filter DNS AAAA Records with a Hostname:

```
data "kopicloud_dns_aaaa_records_list" "test_aaaa_hostname" {
  hostname = "computer70v6"
}
```


Returns all DNS AAAA Records that matches the Hostname:

```
output "OUTPUT_dns_aaaa_records_list_hostname" {
  description = "List existing DNS AAAA Records filtered by Hostname"
  value       = data.kopicloud_dns_aaaa_records_list.test_aaaa_hostname
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-aaaa-records)
