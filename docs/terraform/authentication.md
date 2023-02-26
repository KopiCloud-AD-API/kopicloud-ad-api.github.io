---
title: Terraform Authentication
description: KopiCloud AD Terraform Provider Authentication
---

# Terraform Authentication

Understand how to configure **KopiCloud AD Terraform Provider** authentication.

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
