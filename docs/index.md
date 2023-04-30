---
title: Welcome to KopiCloud AD API
description: Welcome to KopiCloud AD API
date: 2023-03-01
---

# KopiCloud AD API Intro

**KopiCloud AD API** is a REST API designed to manage **Microsoft Active Directory and DNS** in a secure way from custom applications, automation tools, DevOps pipelines, and Terraform.

----

## Why KopiCloud AD API

So, why do you need to use KopiCloud Active Directory API? 


<div class="wrapper" markdown>

-   ![Token List](https://help.kopicloud-ad-api.com/assets/icons/api.png) <span style="color:dodgeblue">No official API from Microsoft</span>

    ---

    There is no official Microsoft API, so if you want to automate access to the Active Directory or DNS, you must write your own API or execute PowerShell commands.



-   ![Token List](https://help.kopicloud-ad-api.com/assets/icons/secure.png) We use Tokens instead of Passwords

    ---

    Instead of using usernames and passwords with WinRM to access Active Directory or DNS, we use an API with authentication tokens. WinRM no required. These tokens can be used for a limited time or forever.



-   ![Token List](https://help.kopicloud-ad-api.com/assets/icons/log.png) We keep a log of everything

    ---

    Every task or action executed is written in a log, so you know who and when they call any API method. Coming soon, you will be able to forward events to several SIEMs.


-   ![Token List](https://help.kopicloud-ad-api.com/assets/icons/terraform.png) Automate AD with our Terraform Provider

    ---

    Create service accounts in AD, create DNS records, create AD Users, create AD Groups, create AD Organization Unit, reset AD User passwords, and more.



-   ![Token List](https://help.kopicloud-ad-api.com/assets/icons/buildings.png) Designed for all kinds of companies

    ---

    We have plenty of pre-configured security access groups. The API provides many options if you are a small company or a large enterprise with a dedicated security team.


-   ![Token List](https://help.kopicloud-ad-api.com/assets/icons/test.png) Production or Test Environment?

    ---

    Both. If you are in production, every call is secured using a token, and everything is logged. Or you can disable the token authentication if running in a test environment.
</div>

----

## A Bit of History

**KopiCloud AD API** was born many years ago from a personal need, as most of our KopiCloud tools. 

In 2014, I started a project called KopiBoot, a tool to automate the deployment of Windows applications on the public and private cloud. This project included the initial code to create resources in Active Directory and DNS, used by this API.

After that, I developed a simple API for customers to integrate their existing apps with Active Directory.

Over the years, I used and expanded the API with many new functionalities for more customers, including DNS and integration with cloud-managed Active Directories, such as **AWS Managed Microsoft AD** and **Azure Active Directory Domain Services (Azure AD DS)**. 

It was implemented in cloud environments in AWS, Azure, GCP, and OCI, from global insurance companies to government entities and startups. 

And lots of these customers loved it so much that they asked to publish it, so they don’t need to maintain it anymore 😊

Publishing a very large and complex web app required lots of time and effort from a team of developers for over a year.

We improved the UI, we created a new setup application, we added new methods, and we add extended some of the existing methods with more functionalities.

We need to test the code to make sure it works perfectly and need to spend hours and hours documenting the API. 

Some of our previous customers, called the API from Terraform and so we decided to create a Terraform Provider, so we need to make many changes so they can work with our Terraform Provider.

And creating the Terraform Provider required rewriting over 40% of the methods and adding a few extra methods.

Our team has worked very hard for more than a year so you don't have to.
