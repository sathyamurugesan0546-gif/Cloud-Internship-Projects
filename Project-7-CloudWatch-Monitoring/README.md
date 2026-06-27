# 🌐 AWS CloudWatch Monitoring and Alarm Configuration Project

## 📌 Objective

To monitor an Amazon EC2 instance using Amazon CloudWatch by viewing performance metrics and creating a CloudWatch alarm to monitor CPU utilization.

---

## 🛠️ Tools & Technologies

* Amazon Web Services (AWS)
* Amazon EC2
* Amazon CloudWatch
* Amazon Linux 2023
* CloudWatch Metrics
* CloudWatch Alarms
* AWS Management Console

---

## 📂 Project Steps

### 1. Launch an EC2 Instance

* Created an EC2 instance named **CloudWatch-Monitoring-Server**
* Selected **Amazon Linux 2023 AMI**
* Chose **t3.micro** instance type
* Configured key pair and security settings
* Verified successful instance launch

---

### 2. Monitor EC2 Metrics

* Opened the EC2 Monitoring tab
* Viewed CloudWatch performance metrics
* Verified CPU Utilization metrics
* Monitored Network In and Network Out metrics
* Confirmed CloudWatch was collecting monitoring data

---

### 3. Create a CloudWatch Alarm

* Opened Amazon CloudWatch
* Selected the **CPUUtilization** metric for the EC2 instance
* Configured an alarm with a static threshold
* Set the threshold to trigger when CPU utilization exceeds **80%**
* Created the CloudWatch alarm successfully

---

### 4. Verify Alarm Status

* Viewed the alarm in the CloudWatch Alarms dashboard
* Confirmed the alarm state changed to **OK**
* Verified alarm conditions and monitoring configuration

---

### 5. Clean Up Resources

* Terminated the EC2 instance after project completion
* Deleted the CloudWatch alarm
* Cleaned up AWS resources to avoid unnecessary charges

---

## 🎯 Outcome

* Successfully launched an Amazon EC2 instance
* Monitored EC2 performance metrics using Amazon CloudWatch
* Created and configured a CloudWatch alarm for CPU utilization
* Verified the alarm status and monitoring functionality
* Learned how CloudWatch helps monitor AWS resources and improve operational visibility

---

## ⚠️ Key Learnings

* Amazon CloudWatch continuously monitors AWS resources and applications.
* CloudWatch Metrics provide real-time performance data for EC2 instances.
* CloudWatch Alarms automatically monitor metrics against defined thresholds.
* CPU Utilization is a key metric used to evaluate EC2 instance performance.
* CloudWatch helps improve system reliability through proactive monitoring.
* AWS resources should be terminated after use to prevent unnecessary costs.

---

## 📸 Screenshots

1. 01-EC2-Instance-Running.png
2. 02-CloudWatch-Monitoring-Metrics.png
3. 03-CloudWatch-Alarm-OK.png

---

## 🚀 Conclusion

This project demonstrates how to use Amazon CloudWatch to monitor the health and performance of an Amazon EC2 instance. By viewing real-time metrics and configuring a CloudWatch alarm based on CPU utilization, the project provides practical experience in AWS monitoring and operational management. It strengthens foundational cloud monitoring skills and highlights the importance of proactive infrastructure monitoring in cloud environments.