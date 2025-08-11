# Domain 1 — **Cloud Concepts** (CLF-C02) — Lesson 1

Alright — we’re kicking off with **Cloud Concepts**. I’ll teach the essentials you *must* know for the exam and for real life, then you’ll get an exam-style quiz (real AWS-style questions + clear explanations). No fluff. Big points first:

---

How to use this page
- Read each question and choose your answer first.
- Click “Reveal answer and explanation” to check yourself.
- For multi-select, choose exactly the number requested.

CLF-C02 Exam Domains & Weightings (from AWS Exam Guide)
- Domain 1: Cloud Concepts — 24%
- Domain 2: Security & Compliance — 30%
- Domain 3: Cloud Technology & Services — 34%
- Domain 4: Billing, Pricing & Support — 12%

---

**What AWS expects you to know in Domain 1 (short):**

* Benefits/value of the AWS Cloud.
* Core design principles for cloud architecture.
* Migration benefits and common strategies.
* Cloud economics fundamentals (TCO, CapEx vs OpEx, pricing models).
  (These task statements come from the official CLF-C02 exam guide.) ([AWS Static][1])

---

## 1.1 — Benefits of the AWS Cloud (what to *actually* say on the exam)

Core benefits — short list you must memorize and be able to explain with examples:

* **On-demand elasticity & scalability** — spin up/down compute and storage quickly to match load (no big upfront hardware buy). Example: scale web servers during a sale. ([AWS Static][1])
* **Pay-for-what-you-use (OPEX)** — you pay for the capacity you actually use; no capital outlay for idle servers. ([AWS Static][1])
* **Global footprint / reach** — AWS has regions and edge locations so you can place resources near customers for lower latency. ([AWS Static][1])
* **Security & compliance tooling** — broad set of managed controls, logging, identity, encryption tools (but remember: shared responsibility model). ([AWS Static][1])
* **Faster time to market & innovation** — managed services (databases, ML, analytics) let teams ship features faster.

**Exam tip:** When a question asks “which of these is a benefit of cloud?” pick answers that map to elasticity, cost model, global availability, speed of provisioning, or managed services. Avoid distractors like “you own the physical hardware” or “no need for any security” (those are wrong).

---

## 1.2 — Cloud design principles (practical, exam-ready)

You don’t need the full SAA deep dive — just these principles:

* **Design for failure** — assume components will fail; design recovery and redundancy.
* **Loose coupling** — services/components should be independent (use queues, events).
* **Scalability & elasticity** — use autoscaling, managed services, and stateless designs.
* **Security first** — least privilege, use IAM, encrypt data-in-transit & at-rest.
* **Optimize for operations & cost** — monitor, right-size resources, use managed services to reduce ops burden.

**Exam tip:** Questions will often test which architecture choice supports scalability, reliability, or cost reduction — match the principle to outcomes.

---

## 1.3 — Migration benefits & strategies (short, practical)

Why migrate to AWS? common exam answers:

* Reduce infrastructure cost and ops overhead.
* Improve agility and time to market.
* Improve global reach and resilience.

Common migration strategies (the “6 R’s” simplified):

* **Rehost** (lift-and-shift) — quick; minimal code changes.
* **Replatform** — small changes to take advantage of managed services.
* **Refactor/Re-architect** — full modernization for cloud-native benefits.
* **Retire** — shut down unused assets.
* **Retain** — keep some on-prem for now.
* **Replace** — move to SaaS.

**Exam tip:** If a question mentions “fastest path with minimal changes,” the answer often is **Rehost**. If it mentions “use managed service and remove ops burden,” the answer leans toward **Replatform** or **Replace**.

---

## 1.4 — Cloud economics (what actually matters)

* **CapEx → OpEx**: You move from buying hardware to paying for usage — this affects cash flow and accounting.
* **TCO (Total Cost of Ownership)**: Compare in-house vs cloud not only on raw compute but on personnel, ops, power, cooling, support, and flexibility.
* **Pricing models**: On-Demand, Reserved (savings for commitment), Spot (huge discounts for interruptible workloads).
* **Cost optimization**: Rightsizing, Auto Scaling, reserved instances/savings plans, deleting idle resources, and using serverless where appropriate.

**Exam tip:** If the question asks which pricing option is best for a non-critical batch job that can be interrupted — **Spot** is usually correct.

---

## Quick references / sources

* Official AWS Certified Cloud Practitioner exam guide and practice materials (this is the canonical source for exam scope and sample questions). ([AWS Static][1])

---

Q1. Which of the following is a primary benefit of using the AWS Cloud for a company with customers in multiple countries?
- [ ] A. The company operates physical data centers in every country.
- [ ] B. The company can reduce latency by deploying resources to AWS Regions and edge locations.
- [ ] C. The company no longer needs to manage data sovereignty.
- [ ] D. The company will no longer incur any operational costs.

<details><summary>Reveal answer and explanation</summary>
Correct: B — Regions and edge locations reduce latency by placing resources close to users.
</details>

Q2. A company wants to move a workload to AWS immediately with minimal code changes. Which migration strategy best fits this requirement?
- [ ] A. Refactor
- [ ] B. Rehost (lift-and-shift)
- [ ] C. Replace with SaaS
- [ ] D. Retire

<details><summary>Reveal answer and explanation</summary>
Correct: B — Rehost is the fastest with minimal code changes.
</details>

Q3 (Multi-select — choose TWO). Which two are core characteristics of cloud computing?
- [ ] A. On-demand self-service
- [ ] B. Fixed monthly pricing for all resources
- [ ] C. Broad network access
- [ ] D. Managing physical security of AWS data centers

<details><summary>Reveal answer and explanation</summary>
Correct: A and C — On-demand self-service and broad network access are core characteristics.
</details>

Q4. Which pricing option provides the lowest cost for fault-tolerant, non-time-sensitive batch jobs that can be interrupted?
- [ ] A. On-Demand Instances
- [ ] B. Reserved Instances
- [ ] C. Spot Instances
- [ ] D. Dedicated Hosts

<details><summary>Reveal answer and explanation</summary>
Correct: C — Spot Instances offer steep discounts for interruptible workloads.
</details>

Q5. Which of the following best defines the “design for failure” principle?
- [ ] A. Assume components will fail and design systems to recover and continue to operate.
- [ ] B. Ensure no component ever fails by using identical hardware.
- [ ] C. Avoid backups to minimize costs.
- [ ] D. Use a single database server for simplicity.

<details><summary>Reveal answer and explanation</summary>
Correct: A — Build redundancy, retries, and failover assuming failures happen.
</details>

Q6. Which of these is an economic advantage of moving from CapEx to OpEx with AWS?
- [ ] A. You must buy more hardware upfront.
- [ ] B. Predictable large capital expenditure.
- [ ] C. Pay only for what you use, converting CapEx into OpEx.
- [ ] D. You will stop paying for IT staff.

<details><summary>Reveal answer and explanation</summary>
Correct: C — Pay-as-you-go improves cash flow and flexibility.
</details>

