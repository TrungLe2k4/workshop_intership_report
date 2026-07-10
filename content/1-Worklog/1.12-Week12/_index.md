---
title: "Week 12: ReactJS Frontend, System Integration & Go-Live"
date: 2026-07-03
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:
* Finalize the ReactJS (Vite + Tailwind CSS) client application and synchronize it seamlessly with the Serverless API Gateway.
* Enforce secure IAM identity verification through Amazon Cognito (Challenge Password & JWT Token authorization).
* Implement advanced UI/UX components (Side-by-side verification, Progress bar budgets).
* Execute Integration Testing, finalize the Resource Cleanup Protocol, and Go-Live utilizing S3 Static Hosting and CloudFront.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - **Cognito Identity & Authentication:**<br>&emsp; + Configure `idp-react-app` User Pool, disabling Self-registration to prevent rogue signups.<br>&emsp; + Code `Login.jsx` to handle Cognito OTP, Challenge Password (force password change on first login), and JWT token management. | 06/07/2026 | 06/07/2026 | React/Vite / SDK |
| **Tuesday**<br>(Day 2) | - **API Integration & Data Visualization:**<br>&emsp; + Integrate `CognitoUserPoolAuthorizer` into API Gateway GET methods (leaving OPTIONS unprotected for CORS).<br>&emsp; + Build `Dashboard.jsx` using `recharts` for financial analysis and a smart budget Progress Bar (Green/Yellow/Red alerts). | 07/07/2026 | 07/07/2026 | React / Recharts |
| **Wednesday**<br>(Day 3) | - **Advanced UX (Side-by-side AI Verification):**<br>&emsp; + Develop `InvoiceEditModal.jsx`.<br>&emsp; + Design a side-by-side view (Left: Raw Document Image/PDF, Right: Textract Extracted Form) enabling human-in-the-loop Data Quality Control. | 08/07/2026 | 08/07/2026 | React / Tailwind |
| **Thursday**<br>(Day 4) | - **Integration Testing & Cleanup Protocol:**<br>&emsp; + Execute 4 core test cases: Login flow, Presigned URL upload, Filters, and Budget UI Alerts.<br>&emsp; + Author a comprehensive Resource Cleanup Protocol to prevent post-project billing leaks. | 09/07/2026 | 09/07/2026 | Testing Doc |
| **Friday**<br>(Day 5) | - **Production Go-Live:**<br>&emsp; + Run `npm run build` to optimize the static assets.<br>&emsp; + Deploy the `dist/` artifacts to Amazon S3 (`idp-frontend-bucket-1`).<br>&emsp; + Provision an Amazon CloudFront distribution pointing to the S3 origin to serve the application globally over HTTPS. | 10/07/2026 | 10/07/2026 | AWS Console |

### Achievements:
* Delivered a highly polished, commercial-grade Single Page Application (SPA) natively integrated with AWS backend services.
* Hardened application access via Amazon Cognito, protecting against Account Enumeration attacks by mandating Admin-provisioned accounts and forced initial password resets.
* Innovated the AI verification process with a Side-by-side UX, drastically reducing data entry errors and keeping human oversight in the AI loop.
* Successfully launched the IDPCloud system into Production (Go-Live) using a globally distributed, highly secure CloudFront CDN architecture.

---

![Cognito Authentication UI](/images/1-Worklog/1.12-Week12/week12-1.png)
<p align="center"><i>Figure 1: Secure authentication flow handling Amazon Cognito's Challenge Password requirements.</i></p>

![IDP Dashboard](/images/1-Worklog/1.12-Week12/week12-2.png)
<p align="center"><i>Figure 2: Financial Dashboard featuring dynamic data visualization and real-time budget threshold alerts.</i></p>

![Side-by-side UX](/images/1-Worklog/1.12-Week12/week12-3.png)
<p align="center"><i>Figure 3: Side-by-side Data Quality Control interface, allowing human validation against Textract AI output.</i></p>