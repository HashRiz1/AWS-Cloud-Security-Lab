# AWS Cloud Security Lab

## Overview
This project documents the design and deployment of a secure cloud infrastructure environment using Amazon Web Services. The lab simulates how a real company would configure and secure their cloud environment, covering networking, identity and access management, compute, storage, and audit logging.

## Lab Architecture
```
AWS Cloud
│
├── VPC — lab-vpc
│   │
│   ├── Security Group — lab-sg
│   │   └── EC2 Instance — lab-server (t3.micro, Amazon Linux 2023)
│   │       └── IAM Role — lab-ec2-role (S3 read-only)
│   │
│   └── IAM Users
│       ├── admin-user (AdministratorAccess)
│       └── limited-user (S3 read-only — access tested)
│
├── S3 Bucket — lab-bucket (public access blocked)
│
└── CloudTrail — lab-trail (management events logged)
```
## Lab Environment
- Cloud Provider: AWS
- Services Used: VPC, Security Groups, IAM, EC2, S3, CloudTrail

## Project Structure
- [CloudTrail Logging](CloudTrail%20Logging/README.md)
- [EC2 Instance](EC2%20Instance/README.md)
- [IAM and Access Control](IAM%20and%20Access%20Control/README.md)
- [S3 Storage](S3%20Storage/README.md)
- [VPC and Security Group](VPC%20and%20security%20group/README.md)
