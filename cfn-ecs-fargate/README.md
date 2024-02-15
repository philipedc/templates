# ECS Fargate

## Description

This solution sets up infrastructure, including a VPC, Security Group, and Subnets, along with an ECS Cluster and an ALB that serves each new service.

![](diagram.png)

## Resources Created

### Infraestructure Template

- Public Subnet AZ-A
- Public Subnet AZ-B
- Public Subnet AZ-C
- Internet Gateway
- Application Load Balancer Security Group
- Container Security Group
- ECS Cluster (**Fargate Compute**)
- Role (AmazonECSTaskExecutionRolePolicy)
- Application Load Balancer

### Service Template

- Task Definition
- Target Group
- Listener 
- ECS Service
- CloudWatch LogGroup

## Input

### Infraestructure Tempalte

- VPC CIDR Block (default: 10.10.0.0/16)
- Subnet A CIDR Block (default: 10.10.1.0/24)
- Subnet B CIDR Block (default: 10.10.2.0/24)
- Subnet C CIDR Block (default: 10.10.3.0/24)

### Service Template

- Infraestructure Stack Name
- Container Image
- Port (same used both for the listener and target group)

## Pricing

- [Load Balancer](https://aws.amazon.com/elasticloadbalancing/pricing/)
- [Fargate](https://aws.amazon.com/fargate/pricing/)