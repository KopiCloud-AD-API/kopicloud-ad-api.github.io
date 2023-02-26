---
description: Welcome to KopiCloud AD API
---

# KopiCloud AD API Intro

**KopiCloud AD API** is an API designed to manage **Microsoft Active Directory and DNS** in secure way from custom applications, automation tools, DevOps pipelines and Terraform.

## Overview

**KopiCloud AD API** was born many years ago from a personal need, as most of our KopiCloud tools. 

In 2014, I started a project called **KopiBoot**, tool to automate deployment of Windows applications on the public and private cloud.
This project, included code to create resouces in Active Directory and DNS.

After that, we developed an simple API for customers to integrate their existing apps with Active Directory. 

Over the years, we used and expanded the API with many new functionalities for more customers, including DNS and integration with cloud-managed Active Directories, such as **AWS Managed Microsoft AD** and **Azure Active Directory Domain Services (Azure AD DS)**. 

It was implemented in cloud environments in AWS, Azure, GCP, and OCI, from global insurance companies to government entities and startups. 

And lots of our customers loved it so much that they asked to publish it, so they don’t need to maintain it anymore 😊

Publishing a very large and complex web app required lots of time and effort from a team of developers for over a year. 

We need to test the code to make sure it works perfectly and need to spend hours and hours documenting the API. 

Some our previous customers, called the API from Terraform and so we decided to create a Terraform Provider, so we need to make many changes so they can work with our Terraform Provider.

## Why KopiCloud AD API

So, why do you want to use KopiCloud Active Directory API? 

> **There is no official API from Microsoft**

So if you want to automate access to Active Directory or DNS, you must write your API or call PowerShell Commands.

> **It is secure**

Instead of using usernames and passwords to access Active Directory or DNS, we use tokens. 
These tokens can be used for a limited time or forever. 

> **We keep a log of everything**

Every task or action is written in a log, so you know who did everything and when they did. 

We will extend logging capabilities to write the log to AWS CloudWatch, Azure Log Analytics, Splunk, Datadog, and other options in the upcoming months.

> **The API was designed with automation in mind**

You can consume the API from your application or use our Terraform module to automate your pipelines.

> **Automate your deployment on the cloud (or on-prem) with our Terraform Module**

Create service accounts in AD, create DNS records, clean up old machines (we hate these machine accounts after a Terraform destroy!), and do everything you can do with the API.

> **Designed for all kinds of companies**

The API provides many options if you are a small company or a large enterprise with a dedicated security team. 

You can create a single account with full access or use a dedicated group with read-only for your information security groups.

We have plenty of pre-configured options, for example, a group to manipulate only DNS records.

> **Production or Development?**

Both are covered. 

If you run in production, we must make a secure call using the token and everything is logged. 

Or you can disable the token authentication if you are running in development.