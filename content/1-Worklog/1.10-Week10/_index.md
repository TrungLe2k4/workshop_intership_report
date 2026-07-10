---
title: "Week 10: Architecture Design & FinOps for Serverless IDP"
date: 2026-06-19
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:
* Design the complete Runtime Architecture for the "Serverless Intelligent Document Processing (IDP) System".
* Implement Event-Driven Architecture to solve bandwidth bottlenecks when handling large files.
* Architect a Defense-in-Depth Edge Security perimeter integrating Route 53, CloudFront, AWS WAF, and Amazon Cognito.
* Optimize cloud financial operations (FinOps) to maintain the system's running cost under $30/month.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - **Architecture Blueprinting:**<br>&emsp; + Map out the network boundaries: Global Services, Regional Services, and Private VPC.<br>&emsp; + Separate Runtime Architecture from Deployment Architecture. | 22/06/2026 | 22/06/2026 | Project Documentation |
| **Tuesday**<br>(Day 2) | - **Event-Driven & API Bypass Design:**<br>&emsp; + Design a secure file upload workflow bypassing API Gateway using S3 Presigned URLs.<br>&emsp; + Decouple the AI extraction process using Amazon S3 Events and SQS. | 23/06/2026 | 23/06/2026 | Project Documentation |
| **Wednesday**<br>(Day 3) | - **Edge Security & Identity Layout:**<br>&emsp; + Attach AWS WAF for global threat mitigation.<br>&emsp; + Blueprint the CognitoUserPoolAuthorizer flow to enforce JWT Token validation at the API Gateway. | 24/06/2026 | 24/06/2026 | Project Documentation |
| **Thursday**<br>(Day 4) | - **FinOps & Cost Optimization:**<br>&emsp; + Redesign the network topology: Remove expensive NAT Gateways.<br>&emsp; + Replace with VPC Gateway Endpoints to route S3 and DynamoDB traffic internally at $0 data transfer cost. | 25/06/2026 | 25/06/2026 | Project Documentation |
| **Friday**<br>(Day 5) | - **Well-Architected Review:**<br>&emsp; + Apply color-coded data flows and legends to the diagram.<br>&emsp; + Finalize the architecture, ensuring it meets AWS Well-Architected Framework standards, ready for the 5-member team deployment. | 26/06/2026 | 26/06/2026 | Project Documentation |

### Achievements:
* Delivered a highly professional, enterprise-grade architecture diagram featuring clear network segregation and data flows.
* Solved the "Cloud Waste" financial trap by engineering a 100% Serverless ecosystem (zero EC2 instances running 24/7) and utilizing Gateway Endpoints instead of NAT Gateways.
* Embraced an Event-Driven paradigm, ensuring the system can automatically scale from 0 to thousands of concurrent document processing requests without bottlenecks.

---

![IDP Architecture Diagram](/images/1-Worklog/1.10-Week10/week10-1.png)
<p align="center"><i>Figure 1: Comprehensive Runtime Architecture for the Serverless Intelligent Document Processing system.</i></p>

