---
title: "Week 11: Serverless Backend & AI Textract Integration"
date: 2026-06-26
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:
* Build the Event-Driven storage backbone using Amazon S3, SQS, and DynamoDB (On-demand).
* Develop serverless logic (AWS Lambda - Python 3.12) to bypass API Gateway using Presigned URLs.
* Integrate Amazon Textract to automatically extract critical data from unstructured invoices.
* Implement Zero Trust security mechanisms including Data Masking (PII protection) and API Rate Limiting (AWS WAF).

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - **Storage & Queuing Setup:**<br>&emsp; + Provision `idp-ingest-bucket-1` (Block all public access).<br>&emsp; + Create an SQS standard queue (`idp-document-queue`) with a 2-minute visibility timeout.<br>&emsp; + Create DynamoDB `InvoicesData` table (On-demand capacity). | 29/06/2026 | 29/06/2026 | AWS Console |
| **Tuesday**<br>(Day 2) | - **Event Triggers & Lifecycle (FinOps):**<br>&emsp; + Configure S3 Event Notification to push object creation events (`SendToSQS`) to the queue.<br>&emsp; + Define an S3 Lifecycle Rule (`Auto-Delete-Raw-Invoices`) to expire raw uploads after 1 day. | 30/06/2026 | 30/06/2026 | AWS Console |
| **Wednesday**<br>(Day 3) | - **Serverless Compute (Lambda Python 3.12):**<br>&emsp; + Write `idp-api-presign` function to generate strict Presigned URLs (300s expiry) locking the `ContentType`.<br>&emsp; + Apply IAM Role `idp-lambda-ai-role` enforcing the Principle of Least Privilege. | 01/07/2026 | 01/07/2026 | IDE / AWS Lambda |
| **Thursday**<br>(Day 4) | - **AI Integration (Amazon Textract):**<br>&emsp; + Code the `idp-ai-worker` triggered by SQS (Batch size: 10).<br>&emsp; + Utilize Textract `QUERIES` to precisely extract Invoice Number, Date, Total Amount, and Vendor Name, persisting results to DynamoDB. | 02/07/2026 | 02/07/2026 | AWS Textract SDK |
| **Friday**<br>(Day 5) | - **API Security & Data Masking:**<br>&emsp; + Write `idp-api-get-invoices` incorporating Data Masking to hide sensitive TaxIDs (e.g., `******1234`).<br>&emsp; + Configure AWS WAF (`idp-api-waf-shield`) with `BlockSpamIP` rate limit rule (100 req/5 mins). | 03/07/2026 | 03/07/2026 | AWS WAF & API Gateway |

### Achievements:
* Successfully engineered a completely Decoupled Architecture, ensuring backend AI workers scale smoothly without causing synchronous API timeouts.
* Protected critical PII data by utilizing strict Backend Data Masking, proving a strong Zero Trust mindset (never trusting the frontend to hide data).
* Eliminated the risk of wallet-busting DDoS attacks by implementing an aggressive AWS WAF rate-limiting rule.
* Enforced automated FinOps governance by deploying S3 Lifecycle rules to continually purge raw data and cut hot-storage costs.

---

![S3 Event & Lifecycle](/images/1-Worklog/1.11-Week11/week11-1.png)
<p align="center"><i>Figure 1: Establishing Event-Driven pipelines via S3 Event Notifications and FinOps compliance via S3 Lifecycle rules.</i></p>

![Serverless AI Worker](/images/1-Worklog/1.11-Week11/week11-2.png)
<p align="center"><i>Figure 2: AWS Lambda configured as an AI Worker, triggered by SQS to process invoices using Amazon Textract.</i></p>

![AWS WAF Rate Limiting](/images/1-Worklog/1.11-Week11/week11-3.png)
<p align="center"><i>Figure 3: Enforcing API security and preventing DDoS attacks via AWS WAF Rate-based rules (BlockSpamIP).</i></p>