---
title: Configuring KopiCloud AD API
description: Configure KopiCloud AD API Server
date: 2023-04-08
---

# Configuring KopiCloud AD API Setup
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Configuring the KopiCloud AD API on your server

----

## Launching the Setup Config Tool

We created a tool called **KopiCloudAPIConfig.exe** to simplify the API configuration, located in the **C:\KopiCloud-AD-API-Config** folder.

If the folder **C:\KopiCloud-AD-API-Config** doesn't exist, go to **C:\KopiCloud-AD-API-Setup** folder and execute the file **Launch-Config.exe".

> Note #1: **Launch-Config.exe** download the latest version of **KopiCloudAPIConfig.exe** tool.

> Note #2: You can use the file [kopicloud-ad-api-setup.config](setup-configuration-file.md) to automate the Configuration of KopiCloud AD API.

This tool will execute several tasks for you:

- Validate the machine.
- Check if the user logged in is an AD account.
- Check if Service Account is valid.
- Set folder permissions to the Service Account.
- Configure the IIS API Application Pool to use the Service Account.
- Configure the IIS API Web Site to use the Service Account.
- Generate an SSL self-signing certificate.
- Validate SQL Server database connection.
- Update the Application Settings file.
- Restart the IIS to apply changes.

