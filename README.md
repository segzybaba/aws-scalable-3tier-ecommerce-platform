# 🛒 Scalable 3-Tier E-Commerce Platform on AWS (MapleCart)

## 📌 Project Overview

This project demonstrates a **scalable, secure, and highly available 3-tier architecture** built on AWS for a sample e-commerce platform called **MapleCart**.

The architecture follows industry best practices for cloud design, including **load balancing, auto scaling, secure networking, and monitoring**.

---

## 🧠 Architecture Diagram

![Architecture Diagram](architecture.png)

---

## 🏗️ Architecture Overview

The system is designed using a **3-tier architecture pattern**:


---

## ☁️ AWS Services Used

- Amazon VPC
- Public and Private Subnets
- Internet Gateway
- NAT Gateway
- Application Load Balancer (ALB)
- EC2 Auto Scaling Group
- Amazon RDS (MySQL)
- Amazon S3 (Static Storage)
- IAM Roles
- CloudWatch (Monitoring)
- SNS (Alerts)

---

## 🌐 Network Architecture

The infrastructure is deployed in a **custom VPC** with:

- **Public Subnets**
  - Application Load Balancer

- **Private Subnets**
  - EC2 instances (application layer)
  - RDS database (data layer)

### 🔐 Security Design

- ALB allows traffic from the internet (HTTP)
- EC2 instances accept traffic **only from ALB**
- RDS accepts traffic **only from EC2**
- IAM role used for secure S3 access (no access keys)

---

## 🖼️ VPC Resource Map

![VPC Architecture](screenshots/vpc-resource-map.png)

---

## ⚖️ Load Balancing

Application traffic is distributed using an **Application Load Balancer (ALB)**.

![ALB](https://github.com/segzybaba/aws-scalable-3tier-ecommerce-platform/blob/756e9a07d76f8c3db093fb102465b4ea43ae359e/Apllication-load-balancer.png)

---

## ❤️ Target Group Health

The ALB routes traffic only to **healthy EC2 instances**.

![Target Group](screenshots/target-group-health.png)

---

## 🔁 Auto Scaling

An **Auto Scaling Group** ensures high availability and scalability.

- Maintains minimum number of instances
- Automatically replaces unhealthy instances

![Auto Scaling](https://github.com/segzybaba/aws-scalable-3tier-ecommerce-platform/blob/55de7ec7d4ca899888618c9d54ad60e8ddb58ae0/Auto-scaling-group.png)

---

## 🗄️ Database Layer (RDS)

The application uses **Amazon RDS (MySQL)** for structured data storage.

- Deployed in private subnet
- Not publicly accessible

![RDS](screenshots/rds-database.png)

---

## 📦 Storage (S3)

Amazon S3 is used to store static assets such as:

- Product images
- Files
- Media

EC2 instances access S3 using **IAM roles**.

---

## 📊 Monitoring & Alerts

Monitoring is implemented using:

- **CloudWatch Metrics**
- **SNS Email Alerts**

Alerts are triggered for:

- High EC2 CPU usage
- RDS CPU spikes
- Unhealthy load balancer targets

![CloudWatch](screenshots/cloudwatch-alarms.png)

---

## 🔐 IAM Role Usage

An IAM role is attached to EC2 instances to allow:

- Secure access to S3
- No hardcoded credentials

---

## 🚀 Key Features

- Highly available architecture across multiple AZs
- Secure networking using private subnets
- Load balancing and traffic distribution
- Auto Scaling for dynamic workloads
- Decoupled storage using S3
- Managed database with RDS
- Monitoring and alerting system

---

## 🧠 Key Skills Demonstrated

- AWS Cloud Architecture Design
- VPC Networking (Public & Private Subnets)
- Load Balancing (ALB)
- Auto Scaling
- IAM Role-Based Access Control
- RDS Database Deployment
- S3 Integration
- CloudWatch Monitoring
- SNS Alerting
- High Availability Design

---

## 📈 Future Improvements

- Add CloudFront CDN for faster content delivery
- Enable HTTPS using AWS Certificate Manager (ACM)
- Configure Route 53 custom domain
- Use Terraform for Infrastructure as Code (IaC)
- Implement CI/CD pipeline (GitHub Actions)
- Add AWS WAF for security protection
- Use Secrets Manager for database credentials

---

## 📄 Resume Description

**Scalable 3-Tier E-Commerce Platform on AWS**  
Designed and deployed a secure and scalable AWS architecture using VPC, public/private subnets, Application Load Balancer, EC2 Auto Scaling Group, Amazon RDS, and S3. Implemented IAM roles for secure service access, configured CloudWatch and SNS monitoring, and built a highly available multi-tier environment for a production-style application.

---

## 🎯 Lessons Learned

- Importance of subnet separation for security
- How load balancers distribute traffic
- How IAM roles improve security
- Real-world cloud architecture design patterns
- Monitoring and alerting best practices

---

## 📂 Project Structure


---

## 👤 Author

**Segun Seun Ajiboye**

Cloud & DevOps Enthusiast | AWS Learner
