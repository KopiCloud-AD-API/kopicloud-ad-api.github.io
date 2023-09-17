---
title: Create KopiCloud AD API Authentication Token
description: Create KopiCloud AD API Authentication Token
date: 2023-02-28
---

# Create KopiCloud AD API Authentication Token

[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

**KopiCloud AD API** supports two types of tokens: **JWT Token** and **Basic Token**.

This token will be used to authenticate to the API from application integrations, the API Swagger, and the Terraform Provider.

----

## Login to the KopiCloud AD API Management Portal

Enter your username and password to login:

![Image title](https://adapihelp.kopicloud.com/assets/docs/login.png)

And click on the **Login** button.

----

## Create JWT Token

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

This information can be verified and trusted because it is digitally signed.

JWT tokens  are recommended for applications, for example, Terraform, and they can expire automatically.

To create a **JWT Token**, login to the **KopiCloud AD API Management Portal**, and click on the **JWT Token** menu.

Enter a unique token name and expiration time (or 0 to create a not-expiring token), and click on the **Generate** button.

![Image title](https://adapihelp.kopicloud.com/assets/docs/generate_jwt_token.png)

Then, the token will be generated. Copy the token and store it in a safe place!

![Image title](https://adapihelp.kopicloud.com/assets/docs/generate_jwt_token_result.png)

----

## Create a Basic Token

Basic tokens are created by combining a username and password.

To create a **Basic Token**, login to the **KopiCloud AD API Management Portal**, and click on the **Basic Token** menu.

Enter your username and password, and click on the **Generate** button.

> **Note:** If you change your password, you need to regenerate your **Basic Token**.

![Image title](https://adapihelp.kopicloud.com/assets/docs/generate_basic_token.png)

Then, the token will be generated. Copy the token and store it in a safe place!

![Image title](https://adapihelp.kopicloud.com/assets/docs/generate_basic_token_result.png)
