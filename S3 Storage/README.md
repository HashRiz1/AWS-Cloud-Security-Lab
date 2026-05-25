# S3 Storage Configuration

## Purpose
To configure a secure cloud storage bucket in AWS, demonstrate proper access controls, and validate that public access is blocked.

## Lab Environment
- Service: Amazon S3
  
## Configuration
Created an S3 bucket with Block Public Access enabled across all settings, to ensure no data could be publicly exposed. 

Uploaded a test file to confirm the bucket was functional and accessible only through authenticated AWS accounts with the proper permissions.

![image](/screenshots/s31.png)

![image](/screenshots/s32.png)

## Testing
Logged in as limited-user and attempted to list and access the bucket to verify access restrictions were enforced.

The limited-user was denied permission to list buckets entirely, confirming that S3ReadOnlyAccess alone does not grant bucket enumeration without explicit list permissions.

![image](/screenshots/buckets.png)

## Results
Successfully configured a secure S3 bucket with public access being blocked. Validated through IAM access testing that storage resources are protected from unauthorized access.
