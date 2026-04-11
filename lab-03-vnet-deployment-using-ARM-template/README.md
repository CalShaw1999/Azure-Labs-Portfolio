# Lab 03 - Azure Virtual Network Deployment Using ARM Template

## Objective  
Deploy a virtual network in Azure using an exported and modified ARM template.

---

## Step 1 - Export Existing VNet Template

![Step 1](./screenshots/vnet6.png)
![Step 2](./screenshots/vnet7.png)
![Step 3](./screenshots/vnet8.png)

- Navigated to an existing virtual network  
- Selected **Export template** under Automation  
- Downloaded the **template.json** and **parameters.json** files  

---

## Step 2 - Modify Template and Parameters

![Step 4](./screenshots/vnet9.png)

- Opened both JSON files in Visual Studio Code  
- Modified:
  - Virtual network name  
  - Address space  
  - Subnet names and ranges  
- Ensured consistency across template and parameters  

---

## Step 3 - Deploy Custom Template

![Step 5](./screenshots/vnet10.png)

- Navigated to **Deploy a custom template** in Azure  
- Selected **Build your own template in the editor**

---

## Step 4 - Upload Template and Parameters

![Step 6](./screenshots/vnet11.png)
![Step 7](./screenshots/vnet12.png)
![Step 8](./screenshots/vnet13.png)
![Step 9](./screenshots/vnet14.png)

- Uploaded the modified **template.json**  
- Uploaded the modified **parameters.json**  
- Confirmed configuration values were correct  

---

## Step 5 - Review and Create Deployment

![Step 10](./screenshots/vnet15.png)

- Reviewed deployment settings  
- Validated template  
- Clicked **Create**  

---

## Step 6 - Verify Deployment

![Step 11](./screenshots/vnet16.png)

- Confirmed new virtual network appeared in resource group  

---

## Step 7 - Review Created VNet

![Step 12](./screenshots/vnet17.png)

- Opened the newly created virtual network  
- Verified:
  - Address space  
  - Subnets  
  - Configuration matched template  

---

## Summary

- Exported an existing virtual network as an ARM template  
- Modified template and parameters for a new deployment  
- Deployed infrastructure using Infrastructure as Code  
- Verified successful creation of the new virtual network  
