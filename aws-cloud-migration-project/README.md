![killian_sarsah_architecture_diagram](https://github.com/user-attachments/assets/1383b7c6-30c2-41d2-aad3-7c939e87f938)# AWS Cloud Migration for a Scalable Web Application

This project showcases the design and migration plan of a three-tier monolithic web application from on-premises to Amazon Web Services (AWS). It demonstrates best practices in cloud infrastructure, cost optimization, scheduling, scaling, and secure architecture design.

## 🧱 Architecture Overview

- 🏗️ Custom VPC with public and private subnets
- 🚀 EC2 web/app servers with full control
- 🌐 Application Load Balancer for distributing traffic
- 🛢️ Amazon RDS for backend MySQL database
- 🧠 Auto Scaling and EventBridge for scheduled scaling
- 🔐 IAM, Security Groups, and HTTPS via AWS Certificate Manager
- ☁️ Backups with S3 and AWS Backup

![killian_sarsah_architecture_diagram drawio](https://github.com/user-attachments/assets/6c7898a7-8a32-46d0-878b-c09b367bd1ce)


## 📋 Components

- 📃 [Workplan & Strategy]()
- 🧰 [Inventory of AWS Services](docs/inventory-report.md)
- 💰 [Cost Estimate](https://calculator.aws.amazon.com/#/estimate?id=...) *(Link placeholder)*

## 📈 Outcomes

- Reduced cost by scheduled instance usage (9am–5pm)
- Handled traffic bursts from 100k → 800k requests
- Decoupled the monolith for easier maintenance
- Improved app uptime and disaster recovery via cloud backups



**Killian Sarsah**  
Cloud & Cybersecurity Enthusiast | [LinkedIn](https://linkedin.com/in/your-link) | [Upwork](https://www.upwork.com/freelancers/~01e979827cca6d421f)