Q7 (Scenario). A company needs to ensure that customer data is encrypted at rest and in transit and wants to minimize operational overhead. Which AWS approach is most appropriate?
- [ ] A. Store data in plain text on EC2 instance and manage encryption yourself.
- [ ] B. Use managed AWS services that provide encryption at rest and TLS in transit (e.g., S3 with default encryption enabled).
- [ ] C. Do nothing — AWS encrypts everything automatically without configuration.
- [ ] D. Only encrypt data in transit and ignore encryption at rest.

<details><summary>Reveal answer and explanation</summary>
Correct: B — Managed services with built-in encryption minimize operational burden.
</details>

Q8. Which AWS cloud value proposition helps customers avoid large upfront capital expenses?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Global reach
- [ ] D. Agility

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go shifts CapEx to OpEx.
</details>

Q9. A company has unpredictable traffic spikes. Which AWS cloud characteristic helps them automatically match capacity to demand?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Fault tolerance
- [ ] D. Cost optimization

<details><summary>Reveal answer and explanation</summary>
Correct: B — Elasticity scales up/down with demand.
</details>

Q10. Which is an AWS global service?
- [ ] A. Amazon EC2
- [ ] B. Amazon S3
- [ ] C. AWS IAM
- [ ] D. Amazon RDS

<details><summary>Reveal answer and explanation</summary>
Correct: C — IAM is global; EC2/S3/RDS are regional.
</details>

Q11. Which of the following is not a benefit of cloud computing?
- [ ] A. Trade capital expense for variable expense
- [ ] B. Increase speed and agility
- [ ] C. Maintain physical security of on-premises hardware
- [ ] D. Stop guessing capacity

<details><summary>Reveal answer and explanation</summary>
Correct: C — On-premises physical security is not a cloud benefit.
</details>

Q12. Which pricing model lets you pay a reduced rate in exchange for committing to use AWS services for a 1–3 year term?
- [ ] A. On-Demand
- [ ] B. Reserved Instances
- [ ] C. Spot Instances
- [ ] D. Free Tier

<details><summary>Reveal answer and explanation</summary>
Correct: B — RIs (and Savings Plans) discount for commitment.
</details>

Q13. Which AWS Well-Architected Framework pillar focuses on using IT and computing resources efficiently?
- [ ] A. Reliability
- [ ] B. Performance efficiency
- [ ] C. Cost optimization
- [ ] D. Operational excellence

<details><summary>Reveal answer and explanation</summary>
Correct: B — Performance efficiency emphasizes efficient resource use.
</details>

Q14. Which statement best describes the AWS Shared Responsibility Model?
- [ ] A. AWS is responsible for security “of” the cloud; customers are responsible for security “in” the cloud.
- [ ] B. AWS is responsible for all security measures.
- [ ] C. Customers are responsible for all security measures.
- [ ] D. AWS manages data classification for customers.

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS secures the cloud infrastructure; customers secure what they run in it.
</details>

Q15. Which AWS service enables you to run code without provisioning or managing servers?
- [ ] A. Amazon EC2
- [ ] B. AWS Lambda
- [ ] C. Amazon ECS
- [ ] D. Amazon Lightsail

<details><summary>Reveal answer and explanation</summary>
Correct: B — Lambda is serverless compute.
</details>

Q16. Which AWS tool helps estimate the cost of running your applications on AWS?
- [ ] A. AWS Cost Explorer
- [ ] B. AWS Pricing Calculator
- [ ] C. AWS Budgets
- [ ] D. AWS Trusted Advisor

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pricing Calculator estimates future costs; Cost Explorer analyzes historical spend.
</details>

Q17. Which AWS service allows you to connect your on-premises network to AWS using a dedicated network link?
- [ ] A. Amazon CloudFront
- [ ] B. AWS Direct Connect
- [ ] C. AWS VPN
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: B — Direct Connect provides a private, dedicated link.
</details>

Q18. Which benefit of cloud computing allows users to experiment and innovate quickly?
- [ ] A. Elasticity
- [ ] B. Agility
- [ ] C. Security
- [ ] D. Global reach

<details><summary>Reveal answer and explanation</summary>
Correct: B — Agility from rapid provisioning accelerates experimentation.
</details>

Q19. Which Amazon S3 storage class is ideal for data that is rarely accessed but must be retrieved within milliseconds when needed?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier Deep Archive
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: B — Standard-IA: infrequent access with ms retrieval.
</details>

Q20. Which type of cloud deployment model allows an organization to use both on-premises infrastructure and AWS cloud services?
- [ ] A. Public cloud
- [ ] B. Private cloud
- [ ] C. Hybrid cloud
- [ ] D. Multi-cloud

<details><summary>Reveal answer and explanation</summary>
Correct: C — Hybrid combines on-prem and public cloud.
</details>

Q21. Which AWS service provides a content delivery network to distribute content globally with low latency?
- [ ] A. Amazon CloudFront
- [ ] B. AWS Global Accelerator
- [ ] C. Amazon Route 53
- [ ] D. Amazon S3

<details><summary>Reveal answer and explanation</summary>
Correct: A — CloudFront is the CDN.
</details>

Q22. Which AWS service helps you automate the deployment of infrastructure using templates?
- [ ] A. AWS CloudFormation
- [ ] B. AWS OpsWorks
- [ ] C. AWS CodePipeline
- [ ] D. AWS Elastic Beanstalk

<details><summary>Reveal answer and explanation</summary>
Correct: A — CloudFormation is infrastructure as code via templates.
</details>

Q23. What is the main purpose of AWS Availability Zones?
- [ ] A. To cache data closer to users
- [ ] B. To provide low-latency global networking
- [ ] C. To provide isolated locations within a Region for fault tolerance
- [ ] D. To secure AWS accounts

<details><summary>Reveal answer and explanation</summary>
Correct: C — AZs are isolated for resilience within a Region.
</details>

Q24. Which AWS Support plan includes access to a Technical Account Manager (TAM)?
- [ ] A. Basic
- [ ] B. Developer
- [ ] C. Business
- [ ] D. Enterprise

<details><summary>Reveal answer and explanation</summary>
Correct: D — Enterprise Support provides a TAM.
</details>

Q25. Which AWS service is designed to run containerized applications without managing servers or clusters?
- [ ] A. Amazon ECS on EC2
- [ ] B. Amazon ECS with AWS Fargate
- [ ] C. AWS Lambda
- [ ] D. AWS Batch

<details><summary>Reveal answer and explanation</summary>
Correct: B — Fargate runs containers without managing instances.
</details>

Q26. Which AWS service provides visual tools to help you design your AWS architecture?
- [ ] A. AWS CloudFormation
- [ ] B. AWS Architecture Center
- [ ] C. AWS Well-Architected Tool
- [ ] D. AWS Management Console

<details><summary>Reveal answer and explanation</summary>
Correct: B — Architecture Center provides reference architectures and diagrams.
</details>

Q27. Which term refers to the AWS feature of providing resources across multiple Regions and Availability Zones for resilience?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Scalability
- [ ] D. Fault tolerance

<details><summary>Reveal answer and explanation</summary>
Correct: A — Multi-AZ/Region designs improve availability.
</details>

