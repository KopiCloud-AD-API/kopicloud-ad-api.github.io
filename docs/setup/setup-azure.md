---
title: Deploying KopiCloud AD API in Azure
description: Deploying KopiCloud AD API in Azure
date: 2023–05-01
---

# Deploying KopiCloud AD API in Azure
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Explore options for running KopiCloud AD API in Microsoft Azure

----

## Manual Deployment in Azure

To deploy an Azure Virtual Machine with KopiCloud AD API, follow the procedure below:

1) Create a Windows Server 2019 or Windows Server 2022 virtual machine from the Azure Portal or PowerShell.

2) Login into the virtual machine and then open the PowerShell console.

3) Paste the PowerShell script located on this [repo](https://github.com/KopiCloud-AD-API/kopicloud-ad-api-setup-scripts) in the PowerShell console, depending on the operating system.

Scripts to setting up the KopiCloud AD API:

* setup-win2019.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2019/SQL Server 2019 Express

* setup-win2022.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2022/SQL Server 2022 Express

4) After the script deployment is completed, restart the machine.

5) Join the machine to the AD Domain to manage using this **KopiCloud AD API** server.

6) Run the **KopiCloud AD API Config tool** located in the folder C:\KopiCloud-AD-API-Config

----

## Deploying in Azure using Terraform

Coming soon!

----

## Deploying in Azure using the Azure Marketplace

Coming soon!
