# Lab 02 - Azure Virtual Network (VNet) Creation

## Objective  
Create a virtual network in Azure, define an address space, and configure subnets.

---

## Step 1 - Navigate to Virtual Networks

![Step 1](./screenshots/Vnet1.png)

- Went to Azure Portal  
- Searched for **Virtual networks**  
- Selected **Create**

---

## Step 2 - Configure Basics

![Step 2](./screenshots/Vnet2.png)

- Selected subscription  
- Chose resource group (VNETRG)  
- Set virtual network name (CoreVnet)  
- Selected region (East US)  

---

## Step 3 - Configure Address Space

![Step 3](./screenshots/Vnet3.png)

- Set IPv4 address space to **10.20.0.0/16**  
- Reviewed available IP range  
- Prepared to segment network into subnets  

---

## Step 4 - Create Subnet

![Step 4](./screenshots/Vnet4.png)

- Added new subnet  
- Named subnet: **Leadership_Subnet**  
- Set subnet range to **10.20.20.0/24**  
- Enabled private subnet setting (no default outbound access)  

---

## Step 5 - Deploy and Review VNet

![Step 5](./screenshots/Vnet5.png)

- Reviewed configuration  
- Deployed virtual network  
- Verified address space and subnet creation  

---

## Summary

- Created a virtual network in Azure  
- Defined a custom IP address space  
- Created and configured a subnet  
- Deployed and validated the network configuration  
