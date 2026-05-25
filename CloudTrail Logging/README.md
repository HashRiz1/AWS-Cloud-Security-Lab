# CloudTrail Audit Logging

## Purpose
To enable audit logging across the AWS environment, this captures all account activity and stores logs securely in S3 for review and compliance purposes.

## Lab Environment
- Service: AWS CloudTrail
- Log Storage: Amazon S3

## Configuration
Created a CloudTrail named lab-trail configured to log all management events across the AWS account. Logs are automatically sent to the dedicated S3 bucket, providing an audit record of every action taken in the environment.

![image](/screenshots/trail1.png)

## Testing
Performed several actions in the AWS console, including IAM user creation, EC2 instance management, and S3 bucket configuration. These actions were captured by CloudTrail as management events.

## Investigation
Navigated to the CloudTrail Event History to confirm events were being recorded. Verified that user actions, resource modifications, and access attempts were all logged with timestamps and source information.

![image](/screenshots/trail2.png)

## Results
Successfully enabled account-wide audit logging through CloudTrail. All management actions performed throughout this lab are captured and stored, demonstrating an understanding of how cloud compliance and audit trail requirements work.