Q28. A video company stores raw files in AWS and accesses them rarely after the first month. Which S3 storage class is most cost-effective after the first month?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: C — Glacier (Flexible Retrieval) suits archival data accessed rarely.
</details>

Q29. Which AWS service should they use to deliver final videos globally with low latency?
- [ ] A. Amazon Route 53
- [ ] B. Amazon CloudFront
- [ ] C. AWS Direct Connect
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront is the CDN for global media delivery.
</details>

Q30. Which cloud benefit are they using by avoiding upfront hardware purchases?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Fault tolerance
- [ ] D. Scalability

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go avoids CapEx.
</details>

Q31. Your startup wants to host a machine learning inference API that must stay online 24/7 and scale automatically without you managing the underlying infrastructure. Which service fits best?
- [ ] A. Amazon EC2 Auto Scaling
- [ ] B. AWS Lambda
- [ ] C. AWS Elastic Beanstalk
- [ ] D. Amazon SageMaker Endpoints

<details><summary>Reveal answer and explanation</summary>
Correct: D — SageMaker Endpoints provide fully managed, autoscaling model hosting.
</details>

Q32. A media company stores massive archives in Amazon S3 but rarely accesses them. Retrieval within minutes is acceptable. Which storage class minimizes cost?
- [ ] A. S3 Standard-IA
- [ ] B. S3 One Zone-IA
- [ ] C. S3 Glacier Flexible Retrieval
- [ ] D. S3 Glacier Deep Archive

<details><summary>Reveal answer and explanation</summary>
Correct: C — Minute‑scale retrieval at low cost.
</details>

Q33. Under the Shared Responsibility Model, who is responsible for configuring MFA on the AWS account root user?
- [ ] A. AWS
- [ ] B. Customer
- [ ] C. AWS and Customer equally
- [ ] D. AWS Trusted Advisor

<details><summary>Reveal answer and explanation</summary>
Correct: B — Customers configure root MFA.
</details>

Q34. You’re designing a highly available web app running on EC2 in two AZs in one Region. Which service distributes incoming traffic?
- [ ] A. AWS Global Accelerator
- [ ] B. Amazon CloudFront
- [ ] C. Elastic Load Balancing
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: C — ALB/NLB.
</details>

Q35. Which AWS tool provides pre-built compliance reports (e.g., HIPAA)?
- [ ] A. AWS Artifact
- [ ] B. AWS Config
- [ ] C. AWS Inspector
- [ ] D. AWS CloudTrail

<details><summary>Reveal answer and explanation</summary>
Correct: A — Artifact.
</details>

Q36. Which service can send targeted push notifications based on user attributes?
- [ ] A. Amazon SNS
- [ ] B. Amazon Pinpoint
- [ ] C. Amazon SQS
- [ ] D. Amazon Connect

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pinpoint for campaigns/segments.
</details>

Q37. Dedicated private network connection from on‑prem to AWS?
- [ ] A. AWS VPN
- [ ] B. AWS Direct Connect
- [ ] C. VPC Peering
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — Direct Connect.
</details>

Q38. Run Kubernetes without managing control plane nodes?
- [ ] A. Amazon ECS
- [ ] B. Amazon EKS
- [ ] C. AWS Fargate
- [ ] D. Amazon Lightsail

<details><summary>Reveal answer and explanation</summary>
Correct: B — EKS manages the control plane.
</details>

Q39. Process real-time shipment tracking data and trigger alerts within seconds?
- [ ] A. Amazon Kinesis Data Streams
- [ ] B. Amazon SQS
- [ ] C. AWS Glue
- [ ] D. AWS Batch

<details><summary>Reveal answer and explanation</summary>
Correct: A — Kinesis Data Streams.
</details>

Q40. Create a logically isolated section of the AWS cloud to launch resources?
- [ ] A. AWS PrivateLink
- [ ] B. AWS Direct Connect
- [ ] C. Amazon VPC
- [ ] D. AWS Shield

<details><summary>Reveal answer and explanation</summary>
Correct: C — Amazon VPC.
</details>

Q41. Cache game assets at the edge and deliver globally over HTTPS?
- [ ] A. AWS Global Accelerator
- [ ] B. Amazon CloudFront
- [ ] C. AWS Wavelength
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront.
</details>

Q42. Program for early-stage startups offering credits and guidance?
- [ ] A. AWS Activate
- [ ] B. AWS Well-Architected Tool
- [ ] C. AWS IQ
- [ ] D. AWS Support Concierge

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS Activate.
</details>

Q43. Continuously monitor configurations and compliance against rules?
- [ ] A. AWS Config
- [ ] B. AWS CloudTrail
- [ ] C. AWS Trusted Advisor
- [ ] D. AWS Inspector

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS Config.
</details>

Q44. Run AWS infrastructure at a 5G network edge for ultra-low latency?
- [ ] A. AWS Local Zones
- [ ] B. AWS Wavelength
- [ ] C. AWS Outposts
- [ ] D. AWS Snowball Edge

<details><summary>Reveal answer and explanation</summary>
Correct: B — Wavelength.
</details>

Q45. Analyze large datasets in S3 with standard SQL without loading data?
- [ ] A. Amazon Redshift
- [ ] B. Amazon Athena
- [ ] C. AWS Glue
- [ ] D. Amazon EMR

<details><summary>Reveal answer and explanation</summary>
Correct: B — Athena.
</details>

Q46. Commit to consistent compute usage for a 1–3 year term for big discounts?
- [ ] A. On-Demand
- [ ] B. Reserved Instances
- [ ] C. Spot Instances
- [ ] D. Savings Plans

<details><summary>Reveal answer and explanation</summary>
Correct: D — Savings Plans for compute commitment.
</details>

Q47. Migrate on‑prem Java app to containers without rewriting code?
- [ ] A. AWS App2Container
- [ ] B. AWS Application Migration Service
- [ ] C. AWS CodeBuild
- [ ] D. AWS Elastic Beanstalk

<details><summary>Reveal answer and explanation</summary>
Correct: A — App2Container.
</details>

Q48. Detect unauthorized resource deployments using ML/anomaly detection?
- [ ] A. AWS Shield Advanced
- [ ] B. AWS GuardDuty
- [ ] C. AWS Inspector
- [ ] D. Amazon Detective

<details><summary>Reveal answer and explanation</summary>
Correct: B — GuardDuty.
</details>

Q49. Which support plan includes a TAM and 15‑minute response time for critical issues?
- [ ] A. Developer
- [ ] B. Business
- [ ] C. Enterprise On‑Ramp
- [ ] D. Enterprise

<details><summary>Reveal answer and explanation</summary>
Correct: D — Enterprise Support.
</details>

Q50. Which service enables satellite operators to control and downlink data directly into AWS?
- [ ] A. AWS Snowball Edge
- [ ] B. AWS Ground Station
- [ ] C. Amazon MSK
- [ ] D. AWS DataSync

<details><summary>Reveal answer and explanation</summary>
Correct: B — AWS Ground Station.
</details>

---

