# Module 2 — Compute in the Cloud 💻

Status: ✅ Completed

## What is Amazon EC2?

**Amazon Elastic Compute Cloud (EC2)** is an AWS service that provides the raw compute capacity needed to host your applications. In simple terms, an EC2 instance is a **virtual machine (VM)**, or a virtual server, that you can request and launch in the AWS cloud. Resources are provisioned **based on demand**, allowing you to scale your capacity up or down as your needs change.

Instead of the slow and expensive process of acquiring a physical server, EC2 allows you to launch instances on-demand. When you're done, you can stop or terminate them and only pay for the time they were running.

### Multi-Tenancy and the Hypervisor

EC2 instances run in a **multi-tenant** environment. This refers to a model where **multiple users share the same physical host hardware while maintaining secure isolation from each other**. This isolation is managed by a piece of software called a **hypervisor**, which is handled entirely by AWS.

---

## Foundational EC2 Concepts

### Amazon Machine Images (AMIs)

An **Amazon Machine Image (AMI)** is a pre-configured template for your instances. Its primary role is to **provide a consistent image to launch new instances**. An AMI includes the operating system, software packages, and other required settings. When you launch multiple instances from the same AMI, you ensure they all have the same baseline configuration, which is crucial for scaling applications reliably.

### Interacting with AWS Services

Everything in AWS is an **API** (Application Programming Interface) call. There are three main ways to manage your AWS resources:

1. **AWS Management Console:** A user-friendly, browser-based graphical user interface (GUI). It's great for learning, viewing bills, and performing tasks visually, but it is not ideal for automating repetitive processes.
2. **AWS Command Line Interface (CLI):** A tool that allows you to control AWS services from a terminal using text-based commands. This makes it possible to automate tasks through scripting.
3. **AWS Software Development Kits (SDKs):** Allows you to interact with AWS services using various programming languages like Python, Java, or .NET. This is the foundation for building applications that integrate with AWS.

---

## EC2 Instance Families

EC2 instance types are grouped into families, each offering a unique combination of CPU, memory, storage, and networking. Choosing the right one helps optimize performance and cost.

| Family | Description | Ideal Use Cases |
| --- | --- | --- |
| **General Purpose** | Provides a balanced mix of compute, memory, and networking resources. A flexible and cost-effective choice for a wide variety of workloads. | Web servers, code repositories, new applications with unknown traffic patterns. |
| **Compute Optimized**| Ideal for tasks that require significant CPU power to perform complex computations. | Gaming servers, high-performance computing (HPC), scientific and climate modeling simulations. |
| **Memory Optimized** | Delivers fast performance for workloads that process large datasets in memory. | High-performance databases, real-time big data analytics. |
| **Storage Optimized** | Designed for workloads that need high, sequential read/write access to very large datasets on local storage. | Data warehousing, distributed file systems. |
| **Accelerated Computing**| Uses hardware accelerators (co-processors/GPUs) to perform functions more efficiently than software on CPUs. | Complex visual effects rendering, machine learning, data pattern matching. |

You can also resize an instance (a process called **vertical scaling**) by giving it more CPU or memory if your application's needs change.

---

## EC2 Pricing Options

EC2 provides several billing options to help you optimize costs based on your usage patterns.

| Option | Best For | Description |
| --- | --- | --- |
| **On-Demand** | New applications with unsure traffic, or short-term, spiky workloads. | Pay by the hour or second with **no long-term commitment**. Offers the most flexibility. |
| **Savings Plans** | Consistent, steady-state usage. | Commit to a consistent amount of usage (in $/hour) for a 1- or 3-year term to receive a discount of up to 72%. |
| **Reserved Instances** | **Predictable, long-term workloads** (e.g., 3 years). | Commit to a specific instance type in a specific region for a 1- or 3-year term for up to a 75% discount. |
| **Spot Instances** | Non-time-sensitive, fault-tolerant batch jobs. | Request spare EC2 capacity for up to 90% off the On-Demand price. These instances can be interrupted with a 2-minute warning. |

---

## Scalability, Load Balancing, and Messaging

### Auto Scaling and Elastic Load Balancing

**Amazon EC2 Auto Scaling** and **Elastic Load Balancing (ELB)** work together to create a scalable and highly available architecture.

* **EC2 Auto Scaling** automatically **adds or removes instances based on performance data and application metrics** (monitored by Amazon CloudWatch). It ensures you have enough instances to meet demand but scales down to save money when demand decreases.
* **Elastic Load Balancing (ELB)** acts as a single point of contact for traffic and **distributes those incoming requests evenly across the healthy instances** that Auto Scaling is managing.

### Messaging and Queuing for Decoupled Architectures

To build resilient applications, it's best to create a loosely coupled architecture. This means components are independent; if one component fails, the rest of the system can continue to function normally. This is achieved with messaging services.

* **Amazon SQS (Simple Queue Service):** A message queue used as a buffer between application components. Messages are stored in the queue until they can be processed. This is ideal for tasks that can be processed later and ensures no data is lost if a component is temporarily unavailable.
* **Amazon SNS (Simple Notification Service):** A "publish/subscribe" service for sending time-sensitive, real-time notifications. A single message is "published" to a topic and immediately pushed to all subscribers (e.g., sending an immediate email or SMS when a bug is reported).

---

## Resources

| Resource link | Description |
| --- | --- |
| [Compute on AWS](https://aws.amazon.com/products/compute/) | This resource provides an overview of the different cloud computing services offered by AWS. |
| [AWS Compute Blog](https://aws.amazon.com/blogs/compute/) | This blog provides updates, tutorials, and best practices for using AWS compute services. |
| [AWS Compute Services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html) | This reference provides an in-depth introduction to the compute services available within the AWS Cloud. |
| [Hands-On Tutorials: Compute](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23compute) | This resource provides practical, step-by-step tutorials to help users gain hands-on experience. |
| [Amazon EC2](https://aws.amazon.com/ec2/) | Amazon EC2 runs virtual servers in the cloud with flexible computing capacity. |
| [Amazon EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/) | This guide provides detailed information about the different types of EC2 instances. |
| [Amazon EC2 Pricing](https://aws.amazon.com/ec2/pricing/) | This guide explains the different pricing models for EC2 instances. |
| [Amazon EC2 Auto Scaling](https://aws.amazon.com/ec2/autoscaling/) | Amazon EC2 Auto Scaling automatically adjusts instance count based on demand. |
| [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/) | ELB automatically distributes incoming application traffic across multiple EC2 instances. |
| [Amazon SNS](https://aws.amazon.com/sns/) | Amazon SNS is a messaging service for sending notifications to users or other applications. |
| [Amazon SQS](https://aws.amazon.com/sqs/) | Amazon SQS decouples application components through message queuing. |
