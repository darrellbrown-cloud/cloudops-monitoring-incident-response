\# Sample Incident Report



\## Project



CloudOps Monitoring \& Incident Response on AWS



\## Incident Title



High CPU Utilization Detected on EC2 Instance



\## Incident Summary



A CloudWatch alarm detected high CPU utilization on the monitored EC2 instance. The alarm entered the \*\*In alarm\*\* state after CPU utilization exceeded the configured threshold of 70% for 2 datapoints within 2 minutes.



This incident was intentionally simulated as part of a CloudOps monitoring and incident response project.



\## Affected Resource



\*\*Service:\*\* Amazon EC2  

\*\*Instance name:\*\* cloudops-monitored-server  

\*\*Metric:\*\* CPUUtilization  

\*\*Alarm name:\*\* cloudops-high-cpu-alarm  

\*\*Notification topic:\*\* cloudops-alerts-topic  



\## Impact



The EC2 instance experienced high CPU utilization during the test. In a real environment, sustained high CPU could cause slow application performance, delayed responses, or service instability.



No real customer workload was affected because this was a controlled test environment.



\## Detection



The issue was detected through Amazon CloudWatch.



CloudWatch monitored the EC2 instance CPUUtilization metric and triggered the configured alarm when CPU usage crossed the threshold.



\## Timeline



| Time | Event |

|---|---|

| T0 | EC2 instance running normally |

| T1 | CPU stress test started on EC2 instance |

| T2 | CPU utilization increased above 70% |

| T3 | CloudWatch alarm entered \*\*In alarm\*\* state |

| T4 | Alarm graph confirmed high CPU spike |

| T5 | CPU stress process stopped |

| T6 | CPU utilization returned toward normal |



\## Root Cause



The high CPU condition was caused by a controlled Linux CPU stress command using the `yes` process. This was intentionally done to simulate a server performance incident.



\## Resolution



The CPU stress process was stopped using the following command:



```bash

pkill yes

