# aws-multi-region-disaster-recovery
Multi-Region Disaster Recovery Architecture using AWS EC2, ALB, VPC, and Target Groups across Mumbai and Singapore regions.
# AWS Multi-Region Infrastructure with Disaster Recovery

## Project Overview

This project demonstrates a Multi-Region Infrastructure deployed across AWS Mumbai (ap-south-1) and Singapore (ap-southeast-1) regions to improve availability and disaster recovery readiness.

## Architecture

### Primary Region

* Mumbai (ap-south-1)

### Secondary Region

* Singapore (ap-southeast-1)

## AWS Services Used

* Amazon EC2
* Amazon VPC
* Public Subnets
* Internet Gateway
* Route Tables
* Security Groups
* Target Groups
* Application Load Balancers (ALB)

## Infrastructure Setup

### Mumbai Region

* Custom VPC
* Public Subnets
* EC2 Web Server
* Target Group
* Application Load Balancer

### Singapore Region

* Custom VPC
* Public Subnets
* EC2 Web Server
* Target Group
* Application Load Balancer

## User Data Script

```bash
#!/bin/bash
dnf update -y
dnf install -y httpd

echo "<h1>Web Server Running</h1>" > /var/www/html/index.html

systemctl start httpd
systemctl enable httpd
```

## Features

* Multi-Region Deployment
* High Availability Architecture
* Load Balancing
* Disaster Recovery Readiness
* Independent Regional Infrastructure

## Future Enhancements

* Route 53 Automatic Failover
* Auto Scaling Groups
* CloudWatch Monitoring
* Infrastructure as Code using Terraform

## Project Outcome

Successfully deployed web infrastructure in Mumbai and Singapore regions using AWS services and validated application accessibility through Application Load Balancers.
