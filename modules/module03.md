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

## Containers on AWS

Containers solve the classic "it works on my machine" problem. By **packaging an application in a container that includes all of its code, runtime, and dependencies**, you create a single, portable unit. This ensures the application runs consistently across all development, testing, and production environments.

### Container Orchestration

Managing the lifecycle of containers at scale (starting, stopping, scaling, monitoring) is complex. **Container orchestration services** automate this process. After storing an image in a registry, you need an orchestrator to manage the deployment.

1. **Amazon ECS (Elastic Container Service):** A highly scalable, high-performance container orchestration service that is deeply integrated with the AWS ecosystem.
2. **Amazon EKS (Elastic Kubernetes Service):** A managed service that makes it easy to run **Kubernetes** on AWS. Kubernetes is a powerful, open-source platform that offers a high degree of control and flexibility.

### Container Registry and Compute Options

* **Amazon ECR (Elastic Container Registry):** A fully managed container registry where you can store, manage, and deploy your container images securely.
* **Compute Options:** Once you've chosen an orchestrator, you need to decide where your containers will run.
  * **Amazon EC2:** You manage the cluster of EC2 instances that run your containers. This gives you maximum control.
  * **AWS Fargate:** A **serverless** compute engine for containers. With Fargate, AWS manages the servers, so you only need to focus on your containers.

---
