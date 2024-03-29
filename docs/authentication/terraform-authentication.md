---
title: Terraform Authentication
description: KopiCloud AD Terraform Provider Authentication
date: 2023-05-15
---

# Terraform Authentication
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Understand how to configure **KopiCloud AD Terraform Provider** authentication.

----

## Set up the Terraform Provider

Login to the **KopiCloud AD API Management Portal** and [generate a token](token-authentication.md).

In your **provider.tf** file, configure the **KopiCloud AD Terraform Provider** with the hostname of your API server and the authentication token.

```
terraform {
  required_providers {
    kopicloud = {
      source = "kopicloud-ad-api/ad"
    }
  }
}

provider "kopicloud" {
  host  = "https://api.kopicloud.local"
  token = "Basic b3NjYWI8UzFsdkyQMVsuD70"
}
```
