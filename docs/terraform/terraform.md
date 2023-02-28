---
title: Active Directory as Code
description: Active Directory as Code with Terraform
date: 2023-03-01
---

# Active Directory as Code

Use **KopiCloud AD Terraform Provider** to automate your Active Directory and Microsoft DNS tasks in the public cloud (AWS, Azure, GCP).

![azure-gcp-aws-terraform](https://help.kopicloud-ad-api.com/assets/docs/logos-azure-gcp-aws-terraform.png "Active Directory as Code with Terraform")

We developed a Terraform Provider to interact with the KopiCloud AD API from your IaC code and CI/CD pipelines.

Explore our **Terraform Provider Documentation** or clone examples from our [GitHub Repos](https://github.com/orgs/KopiCloud-AD-API/repositories) and you can create CI/CD pipelines to interact with AD and Microsoft DNS in minutes!

----

# Set up the Terraform Provider

To configure the Terraform provider, login to the **KopiCloud AD API Management Website** and generate an [Authentication Token](../authentication/token-authentication.md).

 > KopiCloud AD uses Authentication Tokens to authenticate to AD instead of usernames and passwords.

Then configure the **KopiCloud AD Terraform Provider** with the hostname of your API server and the authentication token.

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





