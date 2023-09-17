---
title: Deploying KopiCloud AD API in AWS
description: Deploying KopiCloud AD API in AWS
date: 2023–05-15
---

# Deploying KopiCloud AD API in AWS
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

Explore options for running KopiCloud AD API in Amazon Web Services (AWS)

----

## How to Set Up KopiCloud AD API in AWS

1. Get a License - Generate a free trial license (no credit card required) or purchase a license [here](https://adapi.kopicloud.com/get-license)

2. Deploy a **KopiCloud AD API** using the information listed below

3. Join the machine to the AD Domain to manage using the API

4. Create a Service Account with Domain Administrators permissions for the KopiCloud AD API.

5. Run the **KopiCloud AD API Config tool** located in the folder **C:\KopiCloud-AD-API-Config**

----

## Manual Deployment in AWS

To deploy an AWS EC2 Instance with KopiCloud AD API, follow the procedure below:

1. Create a Windows Server 2019 or Windows Server 2022 EC2 Instance from the AWS Portal, AWS PowerShell, or AWS CLI.

2. Login into the EC2 Instance and then open the PowerShell console.

3. Paste the PowerShell script located on this [repo](https://github.com/KopiCloud-AD-API/kopicloud-ad-api-setup-scripts) in the PowerShell console, depending on the operating system.

Scripts to setting up the KopiCloud AD API:

* setup-win2019.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2019/SQL Server 2019 Express

* setup-win2022.ps1 = Script to install and Configure KopiCloud AD API in Windows Server 2022/SQL Server 2022 Express

4. After the script deployment is completed, restart the machine.

----

## Deploying in AWS using Terraform

To deploy an AWS EC2 Instance with KopiCloud AD API using Terraform, check the repos listed below:

* Windows Server 2019/SQL Server 2019 Express, use this [repo](https://github.com/KopiCloud-AD-API/terraform-aws-kopicloud-ad-api-instance-win2019)

* Windows Server 2022/SQL Server 2022 Express, use this [repo](https://github.com/KopiCloud-AD-API/terraform-aws-kopicloud-ad-api-instance-win2022)

### Network Configuration

- The code will create a network (VPC and Subnet); if you want to deploy to existing VPC and Subnet, edit the **api-vm-main.tf** file.

in the **aws_security_group** section, comment the vpc_id = aws_vpc.vpc.id line and add the existing vpc id reference, following the example below:

```
resource "aws_security_group" "api-sg" {
  name        = "${lower(var.app_name)}-${var.app_environment}-sg"
  description = "Allow incoming connections"
  //vpc_id      = aws_vpc.vpc.id
  vpc_id      = "vpc-07bc47fcb892f49c2"
```

and then in **aws_instance** section, comment the subnet_id = aws_subnet.public-subnet.id line and add the existing subnet id reference, following the example below:

```
resource "aws_instance" "api-server" {
  ami           = data.aws_ami.windows-2019.id
  instance_type = var.api_instance_type
  //subnet_id     = aws_subnet.public-subnet.id
  subnet_id     = "subnet-0de7e64c5c78e47f4"
```

### Public IP

By default, the code adds a public IP address to the EC2 instance.

If you don't want to publish the API using an external IP, remove the **resource "aws_eip"** and **resource "aws_eip_association"** sections.

And set the variable **api_associate_public_ip_address** to false.

### Notes

- By default, the download and installation of **SQL Server Management Studio** is disabled because it will take lots of time.

- The default Windows username is **Administrator**, and get the password from the AWS Console.

----

## Configuring AWS Credentials for Terraform

Please read **[How to create an IAM account and configure Terraform to use AWS static credentials](https://medium.com/@gmusumeci/how-to-create-an-iam-account-and-configure-terraform-to-use-aws-static-credentials-a8ea4dd4fdfc)** to configure your AWS credentials.

