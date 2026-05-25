# IAM and Access Control

## Purpose
To demonstrate identity and access management in AWS by creating users with defined permissions and validating least privilege access controls across multiple services.

## Lab Environment
- Cloud Provider: AWS
- Services Involved: IAM, S3, EC2

## Configuration

### Admin User
Created a dedicated IAM admin user to avoid using the root account for daily tasks. Attached the AdministratorAccess policy to this user and used it as the primary account throughout the lab.

![image](/screenshots/iam2.png)
![image](/screenshots/iam2.png.jpg)

### Limited User
Created a second IAM user named limited-user with only AmazonS3ReadOnlyAccess attached, simulating what a restricted employee account looks like with access to only what their role requires.

![image](/screenshots/iam3.png)
![image](/screenshots/iam4.png)

### IAM Role
Created an IAM role named lab-ec2-role with AmazonS3ReadOnlyAccess and attached it to the EC2 instance, allowing the instance to interact with S3 without requiring hardcoded credentials.

![image](/screenshots/role.png)

## Testing
Logged into AWS as limited-user and attempted to access EC2 and S3 to verify access limits were implemented correctly.

### EC2 Access Attempt
Navigated to EC2 as limited-user. Access was denied across all EC2 resources, confirming that the user had no permissions.

![image](/screenshots/ec2attempt.png)

### S3 Access Attempt
Navigated to S3 as limited-user. The user was denied permission to list buckets entirely, confirming that read access was set up correctly, and the user could not view company storage resources.

![image](/screenshots/buckets.png)

## Results
Successfully demonstrated least privilege access control across IAM users and roles. The limited-user was restricted to only their given assigned permissions and was denied access to all other AWS services as intended.
