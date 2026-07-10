---
title: "Week 2: Identity & Access Management (AWS IAM) and CLI Configuration"
date: 2026-04-24
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:
* Master identity management and secure authorization mechanisms with AWS IAM following the Least Privilege and Zero Trust principles.
* Understand and construct custom JSON IAM Policies.
* Install, configure, and proficiently interact with AWS via the Command Line Interface (AWS CLI).
* Implement Resource Tags for systematic cloud management.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Deep dive into AWS IAM core concepts:<br>&emsp; + Differentiate between Users, Groups, Roles, and Policies.<br>&emsp; + Security best practices: Stop using the Root account. | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - **Account Security Practice:**<br>&emsp; + Enable Multi-Factor Authentication (MFA) for the Root account.<br>&emsp; + Create an IAM Admin Group and an individual IAM User for daily tasks. | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - Learn the structure of a JSON IAM Policy:<br>&emsp; + Understand core elements: Effect, Action, Resource, Condition.<br>&emsp; + Write custom IAM Policies to grant specific permissions. | 29/04/2026 | 29/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **AWS CLI Practice:**<br>&emsp; + Generate Access Key & Secret Key for the IAM User.<br>&emsp; + Install AWS CLI locally and configure credentials (`aws configure`).<br>&emsp; + Verify connection using `aws sts get-caller-identity`. | 30/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - Understand AWS Service Roles & Resource Tags:<br>&emsp; + Why Service Roles should be used for AWS resources instead of hardcoding Access Keys.<br>&emsp; + Define a tagging strategy (e.g., Project: IDPCloud, Env: Dev) for resource tracking and FinOps. | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Established a solid cybersecurity foundation by securing the Root account with MFA and utilizing a dedicated IAM User.
* Mastered the structure of JSON IAM Policies, enabling precise permission grants based on the Least Privilege principle.
* Successfully configured the local development environment with AWS CLI and securely managed Access Keys.
* Formed a clear understanding of IAM Roles for service-to-service communication, preventing future security vulnerabilities caused by hardcoded credentials.

---

<!-- 
Image requirements for this week:
1. week2-1.png: Screenshot showing MFA enabled on the Security credentials page of your Root or IAM account.
2. week2-2.png: Screenshot of a custom JSON policy you created in the IAM Policy visual editor.
-->

![MFA Enabled](/workshop_intership_report/images/1-Worklog/1.2-Week2/week2-1.png)
<p align="center"><i>Figure 1: Successfully secured the AWS account by enabling Multi-Factor Authentication (MFA).</i></p>

![JSON IAM Policy](/workshop_intership_report/images/1-Worklog/1.2-Week2/week2-2.png)
<p align="center"><i>Figure 2: Constructing a custom IAM Policy using JSON format to enforce strict access controls.</i></p>

