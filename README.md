# 🚀 AWS Two-Tier Architecture Project

## 📖 Project Overview

This project demonstrates the design and deployment of a secure and highly available AWS Two-Tier Architecture using Amazon VPC, Public and Private Subnets, EC2 Instances, Internet Gateway, NAT Gateway, Route Tables, and Security Groups.

The architecture follows industry best practices by placing the Web Server in a Public Subnet and the Database Server in a Private Subnet, ensuring secure communication while protecting sensitive data from direct internet access.

---

## 🏗️ Architecture Components

### Networking
- Custom VPC (192.168.0.0/24)
- Public Subnet
- Private Subnet
- Internet Gateway
- NAT Gateway
- Route Tables

### Compute
- EC2 Web Server (Public Subnet)
- EC2 Database Server (Private Subnet)

### Security
- Security Groups
- Private Database Access
- Controlled Traffic Flow

### Web Server
- Apache HTTP Server Installation
- Linux Server Administration

---

## 🔄 Architecture Flow

Internet → Internet Gateway → Public Subnet → EC2 Web Server → Private Subnet → EC2 Database Server

---

## ⚙️ Deployment Steps

### Step 1: Create VPC
- Create Custom VPC (192.168.0.0/24)

### Step 2: Create Subnets
- Create Public Subnet
- Create Private Subnet

### Step 3: Create Internet Gateway
- Attach Internet Gateway to the VPC

### Step 4: Configure Route Tables
- Public Route Table → Internet Gateway
- Private Route Table → NAT Gateway

### Step 5: Launch EC2 Instances
- Launch Web Server in Public Subnet
- Launch Database Server in Private Subnet

### Step 6: Configure Security Groups
- Allow HTTP/HTTPS access to Web Server
- Restrict Database Server access to internal traffic only

### Step 7: Install Apache Web Server

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

---

## 🔐 Why Use a Private Subnet for the Database?

The database server is deployed inside a private subnet to improve security.

Benefits:
- No direct internet access
- Reduced attack surface
- Secure communication through the application server
- Better protection of sensitive data
- Industry-standard cloud architecture

---

## 📚 Key Learnings

- AWS VPC Design
- Subnetting
- Route Table Configuration
- Internet Gateway Setup
- NAT Gateway Configuration
- Security Group Management
- EC2 Deployment
- Linux Administration
- Cloud Network Security

---

## 🌍 Real-World Use Cases

- Company Websites
- E-Commerce Platforms
- Banking Applications
- ERP Systems
- CRM Platforms
- Healthcare Applications
- Internal Business Applications

---

## 🎥 Project Demo Video

Watch the complete project demonstration:

**Video Link:** 
https://www.linkedin.com/posts/krishzalavadiya_aws-cloudcomputing-awscloud-ugcPost-7470859613152833536-lwXS/?utm_source=share&utm_medium=member_desktop&rcm=ACoAAE9h_WkBEi-m86kaAEdyLJq4TMB6q4c4ovY

---

## 🛠️ AWS Services Used

- Amazon VPC
- Amazon EC2
- Internet Gateway
- NAT Gateway
- Security Groups
- Route Tables

---

## ⭐ Conclusion

This project provided hands-on experience with AWS networking fundamentals, secure cloud architecture design, subnet planning, routing, security implementation, and infrastructure deployment using AWS services.

It demonstrates how organizations securely host applications by separating public-facing web servers from private backend database servers.
