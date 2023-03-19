---
title: KopiCloud AD API Requirements
description: KopiCloud AD API Requirements
date: 2023-02-28
---

# KopiCloud AD API Requirements
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Review the requirements to install the KopiCloud AD API server.

----

## Requirements

- Windows Server machine

- IIS (Internet Information Server)

- SQL Server Database

- Join AD Domain

- CPU, Memory, and Storage

----

## Windows Server machine

The API runs on a Windows machine; unfortunately, it cannot run on a Windows container today because there are some limitations on Microsoft licensing about what can run on a container. 

It also cannot run on a Linux machine because the DNS module requires components to be installed only on Windows. 

----

## IIS (Internet Information Server)

The API requires **IIS (Internet Information Server)**. 

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

----

## CPU, Memory, and Storage

The minimal configuration is 1vCPU and 2GB of RAM.

The requirements of memory and CPU are very low; we have been running in a large production environment for a couple of years, with several thousand users, with 2vCPU and 4GB of RAM, however, it will depend on your environment. 

The recommended configuration is 2vCPUs and 8GB of RAM.

The storage recommended is at least 30 GB of storage in the C drive, including OS, SQL Server, IIS, and application code.
