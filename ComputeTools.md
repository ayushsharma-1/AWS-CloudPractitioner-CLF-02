Got it 👍 Let’s break these down one by one (CLF-C02 exam focus: features, use cases, scenarios).

---

## **1. AWS Batch**

* **What it is**: Fully managed service to run **batch computing jobs** (large-scale parallel or high-throughput jobs).
* **Features**:

  * Dynamically provisions compute (EC2/Spot/Fargate) for jobs.
  * Handles **job queues, priorities, dependencies**.
  * Supports containerized jobs via Amazon ECS.
  * Pay only for resources used.
* **Use Case**:

  * Genomics processing, financial risk modeling, media rendering, ML training.
* **Scenario Example (Exam)**:

  > You need to run 10,000 batch processing jobs with varying compute needs and want AWS to scale EC2 automatically. **Answer: AWS Batch.**

---

## **2. Amazon EC2 (Elastic Compute Cloud)**

* **What it is**: Virtual servers in the cloud.
* **Features**:

  * Wide instance types (General, Compute-optimized, GPU, Memory-optimized).
  * Pricing models: On-Demand, Spot, Reserved, Savings Plans.
  * Auto Scaling, Elastic Load Balancing integration.
  * Customizable networking (VPC, Security Groups, EBS storage).
* **Use Case**:

  * Hosting web apps, backend systems, custom workloads.
* **Scenario Example (Exam)**:

  > You need full OS-level control of servers for running legacy apps. **Answer: EC2.**

---

## **3. AWS Elastic Beanstalk**

* **What it is**: **PaaS** service for deploying apps without managing infrastructure.
* **Features**:

  * Supports Java, .NET, Python, Node.js, PHP, Go, Ruby, Docker.
  * Handles provisioning (EC2, RDS, Load Balancer, Auto Scaling).
  * Monitoring via CloudWatch.
  * Developers just provide code → AWS manages deployment.
# AWS Compute Services (CLF-C02 Exam Guide)

