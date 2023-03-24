---
title: KopiCloud AD API
description: KopiCloud AD API
date: 2023-02-28
---

# KopiCloud AD API
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

The **KopiCloud AD API** is a REST API.

The API can be consumed by making API calls from:

- Different development languages, such as C#, Python, JavaScript, etc.

- Scripting languages such as PowerShell or Bash.

- From the [Swagger UI](swagger-ui.md).

- Using our [Terraform Provider](../terraform/terraform.md).

- KopiCloud AD SDKs, which are currently under development.

----

## What is a REST API?

* API is short for **Application Programming Interface**, a set of rules that lets programs talk to each other, exposing data and functionality in a consistent format.

* REST stands for **Representational State Transfer** and is an architectural pattern that describes how distributed systems can expose a consistent interface.

----

## API Methods

When people use the term **REST API**, they are generally referring to an API accessed using the HTTP protocol at a predefined set of URLs.

These URLs represent various resources with one or more methods that can be performed on them over HTTP, like GET, POST, PUT, and DELETE.

- <span class="btn-get">GET</span> requests data only – and does not modify it in any way.

- <span class="btn-delete">DELETE</span> delete the resources defined in the API method.

- <span class="btn-post">POST</span> is used to create resources.

- <span class="btn-put">PUT</span> is used to update resources.

----

## API Response Codes

REST APIs use the response codes to inform clients of their request's result.

The KopiCloud AD API will return the following API response codes:

| Code | Description                        |
| ---- | ---------------------------------- |
| 200	 | OK - Successful Request            |
| 400	 | Bad Request - Unexpected Error     |
| 401	 | Unauthorized - Invalid Credentials |
| 403	 | Forbidden - Access Denied          |
| 404	 | Not Found - Object Not Found       |

----

## API Authentication

By default, you need an [Authentication Token](../authentication/token-authentication.md) to make API calls.

**KopiCloud AD API** supports two types of tokens: **JWT Token**, and **Basic Token**.

If your token is invalid or expired, the API call will fail, and you will receive a **401 response code**.

----

## API Licensing

You need to install a license of KopiCloud AD API before you can make API calls or use the Terraform Provider.

Get a free trial license [here](https://www.kopicloud-ad-api.com/trial).

If your license is invalid or expired, the API call will fail, and you will receive a **403 response code**.
