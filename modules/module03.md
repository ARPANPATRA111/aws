# Module 3 — Exploring Compute Services ⚙️

Status: ✅ Completed

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

## Other Purpose-Built Compute Services

AWS also offers several other services designed for specific use cases.

* **AWS Elastic Beanstalk:** An easy-to-use service for deploying and scaling web applications. You upload your code, and Elastic Beanstalk automatically handles the deployment, capacity provisioning, load balancing, and health monitoring.
* **AWS Batch:** This service is designed for running thousands of **compute-heavy, large-scale batch computing jobs**, like pharmaceutical simulations. It automatically schedules jobs and provisions the optimal compute resources, scaling based on demand.
* **Amazon Lightsail:** This service is the best fit for small projects like a **blog for a client with minimal traffic**. It simplifies launching and managing a virtual private server by bundling everything you need (compute, storage, networking) into a basic, cost-effective package with predictable pricing.
* **AWS Outposts:** A service that extends AWS infrastructure and services to your on-premises data center. Outposts is a solution for hybrid cloud deployments that require low latency or have data residency requirements.

---

## Resources

| Resource link | Description |
| :--- | :--- |
| [Containers on AWS](https://aws.amazon.com/containers/) | An overview of the AWS container offerings, including services for container image storage, orchestration, and compute. |
| [Amazon Elastic Container Registry](https://aws.amazon.com/ecr/) | A fully managed service for storing, managing, and deploying container images securely at scale. |
| [Amazon Elastic Container Service](https://aws.amazon.com/ecs/) | A fully managed service that streamlines the deployment, management, and scaling of containerized applications on AWS. |
| [Amazon Elastic Kubernetes Service](https://aws.amazon.com/eks/) | A fully managed Kubernetes service that streamlines running Kubernetes clusters on AWS and on premises. |
| [AWS Fargate](https://aws.amazon.com/fargate/) | A serverless compute engine for running containers without managing servers, integrated with Amazon ECS and Amazon EKS. |
| [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/) | A fully managed service for deploying and scaling web applications without managing infrastructure. |
| [AWS Batch](https://aws.amazon.com/batch/) | A fully managed service for efficiently running large-scale batch computing jobs on AWS. |
| [What is Amazon Lightsail?](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/what-is-amazon-lightsail) | A simplified cloud platform offering VPS, containers, and databases with predictable pricing. |
| [What is AWS Outposts?](https://docs.aws.amazon.com/outposts/latest/server-userguide/what-is-outposts.html) | Extends AWS infrastructure and services to on-premises locations for low-latency, local data processing. |
| [Choosing a modern application strategy](https://docs.aws.amazon.com/decision-guides/latest/modern-apps-strategy-on-aws-how-to-choose/modern-apps-strategy-on-aws-how-to-choose.html) | The AWS Decision Guide helps organizations determine the most suitable development approach—serverless or Kubernetes. |
