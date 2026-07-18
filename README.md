\# CloudOps Monitoring \& Incident Response on AWS



\## Project Overview



This project demonstrates a basic CloudOps monitoring and incident response workflow on AWS.



An EC2 instance was monitored with Amazon CloudWatch. A CloudWatch alarm was configured to detect high CPU utilization. The alarm was connected to an SNS topic for notifications. A CloudWatch dashboard was created to visualize CPU activity, and incident response documentation was written to support troubleshooting and communication.



\## Architecture



```text

EC2 Instance

&#x20;  ↓

CloudWatch Metrics

&#x20;  ↓

CloudWatch Alarm

&#x20;  ↓

SNS Topic

&#x20;  ↓

Email Subscription

&#x20;  ↓

Incident Response Runbook

&#x20;  ↓

Sample Incident Report

&#x20;  ↓

S3 and GitHub Documentation

