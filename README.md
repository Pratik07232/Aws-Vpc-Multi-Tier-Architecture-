# AWS VPC Multi-Tier Architecture

## Project Overview

This project demonstrates the implementation of a secure and scalable AWS VPC Multi-Tier Architecture using public and private subnets.

The architecture includes:
- Public and Private Subnets
- Bastion Host
- NAT Gateway
- Internet Gateway
- Route Tables
- Security Groups
- Private EC2 Connectivity

---

# AWS Services Used

- VPC
- EC2
- NAT Gateway
- Internet Gateway
- Security Groups
- Route Tables
- Network ACLs

---

# Architecture Diagram

(Add your architecture image here)

Example:

![Architecture](architecture.png)

---

# Project Objectives

- Build secure AWS networking architecture
- Configure public and private subnets
- Implement Bastion Host access
- Secure private EC2 instances
- Learn AWS networking and routing

---

# Step-by-Step Implementation

## Step 1: Create Custom VPC

CIDR Block:

```bash
10.0.0.0/16
```

---

## Step 2: Create Public and Private Subnets

Public Subnet:

```bash
10.0.1.0/24
```

Private Subnet:

```bash
10.0.2.0/24
```

---

## Step 3: Configure Internet Gateway

Attached Internet Gateway to VPC for internet access.

---

## Step 4: Configure NAT Gateway

Created NAT Gateway in public subnet for private subnet internet access.

---

## Step 5: Launch Bastion Host

Created Bastion Host in public subnet to securely connect private EC2 instances.

---

## Step 6: Configure Route Tables

Public Route:

```bash
0.0.0.0/0 → Internet Gateway
```

Private Route:

```bash
0.0.0.0/0 → NAT Gateway
```

---

## Step 7: Configure Security Groups

- Allowed SSH access to Bastion Host
- Allowed private EC2 access only from Bastion Host

---

# Security Best Practices

- Private instances without public IP
- Restricted SSH access
- Separate public and private subnets
- Controlled network routing

---

# Project Outcome

Successfully implemented a secure and scalable AWS Multi-Tier Architecture with Bastion Host and private EC2 connectivity.

---

# Future Improvements

- Add Load Balancer
- Configure Auto Scaling
- Implement CloudWatch Monitoring
- Deploy real web application

---

# Author

## Pratik Gadekar

Entry-level Cloud Engineer

GitHub:
https://github.com/Pratik07232

LinkedIn:
https://linkedin.com/in/pratikgadekar
