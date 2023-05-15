---
title: DNS with Terraform
description: Manage Microsoft DNS with Terraform
date: 2023-03-01
---

# DNS with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft DNS Records and DNS Zones using the KopiCloud AD Terraform Provider.

----

## DNS Terraform Resources

The provider includes **Terraform Resources** to manipulate DNS Records and DNS Zones:

- Create and remove DNS A Records

- Create and remove DNS AAAA Records

- Create and remove DNS CNAME Records

- Create and remove DNS Loopkup Zones

- Create and remove DNS Reverse Loopkup Zones

----

## DNS Terraform Data Sources

The provider includes **Terraform Data Sources** to list existing DNS Records and DNS Zones:

- List DNS A Records

- List DNS AAAA Records

- List DNS CNAME Records

- List All DNS Zones

- List DNS Loopkup Zones

- List DNS Reverse Loopkup Zones




---
title: AD Terraform Resources and Data Sources
description: Manage Microsoft AD with KopiCloud AD API
date: 2023-05-15
---

# AD Terraform Resources and Data Sources
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft AD resources using the KopiCloud AD API and Terraform.

----

## Resources

- ad_kopicloud_computer
ad_kopicloud_distribution_group
ad_kopicloud_group_membership
ad_kopicloud_ou
ad_kopicloud_security_group
ad_kopicloud_user
ad_kopicloud_user_disable_account
ad_kopicloud_user_enable_account
ad_kopicloud_user_password_reset
ad_kopicloud_user_rename_account
ad_kopicloud_user_unlock_account


----

## Data Sources



ad_kopicloud_computer_list
ad_kopicloud_distribution_group_list
ad_kopicloud_group_list
ad_kopicloud_group_membership_list
ad_kopicloud_ou_list
ad_kopicloud_security_group_list
ad_kopicloud_user_list



