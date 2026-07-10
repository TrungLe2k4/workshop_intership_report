---
title: "Week 3: Cloud Compute Infrastructure & Amazon EC2"
date: 2026-05-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:
* Master the lifecycle, configuration, and management of Amazon EC2 (Elastic Compute Cloud) virtual servers.
* Understand different EC2 Instance Types and cost optimization models (On-Demand, Reserved, Spot).
* Implement automated application deployment using EC2 User Data.
* Enforce strict network security at the instance level using Security Groups.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Learn Amazon EC2 fundamentals:<br>&emsp; + Instance Types (Compute/Memory/Storage Optimized).<br>&emsp; + Amazon Machine Images (AMI) concepts. | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - Explore EC2 Storage and Networking:<br>&emsp; + Differentiate between EBS (Elastic Block Store) and Instance Store.<br>&emsp; + Understand Elastic IPs and Public/Private IPv4 addressing. | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - Deep dive into Security Groups (SG):<br>&emsp; + Understand SG as a stateful firewall operating at the ENI level.<br>&emsp; + Formulate rules to restrict SSH (Port 22) to specific admin IPs. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **EC2 Practical Lab (Part 1):**<br>&emsp; + Launch a Linux EC2 instance (Amazon Linux 2023).<br>&emsp; + Create and securely download an SSH Key Pair (.pem).<br>&emsp; + Successfully connect to the instance via SSH. | 07/05/2026 | 07/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - **EC2 Practical Lab (Part 2):**<br>&emsp; + Inject a Bash script via EC2 User Data to automatically install an Apache Web Server (httpd).<br>&emsp; + Modify the Security Group to allow inbound HTTP (Port 80) traffic and verify the web page. | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Successfully deployed and managed a virtual server in the cloud, utilizing Amazon EC2.
* Automated the bootstrap process of a web server using EC2 User Data, significantly reducing manual configuration time.
* Established a solid defensive perimeter by applying strict Security Group rules, ensuring that administrative ports (like SSH) are not exposed to the public internet (`0.0.0.0/0`).
* Proficiently managed SSH cryptographic key pairs for secure remote access.

---

<!-- 
Image requirements for Week 3:
1. week3-1.png: Screenshot of the EC2 Dashboard showing your running instance (Instance state: Running).
2. week3-2.png: Screenshot of the Security Group inbound rules showing Port 22 and Port 80 configured.

-->

![EC2 Instance Running](/workshop_intership_report/images/1-Worklog/1.3-Week3/week3-1.png)
<p align="center"><i>Figure 1: Successfully provisioned and launched a Linux Amazon EC2 instance.</i></p>

![Security Group Configuration](/workshop_intership_report/images/1-Worklog/1.3-Week3/week3-2.png)
<p align="center"><i>Figure 2: Configuring stateful firewall rules via Security Groups to allow HTTP and restricted SSH traffic.</i></p>

