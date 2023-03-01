---
title: DNS CNAME Records with Terraform
description: Manage Microsof DNS CNAME Records with Terraform
---

# DNS CNAME Records
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS CNAME Records in AD DNS using the KopiCloud AD Terraform Provider:

----

## Create a DNS CNAME Record

Create a DNS CNAME Record for a Computer:

```
resource "kopicloud_dns_cname_record" "test_cname" {
  hostname       = "tftestcn01"
  hostname_alias = "tftestcn01_alias"
  zone_name      = "kopicloud.local"
}
```

Output the created DNS CNAME Record:

```
output "dns_cname_record" {
  description = "Created DNS CNAME Record"
  value       = resource.kopicloud_dns_cname_record.test_cname
}
```

----

## List All DNS CNAME Records

List All DNS CNAME Records:

```
data "kopicloud_dns_cname_records_list" "test_cname_all" {}
```

Returns All DNS CNAME Records:

```
output "OUTPUT_dns_cname_records_list_all" {
  description = "List ALL existing DNS CNAME records"
  value       = data.kopicloud_dns_cname_records_list.test_cname_all
}
```

----

## Filter DNS CNAME Records with the Zone Name

Filter DNS CNAME Records with the Zone Name:

```
data "kopicloud_dns_cname_records_list" "test_cname_zone_name" {
  zone_name = "kopicloud.local"
}
```

Returns all DNS CNAME Records that matches the Zone Name:

```
output "OUTPUT_dns_cname_records_list_zone_name" {
  description = "List existing DNS CNAME records in a Zone"
  value       = data.kopicloud_dns_cname_records_list.test_cname_zone_name
}
```

----

## Filter DNS CNAME Records with an Alias


Filter DNS CNAME Records with an Alias:

```
data "kopicloud_dns_cname_records_list" "test_cname_alias" {
  hostname_alias = "computer70_alias"
}
```

Returns all DNS CNAME Records that matches the Alias:

```
output "OUTPUT_dns_cname_records_list_ip_address" {
  description = "List existing DNS CNAME Records with the Alias"
  value       = data.kopicloud_dns_cname_records_list.test_cname_alias
}
```

----

## Filter DNS CNAME Records with a Hostname

Filter the DNS CNAME Records with a Hostname:

```
data "kopicloud_dns_cname_records_list" "test_cname_hostname" {
  hostname = "computer33"
}
```

Returns all DNS CNAME Records that matches the Hostname:

```
output "OUTPUT_dns_cname_records_list_hostname" {
  description = "List Existing DNS CNAME Records"
  value       = data.kopicloud_dns_cname_records_list.test_cname_hostname
}
```

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-cname-records)
