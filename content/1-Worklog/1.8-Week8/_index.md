---
title: "Week 8: Cloud Migration Workflow & Disaster Recovery"
date: 2026-06-05
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:
* Master the "Lift-and-Shift" migration strategy for moving physical servers to the AWS cloud.
* Execute VM Import/Export workflows using AWS CLI and Amazon S3.
* Verify Disaster Recovery (DR) readiness through Test Restore procedures.
* Secure virtual machine disk images (VM Images) against unauthorized access during migration.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Learn Cloud Migration Strategies:<br>&emsp; + The 6 R's of migration (Rehost, Replatform, Refactor...).<br>&emsp; + Introduction to AWS Application Migration Service (MGN). | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - **VM Import/Export Theory:**<br>&emsp; + Understand the workflow of packaging on-premises VMs (OVA/VMDK).<br>&emsp; + Requirements for S3 bucket staging and IAM Service Roles (`vmimport`). | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - **Migration Practice (Lab 14 - Part 1):**<br>&emsp; + Securely upload an exported VM disk image to Amazon S3.<br>&emsp; + Configure strict Access Control Lists (ACLs) to protect the image file. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **Migration Practice (Lab 14 - Part 2):**<br>&emsp; + Use AWS CLI to initiate the `import-image` task.<br>&emsp; + Monitor the conversion process and successfully launch an EC2 instance from the newly generated AMI. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - **Disaster Recovery Testing (Lab 13 Extension):**<br>&emsp; + Execute a Test Restore job from an existing Backup Vault.<br>&emsp; + Validate data integrity post-restoration to ensure RTO/RPO commitments. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Successfully actualized a "Lift-and-Shift" cloud migration by converting a local virtual machine image into a fully functional AWS AMI.
* Demonstrated a cybersecurity-first migration approach by strictly enforcing S3 ACLs, ensuring highly sensitive OS disk files were not exposed during the transfer.
* Validated the organization's Disaster Recovery plan by successfully performing a Test Restore, guaranteeing that backups are not only taken but are fully recoverable.

---
