# AWS High Availability Web Application

## Architecture Overview

The application is designed to run across multiple Availability Zones in AWS.

### Architecture Components

- **Amazon VPC:** Provides an isolated network for the application.
- **Public Subnets:** Host the internet-facing Application Load Balancer.
- **Application Load Balancer (ALB):** Receives incoming HTTP traffic and distributes requests across registered targets.
- **Private Subnets:** Host EC2 application instances without direct public IP addresses.
- **Auto Scaling Group (ASG):** Maintains and scales the EC2 instances according to its configuration.
- **NAT Gateway:** Provides outbound internet access for resources in private subnets when routes are configured to use it.
- **Amazon CloudWatch:** Planned for monitoring and metrics.

### Traffic Flow

Internet → Application Load Balancer → EC2 Instances in Private Subnets

### Project Status

CloudWatch monitoring and final validation are still to be completed.
