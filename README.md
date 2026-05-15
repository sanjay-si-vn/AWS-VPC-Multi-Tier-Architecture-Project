# AWS VPC Multi-Tier Architecture on AWS

## Project Overview

This project demonstrates the setup of a secure and scalable AWS VPC architecture using public and private subnets. The infrastructure simulates a real-world production environment where public-facing services are separated from internal backend resources.

The project focuses on core AWS networking concepts including:

* VPC creation
* CIDR planning
* Public & Private Subnets
* Internet Gateway
* NAT Gateway
* Route Tables
* Security Groups
* EC2 instances
* SSH connectivity
* NGINX web hosting
* Bastion host architecture

---

# Architecture Diagram

Internet
   ↓
Internet Gateway
   ↓
Public Subnet
   ├── Public EC2 (NGINX / Bastion Host)
   └── NAT Gateway

Private Subnet
   └── Private EC2
```

---

# Services Used

| Service          | Purpose                              |
| ---------------- | ------------------------------------ |
| Amazon VPC       | Isolated cloud network               |
| Public Subnet    | Internet-facing resources            |
| Private Subnet   | Internal secure resources            |
| Internet Gateway | Internet access for public subnet    |
| NAT Gateway      | Outbound internet for private subnet |
| Route Tables     | Traffic routing                      |
| EC2              | Virtual servers                      |
| Security Groups  | Firewall rules                       |
| NGINX            | Web server hosting                   |

---

# Project Workflow

## 1. Created Custom VPC

* Configured custom CIDR block
* Designed isolated AWS network

## 2. Created Public & Private Subnets

* Public subnet for internet-facing resources
* Private subnet for backend/internal resources

## 3. Configured Internet Gateway

* Attached IGW to VPC
* Enabled public internet connectivity

## 4. Configured Route Tables

### Public Route Table

0.0.0.0/0 → Internet Gateway

### Private Route Table

0.0.0.0/0 → NAT Gateway

## 5. Launched Public EC2

* Configured SSH access
* Installed and configured NGINX
* Hosted default NGINX webpage

## 6. Configured NAT Gateway

* Allowed outbound internet access from private subnet
* Implemented secure private networking concept

## 7. Created Private EC2

* Disabled public IP
* Implemented private subnet architecture
* Configured internal communication concepts

## 8. Security Group Configuration

* Controlled SSH access
* Managed HTTP traffic
* Practiced cloud firewall troubleshooting

---

# Key Learning Outcomes

Through this project, I learned:

* AWS VPC networking fundamentals
* Difference between public and private subnets
* Route table configurations
* Internet Gateway vs NAT Gateway
* Security Group management
* SSH troubleshooting
* Real-world cloud networking architecture
* Bastion host concepts
* Internal VPC communication
* Production-style infrastructure design

---

# Real-World Relevance

This architecture reflects how modern production systems are designed:

* Public resources exposed securely
* Backend resources isolated in private subnets
* Controlled access using security groups
* Secure outbound internet via NAT Gateway

---

# Technologies Used

* AWS VPC
* Amazon EC2
* Internet Gateway
* NAT Gateway
* Route Tables
* Security Groups
* Ubuntu Linux
* NGINX
* SSH

---

# Future Improvements

Planned enhancements:

* RDS in private subnet
* Application Load Balancer
* Auto Scaling
* Route53
* CloudWatch monitoring
* Docker deployment
* Terraform automation

---

# Author

Sanjay
Aspiring Cloud & DevOps Engineer

---

## Screenshots
<img width="1534" height="487" alt="Screenshot 2026-05-14 221308" src="https://github.com/user-attachments/assets/b6753f6b-0947-4b19-a9ed-e83814ee2e02" />
<img width="1589" height="449" alt="Screenshot 2026-05-14 220845" src="https://github.com/user-attachments/assets/a4902a4a-81f7-4ad0-82e2-7ab9ea43cd0d" />
<img width="1883" height="513" alt="Screenshot 2026-05-14 220829" src="https://github.com/user-attachments/assets/443f91d4-11a9-45e0-a6cf-a94720bb37e4" />