<details><summary>Master Answer Key (Q1–Q50)</summary>
1) B 2) B 3) A,C 4) C 5) A 6) C 7) B 8) B 9) B 10) C 11) C 12) B 13) B 14) A 15) B 16) B 17) B 18) B 19) B 20) C 21) A 22) A 23) C 24) D 25) B 26) B 27) A 28) C 29) B 30) B 31) D 32) C 33) B 34) C 35) A 36) B 37) B 38) B 39) A 40) C 41) B 42) A 43) A 44) B 45) B 46) D 47) A 48) B 49) D 50) B
</details>

---

Sample Question (Domain 1: Cloud Concepts)
Q: Which of the following channels shares a collection of offerings to help you achieve specific business outcomes related to enterprise cloud adoption through paid engagements in several specialty practice areas?

- [ ] A. AWS Enterprise Support
- [ ] B. Concierge Support
- [ ] C. AWS Professional Services
- [ ] D. AWS Technical Account Manager

<details><summary>Reveal answer and explanation</summary>
Correct: C — AWS Professional Services delivers guided, paid engagements (often using the AWS CAF) to accelerate adoption.
</details>

---

Domain 1: Cloud Concepts
20-question AWS CLF-C02 mock quiz + 1 mini case study scenario exactly in the style of AWS exam questions. Answers appear under each question.

Part A – 20 AWS Cloud Concepts Practice Questions

Q1. Which AWS cloud value proposition helps customers avoid large upfront capital expenses?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Global reach
- [ ] D. Agility

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go shifts CapEx to OpEx.
</details>

Q2. A company has unpredictable traffic spikes. Which AWS cloud characteristic helps them automatically match capacity to demand?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Fault tolerance
- [ ] D. Cost optimization

<details><summary>Reveal answer and explanation</summary>
Correct: B — Elasticity scales up/down with demand.
</details>

Q3. Which is an AWS global service?
- [ ] A. Amazon EC2
- [ ] B. Amazon S3
- [ ] C. AWS IAM
- [ ] D. Amazon RDS

<details><summary>Reveal answer and explanation</summary>
Correct: C — IAM is global; EC2/S3/RDS are regional.
</details>

Q4. Which of the following is not a benefit of cloud computing?
- [ ] A. Trade capital expense for variable expense
- [ ] B. Increase speed and agility
- [ ] C. Maintain physical security of on-premises hardware
- [ ] D. Stop guessing capacity

<details><summary>Reveal answer and explanation</summary>
Correct: C — On-premises physical security is not a cloud benefit.
</details>

Q5. Which pricing model lets you pay a reduced rate in exchange for committing to use AWS services for a 1–3 year term?
- [ ] A. On-Demand
- [ ] B. Reserved Instances
- [ ] C. Spot Instances
- [ ] D. Free Tier

<details><summary>Reveal answer and explanation</summary>
Correct: B — RIs (and Savings Plans) discount for commitment.
</details>

Q6. Which AWS Well-Architected Framework pillar focuses on using IT and computing resources efficiently?
- [ ] A. Reliability
- [ ] B. Performance efficiency
- [ ] C. Cost optimization
- [ ] D. Operational excellence

<details><summary>Reveal answer and explanation</summary>
Correct: B — Performance efficiency emphasizes efficient resource use.
</details>

Q7. Which statement best describes the AWS Shared Responsibility Model?
- [ ] A. AWS is responsible for security “of” the cloud; customers are responsible for security “in” the cloud.
- [ ] B. AWS is responsible for all security measures.
- [ ] C. Customers are responsible for all security measures.
- [ ] D. AWS manages data classification for customers.

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS secures the cloud infrastructure; customers secure what they run in it.
</details>

Q8. Which AWS service enables you to run code without provisioning or managing servers?
- [ ] A. Amazon EC2
- [ ] B. AWS Lambda
- [ ] C. Amazon ECS
- [ ] D. Amazon Lightsail

<details><summary>Reveal answer and explanation</summary>
Correct: B — Lambda is serverless compute.
</details>

Q9. Which AWS tool helps estimate the cost of running your applications on AWS?
- [ ] A. AWS Cost Explorer
- [ ] B. AWS Pricing Calculator
- [ ] C. AWS Budgets
- [ ] D. AWS Trusted Advisor

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pricing Calculator estimates future costs; Cost Explorer analyzes historical spend.
</details>

Q10. Which AWS service allows you to connect your on-premises network to AWS using a dedicated network link?
- [ ] A. Amazon CloudFront
- [ ] B. AWS Direct Connect
- [ ] C. AWS VPN
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: B — Direct Connect provides a private, dedicated link.
</details>

Q11. Which benefit of cloud computing allows users to experiment and innovate quickly?
- [ ] A. Elasticity
- [ ] B. Agility
- [ ] C. Security
- [ ] D. Global reach

<details><summary>Reveal answer and explanation</summary>
Correct: B — Agility from rapid provisioning accelerates experimentation.
</details>

Q12. Which Amazon S3 storage class is ideal for data that is rarely accessed but must be retrieved within milliseconds when needed?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier Deep Archive
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: B — Standard-IA: infrequent access with ms retrieval; One Zone-IA lacks multi-AZ durability.
</details>

Q13. Which type of cloud deployment model allows an organization to use both on-premises infrastructure and AWS cloud services?
- [ ] A. Public cloud
- [ ] B. Private cloud
- [ ] C. Hybrid cloud
- [ ] D. Multi-cloud

<details><summary>Reveal answer and explanation</summary>
Correct: C — Hybrid combines on-prem and public cloud.
</details>

Q14. Which AWS service provides a content delivery network to distribute content globally with low latency?
- [ ] A. Amazon CloudFront
- [ ] B. AWS Global Accelerator
- [ ] C. Amazon Route 53
- [ ] D. Amazon S3

<details><summary>Reveal answer and explanation</summary>
Correct: A — CloudFront is the CDN. Global Accelerator optimizes TCP/UDP routing.
</details>

Q15. Which AWS service helps you automate the deployment of infrastructure using templates?
- [ ] A. AWS CloudFormation
- [ ] B. AWS OpsWorks
- [ ] C. AWS CodePipeline
- [ ] D. AWS Elastic Beanstalk

<details><summary>Reveal answer and explanation</summary>
Correct: A — CloudFormation is infrastructure as code via templates.
</details>

Q16. What is the main purpose of AWS Availability Zones?
- [ ] A. To cache data closer to users
- [ ] B. To provide low-latency global networking
- [ ] C. To provide isolated locations within a Region for fault tolerance
- [ ] D. To secure AWS accounts

<details><summary>Reveal answer and explanation</summary>
Correct: C — AZs are isolated for resilience within a Region.
</details>

Q17. Which AWS Support plan includes access to a Technical Account Manager (TAM)?
- [ ] A. Basic
- [ ] B. Developer
- [ ] C. Business
- [ ] D. Enterprise

<details><summary>Reveal answer and explanation</summary>
Correct: D — Enterprise Support provides a TAM.
</details>

Q18. Which AWS service is designed to run containerized applications without managing servers or clusters?
- [ ] A. Amazon ECS on EC2
- [ ] B. Amazon ECS with AWS Fargate
- [ ] C. AWS Lambda
- [ ] D. AWS Batch

<details><summary>Reveal answer and explanation</summary>
Correct: B — Fargate runs containers without managing instances.
</details>

