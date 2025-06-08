# Workplan: Cloud Environment Setup

1. **Create a new VPC**
   - Configure public and private subnets
   - Add Internet Gateway and NAT Gateway

2. **Set up Security Groups**
   - Allow HTTPS only for web access
   - Restrict SSH access to specific engineer IPs

3. **Provision EC2 Instances**
   - Launch EC2 in public subnet for web/app tier
   - Use long-running instances (e.g., t3.medium)

4. **Deploy Application Load Balancer**
   - Forward requests to EC2s in the Auto Scaling Group

5. **Set Up RDS (MySQL)**
   - Launch in private subnet with backups enabled

6. **Enable Backups**
   - Use AWS Backup for EC2 and RDS
   - Store in Amazon S3

7. **Enforce Security Policies**
   - IAM roles and HTTPS via AWS Certificate Manager

8. **Schedule Instances**
   - EventBridge to start/stop EC2s daily

9. **Monitoring**
   - CloudWatch for EC2, RDS, and ALB

10. **Test and Optimize**
   - Simulate traffic, adjust instance types and scaling policies
