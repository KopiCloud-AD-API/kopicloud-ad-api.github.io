---
title: KopiCloud AD API Requirements
description: KopiCloud AD API Requirements
date: 2023–03-24
---

# KopiCloud AD API Requirements
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Review the requirements to install the KopiCloud AD API server in your machine.

- Windows Server machine
- IIS (Internet Information Server)
- SQL Server Database
- Join AD Domain
- CPU, Memory, and Storage
- Operating System

----

## Windows Server Machine

The API runs on a Windows machine; unfortunately, it cannot run on a Windows container today because there are some limitations on Microsoft licensing about what can run on a container.

It also cannot run on a Linux machine because the DNS module requires components to be installed only on Windows machines.

----

## IIS (Internet Information Server)

The API requires **IIS (Internet Information Server)** as a web server.

IIS is automatically installed, if required, and configured with the help of the Setup application.

----

## SQL Server Database

The API requires a **SQL Server Database** to store the information.

The free edition of SQL Server (SQL Server Express) is installed by default.

However, you can update the SQL connection string to connect to another SQL Server.

The installer will take care of all these tasks for you.

----

## Join AD Domain

And the machine needs to be joined to the Active Directory domain that we will manage.

Currently, **the API can only support one AD domain**.

In the future, we will add support for trusted domains.

> **Note:** You can only login into the **KopiCloud AD API Management Console** with an AD joined machine.

----

## CPU, Memory, and Storage

The minimal configuration is 1vCPU and 2GB of RAM.

The memory and CPU requirements are very low; we have been running in a large production environment for several years, with several thousand users,2vCPU, and 8GB of RAM. However, it will depend on your environment.

The recommended configuration is 2vCPUs and 8GB of RAM. 

However the API can run very well in 2vCPUs and 4GB of RAM.

The recommended storage is at least 30 GB in the C drive, including OS, SQL Server, IIS, and application code. 

> **Note:** The minimum storage required will vary depending on your cloud provider. For example, AWS allows the deployment of Windows Servers with 30GB EBS disks, when GCP requires 50GB disks.

----

## Operating Systems

We tested **KopiCloud AD API** in Windows Server 2022 and Windows Server 2019.

We tested two different recommended scenarios:

- Windows Server 2022 with SQL Server 2022
- Windows Server 2019 with SQL Server 2019.

These two scenarios were successfully tested on AWS, Azure, GCP, OCI, VMware, and Hyper-V.
