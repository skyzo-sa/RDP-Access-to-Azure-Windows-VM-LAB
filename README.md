# RDP Access to Azure Windows VM (Port Forwarding) LAB

## Objective

The main objective of this LAB is to allow RDP to Windows Server VM in Azure.

### Job Skills Learned

- Cloud Networking & Security
- Deploying Sophos XG/XGS firewall in Azure
-  Configuring WAN and LAN interfaces
- Network Segmentation & Routing
- Cybersecurity & Compliance


### Tools Used

- Microsoft Azure Portal
- Sophos XGS Firewall v21.0 (virtual instance) 
- Access to the Sophos Central Management Portal
- SFOS 21.0 Web Interface (GUI)
- SFOS 21.0 Command Line Interface (CLI)
- Control Center Dashboard: Built-in monitoring tool for real-time traffic and event analysis.


*Ref 1: Network Diagram*
![image](https://github.com/user-attachments/assets/d49ecb0d-2977-440f-a3c3-0e56ac6c9940)

 




## CONFIGURATION STEPS

This outlines the steps needed to enable Remote Desktop Protocol (RDP) access to a Windows Server Virtual Machine (VM) in Azure, ensuring proper network configuration and security policies.
![image](https://github.com/user-attachments/assets/4aed08af-f642-4c4a-a664-3fee597d33cb)

 

-	1. Create Windows VM in Azure	
![image](https://github.com/user-attachments/assets/b8e26b8a-c00c-4cef-9e85-ef0ac577aec7)
![image](https://github.com/user-attachments/assets/f431850d-b686-44c1-a614-10554449b5a2)
![image](https://github.com/user-attachments/assets/a3601499-4bac-43ba-9067-48ba127d558e)
![image](https://github.com/user-attachments/assets/4f92540b-a2f1-4fa4-8b16-356d1b4b26f7)
![image](https://github.com/user-attachments/assets/c44e3814-a1a0-4e0d-b121-1ce2ff2c8fb8)
 
 
 
 
 
 


-	2. Create Route Table	
  ![image](https://github.com/user-attachments/assets/65274ae9-c6aa-4b5d-b722-ad3de87d70a1)
 ![image](https://github.com/user-attachments/assets/8865459e-3ed5-4e6e-8033-cbb698c3f590)
![image](https://github.com/user-attachments/assets/a9236cd9-0fb1-4fd3-b43f-61ca67a322c8)
![image](https://github.com/user-attachments/assets/7a418b38-3983-4502-98c1-2c6d7318345e)
![image](https://github.com/user-attachments/assets/ff804fe5-1df0-4f7e-876a-9dd8a32f22a8)
![image](https://github.com/user-attachments/assets/4c072a73-5518-4161-8413-1da732de0a18)

 
Add Subnets
![image](https://github.com/user-attachments/assets/d06cba41-e259-49b3-9925-7fcbc5b26968)
![image](https://github.com/user-attachments/assets/8f401fc8-0a9c-4f30-92cd-5da985a6e891)
 
 


-	3. Allow RDP in Security Groups	
![image](https://github.com/user-attachments/assets/bec5feca-fc98-43b1-8e6c-89c26be7726a)
![image](https://github.com/user-attachments/assets/fd799ad1-08cf-47be-a98f-943e41c744f4)
	 


-	4. Create DNAT Rules in Sophos
![image](https://github.com/user-attachments/assets/a347c5d8-f1f4-4bd5-927b-934bcbbf492a)
![image](https://github.com/user-attachments/assets/78ba078e-336c-4a3e-80ab-5967748b92c1)
 
 
Add IP Host of the Windows Server
![image](https://github.com/user-attachments/assets/6e3050d9-5e72-4de9-a726-06563fcf9413)
 
Add  Services
![image](https://github.com/user-attachments/assets/96aeae60-2a1f-4b0c-9f10-80f6b9dba09a)

 
Rules and Policies
![image](https://github.com/user-attachments/assets/398b9e09-e730-412d-816f-2b518c38ebaa)
![image](https://github.com/user-attachments/assets/34f962e1-7564-42f3-b452-8ffc47333a4e)
![image](https://github.com/user-attachments/assets/e29ac5d8-faa4-403b-ae3e-666e6543f993)
 
 
 
DNAT to Azure AD server rules has been created and NAT rules
![image](https://github.com/user-attachments/assets/420d331a-603d-4195-8ff5-d9e39a225ee0)
![image](https://github.com/user-attachments/assets/ea1f54fd-c442-480a-8afc-77ea348b6eb8)
![image](https://github.com/user-attachments/assets/e14bf16b-9a57-4567-a533-f004d61c14b9)
![image](https://github.com/user-attachments/assets/d9b22721-1eaa-4e7e-b13b-bb15cbd2b558)
![image](https://github.com/user-attachments/assets/ae26305b-7c61-49aa-9df0-e62555ec5a7d)
 
 
 
 
 
