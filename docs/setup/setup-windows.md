---
title: Deploying KopiCloud AD API in Windows Servers
description: Deploying KopiCloud AD API in Windows Servers
date: 2023–05-01
---

# Deploying KopiCloud AD API in Windows Servers
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Explore options for running KopiCloud AD API in Windows Servers

----

## How to Set Up KopiCloud AD API in Windows Servers

1. Get a License - Generate a free trial license (no credit card required) or purchase a license [here](https://www.kopicloud-ad-api.com/get-license)

2. Deploy a **KopiCloud AD API** using the information listed below

3. Join the machine to the AD Domain to manage using the API

4. Run the **KopiCloud AD API Config tool** located in the folder **C:\KopiCloud-AD-API-Config**

----

## Manual Deployment in Windows Servers

To deploy a Windows Servers with KopiCloud AD API, follow the procedure below:

1. Create a Windows Server 2019 or Windows Server 2022 virtual machine or physical server.

2. Login into the Windows Servers and then open the PowerShell console.

3. Paste the PowerShell script located on this [repo](https://github.com/KopiCloud-AD-API/kopicloud-ad-api-setup-scripts) in the PowerShell console, depending on the operating system.

Scripts to setting up the KopiCloud AD API:

* setup-win2019.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2019/SQL Server 2019 Express

* setup-win2022.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2022/SQL Server 2022 Express

4. After the script deployment is completed, restart the machine.
