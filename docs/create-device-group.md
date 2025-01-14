# Create Device Group from Fleet Manager


**Job Tags**
* create_device_group
  
**Job Variables**
```
---
#########################################################
## Directories
### For Tower 
## for workstation: iso_download_directory: "/opt/generated_iso"
iso_download_directory: "/tmp/generated_iso"

### For Tower 
## for workstation: workspace: "/opt/lib/aws/projects/workspace"
workspace: "/tmp"

#########################################################
## Required Files
ssh_pub_key: "CHANGEME"

#########################################################
## required variables
create_device_name_group: true
device_group_name: "my-device-name-group"
create_image: true

#########################################################
## image atrributes
image_name: "test-image" # Example: "test-image-11-13-2022-b1"
username: "admin"
distribution: "rhel-87"
description: "sample description"
packages: "curl net-tools podman tar bind-utils git"
arch: "x86_64"
enable_kickstart: false 
kickstart_path: "https://raw.githubusercontent.com/Red-Hat-SE-RTO/rhel-fleet-management/main/inventories/lab/applications/quarkuscoffeeshop-majestic-monolith-fleet-manger/fleet.kspost"

#########################################################
## automated management variables
## https://access.redhat.com/management/activation_keys
rhc_org_id: "1111111"
rhc_activation_key: "CHANGEME"

#########################################################
## optional variables
## osinfo-query os
os_variant: "rhel8.7"

#########################################################
## Dont need to change 
compiled_uri_headers: {}
```


### Survey Variables

**RHEL Username**
* Required: true  
* Question:`RH Username:` . 
* Answer variable name: `rh_authentication_basic_username` . 


**RHEL Password**
* Required: true   
* Question: `RH Password:` . 
* Answer variable name: `rh_authentication_basic_password` . 


**API Token:**
> [Red Hat API Tokens](https://access.redhat.com/management/api) . 
* Required: true  
* Question: `RH Offline API Token:` . 
* Answer variable name: `rh_offline_authentication_api_bearer_token` . 


**Device Group Name:**
* Required: true  
* Question: `Enter Device Group Name:` . 
* Answer variable name: `device_group_name` . 

![image](https://user-images.githubusercontent.com/1975599/233221646-a5ab0ed1-d9e4-43c7-b79e-0e02a1fdfca9.png)
![image](https://user-images.githubusercontent.com/1975599/233221795-87286d29-d4f9-412c-8e08-7caf8b507b73.png)
