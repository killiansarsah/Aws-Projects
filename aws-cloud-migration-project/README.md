# Cloud Design Proposal for Web Application Migration to AWS

**Prepared by:** Killian Sarsah

## Table of Contents
- [Overview](#overview)
- [Justification for Cloud Migration](#justification-for-cloud-migration)
- [Architecture Overview](#architecture-overview)
- [Service Inventory](#service-inventory)
- [Implementation Workplan](#implementation-workplan)
- [Cost Estimation](#cost-estimation)
- [Getting Started](#getting-started)

## Overview

This document outlines the comprehensive plan for migrating our company's web application to Amazon Web Services (AWS). The migration will transform our current infrastructure into a scalable, secure, and cost-effective cloud solution capable of handling traffic fluctuations from 100,000 to 800,000 requests.

## Justification for Cloud Migration

### Key Benefits

- **💰 Cost Optimization**
  - Eliminates capital expenditure (CapEx) for on-premises infrastructure
  - Implements pay-as-you-go pricing model
  - Reduces operational overhead

- **📈 Scalability**
  - Dynamic scaling to handle traffic spikes
  - Auto Scaling capabilities for demand fluctuations
  - Support for 100K-800K request variations

- **🔒 Enhanced Security**
  - HTTPS enforcement through AWS Certificate Manager
  - IP-based access control via Security Groups
  - Data encryption at rest and in transit
  - Advanced AWS security features

- **⚡ Improved Availability**
  - Built-in redundancy across availability zones
  - Global infrastructure for better uptime
  - Reduced downtime through fault tolerance

- **🤖 Automation & Scheduling**
  - EC2 Auto Scaling for dynamic resource management
  - EventBridge for scheduled instance operations
  - Cost optimization through automated scheduling

- **🏗️ Architecture Modernization**
  - Migration from monolithic to decoupled services
  - Cloud-native design patterns
  - Microservices-ready infrastructure

## Architecture Overview

### Core Components

The AWS architecture includes the following key components:
![killian_sarsah_architecture_diagram drawio](https://github.com/user-attachments/assets/5cc31e55-f0b7-4475-8a82-030c5bc29e46)




### Infrastructure Components

- **VPC**: Isolated network environment with public and private subnets
- **Internet Gateway**: Enables public subnet internet access
- **NAT Gateway**: Secure outbound internet traffic for private subnets
- **Application Load Balancer**: Traffic distribution across EC2 instances
- **EC2 Instances**: Web and application servers in public subnet
- **RDS MySQL**: Database service in private subnet
- **S3**: Backup storage and static assets
- **Security Groups & Route Tables**: Network access control and routing

### Supporting Services

- **IAM**: Identity and access management
- **CloudWatch**: Monitoring and alerting
- **Auto Scaling**: Dynamic resource scaling
- **EventBridge**: Scheduled operations
- **AWS Backup**: Automated backup solutions

## Service Inventory

| Service Name | Purpose/Use Case |
|--------------|------------------|
| **Amazon VPC** | Isolated network environment with public/private subnets |
| **Amazon EC2** | Web and application servers with full administrative control |
| **Elastic Load Balancer** | Distribute traffic across multiple EC2 instances |
| **Amazon RDS (MySQL)** | Managed relational database service |
| **Amazon S3** | Object storage for backups and static assets |
| **IAM** | Secure access management for AWS resources |
| **AWS CloudWatch** | Application performance monitoring and alerting |
| **AWS EventBridge** | Schedule EC2 start/stop events for cost optimization |
| **Auto Scaling Group** | Automatically scale EC2 instances based on demand |
| **AWS Backup** | Automated backup for EC2 and RDS instances |
| **AWS Certificate Manager** | SSL/TLS certificate provisioning for HTTPS |
| **AWS Systems Manager** | Secure patch and instance management |

## Implementation Workplan

### Phase 1: Network Foundation
1. **Create VPC**
   - Configure public and private subnets
   - Set up Internet Gateway and NAT Gateway
   - Configure route tables

2. **Security Configuration**
   - Create Security Groups for HTTPS-only web access
   - Restrict SSH access to specific engineer IP addresses
   - Set up IAM roles and policies

### Phase 2: Compute and Database
3. **Provision EC2 Instances**
   - Launch EC2 instances (Amazon Linux/Ubuntu) in public subnet
   - Configure t3.medium instances with custom AMIs
   - Set up web and application tiers

4. **Deploy Load Balancer**
   - Configure Application Load Balancer
   - Set up health checks and target groups
   - Integrate with Auto Scaling Group

5. **Database Setup**
   - Launch RDS MySQL instance in private subnet
   - Enable automatic backups
   - Configure security groups for database access

### Phase 3: Backup and Security
6. **Backup Configuration**
   - Set up AWS Backup for EC2 and RDS
   - Configure S3 as backup destination
   - Establish backup retention policies

7. **Security Implementation**
   - Apply IAM roles and policies
   - Enable HTTPS via AWS Certificate Manager
   - Configure encryption for data at rest and in transit

### Phase 4: Automation and Monitoring
8. **Scheduling Setup**
   - Configure EventBridge for daily EC2 scheduling (9am-5pm)
   - Set up cost optimization automation
   - Test scheduled operations

9. **Monitoring Configuration**
   - Enable CloudWatch for EC2, RDS, and ALB
   - Set up logs, metrics, and alarms
   - Configure notification systems

### Phase 5: Testing and Optimization
10. **Performance Testing**
    - Conduct load testing with simulated traffic
    - Validate scaling policies and thresholds
    - Optimize instance types and configurations

## Cost Estimation

### Monthly Cost Breakdown

| Service | Configuration | Monthly Cost (USD) |
|---------|---------------|-------------------|
| **EC2 (2x t3.medium)** | Web/App servers | $66.00 |
| **RDS (db.t3.medium)** | MySQL, 20GB storage, backups | $80.00 |
| **S3** | 50GB storage | $1.50 |
| **Application Load Balancer** | 1 ALB, 100GB data processed | $20.00 |
| **Backup & Snapshot** | EC2 & RDS backups | $10.00 |
| **CloudWatch** | Logs, metrics, alarms | $5.00 |
| **NAT Gateway** | 1 NAT, low data usage | $15.00 |
| **EventBridge** | Scheduling | Free |
| **Certificate Manager** | SSL for HTTPS | Free |

### **Estimated Monthly Total: ~$197.50**

> **Note:** Costs may vary based on actual usage patterns, data transfer, and additional services. Regular cost monitoring and optimization are recommended.

## Getting Started

### Prerequisites
- AWS Account with appropriate permissions
- Basic understanding of AWS services
- Access to current application codebase and database

### Next Steps
1. Review and approve this proposal
2. Set up AWS account and billing alerts
3. Begin Phase 1 implementation
4. Schedule regular progress reviews
5. Plan for application deployment and testing

### Support and Documentation
- AWS Documentation: [docs.aws.amazon.com](https://docs.aws.amazon.com)
- AWS Cost Calculator: [calculator.aws](https://calculator.aws)
- AWS Support: Available through AWS Console

