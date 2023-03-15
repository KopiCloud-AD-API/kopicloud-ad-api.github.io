---
title: Setup Details
description: Setup Details
date: 2023-xx-xx
---

# Setup Details
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Details about the Setup Tool for KopiCloud AD API.

-----

## Building the Setup Tool

When we decided to publish **KopiCloud AD API**, one of the first tasks was create a Setup to deploy it in a server.

The webapp is very complex to deploy so we don't want the customers spent time installing it.

We evalauted and tested several tools to deploy **KopiCloud AD API**, but we were unable to find a good tool to do it.

So we decided to write it :)

-----

## The Setup Process

The setup process is a very long and complex process:

1. Launch the launch-setup

2. The launch-setup will download the latest version of our setup application

3. The launch-setup will execute the setup file that will start the installation of the api

4. The setup creates the WebSite Folder to deploy the Code, by default is C:\KopiCloud-AD-API

5. The setup will verify prerequisites - is the machine a Windows Server?

6. The setup will verify prerequisites - is SQL Server installed?

7. The setup will verify prerequisites - is IIS installed?

8. The setup will verify prerequisites - is the machine joined to an AD Domain?

9. Create a random password for the **KopiCloudADSvc** user.

10. Create a Local Service Account Username, called **KopiCloudADSvc**.

11. Add **KopiCloudADSvc** to the local **Administrators** group.

12. Assign Permissions to the Website Folder with the user **KopiCloudADSvc**

13. Assign Permissions to the Website Folder with the user **KopiCloudADSvc**

14. Download the KopiCloud AD API Code

15. Extract the Files to the WebSite Folder

16. Download the SQL Server executable

17. Extract the SQL Server Media

18. Install the SQL Server

19. Install IIS Service and required components


x. Set permissions
