# 🏗️ AWS Infrastructure as Code: Load-Balanced & Secure PHP Application Deployment

This project demonstrates how to deploy a scalable, secure, and highly available PHP application on AWS using infrastructure-as-code principles. It includes setting up an RDS MySQL database, an Application Load Balancer, Auto Scaling Groups, and importing a dataset.

---

## 📌 Project Overview

The application architecture follows best practices:

- **Decoupled database and application layers**
- **Scalability via Auto Scaling Groups**
- **High availability through Load Balancing**
- **Secure configuration with private subnets and Secrets Manager**

---

## 🚀 Steps and Components

### 1. 📦 Amazon RDS MySQL Setup
- Created a MySQL database using Amazon RDS.
- Placed in a **private subnet** for security.
- Allowed access only from application servers via a **Security Group**.
- Managed database credentials using **AWS Secrets Manager**.

### 2. ⚖️ Application Load Balancer
- Deployed an **Application Load Balancer (ALB)** across two public subnets.
- Used to distribute traffic evenly and ensure high availability.

### 3. 📈 Auto Scaling Group for PHP App
- Launched EC2 instances via a **Launch Template**.
- Deployed inside **private subnets**.
- Set up **Auto Scaling** to handle varying traffic loads.
- Application code and SQL dump included in the template.

### 4. 🗃️ Data Import
- Loaded the SQL dataset (`Countrydatadump.sql`) into the RDS database.
- Used **MySQL client** with credentials securely pulled from **Secrets Manager**.

### 5. 🔍 Final Testing
- Accessed the application using the Load Balancer’s DNS.
- Verified successful database queries and page rendering.
- Confirmed smooth operation of all components together.

---

## ✅ Result

A fully working, load-balanced PHP web application that:
- Scales based on traffic
- Stores data securely in RDS
- Protects infrastructure using private networking and IAM best practices

---

## 🛠️ Tools & Services Used
- Amazon RDS (MySQL)
- EC2, Auto Scaling Group
- Elastic Load Balancer (ALB)
- AWS Secrets Manager
- VPC with public/private subnets
- MySQL client

---

## 📂 Files
- `Countrydatadump.sql`: SQL data import
- EC2 Launch Template (preconfigured)
- VPC, RDS, and Load Balancer configuration via AWS Console or IaC


