\# Architecture Overview



\## Project



CloudOps Monitoring \& Incident Response on AWS



\## Purpose



This project demonstrates a basic CloudOps monitoring and incident response workflow for an EC2 instance. The goal is to show how AWS services can be used to monitor infrastructure, detect high CPU utilization, send alerts, and support a documented response process.



\## Architecture Flow



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

Support Engineer Investigation

&#x20;  ↓

Incident Response Runbook

&#x20;  ↓

Sample Incident Report

&#x20;  ↓

S3 and GitHub Documentation

