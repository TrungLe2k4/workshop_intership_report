---
title: "AWS First Cloud AI Journey Community Day"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


## Event Objectives

The AWS First Cloud AI Journey Community Day was organized to introduce participants to the latest advancements in Artificial Intelligence and AWS Cloud technologies. The event focused on three primary goals:

- Expanding participants' understanding of Generative AI, Large Language Models (LLMs), and Multi-Agent systems.
- Introducing AWS solutions for cloud security, infrastructure optimization, and cost management.
- Sharing practical experiences from industry experts about software development, cloud engineering, and product innovation.

---

## Summary of the Event

### 1. Enterprise Multi-Agent Systems for Startup Credit Assessment

**Speaker:** Vy Lam – Senior Business Systems Analyst, VPBank

The speaker explained the limitations of traditional credit scoring methods when evaluating startup companies. Since startups usually have limited financial history, conventional assessment models often fail to produce reliable results.

To solve this issue, a Multi-Agent architecture was introduced. Instead of relying on a single AI model, several specialized agents work together, each responsible for financial analysis, market research, team evaluation, risk assessment, and compliance checking.

This collaborative approach improves decision quality while reducing processing time and operational costs.

---

### 2. Understanding the Non-Deterministic Nature of LLMs

**Speaker:** Duc Dao – Solution Architect, Cloud Kinetics

This session focused on why Large Language Models cannot always generate identical outputs.

Although many developers believe that setting the Temperature parameter to zero guarantees consistent responses, small numerical differences caused by GPU floating-point operations may still lead to different predictions.

Rather than attempting to eliminate randomness completely, the speaker recommended using structured JSON outputs with a low temperature setting (around 0.1) to improve stability while maintaining flexibility.

---

### 3. Building UTMorpho During Lotus Hacks 2026

**Speaker:** Team VIB

The VIB team shared their experience of creating UTMorpho, a Sketch-to-App application powered by Claude Vision during a 36-hour hackathon.

Throughout the competition, the team faced several challenges, including API token limitations, uncontrolled feature expansion, and AI-generated code that introduced unexpected software bugs.

Their experience demonstrated that successful projects depend on strong teamwork, clear communication, and prioritizing core functionality before implementing additional features.

---

### 4. Optimizing Cloud Infrastructure with Amazon CloudFront

**Speaker:** Nguyen Tuan Thinh – DevOps Engineer

The presentation introduced Amazon CloudFront as an effective solution for improving application performance and security.

CloudFront distributes content through hundreds of edge locations worldwide, helping reduce latency while protecting applications from DDoS attacks through AWS Shield and AWS WAF.

The speaker also recommended using Origin Access Control (OAC), Mutual TLS (mTLS), and Lambda@Edge to strengthen infrastructure security and improve edge computing capabilities.

---

### 5. The Importance of Context in AI Systems

**Speaker:** Tinh Truong – Platform Engineer, GoTymeX

According to the speaker, poor AI responses are often caused by low-quality context instead of weak AI models.

Providing excessive or irrelevant information increases token consumption while reducing response accuracy. Well-designed AI systems should define clear objectives, strict constraints, and carefully selected contextual information.

The presentation also highlighted the value of long-term contextual memory for building more intelligent and personalized AI applications.

---

### 6. Improving Productivity with Amazon Q

**Speaker:** Pham Ng Hai Anh – G-AsiaPacific Vietnam, AWS Community Builder

The final session demonstrated how Amazon Q can automate routine business tasks such as generating meeting minutes, writing follow-up emails, and scheduling activities.

Amazon Q also supports integration with multiple enterprise data sources while maintaining strict access control and security policies. The speaker further introduced AI-powered security auditing as a promising direction for future cloud environments.

---

## Personal Reflection

Participating in this event helped me better understand how AI and cloud technologies are applied in real-world systems.
Several ideas can be directly applied to my own projects.
1. **First**, I will use structured JSON responses together with retry mechanisms instead of relying only on a Temperature value of zero. This approach improves reliability when integrating LLMs into backend services.
2. **Second**, I intend to redesign cloud infrastructure by using CloudFront and Origin Access Control to better protect backend resources from unauthorized access.
3. **Third**, I learned the importance of providing only relevant contextual information to AI models, which can reduce computational cost while improving prediction accuracy.
4. **Finally**, the product development experience shared by Team VIB reminded me that delivering a stable minimum viable product should always come before adding extra features.

> **Conclusion:**  
> This event provided valuable insights into AI engineering, cloud infrastructure, and modern software development practices. It encouraged me to think beyond programming and focus more on designing secure, scalable, and reliable cloud-based AI systems.

## Event Photos

![](/images/4-EventParticipated/4.1-Event1/event-1.png)