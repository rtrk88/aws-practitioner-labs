# EC2 Accessing S3 Using IAM Role

## Objective

Demonstrate secure access from an Amazon EC2 instance to an Amazon S3 bucket using an IAM Role instead of access keys.

## Architecture

EC2 Instance
    ↓
IAM Role
    ↓
Amazon S3 Bucket

## Tasks Performed

- Create IAM Role for EC2
- Attach S3 permissions to the role
- Launch EC2 instance
- Attach IAM Role to EC2
- Connect to EC2
- Verify AWS identity using STS
- Access S3 bucket without access keys

## Evidence

### IAM Role Created

(Screenshot)

### EC2 Instance

(Screenshot)

### STS Identity Verification

(Screenshot)

### S3 Access Test

(Screenshot)

## Key Learnings

- IAM Roles provide temporary credentials.
- Access keys should be avoided when possible.
- EC2 can securely access AWS services through IAM Roles.
- AWS STS provides temporary security credentials.
