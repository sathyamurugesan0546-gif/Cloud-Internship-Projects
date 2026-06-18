# 🌐 AWS VPC with Public and Private Subnets Project

## 📌 Objective

To create a custom Amazon VPC with one public subnet and one private subnet, configure internet connectivity, and implement basic network segmentation in AWS.

---

## 🛠️ Tools & Technologies

* Amazon Web Services (AWS)
* Amazon VPC
* Subnets
* Route Tables
* Internet Gateway
* AWS Management Console

---

## 📂 Project Steps

### 1. Create a Custom VPC

* Created a VPC named **Project4-VPC**
* Configured IPv4 CIDR block: **10.0.0.0/16**
* Verified successful VPC creation

---

### 2. Create Public and Private Subnets

* Created **Public-Subnet** with CIDR block **10.0.1.0/24**
* Created **Private-Subnet** with CIDR block **10.0.2.0/24**
* Placed subnets in different Availability Zones
* Enabled auto-assign public IPv4 address for the public subnet

---

### 3. Create and Attach Internet Gateway

* Created an Internet Gateway named **Project4-IGW**
* Attached the Internet Gateway to **Project4-VPC**
* Verified successful attachment

---

### 4. Configure Route Table

* Created a route table named **Public-RT**
* Added a route:
  * Destination: **0.0.0.0/0**
  * Target: **Project4-IGW**
* Verified active route configuration

---

### 5. Associate Public Subnet

* Associated **Public-Subnet** with **Public-RT**
* Verified subnet association
* Confirmed internet access path through the Internet Gateway

---

### 6. Verify Network Architecture

* Reviewed the VPC Resource Map
* Verified connectivity between:
  * VPC
  * Public Subnet
  * Private Subnet
  * Route Table
  * Internet Gateway
* Confirmed proper network segmentation

---

## 🎯 Outcome

* Successfully created a custom Amazon VPC
* Configured public and private subnets
* Attached an Internet Gateway for internet access
* Implemented route table configuration
* Established a basic secure AWS network architecture
* Gained hands-on experience with AWS networking services

---

## ⚠️ Key Learnings

* A VPC provides an isolated network environment in AWS
* Public subnets require a route to an Internet Gateway
* Route tables control network traffic flow
* Internet Gateways enable communication with the internet
* Private subnets remain isolated unless explicitly configured
* Proper subnet segmentation improves security and network management

---

## 📸 Screenshots

1. Step1-VPC-Creation.png
2. Step2-Subnets-Creation.png
3. Step3-Internet-Gateway.png
4. Step4-Public-Route-Table.png
5. Step5-Subnet-Association.png
6. Step6-Final-Architecture.png

---

## 🚀 Conclusion

This project demonstrates practical knowledge of AWS networking fundamentals, including VPC creation, subnet design, route table configuration, and Internet Gateway integration. It provides hands-on experience in building a basic cloud network architecture with public and private resources while following networking best practices.