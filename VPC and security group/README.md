# VPC and Security Group Configuration

## Purpose
To create an isolated virtual network within Amazon Web Services (AWS) and configure a security group to control inbound and outbound traffic using least privilege principles.

## Lab Environment
- Cloud Provider: AWS
- VPC CIDR Block: 10.0.0.0/16

## Configuration

### VPC
Created a custom VPC named lab-vpc with a /16 CIDR block, providing an isolated network environment separate from the default AWS infrastructure.

(SCREENSHOT: VPC successfully created screen showing lab-vpc 
name and VPC ID)

### Security Group
Created a security group named lab-sg and attached it to lab-vpc. 
Configured the inbound rules to allow SSH access restricted to my IP address only, ensuring there's no public access. 

(SCREENSHOT: Inbound rules showing SSH restricted to My IP only)

## Testing
Temporarily opened SSH to 0.0.0.0/0 to establish an EC2 
Instance Connect session for testing, then I immediately reverted the rule back to My IP only after the session was complete.

(SCREENSHOT: Inbound rules after reverting back to My IP only, 
showing the rule locked back down)

## Results
Successfully created an isolated VPC and enforced least privilege network access through security group rules. 
Confirmed that unrestricted access was closed immediately after temporary use.
