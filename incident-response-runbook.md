\# Incident Response Runbook



\## Project



CloudOps Monitoring \& Incident Response on AWS



\## Purpose



This runbook provides a basic response process for a CloudOps support engineer when an EC2 instance triggers a high CPU CloudWatch alarm.



\## Alert Details



\*\*Alarm name:\*\* cloudops-high-cpu-alarm  

\*\*Service:\*\* Amazon EC2  

\*\*Metric:\*\* CPUUtilization  

\*\*Threshold:\*\* CPUUtilization greater than 70%  

\*\*Evaluation:\*\* 2 datapoints within 2 minutes  

\*\*Notification path:\*\* CloudWatch Alarm → SNS Topic → Email Subscription  



\## Business Impact



High CPU utilization may indicate that the server is under heavy load, experiencing an application issue, or running an unexpected process. If not investigated, the server may become slow, unstable, or unavailable to users.



\## Initial Response Steps



1\. Open the CloudWatch alarm.

2\. Confirm the alarm state is \*\*In alarm\*\*.

3\. Review the CPUUtilization graph.

4\. Identify when the CPU spike began.

5\. Check whether the spike is temporary or sustained.

6\. Open the EC2 console.

7\. Confirm the instance is running and passing status checks.

8\. Connect to the EC2 instance using EC2 Instance Connect.

9\. Check for high CPU processes.

10\. Stop or investigate the process causing the issue.

11\. Continue monitoring until CPU returns to normal.



\## Linux Investigation Commands



Use the following commands after connecting to the EC2 instance.



\### View live CPU and process activity



```bash

top

```



\### Show the top CPU-consuming processes



```bash

ps aux --sort=-%cpu | head

```



\### Check whether the test CPU process is running



```bash

pgrep yes

```



\### Stop the test CPU process if needed



```bash

pkill yes

```



\## Escalation Criteria



Escalate the incident if:



\- CPU remains high after stopping the suspected process

\- The instance fails EC2 status checks

\- The application becomes unavailable

\- The cause is unknown

\- The issue affects customers or production users



\## Resolution Steps



1\. Stop or correct the process causing high CPU.

2\. Confirm CPU utilization drops below the alarm threshold.

3\. Confirm the CloudWatch alarm returns to \*\*OK\*\*.

4\. Document the timeline, impact, root cause, and resolution.

5\. Add screenshots or evidence to the incident record.



\## Post-Incident Review



After the incident is resolved, review:



\- What caused the alarm?

\- Was the alert threshold appropriate?

\- Was the response process clear?

\- Were notifications delivered successfully?

\- Is additional monitoring needed?



\## Project Notes



During this project, high CPU was intentionally simulated on an EC2 instance to test the monitoring and incident response workflow.



The CloudWatch alarm successfully entered the \*\*In alarm\*\* state when CPU utilization crossed the configured threshold.



The SNS topic was created and attached to the CloudWatch alarm. Email subscriptions were created, but confirmation emails were delayed or not received during testing. This was documented as a troubleshooting issue.