## Table of Contents
1. [AWS Batch](#aws-batch)
2. [Amazon EC2](#amazon-ec2)
3. [AWS Elastic Beanstalk](#aws-elastic-beanstalk)
4. [AWS Local Zones](#aws-local-zones)
5. [AWS Wavelength](#aws-wavelength)
6. [AWS Outposts](#aws-outposts)
7. [AWS Lightsail](#aws-lightsail)
8. [AWS Fargate](#aws-fargate)
9. [Amazon EKS](#amazon-eks)
10. [Amazon ECS](#amazon-ecs)
11. [AWS Elastic Container Registry (ECR)](#aws-elastic-container-registry-ecr)

---

## AWS Batch
Fully managed service to run batch computing jobs (large-scale parallel or high-throughput jobs).

### Features
- Dynamically provisions compute (EC2/Spot/Fargate) for jobs
- Handles job queues, priorities, dependencies
- Supports containerized jobs via Amazon ECS
- Pay only for resources used

### Use Cases
- Genomics processing, financial risk modeling, media rendering, ML training

### Scenario Example
You need to run 10,000 batch processing jobs with varying compute needs and want AWS to scale EC2 automatically. **Answer: AWS Batch**

---

## Amazon EC2 (Elastic Compute Cloud)
Virtual servers in the cloud.

### Features
- Wide instance types (General, Compute-optimized, GPU, Memory-optimized)
- Pricing models: On-Demand, Spot, Reserved, Savings Plans
- Auto Scaling, Elastic Load Balancing integration
- Customizable networking (VPC, Security Groups, EBS storage)

### Use Cases
- Hosting web apps, backend systems, custom workloads

### Scenario Example
You need full OS-level control of servers for running legacy apps. **Answer: EC2**

---

## AWS Elastic Beanstalk
PaaS service for deploying apps without managing infrastructure.

### Features
- Supports Java, .NET, Python, Node.js, PHP, Go, Ruby, Docker
- Handles provisioning (EC2, RDS, Load Balancer, Auto Scaling)
- Monitoring via CloudWatch
- Developers just provide code; AWS manages deployment

### Use Cases
- Deploy a web app quickly without deep infra knowledge

### Scenario Example
You have a Python Flask app and want AWS to manage servers, scaling, and updates automatically. **Answer: Elastic Beanstalk**

---

## AWS Local Zones
Extension of AWS regions that places compute, storage, and databases closer to large population/industry centers.

### Features
- Reduces latency (<10 ms)
- Supports EC2, ECS/EKS, VPC, FSx, ELB, etc.
- Ideal for apps requiring real-time response

### Use Cases
- Gaming, video streaming, real-time trading, healthcare imaging

### Scenario Example
A gaming company needs <10ms latency for users in LA while still using AWS services. **Answer: AWS Local Zones**

---

## AWS Wavelength
Brings AWS compute and storage services to the edge of telecom 5G networks, minimizing latency by running apps closer to end-users and devices.

### Features
- Ultra-Low Latency: compute at the edge inside telecom 5G networks
- Edge Zones: Wavelength Zones managed as part of your AWS environment
- Familiar AWS Services: EC2, EBS, VPC, ECS, EKS, Load Balancing
- Seamless Integration: connected to parent AWS Region
- Pay-as-You-Go: same AWS pricing model
- Scalable & Elastic: scale applications in Wavelength Zones

### Use Cases
- AR/VR & Gaming
- IoT & Smart Cities
- Autonomous Vehicles
- Live Video Streaming
- Healthcare & Remote Surgery

### Exam-Oriented Notes
- Wavelength = AWS + Telecom 5G Edge
- Focus: ultra-low latency apps
- Wavelength Zones = part of a specific AWS Region
- Managed with AWS Console, CLI, SDKs
- Compared with Outposts (on-premise AWS) and Local Zones (AWS-managed nearby infra)

### Scenario Questions
1. Deploy a mobile gaming app requiring sub-10 ms latency for players worldwide. **Answer: AWS Wavelength**
2. Difference from Outposts? Outposts brings AWS on-premises, Wavelength brings AWS to 5G edge networks.

---

## AWS Outposts
Fully managed service that brings AWS infrastructure and services to your on-premises or co-location data centers. Designed for workloads needing low latency, local data processing, or data residency requirements.

### Features
- Hybrid Cloud: run AWS services (EC2, EBS, RDS, ECS, EKS, S3, etc.) on-premises
- Consistency: same APIs, services, tools, and management console as AWS cloud
- Fully Managed: AWS delivers, installs, operates, and maintains hardware
- Connectivity: requires connection to AWS region
- Low Latency Processing: process data locally
- Data Residency Compliance: keep sensitive workloads/data within a specific location
- Flexible Form Factors: Outposts Rack (large-scale), Outposts Servers (edge/branch)

### Use Cases
- Low-Latency Applications
- Local Data Processing
- Data Residency
- Edge Computing
- Hybrid Modernization

### Exam-Focused Notes
- Outposts = AWS hardware in your data center
- Use for <10ms latency or data residency
- Managed by AWS, physically at customer site
- Supports EC2, EBS, ECS, EKS, RDS, S3 (subset)
- Difference from Snow Family: Outposts = long-term hybrid cloud, Snow = edge storage/compute for migration/disconnected sites

### Scenario Example
A hospital must process patient data locally due to government regulations but also wants to use AWS services and scale when needed. **Answer: AWS Outposts**

---

## AWS Lightsail
Simplified cloud platform to build and run applications/websites quickly, without deep AWS expertise.

### Features
- Preconfigured Instances: easy VPS launch with OS + app stacks (WordPress, LAMP, Node.js, etc.), fixed monthly pricing
- Simplified Networking: static IPs, DNS management, firewall rules, load balancers
- Managed Databases: MySQL, PostgreSQL, automated backups, scaling, failover
- Storage Options: block storage, object storage buckets
- Containers & Kubernetes: simple deployment of containerized apps
- Monitoring & Alerts: integrated metrics and health checks
- Integration: connect with S3, CloudWatch, Route53

### Exam-Oriented Questions
- Lightsail: easy-to-use, cost-effective VPS for simple workloads
- Pricing: fixed monthly plans
- Difference: Lightsail is simplified, EC2 offers full customization

### Scenario Questions
1. Host a WordPress website with predictable monthly cost. **Answer: Lightsail**
2. Learn cloud by setting up a LAMP stack with minimum setup complexity. **Answer: Lightsail**
3. Need a simple, managed database for an app, without complex AWS setup. **Answer: Lightsail Managed Database**

---

## AWS Fargate (Serverless Compute for Containers)
Serverless compute engine that runs containers without provisioning or managing EC2 instances. Works with Amazon ECS and Amazon EKS.

### Features
- Serverless for containers: no EC2 clusters to manage
- Automatic Scaling: adjusts resources automatically
- Pay-per-use: billed based on vCPU + memory requested
- Security isolation: each task/pod runs in its own environment
- Integration: CloudWatch, IAM, ALB, VPC, ECR
- Consistency: same config across dev, test, prod

### When to Use Fargate
- Microservices without managing servers
- Batch jobs or event-driven container workloads
- Apps needing rapid scaling
- Teams focusing on apps, not infrastructure

### Comparison
- ECS on EC2: you manage EC2 instances
- EKS on EC2: Kubernetes with EC2 nodes
- Fargate: no servers to manage, just define CPU/memory

### Exam Questions
1. Run containers without managing EC2 servers? **Answer: AWS Fargate**
2. Does Fargate require ECS/EKS? **Answer: Yes**
3. Pricing for Fargate? **Answer: vCPU and memory requested per container**

### Scenario Questions
1. Deploy a microservices app in containers without managing servers/clusters. **Answer: AWS Fargate**
2. Run Kubernetes app but avoid managing worker nodes. **Answer: Amazon EKS with Fargate**
3. App with unpredictable traffic, want automatic scaling of containers. **Answer: Fargate**

---

## Amazon EKS (Elastic Kubernetes Service)
Fully managed Kubernetes service to run, scale, and secure containerized applications using Kubernetes on AWS without managing the control plane.

### Features
- Managed Kubernetes Control Plane: AWS runs master nodes, highly available
- Integration: IAM, CloudWatch, VPC, ALB/ELB, EBS, EFS, App Mesh
- Hybrid & Multi-Cloud: EKS Anywhere (on-premises), EKS Blueprints (automate setup)
- Compute Options: EC2 or Fargate
- Security & Compliance: IAM + RBAC, VPC isolation, KMS encryption
- Scalability: auto scaling via Cluster Autoscaler, EC2 ASG, Fargate

### When to Use EKS
- Already use Kubernetes, want AWS to manage control plane
- Hybrid workloads (cloud + on-prem)
- Migrate Kubernetes workloads into AWS
- Run serverless Kubernetes using Fargate

### Exam-Oriented Scenarios
1. Run Kubernetes workloads on AWS without managing control plane. **Answer: Amazon EKS**
2. Run Kubernetes on AWS and on-prem for hybrid setup. **Answer: EKS Anywhere**
3. Serverless Kubernetes pods without EC2 nodes. **Answer: EKS with Fargate**

---

## Amazon ECS (Elastic Container Service)
Fully managed container orchestration service to run, stop, and manage Docker containers on EC2 instances or with AWS Fargate.

### Features
- Launch Types: EC2 (manage your own instances), Fargate (serverless)
- Task Definitions: JSON blueprint for containers (image, CPU, memory, networking, IAM roles)
- Service Management: desired number of tasks, rolling updates, blue/green deployments
- Scalability: auto scaling based on demand, integrates with CloudWatch metrics
- Networking: ALB/NLB integration, VPC networking (awsvpc mode)
- Integration: ECR, CloudWatch, IAM, Secrets Manager, Service Discovery, App Mesh
- Security: IAM roles per task, private networking with VPC

### Exam-Oriented Questions
- What is ECS used for?
- Difference: EC2 launch type vs Fargate launch type
- What is a task definition in ECS?

### Scenario Questions
1. Run containers without managing servers. **Answer: ECS with Fargate**
2. Tight control over EC2 instances running containers. **Answer: ECS with EC2 launch type**
3. Store and pull private container images. **Answer: Amazon ECR with ECS**
4. Containers auto scale with traffic. **Answer: ECS Service Auto Scaling + ALB**

---

## AWS Elastic Container Registry (ECR)
Fully managed container image registry to store, manage, share, and deploy Docker/OCI container images. Integrates with ECS, EKS, Lambda.

### Features
- Fully Managed: no registry infrastructure to manage
- High Availability & Durability: built on S3 backend
- Security: private repos, IAM permissions, image scanning, encryption at rest/in transit
- Integration: ECS, EKS, Fargate, Lambda, CodePipeline, CodeBuild
- Lifecycle Policies: clean up old/unused images
- Cross-Region & Cross-Account Replication
- Public Registry: share images with community
- Performance: fast retrieval for deployments
- Tagging & Versioning: multiple versions with tags

### Use Cases
- Store Docker/OCI images for ECS/EKS workloads
- CI/CD pipelines (CodePipeline + CodeBuild + ECR + ECS)
- Share public container images
- Private secure images with vulnerability scanning
- Multi-region apps with replicated images

### Exam Style Questions
1. What is Amazon ECR primarily used for?
   - Answer: Storing container images
2. Store Docker images securely, scan for vulnerabilities, use in ECS. **Answer: Amazon ECR**
3. Optimize storage costs for unused old image versions. **Answer: Use ECR Lifecycle Policies**
   * Highly available across multiple AZs.



2. **Integration with AWS Ecosystem**


