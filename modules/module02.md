# Module 2 — Compute in the Cloud 💻

Status: 🟡 In Progress

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

