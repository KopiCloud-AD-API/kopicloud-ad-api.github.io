---
title: Marketplace Images Credentials
description: KopiCloud AD API Marketplace Images Credentials
date: 2023-03-18
---

# KopiCloud AD API Marketplace Images Credentials
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

When you deploy a **KopiCloud AD API** server using a cloud provider marketplace (AWS, Azure, GCP), your server will be provisioned with serveral DEFAULT credentials.

> **Note:** to keep your server safe, is recommended to change these passwords with a secure password.

-----

## List of Credentials

This is the list of users required by KopiCloud AD API:

**Local User Accounts**

Windows local accounts used to authenticate to the server, manage IIS and login into the KopiCloud AD API management portal.

- Administrator: used to login to the server
- KopiCloudSvc: service account used by IIS

**SQL Accounts:

- SQL SA: used to manage the SQL Server in SQL Mode
- KopiCloudAPI: used to authenticate to SQL Server Database

-----

## Administrator

Windows local administrator account used to authenticate to the server.

Username: Administrator
Password: **K0p1Cl0ud**

-----

## KopiCloudSvc

Windows local administrator account used by IIS.

Username: KopiCloudSvc
Password: **K0p1Cl0ud**

-----

 ## SQL SA

Account used in SQL Mode to manage the SQL Server.

Username: sa
Password: **K0p1Cl0udAdm1n**

-----

## KopiCloudAPI:

SQL Account used to authenticate to SQL Server Database

Username: KopiCloudAPI
Password: K0p1Cl0ud
