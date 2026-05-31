# 🚀 AWS VPC Networking Architecture — Hands-On Cloud Project

> A practical AWS networking project where I designed and configured a secure multi-tier VPC environment from scratch in the **Mumbai (ap-south-1)** region.

---

## 📌 Project Overview

This project demonstrates real-world AWS cloud networking skills by building a fully functional, secure VPC architecture with isolated environments, controlled traffic flow, and verified inter-VPC communication.

---

## 🏗️ Architecture Diagram

```
┌─────────────────────────────────────────────────────────┐
│                    AWS Mumbai Region                    │
│                                                         │
│  ┌──────────────────────┐   VPC Peering   ┌──────────────────────┐  │
│  │    Test VPC          │◄───────────────►│  Production VPC      │  │
│  │   10.0.0.0/24        │                 │   192.0.0.0/16       │  │
│  │                      │                 │                      │  │
│  │  ┌────────────────┐  │                 │  ┌────────────────┐  │  │
│  │  │ Public Subnet  │  │                 │  │ Public Subnet  │  │  │
│  │  │  (Internet GW) │  │                 │  │  (Internet GW) │  │  │
│  │  └────────────────┘  │                 │  └────────────────┘  │  │
│  │  ┌────────────────┐  │                 │  ┌────────────────┐  │  │
│  │  │ Private Subnet │  │                 │  │ Private Subnet │  │  │
│  │  │  (Isolated)    │  │                 │  │  (Isolated)    │  │  │
│  │  └────────────────┘  │                 │  └────────────────┘  │  │
│  └──────────────────────┘                 └──────────────────────┘  │
└─────────────────────────────────────────────────────────────────────┘
```

---

## ✅ Project Highlights

| Feature | Details |
|---|---|
| **Test VPC CIDR** | `10.0.0.0/24` |
| **Production VPC CIDR** | `192.0.0.0/16` |
| **Region** | Mumbai (`ap-south-1`) |
| **Subnet Types** | Public + Private across Availability Zones |
| **Connectivity** | VPC Peering for secure inter-VPC communication |
| **Testing** | EC2 instances with ICMP (ping) verification |

---

## 🛠️ What Was Built

- **Custom VPCs** — Created separate VPCs for test and production environments
- **Public & Private Subnets** — Configured across multiple availability zones for redundancy
- **Internet Gateway** — Attached to public subnets for outbound internet connectivity
- **Custom Route Tables** — Designed for controlled and deliberate traffic flow
- **VPC Peering Connection** — Established secure communication between test and production VPCs
- **Private Communication** — Enabled isolated network-to-network connectivity
- **Security Groups** — Applied least-privilege rules and network segmentation best practices
- **Connectivity Testing** — Verified end-to-end communication using EC2 instances and ICMP ping

---

## 🧱 Architecture Components

### VPCs
| Environment | CIDR Block |
|---|---|
| Test | `10.0.0.0/24` |
| Production | `192.0.0.0/16` |

### Subnets
- Public subnets with Internet Gateway routes
- Private subnets isolated from direct internet access

### Networking Resources
- **Internet Gateways** — One per VPC for public subnet internet access
- **Route Tables** — Custom tables per subnet for precise traffic control
- **VPC Peering** — Enables secure, private communication between test and production
- **Security Groups** — Stateful firewall rules applied at the instance level

---

## 🔑 Key Skills Practiced

`AWS VPC` · `Subnets` · `Route Tables` · `Internet Gateway` · `Security Groups` · `EC2` · `VPC Peering` · `Cloud Networking`

---

## 📚 What I Learned

- How to design and implement a **multi-tier VPC architecture** from scratch
- The difference between **public and private subnet** configurations and their use cases
- How **VPC Peering** works and how to configure routing for inter-VPC communication
- How to apply **security groups and network segmentation** best practices
- Hands-on troubleshooting of connectivity using **EC2 and ICMP testing**
- Importance of **route table design** for secure, intentional traffic flow

---

## 📸 Screenshots

> AWS Console screenshots showing the VPC Resource Map, Subnets, Route Tables, and Network Connections.

*(Add your screenshots to a `/screenshots` folder and reference them here)*

```markdown
![VPC Resource Map](screenshots/vpc-resource-map.png)
![Subnet Configuration](screenshots/subnets.png)
![Route Tables](screenshots/route-tables.png)
```

---

## 🚀 How to Replicate This Project

1. **Log in to AWS Console** and navigate to the VPC service in the Mumbai region (`ap-south-1`)
2. **Create Test VPC** with CIDR `10.0.0.0/24`
3. **Create Production VPC** with CIDR `192.0.0.0/16`
4. **Create subnets** (public + private) in each VPC across at least 2 AZs
5. **Attach Internet Gateways** to both VPCs
6. **Create and associate Route Tables** — route public subnets through IGW
7. **Create a VPC Peering Connection** between the two VPCs and accept it
8. **Update route tables** in both VPCs to allow peered CIDR traffic
9. **Launch EC2 instances** in each VPC and verify connectivity with ping (ICMP)
10. **Apply Security Groups** to allow ICMP and restrict unnecessary traffic

---

## 👤 Author

**Umar Shaikh**
- IT Engineer | AWS Certified Solutions Architect – Associate
- Cloud & DevOps Enthusiast

---

## 🏷️ Tags

`#AWS` `#CloudComputing` `#AWSVPC` `#DevOps` `#CloudNetworking` `#HandsOnCloud`
