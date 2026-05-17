# AWS Secure VPC Bastion Host Project

##  Overview
secure AWS network architecture using Amazon VPC with public and private subnets.  
bastion host is used as a secure entry point to access a private EC2 instance.

AWS არქიტექტურა Amazon VPC-ს გამოყენებით საჯარო და დახურული საბნეტებისთვის. 
Bastion host გამოყენება როგორც უსაფრთხო შესასვლელი private EC2 instance-ზე

---


##  Architecture Design
მოიცავს შემდეგს:

custom VPC (secure-vpc)
public subnet (Bastion Host)
private subnet (Application Server)
internet gateway (IGW)
route tables for public and private subnets
security Groups for controlled access

---

##  Security 
უსაფრთხოების / SG გამოყენება

private EC2 instance has no direct public access
bastion host is the only entry point from the internet
SSH access to private subnet is allowed only from Bastion
security groups restrict unnecessary traffic

---


##  AWS Services 
გამოყენებული სერვისები

Amazon VPC
Amazon EC2
security groups
internet gateway
route tables
SSH (Secure Shell)

---

##  Connectivity 
დაკავშირების პრინციპი

1. user connects to Bastion Host via SSH
2. bastion Host connects to Private EC2 instance
3. private instance is not directly accessible from the internet

---


## Screenshots
სცრინები

### VPC
![VPC](screenshots/VPC.png)
---

### Public Subnet
![Public Subnet](screenshots/public_subnet.png)
---

### Private Subnet
![Private Subnet](screenshots/private_subnet.png)
---

### Internet Gateway
![Internet Gateway](screenshots/IGW.png)
---

### Route Tables
![Route Table](screenshots/RT.png)
![Public Route Table](screenshots/Public-RT.png)
![Private Route Table](screenshots/Private-RT.png)
---

### Security Groups
![Bastion Security Group](screenshots/Bastion-SG.png)
![Private Security Group](screenshots/Private-SG.png)

---

### EC2 Instances
![Bastion EC2](screenshots/EC2-Bastion.png)
![Private EC2](screenshots/EC2-Private.png)
---

### Bastion to Private Connection
![SSH Connection](screenshots/bastion_to_private.png)
---





##  Author
Giorgi Petriashvili
გიორგი პეტრიაშვილი

Network Engineer (NOC Experience)  
Building Cloud skills with AWS (VPC, EC2, IAM, S3, CloudWatch)  
Preparing for AWS Certified Solutions Architect certification
