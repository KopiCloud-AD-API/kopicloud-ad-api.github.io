---
title: Cannot Log in to the Portal Troubleshooting
description: Cannot Log in to the Portal Troubleshooting
date: 2023-05-14
---

# Troubleshooting: Cannot Log In to the KopiCloud AD API Portal
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

This article explains how to troubleshoot logging in to the KopiCloud AD API Portal issues.

----

## Causes

Common causes of log-in issues:

- You are trying to log in with the API Service Account. For security reasons, logging in with the service account is NOT allowed.

- The KopiCloud AD API server is NOT part of the Active Directory domain.

- The user is NOT a member of the Active Directory domain admins or [KopiCloud AD API authentication groups](../security/matrix.md).

- The [DNS Configuration](../settings/dns-config.md) is not correct in the settings file.

- The [Service Account Configuration](../settings/service-account.md) is not correct in the settings file.

