---
title: Configuring KopiCloud AD API
description: Configure KopiCloud AD API Server
date: 2023-04-08
---

# Configuring KopiCloud AD API Setup
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Configuring the KopiCloud AD API on your server

----

## Launching the Setup Config Tool

To simplify the API configuration, we created a tool called **KopiCloudAPIConfig.exe**, located in the **C:\KopiCloud-AD-API-Setup** folder.

This tool will execute several tasks for you:

- Validate the machine.
- Check if the user logged in is an AD account.
- Check if Service Account is valid.
- Set folder permissions to the Service Account.
- Configure the IIS API Application Pool to use the Service Account.
- Configure the IIS API Web Site to use the Service Account.
- Generate an SSL self-signing certificate.
- Restart the IIS to apply changes.
