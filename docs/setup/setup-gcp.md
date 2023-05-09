---
title: Deploying KopiCloud AD API in GCP
description: Deploying KopiCloud AD API in GCP
date: 2023–05-10
---

# Deploying KopiCloud AD API in GCP
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Explore options for running KopiCloud AD API in Google Cloud Platform (GCP)

----

## How to Set Up KopiCloud AD API in GCP

1. Get a License - Generate a free trial license (no credit card required) or purchase a license [here](https://www.kopicloud-ad-api.com/get-license)

2. Deploy a **KopiCloud AD API** using the information listed below

3. Join the machine to the AD Domain to manage using the API

4. Run the **KopiCloud AD API Config tool** located in the folder **C:\KopiCloud-AD-API-Config**

----

## Manual Deployment in GCP

To deploy a GCP Virtual Machine with KopiCloud AD API, follow the procedure below:

1. Create a Windows Server 2019 or Windows Server 2022 virtual machine from the GCP Portal or gcloud CLI.

2. Login into the virtual machine and then open the PowerShell console.

3. Paste the PowerShell script located on this [repo](https://github.com/KopiCloud-AD-API/kopicloud-ad-api-setup-scripts) in the PowerShell console, depending on the operating system.

Scripts to setting up the KopiCloud AD API:

* setup-win2019.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2019/SQL Server 2019 Express

* setup-win2022.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2022/SQL Server 2022 Express

4. After the script deployment is completed, restart the machine.

----

## Deploying in GCP using Terraform

To deploy a GCP Virtual Machine with KopiCloud AD API using Terraform, check the repos listed below:

Windows Server 2019/SQL Server 2019 Express, use this [repo](https://github.com/KopiCloud-AD-API/terraform-gcp-kopicloud-ad-api-instance-win2019)

Windows Server 2022/SQL Server 2022 Express, use this [repo](https://github.com/KopiCloud-AD-API/terraform-gcp-kopicloud-ad-api-instance-win2022)

### Network Configuration

The code will create the network resources (VCP, and Subnet).

### Notes

- By default, the download and installation of **SQL Server Management Studio** is disabled because it will take lots of time.

- To get the credentials, login to GCP console and reset the password.

### Configuring Google Cloud Credentials

Please read **How to Create a Service Account for Terraform in GCP (Google Cloud Platform)** to configure your GCP credentials.
https://medium.com/@gmusumeci/how-to-create-a-service-account-for-terraform-in-gcp-google-cloud-platform-f75a0cf918d1

----

## Deploying in GCP using the GCP Marketplace

Coming soon!
