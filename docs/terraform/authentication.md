---
title: Terraform Authentication
description: KopiCloud AD Terraform Provider Authentication
---

# Terraform Authentication

Understand how to configure **KopiCloud AD Terraform Provider** authentication.

[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)


----

# Set up the Terraform Provider

Login to the KopiCloud AD API Terraform Provider management website and generate a token.

Configure the KopiCloud Provider with the hostname of your API server and the authentication token.

```
terraform {
  required_providers {
    kopicloud = {
      source = "kopicloud/ad"
    }
  }
}

provider "kopicloud" {
  host  = "https://api.kopicloud.local"
  token = "Basic b3NjYWI8UzFsdkyQMVsuD70"
}
```
