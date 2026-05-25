# VPC and Security Group Configuration

## Purpose
To create an isolated virtual network within Amazon Web Services (AWS) and configure a security group to control inbound and outbound traffic using least privilege principles.

## Lab Environment
- Cloud Provider: AWS
- VPC CIDR Block: 10.0.0.0/16

## Configuration

### VPC
Created a custom VPC named lab-vpc with a /16 CIDR block, providing an isolated network environment separate from the default AWS infrastructure.

![image](/screenshots/vpc.png)

### Security Group
Created a security group named lab-sg and attached it to lab-vpc. 
Configured the inbound rules to allow SSH access restricted to my IP address only, ensuring there's no public access. 

![image](/screenshots/sg1.png)
![image](/screenshots/sg2.png)


## Testing
Temporarily opened SSH to 0.0.0.0/0 to establish an EC2 Instance Connect session for testing, then I immediately reverted the rule back to my IP only after the session was complete.

## Results
Successfully created an isolated VPC and enforced least privilege network access through security group rules. 

Confirmed that unrestricted access was closed immediately after temporary use.
