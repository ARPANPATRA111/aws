# Module 3 — Exploring Compute Services ⚙️

Status: 🟡 In Progress

## Managed vs. Unmanaged Services

AWS offers a spectrum of services that range from unmanaged to managed, giving you a choice between control and convenience.

* **Unmanaged Services:** These services, like **Amazon EC2**, provide you with a high degree of control over configuration. You are responsible for management tasks like patching the operating system, scaling, and ensuring high availability. AWS manages the underlying physical infrastructure, but you manage the resource itself.

* **Managed Services:** These services shift more operational responsibility to AWS. You configure the service, and AWS handles the underlying infrastructure management, including provisioning, scaling, and maintenance. Services like **Elastic Load Balancing (ELB)** and **Amazon SQS** are examples.

### Serverless Computing

**Serverless** is a service model where you can focus solely on writing and deploying your **application code** without managing servers, handling scaling, or worrying about infrastructure availability. AWS fully manages the underlying infrastructure. This model is perfect for developers who want to maximize their time spent on building features.

---

## AWS Lambda: Function as a Service

**AWS Lambda** is a serverless, event-driven compute service. With Lambda, you don't need to think about servers at all. A great use case for Lambda is automatically processing images as users upload them to an Amazon S3 bucket. It is event-driven, scalable, and perfect for short-running tasks.

**Key Features:**

* **Event-Driven:** Runs code in response to triggers from over 200 AWS services.
* **Automatic Scaling:** Scales automatically to handle any number of requests.
* **Pay for What You Use:** You are billed only for the compute time you consume.
* **Max Duration:** A single Lambda function invocation can run for a maximum of **15 minutes**, making it unsuitable for long-running, high-performance computing workloads.

---
