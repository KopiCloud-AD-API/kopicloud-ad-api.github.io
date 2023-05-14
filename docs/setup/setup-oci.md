---
title: Deploying KopiCloud AD API in OCI
description: Deploying KopiCloud AD API in OCI
date: 2023–05-14
---

# Deploying KopiCloud AD API in OCI
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Explore options for running KopiCloud AD API in Oracle Cloud Infrastructure (OCI)

----

## How to Set Up KopiCloud AD API in OCI

1. Get a License - Generate a free trial license (no credit card required) or purchase a license [here](https://www.kopicloud-ad-api.com/get-license)

2. Deploy a **KopiCloud AD API** using the information listed below

3. Join the machine to the AD Domain to manage using the API

4. Create a Service Account with Domain Administrators permissions for the KopiCloud AD API.

5. Run the **KopiCloud AD API Config tool** located in the folder **C:\KopiCloud-AD-API-Config**

----

## Manual Deployment in OCI

To deploy a OCI Virtual Machine with KopiCloud AD API, follow the procedure below:

1. Create a Windows Server 2019 or Windows Server 2022 virtual machine from the OCI Portal.

2. Login into the virtual machine and then open the PowerShell console.

3. Paste the PowerShell script located on this [repo](https://github.com/KopiCloud-AD-API/kopicloud-ad-api-setup-scripts) in the PowerShell console, depending on the operating system.

Scripts to setting up the KopiCloud AD API:

* setup-win2019.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2019/SQL Server 2019 Express

* setup-win2022.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2022/SQL Server 2022 Express

4. After the script deployment is completed, restart the machine.

----

## Deploying the API in OCI using Terraform

To deploy an AWS EC2 Instance with KopiCloud AD API using Terraform, check the repos listed below:

Windows Server 2019/SQL Server 2019 Express, use this [repo](https://github.com/KopiCloud-AD-API/terraform-oci-kopicloud-ad-api-instance-win2019)

Windows Server 2022/SQL Server 2022 Express, use this [repo](https://github.com/KopiCloud-AD-API/terraform-oci-kopicloud-ad-api-instance-win2022)

### Network Configuration

The code will create the network resources (VCN, Subnet, Internet Gateway, Routes).

### Notes

- By default, the download and installation of **SQL Server Management Studio** is disabled because it will take lots of time.

- The default Windows username is **opc**, and get the password from the Terraform output.

```
api_admin_password = "B21AqTpHlai[5"
api_admin_user = "opc"
api_public_ip = "xxx.xxx.xxx.xxx"
```

----

## Configuring OCI Credentials for Terraform

Please read **[How to Configure the Terraform Provider for OCI (Oracle Cloud Infrastructure) with API Key Authentication](https://medium.com/@gmusumeci/how-to-configure-the-terraform-provider-for-oci-oracle-cloud-infrastructure-with-api-key-756b368647b1)** to configure your OCI credentials.
