---
title: "Week 7: Multi-Tier Storage Ecosystem & Data Governance"
date: 2026-05-29
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:
* Master the AWS multi-tier storage ecosystem: Amazon S3 (Object), Amazon EFS (Linux File), and Amazon FSx (Windows File).
* Build a Hybrid Cloud Storage bridge using AWS Storage Gateway.
* Automate centralized data protection and compliance using AWS Backup.
* Enforce strict Object-level security and prevent S3 data breaches.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Explore advanced storage solutions:<br>&emsp; + Compare use cases for EFS and FSx.<br>&emsp; + Learn AWS Storage Gateway architecture (File, Volume, Tape Gateways). | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - **Hybrid Storage Practice (Lab 24):**<br>&emsp; + Deploy an AWS Storage Gateway (File Gateway).<br>&emsp; + Connect an on-premises simulated server to Amazon S3 via NFS/SMB protocols. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - Learn Centralized Data Protection:<br>&emsp; + AWS Backup core concepts (Backup Vaults, Backup Plans).<br>&emsp; + Lifecycle rules for cost-effective cold storage archiving. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **AWS Backup Practice (Lab 13):**<br>&emsp; + Create a centralized Backup Plan for EC2 and RDS instances.<br>&emsp; + Define backup windows and retention periods to meet compliance standards. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - **S3 Security & Risk Management (Lab 57):**<br>&emsp; + Apply the "Least Privilege" principle using Object Permissions.<br>&emsp; + Practice enabling/disabling "Block all public access" to understand data leak boundaries. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Successfully bridged on-premises infrastructure with cloud storage using AWS Storage Gateway, solving infinite scaling needs without changing traditional file protocols.
* Transitioned from fragmented, manual snapshots to a Centralized Backup strategy, ensuring automated data protection across all AWS services.
* Strengthened cybersecurity posture by mastering Amazon S3 access controls, effectively preventing the #1 cause of cloud data breaches (misconfigured public buckets).
* Performed rigorous FinOps cleanup by removing unused Storage Gateways and empty Backup Vaults.

---



![AWS Backup Plan](/images/1-Worklog/1.7-Week7/week7-2.png)
<p align="center"><i>Figure 1: Centralized AWS Backup Plan configured to automate data protection and compliance.</i></p>

![S3 Block Public Access](/images/1-Worklog/1.7-Week7/week7-3.png)
<p align="center"><i>Figure 2: Enforcing robust cloud security by applying strict Block Public Access policies on Amazon S3.</i></p>