Q19. Which AWS service provides visual tools to help you design your AWS architecture?
- [ ] A. AWS CloudFormation
- [ ] B. AWS Architecture Center
- [ ] C. AWS Well-Architected Tool
- [ ] D. AWS Management Console

<details><summary>Reveal answer and explanation</summary>
Correct: B — Architecture Center provides reference architectures and diagrams.
</details>

Q20. Which term refers to the AWS feature of providing resources across multiple Regions and Availability Zones for resilience?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Scalability
- [ ] D. Fault tolerance

<details><summary>Reveal answer and explanation</summary>
Correct: A — Multi-AZ/Region designs improve availability.
</details>

Q21. A video company stores raw files in AWS and accesses them rarely after the first month. Which S3 storage class is most cost-effective after the first month?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: C — Glacier (Flexible Retrieval) suits archival data accessed rarely.
</details>

Q22. Which AWS service should they use to deliver final videos globally with low latency?
- [ ] A. Amazon Route 53
- [ ] B. Amazon CloudFront
- [ ] C. AWS Direct Connect
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront is the CDN for global media delivery.
</details>

Q23. Which cloud benefit are they using by avoiding upfront hardware purchases?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Fault tolerance
- [ ] D. Scalability

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go avoids CapEx.
</details>

Q24. Your startup wants to host a machine learning inference API that must stay online 24/7 and scale automatically without you managing the underlying infrastructure. Which service fits best?
- [ ] A. Amazon EC2 Auto Scaling
- [ ] B. AWS Lambda
- [ ] C. AWS Elastic Beanstalk
- [ ] D. Amazon SageMaker Endpoints

<details><summary>Reveal answer and explanation</summary>
Correct: D — SageMaker Endpoints provide fully managed, autoscaling model hosting.
</details>

Q25. A media company stores massive archives in Amazon S3 but rarely accesses them. Retrieval within minutes is acceptable. Which storage class minimizes cost?
- [ ] A. S3 Standard-IA
- [ ] B. S3 One Zone-IA
- [ ] C. S3 Glacier Flexible Retrieval
- [ ] D. S3 Glacier Deep Archive

<details><summary>Reveal answer and explanation</summary>
Correct: C — Minute‑scale retrieval at low cost.
</details>

Q26. Which AWS service provides visual tools to help you design your AWS architecture?
- [ ] A. AWS CloudFormation
- [ ] B. AWS Architecture Center
- [ ] C. AWS Well-Architected Tool
- [ ] D. AWS Management Console

<details><summary>Reveal answer and explanation</summary>
Correct: B — Architecture Center provides reference architectures and diagrams.
</details>

Q27. Which term refers to the AWS feature of providing resources across multiple Regions and Availability Zones for resilience?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Scalability
- [ ] D. Fault tolerance

<details><summary>Reveal answer and explanation</summary>
Correct: A — Multi-AZ/Region designs improve availability.
</details>

Q28. A video company stores raw files in AWS and accesses them rarely after the first month. Which S3 storage class is most cost-effective after the first month?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: C — Glacier (Flexible Retrieval) suits archival data accessed rarely.
</details>

Q29. Which AWS service should they use to deliver final videos globally with low latency?
- [ ] A. Amazon Route 53
- [ ] B. Amazon CloudFront
- [ ] C. AWS Direct Connect
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront is the CDN for global media delivery.
</details>

Q30. Which cloud benefit are they using by avoiding upfront hardware purchases?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Fault tolerance
- [ ] D. Scalability

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go avoids CapEx.
</details>

Q31. Your startup wants to host a machine learning inference API that must stay online 24/7 and scale automatically without you managing the underlying infrastructure. Which service fits best?
- [ ] A. Amazon EC2 Auto Scaling
- [ ] B. AWS Lambda
- [ ] C. AWS Elastic Beanstalk
- [ ] D. Amazon SageMaker Endpoints

<details><summary>Reveal answer and explanation</summary>
Correct: D — SageMaker Endpoints provide fully managed, autoscaling model hosting.
</details>

Q32. A media company stores massive archives in Amazon S3 but rarely accesses them. Retrieval within minutes is acceptable. Which storage class minimizes cost?
- [ ] A. S3 Standard-IA
- [ ] B. S3 One Zone-IA
- [ ] C. S3 Glacier Flexible Retrieval
- [ ] D. S3 Glacier Deep Archive

<details><summary>Reveal answer and explanation</summary>
Correct: C — Minute‑scale retrieval at low cost.
</details>

Q33. Under the Shared Responsibility Model, who is responsible for configuring MFA on the AWS account root user?
- [ ] A. AWS
- [ ] B. Customer
- [ ] C. AWS and Customer equally
- [ ] D. AWS Trusted Advisor

<details><summary>Reveal answer and explanation</summary>
Correct: B — Customers configure root MFA.
</details>

Q34. You’re designing a highly available web app running on EC2 in two AZs in one Region. Which service distributes incoming traffic?
- [ ] A. AWS Global Accelerator
- [ ] B. Amazon CloudFront
- [ ] C. Elastic Load Balancing
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: C — ALB/NLB.
</details>

Q35. Which AWS tool provides pre-built compliance reports (e.g., HIPAA)?
- [ ] A. AWS Artifact
- [ ] B. AWS Config
- [ ] C. AWS Inspector
- [ ] D. AWS CloudTrail

<details><summary>Reveal answer and explanation</summary>
Correct: A — Artifact.
</details>

Q36. Which service can send targeted push notifications based on user attributes?
- [ ] A. Amazon SNS
- [ ] B. Amazon Pinpoint
- [ ] C. Amazon SQS
- [ ] D. Amazon Connect

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pinpoint for campaigns/segments.
</details>

Q37. Dedicated private network connection from on‑prem to AWS?
- [ ] A. AWS VPN
- [ ] B. AWS Direct Connect
- [ ] C. VPC Peering
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — Direct Connect.
</details>

Q38. Run Kubernetes without managing control plane nodes?
- [ ] A. Amazon ECS
- [ ] B. Amazon EKS
- [ ] C. AWS Fargate
- [ ] D. Amazon Lightsail

<details><summary>Reveal answer and explanation</summary>
Correct: B — EKS manages the control plane.
</details>

Q39. Process real-time shipment tracking data and trigger alerts within seconds?
- [ ] A. Amazon Kinesis Data Streams
- [ ] B. Amazon SQS
- [ ] C. AWS Glue
- [ ] D. AWS Batch

<details><summary>Reveal answer and explanation</summary>
Correct: A — Kinesis Data Streams.
</details>

Q40. Create a logically isolated section of the AWS cloud to launch resources?
- [ ] A. AWS PrivateLink
- [ ] B. AWS Direct Connect
- [ ] C. Amazon VPC
- [ ] D. AWS Shield

<details><summary>Reveal answer and explanation</summary>
Correct: C — Amazon VPC.
</details>

Q41. Cache game assets at the edge and deliver globally over HTTPS?
- [ ] A. AWS Global Accelerator
- [ ] B. Amazon CloudFront
- [ ] C. AWS Wavelength
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront.
</details>

