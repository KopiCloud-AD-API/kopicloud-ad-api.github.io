---
title: AD Users with Terraform
description: Manage AD Users with Terraform
date: 2023-05-15
---

# AD Users with Terraform
[![Terraform](https://img.shields.io/badge/terraform-v1.3+-blue.svg)](https://www.terraform.io/downloads.html) [![KopiCloud_AD_API](https://img.shields.io/badge/kopiCloud_ad-v1.0+-blueviolet.svg)](https://www.kopicloud-ad-api.com)

Manage AD Users in Microsoft Active Directory using the KopiCloud AD Terraform Provider

----

## Resources

### Create an AD User

Create AD User:

```
resource "kopicloud_user" "test" {
  username      = "rsmith"
  password      = var.password
  first_name    = "Robert"
  initials      = "T"
  last_name     = "Smith"
  display_name  = "Robert T Smith"
  company       = "KopiCloud Limited"
  description   = "Marketing Director"
  department    = "Marketing"
  email_address = "robert.smith@kopicloud.net"
}
```

Returns AD User Result:

```
output "OUTPUT_new_user" {
  description = "Created User"
  value       = resource.kopicloud_user.test
  sensitive = true
}
```

----

**Schema**

Required:

- ```password``` (String) - Password
- ```username``` (String) - AD Username

Optional:

- ```change_password_next_logon``` (Boolean) Status of Change Password Next Logon Setting
- ```city``` (String) City
- ```company``` (String) Company Name
- ```country``` (String) Country (use the English Name of the Country)
- ```department``` (String) Company Department
- ```description``` (String) User Description
- ```display_name``` (String) User Display Name
- ```email_address``` (String) User Email Address
- ```first_name``` (String) User First Name
- ```guid``` (String) User GUID
- ```home_folder_directory``` (String) Home Folder Directory
- ```home_folder_drive``` (String) Home Folder Drive
- ```home_folder_path``` (String) Home Folder Path
- ```home_phone``` (String) Home Phone
- ```initials``` (String) User Middle Name Initial
- ```job_title``` (String) Job Title
- ```last_name``` (String) User Last Name
- ```manager``` (String) - Manager Name
- ```mobile_phone``` (String) Mobile Phone
- ```office``` (String) Office Information
- ```office_phone``` (String) Office Phone
- ```ou_path``` (String) OU Path (Distinguished Name) of the User
- ```password_never_expired``` (Boolean) Status of the Password Never Expired Setting
- ```postal_code``` (String) Postal/ZIP Code
- ```profile_logon_script``` (String) Profile Logon Script
- ```profile_path``` (String) Profile Path
- ```rds_allow_logon``` (Boolean) Remote Desktop Allow Logon
- ```rds_connect_drive``` (Boolean) Remote Desktop Connect Drive
- ```rds_home_folder_drive``` (String) Remote Desktop Home Folder
- ```rds_home_folder_path``` (String) Remote Desktop Folder Path
- ```rds_profile_path``` (String) Remote Desktop Profile Path
- ```sam_username``` (String) SAM Account Name (Used by Previous Versions of Windows)
- ```state (String)``` State or Province
- ```street_address``` (String) Street Address
- ```street_po_box``` (String) PO Box Address
- ```username``` (String) Username

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single AD User (see below for nested schema)

----

### Disable an AD User

Disable AD User Account:

```
resource "kopicloud_user_disable_account" "test" {
  username = "guillermo"
}
```

Disabled AD User Account Result:

```
output "OUTPUT_user_disable_account" {
  description = "AD User Enabled"
  value = resource.kopicloud_user_disaable_account.test
}
```

----

**Schema**

Required:

- ```username``` (String) - AD Username to Disable

Optional:

- ```show_fields``` (String) Filter Specific Fields in the Output

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single AD User (see below for nested schema)

----

### Enable an AD User

Enable AD User Account:

```
resource "kopicloud_user_enable_account" "test" {
  username = "guillermo"
}
```

Enabled AD User Account Result:

```
output "OUTPUT_user_enable_account" {
  description = "AD User Enabled"
  value = resource.kopicloud_user_enable_account.test
}
```

----

**Schema**

Required:

- ```username``` (String) - AD Username to Enable

Optional:

- ```show_fields``` (String) Filter Specific Fields in the Output

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single AD User (see below for nested schema)

----

### Reset the Password of an AD User

Reset User Password:

```
resource "kopicloud_user_password_reset" "test" {
  username     = "msmith"
  new_password = var.password
  
  change_password_next_logon = false
}
```

Reset Password Output:

```
output "OUTPUT_user_password_reset" {
  description = "User Password Result"
  value       = resource.kopicloud_user_password_reset.test.result
}
```

----

**Schema**

Required:

- ```new_password``` (String) New Password for the AD User
- ```username``` (String) - AD Username

Optional:

- ```change_password_next_logon``` (Boolean) Force the User to Change the Password on the Next Logon
- ```show_fields``` (String) Filter Specific Fields in the Output

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single AD User (see below for nested schema)

----

### Rename an Active Directory User

Rename AD User:

```
resource "kopicloud_user_rename_account" "test" {
  username     = "carlos"
  new_username = "charlie"
}
```

AD User Rename Result:

```
output "OUTPUT_user_password_rename" {
  description = "Rename AD User"
  value = resource.kopicloud_user_rename_account.test
}
```

----

**Schema**

Required:

- ```username``` (String) - Existing AD Username
- ```new_username``` (String) - New AD Username

Optional:

- ```show_fields``` (String) Filter Specific Fields in the Output

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single AD User (see below for nested schema)

----

### Unlock an Active Directory User

Unlock AD User:

```
resource "kopicloud_user_unlock_account" "test" {
  username = "guillermo"
}
```

Unlock AD User Result:

```
output "OUTPUT_user_unlock_account" {
  description = "User Unlock"
  value = resource.kopicloud_user_unlock_account.test
}
```

----

**Schema**

Required:

- ```username``` (String) - AD Username to Unlock

Optional:

- ```show_fields``` (String) Filter Specific Fields in the Output

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single AD User (see below for nested schema)

----

## Data Sources

### List Users in AD

Get All AD Users:

```
data "kopicloud_user_list" "test_all" { }
```

Returns All AD Users:

```
output "OUTPUT_kopicloud_all_users" {
  description = "All Existing AD Users"
  value       = data.kopicloud_user_list.test_all
}
```

----

Get All AD Users Inside an OU:

```
data "kopicloud_user_list" "test_ou" {
  ou_path = "LDAP://CN=API Service,CN=Managed Service Accounts,DC=kopicloud,DC=local"
}
```

Returns All AD Users Inside an OU:

```
output "OUTPUT_kopicloud_all_users_ou" {
  description = "All Existing AD Users inside an OU"
  value       = data.kopicloud_user_list.test_ou
}
```

----

Get All AD Users Showing Specific Fields :

```
data "kopicloud_user_list" "test_filter" {
  show_fields = "firstName,lastName,displayName"
}
```

Returns all AD Users Showing Specific Fields:

```
output "kopicloud_all_users_filter" {
  description = "All Existing AD Users Showing Specific Fields"
  value       = data.kopicloud_user_list.test_filter
}
```

----

**Schema**

Optional:

- ```ou_path``` (String) OU Path (Distinguished Name)
- ```recursive``` (Boolean) Recursive Search Inside the OU
- ```show_fields``` (String) Filter Specific Fields in the Output

Read-Only:

- ```id``` (String) The ID of this Resource
- ```result``` (List of Objects) Single AD User (see below for nested schema)

----

## Nested Schema for Result

Read-Only:

- ```change_password_next_logon``` (Boolean) Status of Change Password Next Logon Setting
- ```city``` (String) City
- ```company``` (String) Company Name
- ```country``` (String) Country (use the English Name of the Country)
- ```department``` (String) Company Department
- ```description``` (String) User Description
- ```display_name``` (String) User Display Name
- ```email_address``` (String) User Email Address
- ```first_name``` (String) User First Name
- ```guid``` (String) User GUID
- ```home_folder_directory``` (String) Home Folder Directory
- ```home_folder_drive``` (String) Home Folder Drive
- ```home_folder_path``` (String) Home Folder Path
- ```home_phone``` (String) Home Phone
- ```initials``` (String) User Middle Name Initial
- ```job_title``` (String) Job Title
- ```last_name``` (String) User Last Name
- ```manager``` (String) - Manager Name
- ```mobile_phone``` (String) Mobile Phone
- ```office``` (String) Office Information
- ```office_phone``` (String) Office Phone
- ```ou_path``` (String) OU Path (Distinguished Name) of the User
- ```password_never_expired``` (Boolean) Status of the Password Never Expired Setting
- ```postal_code``` (String) Postal/ZIP Code
- ```profile_logon_script``` (String) Profile Logon Script
- ```profile_path``` (String) Profile Path
- ```rds_allow_logon``` (Boolean) Remote Desktop Allow Logon
- ```rds_connect_drive``` (Boolean) Remote Desktop Connect Drive
- ```rds_home_folder_drive``` (String) Remote Desktop Home Folder
- ```rds_home_folder_path``` (String) Remote Desktop Folder Path
- ```rds_profile_path``` (String) Remote Desktop Profile Path
- ```sam_username``` (String) SAM Account Name (Used by Previous Versions of Windows)
- ```state (String)``` State or Province
- ```street_address``` (String) Street Address
- ```street_po_box``` (String) PO Box Address
- ```username``` (String) Username

----

## Notes

**Note #1:** Running this resource with ```terraform apply``` will create or update the AD User and running ```terraform destroy``` will remove this AD User from the Active Directory.

**Note #2:** Use the parameter **ShowFields** to select user fields to show. This optional argument is a comma-separated string with the name of the fields you want to be returned.

- Example: ShowFields=All or ShowFields=* : Return all User Fields

- Example: ShowFields=Username,Firstname : Return Only Username and Firstname Fields

- Example: ShowFields=Null or Empty : Return Default Fields (Username, Firstname, Lastname, Display_Name, Description, Company, Office, Department, Email_Address)

**Note #3:** you cannot set both ```change_password_next_logon = true``` and ```password_never_expires = true``` as is not supported by Active Directory.

**Note #4:** for the Universal Naming Convention (UNC) path of servers in the Profile and the RDS variables use twice backslashes as usual. For example, instead of using ```\\```, use ```\\\\``` and use ```\\``` instead of ```\```.

----

## Source Code

Source code available [here](https://github.com/KopiCloud-AD-API/terraform-kopicloud-ad-api-users)
