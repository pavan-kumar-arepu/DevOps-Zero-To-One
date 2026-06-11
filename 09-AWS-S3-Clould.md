# Phase 9 - AWS S3 Cloud Storage ☁️


After building applications, companies need cloud services.


One basic cloud service:


AWS S3



---


# What Is S3?


Simple Storage Service


Think:


Google Drive for applications.


But with:


- APIs
- Security
- Automation
- Huge scale



---


# Why Companies Use S3?


Store:


- Build files
- Reports
- Logs
- Backups
- Images
- Data



---


# Configure AWS CLI


```bash
aws configure
```



Provide:


Access Key

Secret Key

Region



---


# Create Bucket


```bash
aws s3 mb s3://my-devops-learning-bucket
```



Bucket means:


Storage container



---


# Upload Artifact


```bash
aws s3 cp application-v1.zip s3://my-devops-learning-bucket
```



---


# Verify


```bash
aws s3 ls s3://my-devops-learning-bucket
```



---


# Real Company Flow


CI/CD Pipeline


↓

Generate Artifact


↓

Upload to S3


↓

Other Systems Consume



---


# DevOps Responsibility


Manage:


✔ IAM permissions

✔ Automation scripts

✔ Storage lifecycle

✔ Security