Q42. Program for early-stage startups offering credits and guidance?
- [ ] A. AWS Activate
- [ ] B. AWS Well-Architected Tool
- [ ] C. AWS IQ
- [ ] D. AWS Support Concierge

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS Activate.
</details>

Q43. Continuously monitor configurations and compliance against rules?
- [ ] A. AWS Config
- [ ] B. AWS CloudTrail
- [ ] C. AWS Trusted Advisor
- [ ] D. AWS Inspector

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS Config.
</details>

Q44. Run AWS infrastructure at a 5G network edge for ultra-low latency?
- [ ] A. AWS Local Zones
- [ ] B. AWS Wavelength
- [ ] C. AWS Outposts
- [ ] D. AWS Snowball Edge

<details><summary>Reveal answer and explanation</summary>
Correct: B — Wavelength.
</details>

Q45. Analyze large datasets in S3 with standard SQL without loading data?
- [ ] A. Amazon Redshift
- [ ] B. Amazon Athena
- [ ] C. AWS Glue
- [ ] D. Amazon EMR

<details><summary>Reveal answer and explanation</summary>
Correct: B — Athena.
</details>

Q46. Commit to consistent compute usage for a 1–3 year term for big discounts?
- [ ] A. On-Demand
- [ ] B. Reserved Instances
- [ ] C. Spot Instances
- [ ] D. Savings Plans

<details><summary>Reveal answer and explanation</summary>
Correct: D — Savings Plans for compute commitment.
</details>

Q47. Migrate on‑prem Java app to containers without rewriting code?
- [ ] A. AWS App2Container
- [ ] B. AWS Application Migration Service
- [ ] C. AWS CodeBuild
- [ ] D. AWS Elastic Beanstalk

<details><summary>Reveal answer and explanation</summary>
Correct: A — App2Container.
</details>

Q48. Detect unauthorized resource deployments using ML/anomaly detection?
- [ ] A. AWS Shield Advanced
- [ ] B. AWS GuardDuty
- [ ] C. AWS Inspector
- [ ] D. Amazon Detective

<details><summary>Reveal answer and explanation</summary>
Correct: B — GuardDuty.
</details>

Q49. Which support plan includes a TAM and 15‑minute response time for critical issues?
- [ ] A. Developer
- [ ] B. Business
- [ ] C. Enterprise On‑Ramp
- [ ] D. Enterprise

<details><summary>Reveal answer and explanation</summary>
Correct: D — Enterprise Support.
</details>

Q50. Which service enables satellite operators to control and downlink data directly into AWS?
- [ ] A. AWS Snowball Edge
- [ ] B. AWS Ground Station
- [ ] C. Amazon MSK
- [ ] D. AWS DataSync

<details><summary>Reveal answer and explanation</summary>
Correct: B — AWS Ground Station.
</details>

---

<details><summary>Master Answer Key (Q1–Q50)</summary>
1) B 2) B 3) A,C 4) C 5) A 6) C 7) B 8) B 9) B 10) C 11) C 12) B 13) B 14) A 15) B 16) B 17) B 18) B 19) B 20) C 21) A 22) A 23) C 24) D 25) B 26) B 27) A 28) C 29) B 30) B 31) D 32) C 33) B 34) C 35) A 36) B 37) B 38) B 39) A 40) C 41) B 42) A 43) A 44) B 45) B 46) D 47) A 48) B 49) D 50) B
</details>

---

Sample Question (Domain 1: Cloud Concepts)
Q: Which of the following channels shares a collection of offerings to help you achieve specific business outcomes related to enterprise cloud adoption through paid engagements in several specialty practice areas?

- [ ] A. AWS Enterprise Support
- [ ] B. Concierge Support
- [ ] C. AWS Professional Services
- [ ] D. AWS Technical Account Manager

<details><summary>Reveal answer and explanation</summary>
Correct: C — AWS Professional Services delivers guided, paid engagements (often using the AWS CAF) to accelerate adoption.
</details>

---

Domain 1: Cloud Concepts
20-question AWS CLF-C02 mock quiz + 1 mini case study scenario exactly in the style of AWS exam questions. Answers appear under each question.

Part A – 20 AWS Cloud Concepts Practice Questions

Q1. Which AWS cloud value proposition helps customers avoid large upfront capital expenses?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Global reach
- [ ] D. Agility

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go shifts CapEx to OpEx.
</details>

Q2. A company has unpredictable traffic spikes. Which AWS cloud characteristic helps them automatically match capacity to demand?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Fault tolerance
- [ ] D. Cost optimization

<details><summary>Reveal answer and explanation</summary>
Correct: B — Elasticity scales up/down with demand.
</details>

Q3. Which is an AWS global service?
- [ ] A. Amazon EC2
- [ ] B. Amazon S3
- [ ] C. AWS IAM
- [ ] D. Amazon RDS

<details><summary>Reveal answer and explanation</summary>
Correct: C — IAM is global; EC2/S3/RDS are regional.
</details>

Q4. Which of the following is not a benefit of cloud computing?
- [ ] A. Trade capital expense for variable expense
- [ ] B. Increase speed and agility
- [ ] C. Maintain physical security of on-premises hardware
- [ ] D. Stop guessing capacity

<details><summary>Reveal answer and explanation</summary>
Correct: C — On-premises physical security is not a cloud benefit.
</details>

Q5. Which pricing model lets you pay a reduced rate in exchange for committing to use AWS services for a 1–3 year term?
- [ ] A. On-Demand
- [ ] B. Reserved Instances
- [ ] C. Spot Instances
- [ ] D. Free Tier

<details><summary>Reveal answer and explanation</summary>
Correct: B — RIs (and Savings Plans) discount for commitment.
</details>

Q6. Which AWS Well-Architected Framework pillar focuses on using IT and computing resources efficiently?
- [ ] A. Reliability
- [ ] B. Performance efficiency
- [ ] C. Cost optimization
- [ ] D. Operational excellence

<details><summary>Reveal answer and explanation</summary>
Correct: B — Performance efficiency emphasizes efficient resource use.
</details>

Q7. Which statement best describes the AWS Shared Responsibility Model?
- [ ] A. AWS is responsible for security “of” the cloud; customers are responsible for security “in” the cloud.
- [ ] B. AWS is responsible for all security measures.
- [ ] C. Customers are responsible for all security measures.
- [ ] D. AWS manages data classification for customers.

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS secures the cloud infrastructure; customers secure what they run in it.
</details>

Q8. Which AWS service enables you to run code without provisioning or managing servers?
- [ ] A. Amazon EC2
- [ ] B. AWS Lambda
- [ ] C. Amazon ECS
- [ ] D. Amazon Lightsail

<details><summary>Reveal answer and explanation</summary>
Correct: B — Lambda is serverless compute.
</details>

Q9. Which AWS tool helps estimate the cost of running your applications on AWS?
- [ ] A. AWS Cost Explorer
- [ ] B. AWS Pricing Calculator
- [ ] C. AWS Budgets
- [ ] D. AWS Trusted Advisor

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pricing Calculator estimates future costs; Cost Explorer analyzes historical spend.
</details>

