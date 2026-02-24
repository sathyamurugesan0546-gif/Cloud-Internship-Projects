# Create and Access an EC2 Instance Using SSH

## Project Overview

This project demonstrates how to launch an Amazon EC2 instance on AWS and securely access it using SSH from a local machine. The objective was to understand the complete lifecycle of a cloud virtual server, including configuration, connection, and termination.

---

## Objective

To create a virtual server (EC2 instance) on AWS and securely connect to it using SSH.

---

## Services Used

- Amazon EC2  
- Amazon Linux 2023  
- Security Groups  
- Key Pairs (RSA)  
- SSH (Windows Command Prompt)  

---

## Instance Configuration Details

- **Region:** ap-southeast-2 (Sydney)  
- **Instance Type:** t3.micro  
- **Operating System:** Amazon Linux 2023  
- **Key Pair Type:** RSA (.pem format)  
- **Security Group:** Custom security group allowing SSH (Port 22) from My IP  

---

## Steps Performed

### 1. AWS Console Access

Logged into AWS Management Console and navigated to the EC2 Dashboard.

### 2. Launch EC2 Instance

- Named the instance: `Internship-EC2-SSH-Instance`  
- Selected Amazon Linux 2023 AMI  
- Selected instance type t3.micro  
- Created a new RSA key pair in `.pem` format  

### 3. Configure Security Group

- Created a custom security group  
- Allowed inbound SSH traffic (Port 22)  
- Source set to **My IP** for secure access  

### 4. Connect via SSH

From Windows Command Prompt:

- Updated `.pem` file permissions using `icacls`  
- Connected using SSH:

```bash
ssh -i Internship-EC2-KeyPair.pem ec2-user@<Public-IP>
```

- Verified successful login into Amazon Linux shell  

### 5. Instance Lifecycle Management

- Stopped the instance to avoid billing  
- Terminated the instance after completion of the project  

---

## Outcome

Successfully launched and configured an EC2 instance on AWS and established a secure SSH connection. Demonstrated proper security configuration, access verification, and resource lifecycle management.

---

## Key Learnings

- Understanding EC2 provisioning process  
- Importance of security groups and key pairs  
- SSH authentication process  
- Managing AWS resource lifecycle  
- Cost awareness in cloud environments  

---

This project demonstrates foundational cloud computing skills required for infrastructure management on AWS.