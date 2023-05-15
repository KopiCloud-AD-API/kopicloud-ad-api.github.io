---
title: AD with Terraform
description: Manage Microsoft AD with Terraform
date: 2023-05-15
---

# Active Directory with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage Microsoft Active Directory using the KopiCloud AD Terraform Provider.

----

## AD Terraform Resources

The provider includes **Terraform Resources** to manipulate AD resources:

- ```kopicloud_computer``` - Create, Update, or Destroy an AD Computer

- ```kopicloud_distribution_group``` - Create, Update, or Delete an AD Distribution Group

- ```kopicloud_security_group``` - Create, Update, or Delete an AD Security Group

- ```kopicloud_group_membership``` - Add an AD User to an AD Group

- ```kopicloud_ou``` - Create, Update, or Delete an AD Organization Unit (OU)

- ```kopicloud_user``` - Create, Update, or Delete an AD User

- ```kopicloud_user_disable_account``` - Disable an AD User

- ```kopicloud_user_enable_account``` - Enable an AD User

- ```kopicloud_user_password_reset``` - Reset the Password of an AD User

- ```kopicloud_user_rename_account``` - Rename an AD User

- ```kopicloud_user_unlock_account``` - Unlock an AD User

----

## AD Terraform Data Sources

The provider includes **Terraform Data Sources** to list existing AD resources:

- ```kopicloud_computer_list``` - List AD Computers

- ```kopicloud_distribution_group_list``` - List AD Distribution Groups

- ```kopicloud_security_group_list``` - List AD Security Groups

- ```kopicloud_group_list``` - List all AD Groups

- ```kopicloud_group_membership_list``` - List AD Groups Associated with an AD Username

- ```kopicloud_ou_list``` - List AD Organization Units (OUs)

- ```kopicloud_user_list``` - List Users in the AD

