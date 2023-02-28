---
title: Welcome to KopiCloud AD API
description: Welcome to KopiCloud AD API
date: 2023-02-28
---

# KopiCloud AD API Intro

**KopiCloud AD API** is a REST API designed to manage **Microsoft Active Directory and DNS** in a secure way from custom applications, automation tools, DevOps pipelines, and Terraform.

----

## A Bit of History

**KopiCloud AD API** was born many years ago from a personal need, as most of our KopiCloud tools. 

In 2014, I started a project called KopiBoot, a tool to automate the deployment of Windows applications on the public and private cloud. This project included the initial code to create resources in Active Directory and DNS, used by this API.

After that, I developed a simple API for customers to integrate their existing apps with Active Directory.

Over the years, I used and expanded the API with many new functionalities for more customers, including DNS and integration with cloud-managed Active Directories, such as **AWS Managed Microsoft AD** and **Azure Active Directory Domain Services (Azure AD DS)**. 

It was implemented in cloud environments in AWS, Azure, GCP, and OCI, from global insurance companies to government entities and startups. 

And lots of our customers loved it so much that they asked to publish it, so they don’t need to maintain it anymore 😊

Publishing a very large and complex web app required lots of time and effort from a team of developers for over a year. 

We need to test the code to make sure it works perfectly and need to spend hours and hours documenting the API. 

Some of our previous customers, called the API from Terraform and so we decided to create a Terraform Provider, so we need to make many changes so they can work with our Terraform Provider.

And creating the Terraform Provider required rewriting over 40% of the methods and adding a few extra methods.

----

## Why KopiCloud AD API

So, why do you want to use KopiCloud Active Directory API? 

> **There is no official API from Microsoft**

So if you want to automate access to Active Directory or DNS, you must write your API or call PowerShell Commands.

> **It is secure**

Instead of using usernames and passwords to access Active Directory or DNS, we use [authentication tokens](/authentication/token-authentication.md)

These tokens can be used for a limited time or forever. 

> **We keep a log of everything**

Every task or action is written in a log, so you know who did everything and when they did it. 

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
