# 🌐 AWS EC2 Apache Web Server Deployment Project

## 📌 Objective

To launch an Amazon EC2 instance, install and configure the Apache HTTP Server, and make the web application accessible through a public IP address.

---

## 🛠️ Tools & Technologies

* Amazon Web Services (AWS)
* Amazon EC2
* Amazon Linux 2023
* Apache HTTP Server (httpd)
* Security Groups
* EC2 Instance Connect
* AWS Management Console

---

## 📂 Project Steps

### 1. Launch an EC2 Instance

* Created an EC2 instance named **Apache-WebServer**
* Selected **Amazon Linux 2023 AMI**
* Chose **t3.micro** instance type
* Configured key pair and security settings
* Verified successful instance launch

---

### 2. Configure Security Group

* Configured inbound security group rules
* Allowed SSH access on Port 22
* Allowed HTTP access on Port 80
* Verified network connectivity for web traffic

---

### 3. Install Apache Web Server

* Connected to the EC2 instance using EC2 Instance Connect
* Updated system packages
* Installed Apache HTTP Server (httpd)
* Verified successful installation

---

### 4. Start and Enable Apache Service

* Started the Apache service using systemctl
* Enabled Apache to start automatically on boot
* Verified service status
* Confirmed Apache was running successfully

---

### 5. Deploy and Access Web Page

* Created a custom web page containing project information
* Stored the webpage in Apache's default web directory
* Accessed the webpage using the EC2 public IP address
* Verified successful web server deployment

---

## 🎯 Outcome

* Successfully launched an Amazon EC2 instance
* Installed and configured Apache HTTP Server
* Configured security groups for web access
* Hosted a custom webpage on AWS infrastructure
* Accessed the website through a public IP address
* Gained hands-on experience with web server deployment in AWS

---

## ⚠️ Key Learnings

* Amazon EC2 provides scalable virtual servers in the cloud
* Security Groups act as virtual firewalls for EC2 instances
* Apache HTTP Server is one of the most widely used web servers
* Port 80 is used for HTTP communication
* Linux service management can be performed using systemctl
* Public IP addresses enable external access to hosted applications

---

## 📸 Screenshots

1. Step1-EC2-Instance-Created.png
2. Step2-Security-Group-HTTP-Rule-Added.png
3. Step3-Apache-Installed.png
4. Step4-Apache-Service-Running.png
5. Step5-Custom-Apache-Webpage.png

---

## 🚀 Conclusion

This project demonstrates the deployment of a web server using Apache on an Amazon EC2 instance. It provides practical experience in launching cloud infrastructure, configuring network access, managing Linux services, and hosting web content on AWS. The project strengthens foundational cloud computing skills and introduces real-world web server administration concepts.