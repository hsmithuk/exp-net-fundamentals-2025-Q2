
Overview objective is creation of VPC with two subnets and then create Win2025 + Redhat + Ubuntu Server to link.

I decided to keep the same CIDR as instructor Tim  10.200.123.0/24, as that seemed sensible during the process.
I went with geographical name for the VPC 'aberdeen', as at this early stage I hope this helps with the learning and building out the solution.

# VPC Creation
Preview of the VPC showed as: 
![image](https://github.com/user-attachments/assets/04308e70-b1e8-4da5-87d9-9bf480b83d01)

Post Create shows an additional entry under 'route tables'  that starts with rtb-
This is a 'Main route table' which is not in use for this bootcamp.
![image](https://github.com/user-attachments/assets/105eb27e-6ae4-45f5-8584-3fcbe1461069)

Found official documentation:
**Main route table—The route table that automatically comes with your VPC. It controls the routing for all subnets that are not explicitly associated with any other route table**
 https://docs.aws.amazon.com/vpc/latest/userguide/RouteTables.html

# Key pair creations
From the EC2 in AWS selected  Key Pairs under 'Network and Security' and created two keys
1:  ppk  - to use with Linux
2:  pem  - to use on connection to the Win2025 server.

Kept reference to 'aberdeen' in name.  In hindsight this may have been a bad move, time will tell.
![image](https://github.com/user-attachments/assets/0f2f8dd1-917a-4e3e-9305-1753e877c1c9)

# EC2 creations  
 1:  WIn2K 
![image](https://github.com/user-attachments/assets/96611c2b-4064-40fb-8180-02b52714ede8)

Select Edit
![image](https://github.com/user-attachments/assets/3bda4ced-516c-4b2d-ac97-6982bca84aae)

As have control to better define requirements.
![image](https://github.com/user-attachments/assets/5d2030fe-d5e4-45e2-b1bf-c2bded84ae5d)
Here the public IP has been removed and while the private-ip is not public facing, I have still hidden that .

Created a network interface
![image](https://github.com/user-attachments/assets/1bfced4d-ed35-4ff9-81e2-4d73b54ce391)
Selected the 'Private' one.     **Also make sure to link to Security group, which in this case 'allow login'

 Once created  dashboard view.
 ![image](https://github.com/user-attachments/assets/890b4931-0d6c-4d8f-8eff-4e53ba337ab9)

Then Actions > Attach
![image](https://github.com/user-attachments/assets/c30c709a-f0df-4ca2-8d60-e6b82c78fb12)

There is only one VPC to select.  Here the earlier decision to use 'aberdeen' is starting to look like a good choice!
![image](https://github.com/user-attachments/assets/e3e9824d-ac1f-4325-b176-2e48dc8cc6be)
Then select 'Attach'

Going back to the EC2 instance and under Networking, in this case two NICs show.
I've hidden the public IP
![image](https://github.com/user-attachments/assets/db0189e9-3098-4094-ab77-9b82f7e2d6b5)

RDP to the Win2-Server.   '1' download the RDP file
'2'  'Get password' prompts for the PEM file downloaded earlier,

![image](https://github.com/user-attachments/assets/9fb687c3-ac82-4d3e-87e1-943fce0b35ca)



Upload PEM 
![image](https://github.com/user-attachments/assets/87a68fee-e1eb-4d1a-9fa1-2d31552ab184)

Select 'Decrypt' and copy the password.
![image](https://github.com/user-attachments/assets/aac6f09f-e503-4728-833d-d0ada7e101a4)

RDP to the box , using the copied password
![image](https://github.com/user-attachments/assets/0025e295-9720-4f4b-b013-e989407f9bea)

Here is the server.    Public and private IP shows
![image](https://github.com/user-attachments/assets/7409a4ef-46a5-47a9-9e7b-edfeade6cf50)


 2: Ubuntu 
 3: RH
 

