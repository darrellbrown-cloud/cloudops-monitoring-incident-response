\# Cost Notes



\## Project



CloudOps Monitoring \& Incident Response on AWS



\## AWS Services Used



\- Amazon EC2

\- Amazon CloudWatch

\- Amazon SNS

\- Amazon S3



\## Cost Control Notes



This project was designed to stay low-cost by using a small EC2 instance, basic CloudWatch metrics, a simple SNS topic, and a private S3 bucket for documentation.



\## EC2



The EC2 instance used was a small instance type:



\- Instance type: t3.micro

\- Operating system: Amazon Linux 2023



The instance should be stopped or terminated when the project is complete.



\## CloudWatch



CloudWatch was used for:



\- EC2 CPUUtilization metric

\- CloudWatch alarm

\- CloudWatch dashboard



Only a small number of metrics and one alarm were created.



\## SNS



SNS was used for alert notification routing.



Email subscriptions were created, but confirmation emails were delayed or not received during testing.



\## S3



S3 was used to store project documentation files.



The bucket was kept private with public access blocked.



\## Cleanup Recommendation



To avoid ongoing charges, delete or stop the following resources after the project is documented:



\- EC2 instance

\- CloudWatch alarm

\- CloudWatch dashboard

\- SNS topic and subscriptions

\- S3 bucket and uploaded files

