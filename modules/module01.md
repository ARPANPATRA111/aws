# Module 1 — Introduction to the Cloud ☁️

Status: ✅ Completed

## A Brief History of AWS

Before it was a cloud provider, Amazon.com was a massive e-commerce site. In the early 2000s, to manage its own scaling challenges, the IT team developed a set of standardized, efficient internal tools. By 2003, they realized these tools could be valuable to other businesses.

This led to the launch of the first AWS service, **Amazon Simple Queue Service (SQS)**, in 2004. It was followed by two foundational services in 2006:

* **Amazon Simple Storage Service (S3)** for data storage.
* **Amazon Elastic Compute Cloud (EC2)** for scalable compute.

What began as an internal solution has since grown into a global cloud computing leader, serving millions of customers from small startups to large corporations and government agencies.

---

## What is Cloud Computing?

Cloud computing is the **on-demand delivery of IT resources over the internet with pay-as-you-go pricing.** Let's break that down:

* **On-Demand Delivery:** You get access to resources like storage or compute power exactly when you need them. There's no need to wait for hardware to be ordered and installed.
* **Over the Internet:** You can access and manage your infrastructure from anywhere in the world with an internet connection, right from your web browser.
* **Pay-as-you-go Pricing:** You only pay for the resources you actually consume, for as long as you use them. When you're done with a resource, you can deprovision it and stop paying immediately. No long-term contracts are required.
* **IT Resources:** Instead of building and maintaining your own physical data centers, you use AWS's infrastructure. This allows your teams to stop managing hardware and focus on innovation and your customers.

---

## The Six Advantages of Cloud Computing

Moving to the AWS Cloud provides six primary advantages over traditional on-premises infrastructure.

### 1. Trade Fixed Expense for Variable Expense

Instead of making large, upfront investments in physical servers and data centers (a fixed cost), you pay only for the resources you consume (a variable cost). This lowers the barrier to entry and allows you to start small and scale.

### 2. Benefit from Massive Economies of Scale

Because AWS buys hardware at a massive global scale, they get significant price reductions from suppliers. AWS passes these savings on to you in the form of lower pay-as-you-go prices.

### 3. Stop Guessing Capacity

In a traditional data center, you have to predict your needs years in advance, often leading to wasted resources (over-provisioning) or poor customer experience (under-provisioning). With the cloud, you provision what you need now and **scale** up or down in minutes as your traffic changes.

### 4. Increase Speed and Agility

You can spin up new resources and entire test environments in minutes. This allows your teams to experiment, innovate, and test new ideas quickly without the risk of high-cost hardware investments. If an experiment fails, you simply delete the resources.

### 5. Stop Spending Money on Data Centers

Focus on your business and customers, not on the "undifferentiated heavy lifting" of running a physical data center—like racking servers, stacking hardware, and managing power. AWS handles all of this for you.

### 6. Go Global in Minutes

Easily deploy your applications in multiple geographic locations around the world with just a few clicks. This allows you to provide lower latency and a better experience for your customers at a global scale, without the expense and time of building data centers overseas.

---

## AWS Global Infrastructure

AWS's infrastructure is designed for **high availability** and **fault tolerance**, ensuring your applications are resilient and always accessible. This is achieved through a multi-layered structure. 

* **Regions:** A **Region** is a physical location in the world where AWS clusters data centers (e.g., Ohio, USA; Paris, France; Tokyo, Japan).
* **Availability Zones (AZs):** Each Region consists of three or more isolated and physically separate **Availability Zones**. An AZ is one or more discrete data centers with redundant power, networking, and connectivity. By running applications across multiple AZs, you can protect them from a single point of failure.
* **Data Centers:** These are the secure buildings that house the physical servers and hardware that run the AWS cloud.

If a disaster (or a simple spilled latte) takes out a single data center, your application can failover to another one within the same AZ. If an entire AZ is affected, it can failover to another AZ in the same Region, ensuring your customers are never impacted.

---

## The Shared Responsibility Model

When it comes to security, responsibility is shared between you and AWS. A helpful analogy is securing a house: AWS builds the strong walls and solid doors, but you are responsible for locking them.

### AWS Responsibility: Security **OF** the Cloud

AWS is responsible for protecting the infrastructure that runs all of the AWS services. This includes:

* **Physical Security** of the data centers.
* **Hardware and Software Infrastructure** (compute, storage, networking).
* **Network Infrastructure** and the **Hypervisor** (virtualization) layer.

### Customer Responsibility: Security **IN** the Cloud

You are responsible for securing the resources you create and the data you put in the cloud. This includes:

* **Customer Data:** You control who can access your data and are responsible for encrypting it.
* **Platform, Applications, and Operating System:** You are responsible for patching the OS, managing user access, and securing your applications.
* **Network and Firewall Configuration:** You control your own network access rules, like who can send traffic to your instances.