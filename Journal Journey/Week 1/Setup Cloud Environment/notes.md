
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
 2: Ubuntu 
 3: RH
 