Q10. Which AWS service allows you to connect your on-premises network to AWS using a dedicated network link?
- [ ] A. Amazon CloudFront
- [ ] B. AWS Direct Connect
- [ ] C. AWS VPN
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: B — Direct Connect provides a private, dedicated link.
</details>

Q11. Which benefit of cloud computing allows users to experiment and innovate quickly?
- [ ] A. Elasticity
- [ ] B. Agility
- [ ] C. Security
- [ ] D. Global reach

<details><summary>Reveal answer and explanation</summary>
Correct: B — Agility from rapid provisioning accelerates experimentation.
</details>

Q12. Which Amazon S3 storage class is ideal for data that is rarely accessed but must be retrieved within milliseconds when needed?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier Deep Archive
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: B — Standard-IA: infrequent access with ms retrieval; One Zone-IA lacks multi-AZ durability.
</details>

Q13. Which type of cloud deployment model allows an organization to use both on-premises infrastructure and AWS cloud services?
- [ ] A. Public cloud
- [ ] B. Private cloud
- [ ] C. Hybrid cloud
- [ ] D. Multi-cloud

<details><summary>Reveal answer and explanation</summary>
Correct: C — Hybrid combines on-prem and public cloud.
</details>

Q14. Which AWS service provides a content delivery network to distribute content globally with low latency?
- [ ] A. Amazon CloudFront
- [ ] B. AWS Global Accelerator
- [ ] C. Amazon Route 53
- [ ] D. Amazon S3

<details><summary>Reveal answer and explanation</summary>
Correct: A — CloudFront is the CDN. Global Accelerator optimizes TCP/UDP routing.
</details>

Q15. Which AWS service helps you automate the deployment of infrastructure using templates?
- [ ] A. AWS CloudFormation
- [ ] B. AWS OpsWorks
- [ ] C. AWS CodePipeline
- [ ] D. AWS Elastic Beanstalk

<details><summary>Reveal answer and explanation</summary>
Correct: A — CloudFormation is infrastructure as code via templates.
</details>

Q16. What is the main purpose of AWS Availability Zones?
- [ ] A. To cache data closer to users
- [ ] B. To provide low-latency global networking
- [ ] C. To provide isolated locations within a Region for fault tolerance
- [ ] D. To secure AWS accounts

<details><summary>Reveal answer and explanation</summary>
Correct: C — AZs are isolated for resilience within a Region.
</details>

Q17. Which AWS Support plan includes access to a Technical Account Manager (TAM)?
- [ ] A. Basic
- [ ] B. Developer
- [ ] C. Business
- [ ] D. Enterprise

<details><summary>Reveal answer and explanation</summary>
Correct: D — Enterprise Support provides a TAM.
</details>

Q18. Which AWS service is designed to run containerized applications without managing servers or clusters?
- [ ] A. Amazon ECS on EC2
- [ ] B. Amazon ECS with AWS Fargate
- [ ] C. AWS Lambda
- [ ] D. AWS Batch

<details><summary>Reveal answer and explanation</summary>
Correct: B — Fargate runs containers without managing instances.
</details>

Q19. Which AWS service provides visual tools to help you design your AWS architecture?
- [ ] A. AWS CloudFormation
- [ ] B. AWS Architecture Center
- [ ] C. AWS Well-Architected Tool
- [ ] D. AWS Management Console

<details><summary>Reveal answer and explanation</summary>
Correct: B — Architecture Center provides reference architectures and diagrams.
</details>

Q20. Which term refers to the AWS feature of providing resources across multiple Regions and Availability Zones for resilience?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Scalability
- [ ] D. Fault tolerance

<details><summary>Reveal answer and explanation</summary>
Correct: A — Multi-AZ/Region designs improve availability.
</details>

Q21. A video company stores raw files in AWS and accesses them rarely after the first month. Which S3 storage class is most cost-effective after the first month?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: C — Glacier (Flexible Retrieval) suits archival data accessed rarely.
</details>

Q22. Which AWS service should they use to deliver final videos globally with low latency?
- [ ] A. Amazon Route 53
- [ ] B. Amazon CloudFront
- [ ] C. AWS Direct Connect
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront is the CDN for global media delivery.
</details>

Q23. Which cloud benefit are they using by avoiding upfront hardware purchases?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Fault tolerance
- [ ] D. Scalability

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go avoids CapEx.
</details>

Q24. Your startup wants to host a machine learning inference API that must stay online 24/7 and scale automatically without you managing the underlying infrastructure. Which service fits best?
- [ ] A. Amazon EC2 Auto Scaling
- [ ] B. AWS Lambda
- [ ] C. AWS Elastic Beanstalk
- [ ] D. Amazon SageMaker Endpoints

<details><summary>Reveal answer and explanation</summary>
Correct: D — SageMaker Endpoints provide fully managed, autoscaling model hosting.
</details>

Q25. A media company stores massive archives in Amazon S3 but rarely accesses them. Retrieval within minutes is acceptable. Which storage class minimizes cost?
- [ ] A. S3 Standard-IA
- [ ] B. S3 One Zone-IA
- [ ] C. S3 Glacier Flexible Retrieval
- [ ] D. S3 Glacier Deep Archive

<details><summary>Reveal answer and explanation</summary>
Correct: C — Minute‑scale retrieval at low cost.
</details>

Q26. Which AWS service provides visual tools to help you design your AWS architecture?
- [ ] A. AWS CloudFormation
- [ ] B. AWS Architecture Center
- [ ] C. AWS Well-Architected Tool
- [ ] D. AWS Management Console

<details><summary>Reveal answer and explanation</summary>
Correct: B — Architecture Center provides reference architectures and diagrams.
</details>

Q27. Which term refers to the AWS feature of providing resources across multiple Regions and Availability Zones for resilience?
- [ ] A. High availability
- [ ] B. Elasticity
- [ ] C. Scalability
- [ ] D. Fault tolerance

<details><summary>Reveal answer and explanation</summary>
Correct: A — Multi-AZ/Region designs improve availability.
</details>

Q28. A video company stores raw files in AWS and accesses them rarely after the first month. Which S3 storage class is most cost-effective after the first month?
- [ ] A. S3 Standard
- [ ] B. S3 Standard-IA
- [ ] C. S3 Glacier
- [ ] D. S3 One Zone-IA

<details><summary>Reveal answer and explanation</summary>
Correct: C — Glacier (Flexible Retrieval) suits archival data accessed rarely.
</details>

Q29. Which AWS service should they use to deliver final videos globally with low latency?
- [ ] A. Amazon Route 53
- [ ] B. Amazon CloudFront
- [ ] C. AWS Direct Connect
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront is the CDN for global media delivery.
</details>

Q30. Which cloud benefit are they using by avoiding upfront hardware purchases?
- [ ] A. Elasticity
- [ ] B. Pay-as-you-go pricing
- [ ] C. Fault tolerance
- [ ] D. Scalability

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pay-as-you-go avoids CapEx.
</details>

Q31. Your startup wants to host a machine learning inference API that must stay online 24/7 and scale automatically without you managing the underlying infrastructure. Which service fits best?
- [ ] A. Amazon EC2 Auto Scaling
- [ ] B. AWS Lambda
- [ ] C. AWS Elastic Beanstalk
- [ ] D. Amazon SageMaker Endpoints

