\# Cleanup Steps



\## Project



CloudOps Monitoring \& Incident Response on AWS



\## Cleanup Order



Follow this order to remove project resources safely.



\## 1. Stop or Terminate EC2 Instance



Go to:



EC2 → Instances



Select:



cloudops-monitored-server



Choose:



Instance state → Terminate instance



\## 2. Delete CloudWatch Alarm



Go to:



CloudWatch → Alarms



Select:



cloudops-high-cpu-alarm



Choose:



Actions → Delete



\## 3. Delete CloudWatch Dashboard



Go to:



CloudWatch → Dashboards



Select:



cloudops-monitoring-dashboard



Choose:



Delete



\## 4. Delete SNS Topic



Go to:



SNS → Topics



Select:



cloudops-alerts-topic



Choose:



Delete



\## 5. Delete S3 Bucket Contents



Go to:



S3 → your project bucket



Select all uploaded files.



Choose:



Delete



\## 6. Delete S3 Bucket



After the bucket is empty, delete the bucket.



\## 7. Confirm Cleanup



Check the following services:



\- EC2

\- CloudWatch Alarms

\- CloudWatch Dashboards

\- SNS Topics

\- S3 Buckets



\## Final Note



This cleanup removes the AWS resources created for this project and helps avoid unnecessary charges.

