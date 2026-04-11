# Lab 04 - Azure Network Security Groups (NSG) and Application Security Groups (ASG)

## Objective  
Create an Application Security Group and Network Security Group, associate the NSG with a subnet, and configure inbound and outbound security rules.

---

## Step 1 - Create Application Security Group (ASG)

![Step 1](./screenshots/vnet18.png)

- Navigated to **Application security groups**  
- Clicked **Create**  

---

## Step 2 - Configure ASG Details

![Step 2](./screenshots/vnet19.png)

- Selected subscription  
- Chose resource group (VNETRG)  
- Named ASG: **asg-web**  
- Selected region (East US)  
- Clicked **Review + create**  

---

## Step 3 - Create Network Security Group (NSG)

![Step 3](./screenshots/vnet20.png)

- Navigated to **Network security groups**  
- Clicked **Create**  

---

## Step 4 - Configure NSG Details

![Step 4](./screenshots/vnet21.png)

- Selected subscription  
- Chose resource group (VNETRG)  
- Named NSG: **NSGsecure**  
- Selected region (East US)  
- Clicked **Review + create**  

---

## Step 5 - Access Deployed NSG

![Step 5](./screenshots/vnet22.png)

- Waited for deployment to complete  
- Clicked **Go to resource**  

---

## Step 6 - Navigate to Subnets

![Step 6](./screenshots/vnet23.png)

- Selected **Subnets** under Settings  
- Prepared to associate NSG with a subnet  

---

## Step 7 - Associate NSG with Subnet

![Step 7](./screenshots/vnet24.png)
![Step 8](./screenshots/vnet25.png)

- Clicked **Associate**  
- Selected:
  - Virtual network: **CoreVnet**  
  - Subnet: **Leadership_Subnet**  
- Clicked **OK**  

---

## Step 8 - Create Inbound Security Rule

![Step 9](./screenshots/vnet26.png)
![Step 10](./screenshots/vnet27.png)

- Navigated to **Inbound security rules**  
- Clicked **Add**  
- Configured rule:
  - Source: Application Security Group (**asg-web**)  
  - Ports: **80, 443**  
  - Protocol: **TCP**  
  - Action: **Allow**  
  - Priority: **100**  
  - Name: **AllowASG**  
- Clicked **Add**  

---

## Step 9 - Create Outbound Security Rule

![Step 11](./screenshots/vnet28.png)
![Step 12](./screenshots/vnet29.png)

- Navigated to **Outbound security rules**  
- Clicked **Add**  
- Configured rule:
  - Destination: **Internet (Service Tag)**  
  - Ports: **Any**  
  - Protocol: **Any**  
  - Action: **Deny**  
  - Priority: **4096**  
  - Name: **DenyInternetOutbound**  
- Clicked **Add**  

---

## Step 10 - Verify Security Rules

![Step 13](./screenshots/vnet30.png)

- Reviewed NSG configuration  
- Confirmed:
  - Inbound rule allowing ASG traffic  
  - Outbound rule denying internet access  

---

## Summary

- Created an Application Security Group (ASG)  
- Created a Network Security Group (NSG)  
- Associated NSG with a subnet  
- Configured inbound rule to allow web traffic from ASG  
- Configured outbound rule to block internet access  
- Verified rules were successfully applied
