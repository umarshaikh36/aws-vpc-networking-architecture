# 🌐 AWS Custom VPC Networking Architecture

## 📌 Project Overview

This project demonstrates the design and implementation of a custom AWS networking architecture using Virtual Private Clouds (VPCs), public and private subnets, route tables, Internet Gateway, and VPC Peering.

The objective was to gain hands-on experience with AWS networking fundamentals and secure communication between isolated environments while following cloud networking best practices.

---

## 🏗️ Architecture Overview

### Environment Design

#### Test VPC

* CIDR Block: `10.0.0.0/24`
* Public Subnet
* Private Subnet

#### Production VPC

* CIDR Block: `192.0.0.0/16`
* Public Subnet
* Private Subnet

#### Connectivity Components

* Internet Gateway (IGW)
* Route Tables
* Security Groups
* VPC Peering Connection
* EC2 Instances for Connectivity Testing

---

## 🔧 AWS Services Used

* Amazon VPC
* Public Subnets
* Private Subnets
* Internet Gateway
* Route Tables
* Security Groups
* VPC Peering
* Amazon EC2

---

## 🚀 Implementation Steps

### 1. Created Custom VPCs

Created separate VPCs for:

* Test Environment
* Production Environment

Configured unique CIDR ranges to avoid network overlap.

---

### 2. Configured Public and Private Subnets

Created subnet architecture within each VPC:

* Public Subnet for internet-facing resources
* Private Subnet for internal resources

---

### 3. Attached Internet Gateway

Configured an Internet Gateway for public subnet access and associated appropriate route tables.

---

### 4. Created Custom Route Tables

Implemented route table configurations to:

* Enable internet connectivity for public resources
* Control internal network communication
* Support VPC Peering routes

---

### 5. Established VPC Peering

Created and accepted a VPC Peering Connection between:

* Test VPC
* Production VPC

Updated route tables to enable private communication between both networks.

---

### 6. Configured Security Groups

Applied security group rules to:

* Allow ICMP traffic for testing
* Permit required communication between instances
* Follow network segmentation principles

---

### 7. Connectivity Validation

Launched EC2 instances in both VPCs and verified connectivity using:

```bash
ping <private-ip-address>
```

Successfully confirmed communication across VPCs through the peering connection.

---

## ✅ Project Outcome

Successfully designed and implemented a secure multi-tier AWS networking architecture featuring:

* Multiple VPCs
* Public and Private Subnets
* Internet Gateway Connectivity
* Route Table Management
* VPC Peering
* Inter-VPC Communication
* Security Group Configuration

---

## 🎯 Key Learnings

* AWS VPC Design
* CIDR Planning
* Public vs Private Subnets
* Internet Gateway Configuration
* Route Table Management
* VPC Peering Concepts
* Security Group Best Practices
* Cloud Network Segmentation
* Network Troubleshooting

---

## 🔮 Future Enhancements

* NAT Gateway Implementation
* Bastion Host Deployment
* Multi-AZ Architecture
* Site-to-Site VPN Connectivity
* Transit Gateway Integration
* Network ACL Configuration
* AWS Network Firewall

---

## 👨‍💻 Author

**Umar Shaikh**

AWS Certified Solutions Architect – Associate

### Connect With Me

* LinkedIn: https://www.linkedin.com/in/umarshaikh1822
* GitHub: https://github.com/umarshaikh36