<details><summary>Reveal answer and explanation</summary>
Correct: D — SageMaker Endpoints provide fully managed, autoscaling model hosting.
</details>

Q32. A media company stores massive archives in Amazon S3 but rarely accesses them. Retrieval within minutes is acceptable. Which storage class minimizes cost?
- [ ] A. S3 Standard-IA
- [ ] B. S3 One Zone-IA
- [ ] C. S3 Glacier Flexible Retrieval
- [ ] D. S3 Glacier Deep Archive

<details><summary>Reveal answer and explanation</summary>
Correct: C — Minute‑scale retrieval at low cost.
</details>

Q33. Under the Shared Responsibility Model, who is responsible for configuring MFA on the AWS account root user?
- [ ] A. AWS
- [ ] B. Customer
- [ ] C. AWS and Customer equally
- [ ] D. AWS Trusted Advisor

<details><summary>Reveal answer and explanation</summary>
Correct: B — Customers configure root MFA.
</details>

Q34. You’re designing a highly available web app running on EC2 in two AZs in one Region. Which service distributes incoming traffic?
- [ ] A. AWS Global Accelerator
- [ ] B. Amazon CloudFront
- [ ] C. Elastic Load Balancing
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: C — ALB/NLB.
</details>

Q35. Which AWS tool provides pre-built compliance reports (e.g., HIPAA)?
- [ ] A. AWS Artifact
- [ ] B. AWS Config
- [ ] C. AWS Inspector
- [ ] D. AWS CloudTrail

<details><summary>Reveal answer and explanation</summary>
Correct: A — Artifact.
</details>

Q36. Which service can send targeted push notifications based on user attributes?
- [ ] A. Amazon SNS
- [ ] B. Amazon Pinpoint
- [ ] C. Amazon SQS
- [ ] D. Amazon Connect

<details><summary>Reveal answer and explanation</summary>
Correct: B — Pinpoint for campaigns/segments.
</details>

Q37. Dedicated private network connection from on‑prem to AWS?
- [ ] A. AWS VPN
- [ ] B. AWS Direct Connect
- [ ] C. VPC Peering
- [ ] D. AWS Global Accelerator

<details><summary>Reveal answer and explanation</summary>
Correct: B — Direct Connect.
</details>

Q38. Run Kubernetes without managing control plane nodes?
- [ ] A. Amazon ECS
- [ ] B. Amazon EKS
- [ ] C. AWS Fargate
- [ ] D. Amazon Lightsail

<details><summary>Reveal answer and explanation</summary>
Correct: B — EKS manages the control plane.
</details>

Q39. Process real-time shipment tracking data and trigger alerts within seconds?
- [ ] A. Amazon Kinesis Data Streams
- [ ] B. Amazon SQS
- [ ] C. AWS Glue
- [ ] D. AWS Batch

<details><summary>Reveal answer and explanation</summary>
Correct: A — Kinesis Data Streams.
</details>

Q40. Create a logically isolated section of the AWS cloud to launch resources?
- [ ] A. AWS PrivateLink
- [ ] B. AWS Direct Connect
- [ ] C. Amazon VPC
- [ ] D. AWS Shield

<details><summary>Reveal answer and explanation</summary>
Correct: C — Amazon VPC.
</details>

Q41. Cache game assets at the edge and deliver globally over HTTPS?
- [ ] A. AWS Global Accelerator
- [ ] B. Amazon CloudFront
- [ ] C. AWS Wavelength
- [ ] D. Amazon Route 53

<details><summary>Reveal answer and explanation</summary>
Correct: B — CloudFront.
</details>

Q42. Program for early-stage startups offering credits and guidance?
- [ ] A. AWS Activate
- [ ] B. AWS Well-Architected Tool
- [ ] C. AWS IQ
- [ ] D. AWS Support Concierge

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS Activate.
</details>

Q43. Continuously monitor configurations and compliance against rules?
- [ ] A. AWS Config
- [ ] B. AWS CloudTrail
- [ ] C. AWS Trusted Advisor
- [ ] D. AWS Inspector

<details><summary>Reveal answer and explanation</summary>
Correct: A — AWS Config.
</details>

Q44. Run AWS infrastructure at a 5G network edge for ultra-low latency?
- [ ] A. AWS Local Zones
- [ ] B. AWS Wavelength
- [ ] C. AWS Outposts
- [ ] D. AWS Snowball Edge

<details><summary>Reveal answer and explanation</summary>
Correct: B — Wavelength.
</details>

Q45. Analyze large datasets in S3 with standard SQL without loading data?
- [ ] A. Amazon Redshift
- [ ] B. Amazon Athena
- [ ] C. AWS Glue
- [ ] D. Amazon EMR

<details><summary>Reveal answer and explanation</summary>
Correct: B — Athena.
</details>

Q46. Commit to consistent compute usage for a 1–3 year term for big discounts?
- [ ] A. On-Demand
- [ ] B. Reserved Instances
- [ ] C. Spot Instances
- [ ] D. Savings Plans

<details><summary>Reveal answer and explanation</summary>
Correct: D — Savings Plans for compute commitment.
</details>

Q47. Migrate on‑prem Java app to containers without rewriting code?
- [ ] A. AWS App2Container
- [ ] B. AWS Application Migration Service
- [ ] C. AWS CodeBuild
- [ ] D. AWS Elastic Beanstalk

<details><summary>Reveal answer and explanation</summary>
Correct: A — App2Container.
</details>

Q48. Detect unauthorized resource deployments using ML/anomaly detection?
- [ ] A. AWS Shield Advanced
- [ ] B. AWS GuardDuty
- [ ] C. AWS Inspector
- [ ] D. Amazon Detective

<details><summary>Reveal answer and explanation</summary>
Correct: B — GuardDuty.
</details>

Q49. Which support plan includes a TAM and 15‑minute response time for critical issues?
- [ ] A. Developer
- [ ] B. Business
- [ ] C. Enterprise On‑Ramp
- [ ] D. Enterprise

<details><summary>Reveal answer and explanation</summary>
Correct: D — Enterprise Support.
</details>

Q50. Which service enables satellite operators to control and downlink data directly into AWS?
- [ ] A. AWS Snowball Edge
- [ ] B. AWS Ground Station
- [ ] C. Amazon MSK
- [ ] D. AWS DataSync

<details><summary>Reveal answer and explanation</summary>
Correct: B — AWS Ground Station.
</details>

---

<details><summary>Master Answer Key (Q1–Q50)</summary>
1) B 2) B 3) A,C 4) C 5) A 6) C 7) B 8) B 9) B 10) C 11) C 12) B 13) B 14) A 15) B 16) B 17) B 18) B 19) B 20) C 21) A 22) A 23) C 24) D 25) B 26) B 27) A 28) C 29) B 30) B 31) D 32) C 33) B 34) C 35) A 36) B 37) B 38) B 39) A 40) C 41) B 42) A 43) A 44) B 45) B 46) D 47) A 48) B 49) D 50) B
</details>

---