---
title: Deploying KopiCloud AD API from AWS Marketplace
description: Deploying KopiCloud AD API from AWS Marketplace
date: 2023–05-15
---

# Deploying KopiCloud AD API from AWS Marketplace
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Explore options for running KopiCloud AD API in Amazon Web Services (AWS)

----

## Deploying API from AWS Marketplace

Deploy an AWS EC2 Instance from the AWS Marketplace image.

Generate a license at https://adapi.kopicloud.com/get-license

When the machine is ready, retrieve your initial administrator password using the AWS CLI or AWS Console.

Log in to the EC2 Instance using the default Windows username (Administrator), and the password retrieved in the previous step.

Join the EC2 Instance to the AD Domain that we will manage using the API and restart the machine.

Run the **KopiCloud AD API Config tool** located in the folder **C:\KopiCloud-AD-API-Config** to finish the setup of the API.

