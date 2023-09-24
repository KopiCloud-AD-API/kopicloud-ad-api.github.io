---
title: Deploying KopiCloud AD API from AWS Marketplace
description: Deploying KopiCloud AD API from AWS Marketplace
date: 2023–09-25
---

# Deploying KopiCloud AD API from AWS Marketplace
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Deploying an EC2 Instance with KopiCloud AD API from AWS Marketplace

----

## Deploying API from AWS Marketplace

To deploy an AWS EC2 Instance With KopiCloud AD API from the AWS Marketplace image, follow the procedure below:


1. Open the Amazon EC2 console at (https://console.aws.amazon.com/ec2).


2. From the Amazon EC2 console dashboard, choose **Launch instance**.

![Launch EC2 Instance](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-01.png) 


3. Under **Application and OS Images (Amazon Machine Image)**, type **kopicloud** and click on **Browse more AMIs** link.

![Search AMI](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-02.png) 


4. Choose the **AWS Marketplace AMIs** tab to show all KopiCloud AMIs available:

![List AMIs](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-03.png) 


5. To choose the right KopiCloud AD API product version for you, choose the **Select** button next to the operating system.

A dialog box opens with an overview of the version of the KopiCloud AD API you've selected.

![Selected AMI](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-04.png) 

> Note: You will only pay AWS EC2 costs as the KopiCloud AD API license in AWS is BYOL (Bring your own license).


6. After we selected the image, we need to configure the EC2 Instance

6.1. Under **Name and tags**, for Name, enter a descriptive name for your instance.

![EC2 Instance Name](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-05.png)

6.2. For **Instance type**, select an instance type for your instance. T3.Medium or T3.Large is recommended for the setup.

![EC2 Instance Type](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-06.png)

6.3. Under **Key pair (login)** section, for Key pair name, choose an existing key pair or create a new one.

![EC2 Instance Key Pair](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-07.png)

6.4. Under **Network settings, Firewall (security groups)**, please review the new security group that was created for **KopiCloud AD API**.

The security group includes rules that allow all IPv4 addresses (0.0.0.0/0) access on RDP (port 3389) on Windows.

> Note: We recommend adjusting these rules to allow only a specific address or range of addresses to access your instance over those ports.

![EC2 Instance Security Group](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-08.png)

6.5. In the section **Configure storage**, you can keep or increase the 30 GB default size.

![EC2 Instance Storage](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-09.png)


7. In the **Summary panel**, under Software Image (AMI), check the details of the AMI from which you're about to launch the instance.

Also, check the other configuration details that you specified. When you're ready to launch your instance, choose the **Launch instance** button.

![EC2 Instance Summary](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-10.png)

Depending on the product you've subscribed to, the instance might take a few minutes or more to launch.

You are first subscribed to the product before your instance can launch.

![EC2 Instance Registration](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-11.png)

If there are any problems with your credit card details, you will be asked to update your account details.

When the launch confirmation page displays, choose **View all instances** to go to the **Instances** page.


8. Generate a license at (https://adapi.kopicloud.com/get-license)


9. When the machine is ready, retrieve your initial administrator password using the AWS CLI or AWS Console.

In the AWS Console, select the new instance, then click on **Actions** menu, select **Security**, and then **Get Windows password**.

![EC2 Instance Password](https://adapihelp.kopicloud.com/assets/marketplace/aws-marketplace-12.png)

Follow the instructions to retrieve the password.


10. Log in to the EC2 Instance using the default Windows username (Administrator), and the password retrieved in the previous step.


11. Join the EC2 Instance to the AD Domain that we will manage using the API and restart the machine.

Note: Based on the VPC and Subnet configuration, extra steps may be required to join the machine to the domain.


12. Run the **KopiCloud AD API Config tool** located in the folder **C:\KopiCloud-AD-API-Config** to finish the setup of the API.
