---
title: Cannot Log in to the Portal Troubleshooting
description: Cannot Log in to the Portal Troubleshooting
date: 2023-04-09
---

# Troubleshooting: Cannot Log In to the KopiCloud AD API Portal
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

This article explains how to troubleshoot logging in to the KopiCloud AD API Portal issues.

----

## Causes

Common causes of log-in issues:

- The server running KopiCloud AD API is NOT part of the Active Directory domain.

- The user is NOT a member of the Active Directory domain admins or [KopiCloud AD API authentication groups](../security/matrix.md).

- The [DNS Configuration](../settings/dns-config.md) is not correct in the settings file.

- The [Service Account Configuration](../settings/service-account.md) is not correct in the settings file.

