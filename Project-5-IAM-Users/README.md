# 🔐 AWS IAM Users, Groups, and Policies Project

## 📌 Objective

To create IAM users and groups, assign permissions using policies, and verify controlled access to AWS resources.

---

## 🛠️ Tools & Technologies

* Amazon Web Services (AWS)
* AWS Identity and Access Management (IAM)
* IAM Users
* IAM Groups
* IAM Policies
* AWS Management Console

---

## 📂 Project Steps

### 1. Create an IAM User

* Created an IAM user named **cloudintern-user**
* Enabled AWS Management Console access
* Configured password authentication
* Verified successful user creation

---

### 2. Create an IAM Group

* Created an IAM group named **S3-ReadOnly-Group**
* Used the group to manage permissions centrally
* Verified successful group creation

---

### 3. Attach Policy to the Group

* Attached the AWS managed policy **AmazonS3ReadOnlyAccess**
* Granted read-only access to Amazon S3 resources
* Verified policy attachment

---

### 4. Add User to the Group

* Added **cloudintern-user** to **S3-ReadOnly-Group**
* Inherited permissions through group membership
* Verified group association

---

### 5. Login Using IAM User Credentials

* Logged in using the IAM user account
* Changed password during first login
* Successfully accessed the AWS Management Console

---

### 6. Verify Access Permissions

* Accessed Amazon S3 successfully
* Attempted to access Amazon EC2 services
* Observed permission restrictions and authorization errors
* Confirmed policy-based access control

---

## 🎯 Outcome

* Successfully created an IAM user
* Created and configured an IAM group
* Attached permissions using IAM policies
* Implemented role-based access management
* Verified access control through policy enforcement
* Gained hands-on experience with AWS IAM services

---

## ⚠️ Key Learnings

* IAM users represent individual identities in AWS
* IAM groups simplify permission management
* Policies define allowed and denied actions
* Users inherit permissions from groups
* Principle of least privilege improves security
* IAM helps secure AWS resources through access control

---

## 📸 Screenshots

1. Step1-Create-IAM-Group-And-Attach-Policy.png
2. Step2-Review-IAM-User-And-Permissions.png
3. Step3-IAM-User-Created-Credientials.png
4. Step4-IAM-User-Created-Successfully.png
5. Step5-User-Added-To-IAM-Group.png
6. Step6-Verify-IAM-User-Permissions.png

---

## 🚀 Conclusion

This project demonstrates the implementation of AWS Identity and Access Management (IAM) by creating users, groups, and policies. It provides practical experience in managing permissions, controlling access to AWS resources, and applying security best practices through group-based access management.
