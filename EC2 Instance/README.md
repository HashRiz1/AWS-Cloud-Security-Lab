# EC2 Instance Deployment

## Purpose
To deploy a cloud-based virtual server within the lab's virtual private cloud, configure it securely, and connect to and interact with a live cloud instance.

## Lab Environment
- Instance Type: t3.micro
- AMI: Amazon Linux 2023

## Configuration
- Launched an EC2 instance named lab-server inside lab-vpc using a t3.micro instance type. 

- Attached the lab-sg security group to restrict inbound access and assigned the lab-ec2-role IAM role to allow secure S3 interaction without proper credentials. 

- Created an RSA key pair named lab-key for authentication and assigned an Elastic IP for consistent public access.

![image](/screenshots/ec2instance.png)

## Testing
Connected to the instance using EC2 Instance Connect through AWS. Ran basic system commands to verify the instance was live and fully operational.

## Investigation
Once connected, the following commands to confirm system functionality were run:

- whoami — confirmed ec2-user identity
- uname -a — confirmed Linux kernel and system info
- df -h — confirmed disk space availability
- echo and cat — created and read a test file confirming write access

![image](/screenshots/ec2instance2.png)

## Results
Successfully deployed and connected to a live cloud server. Confirmed the instance was properly configured with least privilege networking, an IAM role, and restricted SSH access.
