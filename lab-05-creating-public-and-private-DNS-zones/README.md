# Lab 05 - Azure DNS and Private DNS Zones

## Objective  
Create a public DNS zone and record, verify name resolution, then create a private DNS zone and link it to a virtual network.

---

## Step 1 - Create Public DNS Zone

![Step 1](./screenshots/vnet31.png)

- Navigated to **DNS zones**  
- Clicked **Create**  

---

## Step 2 - Configure DNS Zone

![Step 2](./screenshots/vnet32.png)

- Selected subscription  
- Chose resource group (VNETRG)  
- Entered domain name: **caljshaw.com**  
- Clicked **Review + create**  

---

## Step 3 - Access DNS Zone

![Step 3](./screenshots/vnet33.png)

- Waited for deployment to complete  
- Clicked **Go to resource**  

---

## Step 4 - Navigate to Record Sets

![Step 4](./screenshots/vnet34.png)

- Selected **Recordsets** under DNS Management  

---

## Step 5 - Create DNS Record

![Step 5](./screenshots/vnet35.png)

- Clicked **Add**  
- Configured record:
  - Name: **www**  
  - Type: **A (IPv4 Address)**  
  - IP Address: **10.1.1.4**  
- Clicked **Add**  

---

## Step 6 - Verify DNS Resolution

![Step 6](./screenshots/vnet36.png)

- Used Command Prompt  
- Ran:
  ```
  nslookup www.caljshaw.com ns1-04.azure-dns.com
  ```
- Confirmed resolution to **10.1.1.4**  

---

## Step 7 - Create Private DNS Zone

![Step 7](./screenshots/vnet37.png)

- Navigated to **Private DNS zones**  
- Clicked **Create**  

---

## Step 8 - Configure Private DNS Zone

![Step 8](./screenshots/vnet38.png)

- Selected subscription  
- Chose resource group (VNETRG)  
- Entered name: **private.caljshaw.com**  
- Clicked **Review + create**  

---

## Step 9 - Access Private DNS Zone

![Step 9](./screenshots/vnet39.png)

- Waited for deployment  
- Clicked **Go to resource**  

---

## Step 10 - Link Virtual Network

![Step 10](./screenshots/vnet40.png)
![Step 11](./screenshots/vnet41.png)

- Selected **Virtual network links**  
- Clicked **Add**  
- Configured:
  - Link name: **Manufacturing-Link**  
  - Virtual network: **ManufacturingVnet**  
- Clicked **Create**  

---

## Step 11 - Create Private DNS Record

![Step 12](./screenshots/vnet42.png)

- Navigated to **Recordsets**  
- Clicked **Add**  
- Configured record:
  - Name: **sensorvm**  
  - Type: **A (IPv4 Address)**  
  - IP Address: **10.1.1.4**  
- Clicked **Add**  

---

## Step 12 - Verify Private DNS Record

![Step 13](./screenshots/vnet43.png)

- Confirmed record appears in DNS zone  
- Verified correct IP address assigned to VM  

---

## Summary

- Created a public DNS zone  
- Added an A record for web resolution  
- Verified DNS using nslookup  
- Created a private DNS zone  
- Linked virtual network to private DNS  
- Added internal DNS record for VM  
- Confirmed internal name resolution  

---

## Key Concepts Learned

- Public DNS zones resolve names over the internet  
- Private DNS zones resolve names within virtual networks  
- A records map hostnames to IP addresses  
- Virtual network links allow private DNS resolution inside Azure networks 
