---
title: Troubleshooting SQL Issues
description: Troubleshooting SQL Issues
date: 2023-04-10
---

# Troubleshooting SQL Server Issues
[![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://adapi.kopicloud.com)

This article explains how to troubleshoot SQL Server database errors.

----

## Error Creating or Connecting to the SQL Server Database

When you run the **KopiCloud AD API Setup** tool, you receive the **A network-related or instance-specific error occurred while establishing a connection to SQL Server** error.

Error #1:
```
System.Data.SqlClient.SqlException
HResult=0x80131904
Message=A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible.
Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)
Source=.Net SqlClient Data Provider
```

Error #2:
```
System.Data.SqlClient.SqlException
HResult=0x80131904
Message=A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible.
Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: SQL Network Interfaces, error: 26 - Error Locating Server/Instance Specified)
```

**Explanation:**

These errors are related to SQL Server Configuration.

**Solution:**

Open SQL Server Connection Manager and verify that all protocols are enabled.

Expand **SQL Native Client 11.0 Configuration (32bit)** / **Client Protocols**

On the right pane, make sure that all protocols are enabled.

If any is disabled, right-click it and select Enable.

Configure **Shared Memory** as order 1, **TCP/IP** as order 2, and **Named Pipes** as order 3.

![Troubleshooting SQL Connections](https://adapihelp.kopicloud.com/assets/docs/troubleshooting_sql_connection_1.png)

Then expand **SQL Server Network Configuration** / **Protocols for MSSQLSERVER**.

On the right pane, make sure that all protocols are enabled.

If any is disabled, right-click it and select Enable.

![Troubleshooting SQL Connections](https://adapihelp.kopicloud.com/assets/docs/troubleshooting_sql_connection_2.png)

Double-click the TCP/IP row to open the **TCP/IP Properties** window.

Click on the IP Address tab to check the correct IP Addresses are Active and Enabled.

![Troubleshooting SQL Connections](https://adapihelp.kopicloud.com/assets/docs/troubleshooting_sql_connection_3.png)

----

> **Note:** Check the [A network-related or instance-specific error occurred while establishing a connection to SQL Server](https://learn.microsoft.com/en-us/troubleshoot/sql/database-engine/connect/network-related-or-instance-specific-error-occurred-while-establishing-connection) support documentation if you still have SQL connection issues.

