# Module 2 — Compute in the Cloud 💻

Status: ✅ Completed

## What is Amazon EC2?

**Amazon Elastic Compute Cloud (Amazon EC2)** is the AWS service that provides secure, resizable compute capacity—essentially, virtual servers—in the cloud. Instead of buying and managing your own physical servers, you can launch **EC2 instances** in minutes and scale your capacity up or down as needed.

EC2 instances are **virtual machines (VMs)**. They run on a physical host machine that is shared with other instances, a concept known as **multi-tenancy**. The isolation and resource management between these VMs is handled by a **hypervisor**, which is managed entirely by AWS. You, the customer, have complete control over the instance itself, including:

* **Operating System (OS):** Choose between various distributions of Linux or Windows.
* **Software:** Install your own business applications, web servers, databases, or third-party software.
* **Sizing:** You can resize an instance by giving it more CPU or memory, a process called **vertical scaling**.
* **Networking:** You control who can access your instance.

You only pay for the time your instances are running, making it a highly flexible and cost-effective way to acquire compute power.

---

## EC2 Instance Types

Just as a coffee shop needs different machines for espresso, drip coffee, and cold brew, different workloads require different types of compute power. EC2 instance types are grouped into **families**, each offering a specific combination of CPU, memory, storage, and networking capacity.

* **General Purpose:** Provide a balance of compute, memory, and networking. Ideal for diverse workloads like web servers or code repositories.
* **Compute Optimized:** For compute-intensive tasks that require high-performance processors, like gaming servers, scientific modeling, or high-performance computing (HPC).
* **Memory Optimized:** Designed for workloads that process large data sets in memory, such as high-performance databases or real-time big data analytics.
* **Accelerated Computing:** Use hardware accelerators (co-processors) for tasks like graphics processing, machine learning, and floating-point calculations.
* **Storage Optimized:** Built for workloads requiring high, sequential read and write access to very large data sets on local storage.

When you select an instance type, you also choose a **size** (e.g., `t2.micro`, `m5.large`). This allows you to balance performance and cost to fit your needs perfectly.

---

## Interacting with AWS Services

Everything you do in AWS is an **API (Application Programming Interface)** call. There are three primary ways to interact with these APIs to manage your resources.

* **AWS Management Console:** A web-based, visual interface. It's great for learning, viewing bills, and performing tasks that don't require automation.
* **AWS Command Line Interface (CLI):** A tool that lets you control AWS services from your terminal using commands. This enables powerful automation through scripting.
* **AWS Software Development Kits (SDKs):** Allows you to manage AWS resources from your favorite programming languages (like Python, Java, or JavaScript), integrating AWS capabilities directly into your applications.

---

## EC2 Pricing Options

EC2 offers several billing options to help you optimize costs based on your usage patterns.

* **On-Demand:** Pay for compute capacity by the hour or second with no long-term commitments. Perfect for applications with short-term, unpredictable workloads.
* **Savings Plans:** Commit to a consistent amount of compute usage (e.g., $10/hour) for a 1 or 3-year term to receive a significant discount (up to 72%). This is a flexible option that applies across instance families and even to other services like AWS Lambda.
* **Reserved Instances (RIs):** For applications with steady-state or predictable usage, you can commit to specific instance types for a 1 or 3-year term for discounts up to 75%.
* **Spot Instances:** Request spare EC2 computing capacity for up to 90% off the On-Demand price. These instances can be interrupted by AWS, making them ideal for workloads that can tolerate interruptions, like batch jobs or data analysis.
* **Dedicated Hosts:** A physical EC2 server dedicated for your use. This helps you address compliance requirements and use existing server-bound software licenses.

---

## Scalability, Elasticity, and Load Balancing

A key benefit of the cloud is the ability to automatically adjust capacity to meet demand.

* **Scalability:** The ability for your system to handle a growing amount of work. In AWS, this is often done via **horizontal scaling** (or scaling out), which means adding more EC2 instances to your resource pool.
* **Elasticity:** The ability to scale capacity up and down automatically based on demand. **Amazon EC2 Auto Scaling** is the service that makes this possible. It monitors your application (using **Amazon CloudWatch** metrics) and automatically adds or removes instances to maintain performance and minimize cost.
* **Load Balancing:** To distribute incoming traffic evenly across your fleet of EC2 instances, you use a load balancer. **Elastic Load Balancing (ELB)** is an AWS service that automatically routes traffic to the healthiest instances, preventing any single instance from becoming a bottleneck. This increases the fault tolerance and availability of your application.

---

## Decoupling Applications: SQS and SNS

In a modern cloud architecture, it's a best practice to build **loosely coupled** systems. This means that if one component fails, it doesn't cause cascading failures throughout the entire system. Messaging and queuing services are essential for achieving this.

* **Amazon SQS (Simple Queue Service):** A fully managed message queuing service. It provides a buffer, or **queue**, between application components. One component can send messages to the queue, and another can process them when ready. This decouples the components, so if the processing application fails, messages can safely wait in the queue until it recovers.
* **Amazon SNS (Simple Notification Service):** A publish/subscribe (pub/sub) service. A "publisher" sends a message to an SNS **topic**, and SNS immediately pushes that message to all "subscribers" of that topic. It's used for sending time-sensitive notifications to a large number of recipients, such as push notifications to mobile devices, SMS messages, or triggering other AWS services.
