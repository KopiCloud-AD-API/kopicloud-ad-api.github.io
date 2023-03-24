---
title: Event Logging
description: Event Logging in KopiCloud AD API
date: 2023-03-23
---

# Event Logging
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

An event is logged each time an API method is invoked.

These event logs are used to **audit actions performed by the API**, so you know who and when they call any API method.

All the information is stored in a database and can be exported to your favorite SIEM (Security Information and Event Management) software.

By default all events are written to **KopiCloud API Event Log** and the **Windows Event Log**. 

----

## KopiCloud API Event Log

To review the **KopiCloud API Event Log**, log in to the **KopiCloud AD API Management Portal** and click on the **Logs** menu.

Use the top right **filter** to filter events using a date range.

![Event Log](https://help.kopicloud-ad-api.com/assets/docs/event-log.png)

----

## Windows Event Log

**KopiCloud AD API** also can write all the events to the Windows Event Viewer.

Change the [Logging Setting Page](../settings/logging.md) to enable or disable writing events to Windows Event Log.

![Event Log](https://help.kopicloud-ad-api.com/assets/docs/windows_event_log.png)

----

## SIEM Support

Coming soon, you can forward events to several SIEMs such as Splunk, Elastic, Azure Log Analytics, AWS CloudWatch, Datadog, Dynatrace, etc.

Please [Request New Features](https://kopicloud-ad-api.com/Feature) or check our [Roadmap](https://kopicloud-ad-api.com/Feature/Roadmap) to prioritize your favorite SIEM.

