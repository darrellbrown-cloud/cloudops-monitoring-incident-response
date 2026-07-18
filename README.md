# CloudOps Monitoring & Incident Response on AWS

## Project Overview

This project demonstrates a basic CloudOps monitoring and incident response workflow on AWS.

An EC2 instance was monitored with Amazon CloudWatch. A CloudWatch alarm was configured to detect high CPU utilization. The alarm was connected to an SNS topic for notifications. A CloudWatch dashboard was created to visualize CPU activity, and incident response documentation was written to support troubleshooting and communication.

## Architecture

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
Incident Response Runbook
   |
   v
Sample Incident Report
   |
   v
S3 and GitHub Documentation
```

## AWS Services Used

- Amazon EC2
- Amazon CloudWatch Metrics
- Amazon CloudWatch Alarm
- Amazon SNS
- Amazon S3
- Security Groups
- GitHub

## Monitored Resource

- Instance name: cloudops-monitored-server
- Instance type: t3.micro
- Metric monitored: CPUUtilization

## Alarm Configuration

- Alarm name: cloudops-high-cpu-alarm
- Metric: CPUUtilization
- Threshold: Greater than 70%
- Evaluation: 2 datapoints within 2 minutes
- Notification topic: cloudops-alerts-topic

## Incident Simulation

A high CPU incident was simulated on the EC2 instance using a Linux CPU load command.

CloudWatch detected the CPU spike and the alarm entered the **In alarm** state.

## Screenshots

Screenshots are stored in the `screenshots/` folder.

Included screenshots:

- CloudWatch alarm in alarm state
- CloudWatch dashboard showing CPU utilization

## Documentation Files

- `architecture-overview.md`
- `incident-response-runbook.md`
- `sample-incident-report.md`
- `cost-notes.md`
- `cleanup-steps.md`

## Key Skills Demonstrated

- EC2 monitoring
- CloudWatch metrics
- CloudWatch alarm configuration
- SNS notification setup
- Incident response documentation
- CloudOps troubleshooting workflow
- AWS cost awareness
- Technical communication

## Project Status

Completed core AWS build.

SNS email subscriptions were created, but confirmation emails were delayed or not received during testing. The issue was documented as part of the troubleshooting process. Paste
