---
title: Manage Microsof DNS AAAA Records with Terraform
---

# Manage Microsof DNS AAAA Records with Terraform

How to manage Microsoft DNS AAAA Records in AD DNS using the KopiCloud AD API Terraform Provider:

## Create DNS AAAA Records

Create a DNS AAAA Record for a computer:

```
resource "kopicloud_dns_aaaa_record" "test_aaaa" {
  hostname     = "computer75v6"
  ipv6_address = "2340:0023:AABA:0A01:0055:5054:9ABC:ABB0"
  zone_name    = "kopicloud.local"
}
```

Output Created DNS AAAA Record:

```
output "dns_aaaa_record" {
  description = "Created DNS AAAA Record"
  value       = resource.kopicloud_dns_aaaa_record.test_aaaa
}
```

```
output "dns_aaaa_record_hostname" {
  description = "Hostname of Created DNS AAAA Record"
  value       = resource.kopicloud_dns_aaaa_record.test_aaaa.hostname
}
```

## List ALL DNS AAAA Records

## List DNS AAAA Records filtered by Zone Name

## List DNS AAAA Records filtered by Hostname

## List DNS AAAA Records filtered by Alias


## Source Code

Source code available at https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-dns-aaaa-records
