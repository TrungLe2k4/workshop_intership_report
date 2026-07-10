---
title: "Week 5: Multi-Tier Database Systems (Amazon RDS & DynamoDB)"
date: 2026-05-15
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:
* Distinguish the use cases and architectures of SQL (Amazon RDS) and NoSQL (Amazon DynamoDB) databases.
* Deploy highly available (HA) database architectures using Multi-AZ deployments and Read Replicas.
* Secure database tiers by isolating them in Private Subnets and implementing strict Security Groups.
* Apply Data-at-Rest encryption using AWS Key Management Service (KMS).

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Learn Relational Database Service (RDS):<br>&emsp; + Concepts of Multi-AZ deployments for Disaster Recovery.<br>&emsp; + Read Replicas for performance scaling.<br>&emsp; + Automated Backups vs. Manual Snapshots. | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - **RDS Practice:**<br>&emsp; + Provision a MySQL/PostgreSQL RDS instance.<br>&emsp; + Place the database strictly in a Private Subnet.<br>&emsp; + Connect to RDS using an EC2 Bastion Host (Jump Server). | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - Learn Amazon DynamoDB (NoSQL):<br>&emsp; + Document & Key-Value data models.<br>&emsp; + Primary Key structures (Partition Key & Sort Key).<br>&emsp; + Provisioned vs. On-Demand capacity modes. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **DynamoDB Practice:**<br>&emsp; + Create a DynamoDB table (`InvoicesData`).<br>&emsp; + Insert, query, and scan items using the AWS Console and AWS CLI. | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - **Database Security Architecture:**<br>&emsp; + Configure Encryption at Rest using AWS KMS.<br>&emsp; + Restrict RDS Security Groups to only accept inbound traffic (Port 3306/5432) from the Web Tier Security Group. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Successfully deployed both relational (SQL) and non-relational (NoSQL) databases on the AWS Cloud.
* Mastered the architectural concept of isolating the Data Tier: placing databases inside Private Subnets so they are never directly exposed to the public internet.
* Enforced robust cybersecurity measures by enabling AWS KMS Encryption for databases to protect sensitive data at rest.
* Successfully tested internal network connectivity by securely accessing the RDS instance via an EC2 Bastion Host.

---

<!-- 
Image requirements for Week 5:
1. week5-1.png: Screenshot of the RDS Dashboard showing the database instance in an "Available" state.
2. week5-2.png: Screenshot of the DynamoDB table (Explore items view) showing some sample data inserted.

-->

![Amazon RDS Deployment](/workshop_intership_report/images/1-Worklog/1.5-Week5/week5-1.png)
<p align="center"><i>Figure 1: Successfully provisioned an Amazon RDS instance within a securely isolated Private Subnet.</i></p>

![DynamoDB Table](/workshop_intership_report/images/1-Worklog/1.5-Week5/week5-2.png)
<p align="center"><i>Figure 2: Interacting with the Amazon DynamoDB NoSQL database by adding and querying items.</i></p>

