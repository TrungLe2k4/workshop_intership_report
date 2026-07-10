---
title: "Week 4: High Availability with Elastic Load Balancing & Auto Scaling"
date: 2026-05-08
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:
* Design and implement highly available, fault-tolerant architectures on AWS.
* Configure Elastic Load Balancing (ELB) to distribute incoming application traffic across multiple targets.
* Automate infrastructure scaling using EC2 Auto Scaling Groups (ASG) based on real-time metrics.
* Enhance edge security by implementing SSL/TLS termination at the load balancer level.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Learn Elastic Load Balancing (ELB):<br>&emsp; + Compare Application Load Balancer (ALB) and Network Load Balancer (NLB).<br>&emsp; + Understand Target Groups and Health Checks. | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - **ALB Practice:**<br>&emsp; + Create an Application Load Balancer.<br>&emsp; + Register multiple EC2 instances into a Target Group.<br>&emsp; + Test traffic distribution and simulate a failure (stopping one EC2). | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - Learn Auto Scaling Groups (ASG):<br>&emsp; + Launch Templates concepts.<br>&emsp; + Dynamic Scaling Policies (Target Tracking, Step Scaling). | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **ASG Practice:**<br>&emsp; + Create a Launch Template with Web Server User Data.<br>&emsp; + Configure an ASG linked to the ALB with a Target Tracking policy (e.g., scale out when CPU > 50%). | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - Explore Web Security Architecture:<br>&emsp; + Conceptualize AWS Certificate Manager (ACM).<br>&emsp; + Redesign Security Groups: EC2 instances only accept traffic from the ALB, blocking direct Internet access. | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Successfully built a resilient, highly available architecture spanning multiple Availability Zones.
* Mastered the integration of ALB and ASG, allowing the system to automatically scale computing resources based on actual traffic demands.
* Applied advanced cybersecurity design patterns: successfully hid backend EC2 instances from the public internet by configuring their Security Groups to only accept inbound HTTP traffic originating strictly from the Application Load Balancer.

---

<!-- 
Image requirements for Week 4:
1. week4-1.png: Screenshot of your Target Group showing instances in a "Healthy" state.
2. week4-2.png: Screenshot of the Auto Scaling Group details or Launch Template configuration.

-->

![Target Group Health](/workshop_intership_report/images/1-Worklog/1.4-Week4/week4-1.png)
<p align="center"><i>Figure 1: Verifying that EC2 instances successfully pass the Application Load Balancer's health checks.</i></p>

![Auto Scaling Group](/workshop_intership_report/images/1-Worklog/1.4-Week4/week4-2.png)
<p align="center"><i>Figure 2: Configuring the Auto Scaling Group to dynamically provision instances based on traffic load.</i></p>

