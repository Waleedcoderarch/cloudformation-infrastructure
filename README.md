# AWS Multi-AZ Web Infrastructure using CloudFormation

## 📌 Project Overview

This project demonstrates a **production-style web infrastructure** deployed entirely using **AWS CloudFormation**.

The architecture provisions a highly available environment across **multiple Availability Zones**, including networking, compute resources, and load balancing.

It simulates a real-world cloud deployment where infrastructure is automated using Infrastructure as Code (IaC).

---

## 🏗 Architecture Summary

The CloudFormation template deploys:

* A custom **Virtual Private Cloud (VPC)**
* Two public subnets in different Availability Zones
* Internet Gateway and routing configuration
* Security group allowing HTTP traffic
* Two EC2 web servers with Apache installed via User Data
* An Application Load Balancer (ALB) distributing traffic

The ALB routes requests between both servers to ensure availability and load balancing.

---

## 🚀 Technologies Used

* AWS CloudFormation
* Amazon VPC
* Amazon EC2
* Elastic Load Balancing (ALB)
* Linux (Amazon Linux 2)
* Apache HTTP Server

---

## 📂 Project Structure

<img width="1041" height="995" alt="roundtrip" src="https://github.com/user-attachments/assets/5b71d77f-7880-40d2-98e7-450a84937700" />



## ⚙️ Deployment Instructions

1. Open AWS Console → CloudFormation
2. Create a new stack
3. Upload the YAML template
4. Select an EC2 Key Pair
5. Launch the stack
6. After deployment, copy the Load Balancer URL from Outputs

Open the URL in a browser to see traffic distributed between servers.

---

## 🔄 Expected Behavior

Refreshing the Load Balancer URL alternates responses between:

* **Hello from Server A**
* **Hello from Server B**

This confirms successful load balancing across multiple AZs.

---

## 🎯 Learning Objectives

This project demonstrates:

* Infrastructure as Code principles
* Multi-AZ architecture design
* Automated EC2 provisioning
* Load balancing and fault tolerance
* AWS networking fundamentals

---

## 📖 Future Improvements

* Auto Scaling Group integration
* Private subnets with NAT Gateway
* HTTPS with SSL certificates
* Monitoring with CloudWatch
* CI/CD pipeline automation

---

## 👤 Author

Waleed Ahmed
Cloud & DevOps Enthusiast

---
