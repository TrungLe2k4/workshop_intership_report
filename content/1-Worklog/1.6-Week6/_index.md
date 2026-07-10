---
title: "Week 6: System Monitoring & Optimization (CloudWatch & CloudTrail)"
date: 2026-05-22
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:
* Implement comprehensive system monitoring using Amazon CloudWatch (Metrics, Dashboards, and Alarms).
* Establish an automated incident notification pipeline using Amazon Simple Notification Service (SNS).
* Create a robust security auditing mechanism by tracking API calls via AWS CloudTrail.
* Analyze architectural best practices and cost optimizations using AWS Trusted Advisor.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Learn Amazon CloudWatch:<br>&emsp; + Differentiate between Metrics, Logs, and Events.<br>&emsp; + Concept of CloudWatch Dashboards for operational visibility. | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - **CloudWatch & SNS Practice:**<br>&emsp; + Create an SNS Topic and subscribe your email address.<br>&emsp; + Configure a CloudWatch Billing Alarm (e.g., alert if estimated charges exceed $10) and trigger an SNS email. | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - Learn AWS CloudTrail:<br>&emsp; + Purpose of CloudTrail for governance, compliance, and auditing.<br>&emsp; + Management Events vs. Data Events. | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **CloudTrail Practice (Forensics):**<br>&emsp; + Explore the Event History console.<br>&emsp; + Perform a security audit task: Filter logs to find exactly which IAM user or Role terminated a specific EC2 instance or modified a Security Group. | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - Operations & FinOps check:<br>&emsp; + Review the AWS Trusted Advisor dashboard for security vulnerabilities (e.g., open ports) and cost-saving opportunities.<br>&emsp; + Explore AWS Cost Explorer to analyze spending trends. | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Successfully established an automated operational monitoring system, ensuring immediate notification (via email) when financial thresholds or CPU limits are breached.
* Built advanced cybersecurity auditing capabilities (Security Monitoring): CloudTrail now provides an undeniable digital audit trail (Audit Trail) to investigate incidents or misconfigurations.
* Mastered the use of AWS Trusted Advisor to continuously scan the cloud environment, bridging the gap between Security Posture and Cost Optimization (FinOps).

---

<!-- 
Image requirements for Week 6:
1. week6-1.png: Screenshot of a CloudWatch Alarm (e.g., Billing Alarm or CPU Alarm) showing its state (OK or In alarm).
2. week6-2.png: Screenshot of an email received from AWS SNS confirming the alert notification.
3. week6-3.png: Screenshot of AWS CloudTrail Event History showing recent API activity (e.g., RunInstances, ConsoleLogin).
-->

![CloudWatch Alarm](/workshop_intership_report/images/1-Worklog/1.6-Week6/week6-1.png)
<p align="center"><i>Figure 1: Setting up an Amazon CloudWatch Alarm to monitor metrics and trigger automated alerts.</i></p>

![SNS Email Notification](/workshop_intership_report/images/1-Worklog/1.6-Week6/week6-2.png)
<p align="center"><i>Figure 2: Successfully receiving an automated alert via email routed through Amazon SNS.</i></p>

![CloudTrail Event History](/workshop_intership_report/images/1-Worklog/1.6-Week6/week6-3.png)
<p align="center"><i>Figure 3: Utilizing AWS CloudTrail to maintain a precise digital audit log of all API activities for cybersecurity forensics.</i></p>