---
title: "Week 9: Virtual Private Cloud & Defense-in-Depth Network Security"
date: 2026-06-12
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:
* Design and build a custom Amazon VPC (Virtual Private Cloud) architecture from scratch.
* Master IP addressing (CIDR Blocks) and network segmentation (Public/Private Subnets).
* Implement Defense-in-Depth network security using stateless NACLs and stateful Security Groups.
* Establish secure outbound internet access via NAT Gateway and inter-VPC communication via VPC Peering.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **Monday**<br>(Day 1) | - Learn Amazon VPC architecture:<br>&emsp; + CIDR blocks and IP planning.<br>&emsp; + VPC, Subnets, and Internet Gateways (IGW). | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Tuesday**<br>(Day 2) | - **VPC Foundation Practice:**<br>&emsp; + Create a custom VPC.<br>&emsp; + Divide the VPC into 1 Public Subnet and 1 Private Subnet.<br>&emsp; + Attach an IGW and configure the Public Route Table (`0.0.0.0/0`). | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Wednesday**<br>(Day 3) | - Implement NAT and Routing:<br>&emsp; + Deploy a NAT Gateway in the Public Subnet.<br>&emsp; + Update the Private Route Table to route outbound traffic through the NAT Gateway for secure patching. | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thursday**<br>(Day 4) | - **Defense-in-Depth Security Setup:**<br>&emsp; + Configure Network Access Control Lists (NACL) at the Subnet tier (Stateless filtering).<br>&emsp; + Interlock NACLs with Instance-tier Security Groups (Stateful) to block malicious IP ranges natively. | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Friday**<br>(Day 5) | - **VPC Peering & Clean Up:**<br>&emsp; + Establish a VPC Peering connection to route traffic securely between two independent VPCs using the AWS backbone.<br>&emsp; + Strictly follow the resource teardown sequence (EC2 -> NAT -> IGW -> VPC) to avoid billing leaks. | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Achievements:
* Successfully architected a custom enterprise-grade network environment entirely isolated from standard default settings.
* Internalized the critical cybersecurity principle of Network Isolation: ensuring sensitive backend resources (e.g., databases) are strictly placed in Private Subnets with one-way internet access via NAT Gateways.
* Constructed a robust Defense-in-Depth shield by layering NACLs (to drop bad IPs at the border) and Security Groups (to filter application ports at the instance level).
* Safely connected disparate cloud networks using VPC Peering, avoiding exposure to the public internet.

---

<!-- 
Image requirements for Week 9:
1. week9-1.png: Screenshot of the VPC Resource Map showing the topology of VPC, Subnets, Route Tables, and IGW/NAT.
2. week9-2.png: Screenshot of a configured Network Access Control List (NACL) showing custom Inbound/Outbound Rules with rule numbers.
3. week9-3.png: Screenshot of the VPC Peering Connections dashboard showing an "Active" peering connection.
-->

![VPC Resource Map](/workshop_intership_report/images/1-Worklog/1.9-Week9/week9-1.png)
<p align="center"><i>Figure 1: Visualizing the custom Amazon VPC topology, detailing the strict segregation of Public and Private Subnets.</i></p>

![Defense-in-Depth NACL](/workshop_intership_report/images/1-Worklog/1.9-Week9/week9-2.png)
<p align="center"><i>Figure 2: Configuring stateless Network Access Control Lists (NACL) to preemptively filter malicious traffic at the subnet perimeter.</i></p>

![VPC Peering Connection](/workshop_intership_report/images/1-Worklog/1.9-Week9/week9-3.png)
<p align="center"><i>Figure 3: Establishing a secure, private network bridge between independent VPCs via VPC Peering.</i></p>