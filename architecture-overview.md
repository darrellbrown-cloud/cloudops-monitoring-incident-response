# Architecture Overview



## Project



CloudOps Monitoring & Incident Response on AWS


 
## Purpose


This project demonstrates a basic CloudOps monitoring and incident response workflow for an EC2 instance. The goal is to show how AWS services can be used to monitor infrastructure, detect high CPU utilization, send alerts, and support a documented response process.



## Architecture Flow



```text
EC2 Instance
   |
   v
CloudWatch Metrics
   |
   v
CloudWatch Alarm
   |
   v
SNS Topic
   |
   v
Email Subscription
   |
   v
Support Engineer Investigation
   |
   v
Incident Response Runbook
   |
   v
Sample Incident Report
   |
   v
S3 and GitHub Documentation
```
