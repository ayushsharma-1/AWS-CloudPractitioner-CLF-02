
# Application Integration Services (CLF-C02 Exam Guide)

## Table of Contents
1. [Amazon EventBridge](#amazon-eventbridge)
2. [Amazon SNS](#amazon-sns)
3. [Amazon SQS](#amazon-sqs)
4. [AWS Step Functions](#aws-step-functions)

---

## Amazon EventBridge

### Definition
Amazon EventBridge is a serverless event bus service that connects applications using events. It helps you build event-driven architectures by routing events from AWS services, SaaS apps, or your own applications to targets (Lambda, SQS, SNS, Step Functions, etc.).

### Key Features
- Event Bus: channels that receive and route events (default, partner, custom)
- Rules: define filtering patterns to match specific events
- Targets: where matched events are sent (Lambda, SQS, SNS, Step Functions, etc.)
- Schema Registry: automatically discovers and stores event structure
- Event Replay: replay past events to test or recover systems
- Integrations: native with AWS services and partner SaaS (Zendesk, Shopify, etc.)
- Serverless & Scalable: fully managed, scales automatically
- Cross-account and Cross-region events: share and route events across accounts

### Direct Exam Questions
1. What is the purpose of Amazon EventBridge?
   - To build event-driven applications by routing events from sources to targets.
2. Difference between CloudWatch Events and EventBridge?
   - EventBridge is the evolution of CloudWatch Events with more integrations (SaaS, schema registry, event replay).
3. Can EventBridge trigger AWS Lambda functions?
   - Yes, Lambda is a common target.
4. Does EventBridge require provisioning servers?
   - No, it’s fully serverless.

### Scenario-Based Questions
1. Your company wants to automatically trigger a Lambda function whenever a new user is created in an external SaaS CRM app (like Zendesk). Which AWS service is best?
   - Answer: Amazon EventBridge (partner integration)
2. An app team wants to capture every EC2 instance state change (start/stop/terminate) and send it to SQS for processing. Which service helps?
   - Answer: EventBridge with rule + SQS target
3. You need to reprocess customer order events from last week to test a new analytics pipeline. How can you do this?
   - Answer: Event Replay in EventBridge
4. Two teams in different AWS accounts want to share event data securely without building APIs. What should they use?
   - Answer: EventBridge cross-account event routing

---

## Amazon SNS (Simple Notification Service)

### Definition
Amazon SNS is a fully managed pub/sub (publish-subscribe) messaging service used for decoupled communication between distributed systems, microservices, and applications.

### Key Features
- Pub/Sub Messaging Model: publishers send messages to a topic; subscribers (SQS, Lambda, HTTP/S endpoints, email, SMS, mobile push) receive messages
- Fan-out Pattern: one message can be delivered to multiple subscribers simultaneously
- Multiple Protocols Supported: HTTP/S, email, SMS, Lambda, SQS, mobile push
- Durability & Availability: messages stored across multiple AZs
- Message Filtering: subscribers can filter messages based on attributes
- Security: IAM policies, resource policies, encryption (SSE with KMS), VPC endpoints
- Scalability: handles millions of messages per second
- Cost-effective: pay-per-request model

### Common Use Cases
- Application-to-Application (A2A): microservices communication, fan-out event distribution (SNS → SQS, Lambda, Kinesis)
- Application-to-Person (A2P): sending SMS alerts, email notifications, push notifications
- Event-driven architectures: trigger actions in multiple services simultaneously
- Decoupling services: avoid direct dependencies between services by using topics

### Exam-Oriented Notes
- Fan-out delivery: SNS + SQS (one message → multiple queues)
- Decoupling producers and consumers: SNS topics
- Delivering notifications directly to users (SMS, email, push): SNS
- Long-term message storage / delayed processing: SQS (not SNS)
- SNS vs EventBridge:
  - SNS: simple pub/sub messaging
  - EventBridge: advanced event bus with routing, filtering, SaaS integration

### Scenario-Based Questions
1. A company needs to send billing alerts to customers via SMS and also trigger a Lambda function to process billing records. Which service should they use?
   - Answer: SNS with multiple subscribers (SMS + Lambda)
2. You need to deliver the same event to multiple microservices asynchronously. Which AWS service should you use?
   - Answer: SNS with SQS or Lambda subscribers
3. A mobile application must push notifications to iOS and Android devices. Which service is best?
   - Answer: SNS Mobile Push Notifications

---

## Amazon SQS (Simple Queue Service)

### Definition
Amazon SQS is a fully managed message queuing service that enables decoupled, scalable, and fault-tolerant communication between distributed components of an application. Allows asynchronous processing by sending, storing, and receiving messages between software systems without direct connectivity.

### Key Features
- Types of Queues:
  - Standard Queue: nearly unlimited throughput, at-least-once delivery, best-effort ordering
  - FIFO Queue: first-in-first-out, exactly-once processing, message groups for ordered parallel processing, lower throughput
- Durability & Availability: messages stored across multiple AZs
- Scalability: automatically scales without provisioning capacity
- Visibility Timeout: message being processed is invisible to other consumers for a set duration
- Dead-Letter Queues (DLQ): handle failed message processing after retries
- Security: IAM policies, encryption at rest (SSE with KMS), TLS in transit
- Integration: works with SNS, Lambda, EC2, ECS, EventBridge, Step Functions
- Long Polling: reduces cost by allowing consumers to wait for messages

### Direct Exam Questions
- Difference between Standard Queue and FIFO Queue
- Purpose of Dead-Letter Queues
- How visibility timeout prevents duplicate processing
- When to use long polling vs short polling
- How SQS integrates with SNS

### Scenario-Based Questions
1. Decoupling Services:
   - Your app needs to process payment transactions independently of order placement. Which service ensures decoupling?
     - Answer: SQS
2. Ordered & Exactly-Once Processing:
   - A stock trading app must process orders in strict sequence with no duplicates. Which queue type?
     - Answer: FIFO Queue
3. Failed Message Handling:
   - Messages keep failing after retries. How can you isolate them for debugging?
     - Answer: Dead-Letter Queue
4. Cost Optimization:
   - How to reduce the cost of continuously polling SQS for messages?
     - Answer: Enable Long Polling

---

## AWS Step Functions

### Definition
AWS Step Functions is a serverless orchestration service that lets you coordinate multiple AWS services into workflows using state machines.

### Key Features
- Visual Workflow Designer: drag-and-drop interface
- State Machines: represent each step (Task, Choice, Parallel, Wait, Success/Fail)
- Integrations: works natively with Lambda, ECS, DynamoDB, SQS, SNS, SageMaker, Glue, etc.
- Error Handling & Retries: built-in error catching, retries, fallback paths
- Types of Workflows:
  - Standard Workflows: long-running (up to 1 year), for complex business processes
  - Express Workflows: high-volume, short-lived (up to 5 mins), cost-optimized
- Serverless & Scalable: no infrastructure to manage, scales automatically
- Auditing & Logging: each step is recorded for debugging and compliance
- Parallel Execution: run multiple tasks at once

### Use Cases
- Automating ETL pipelines (Glue + S3 + Redshift)
- Microservice orchestration (calling multiple Lambda functions in order)
- Machine learning model training workflows (data prep → train → deploy)
- Approval workflows (Choice + Wait states)
- Error recovery (retry logic and fallback paths)

### Exam-Oriented Questions
**Direct Questions**
- What is AWS Step Functions used for?
- Difference between Standard and Express workflows?
- How does Step Functions handle retries and errors?
- Which services can Step Functions integrate with?

**Scenario-Based Questions**
- Your company wants to coordinate multiple Lambda functions into a workflow with error handling. Which AWS service should you use?
  - Answer: Step Functions
- You need to run a data processing workflow that can last for several days. Which workflow type will you choose?
  - Answer: Standard
- A financial app requires real-time high-volume event orchestration with short execution times. Which workflow type fits?
  - Answer: Express

