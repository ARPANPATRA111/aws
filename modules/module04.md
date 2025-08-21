# Module 4 — Going Global 🌐

Status: 🟡 In Progress

## The AWS Global Infrastructure Relationship

It's important to understand the relationship between the core components of AWS's global footprint:

* **AWS Regions** are physical locations around the world where AWS clusters data centers.
* **Availability Zones (AZs)** are the multiple, isolated data centers contained within each AWS Region.
* **Edge Locations** are part of a separate, worldwide network outside of the AWS Regions. They are specifically designed to cache content and deliver data with lower latency.

## Choosing an AWS Region

Each **AWS Region** is a separate geographic area, completely isolated from others. When deciding where to deploy your resources, you must consider these **four key factors** in order:

1. **Compliance:** This is the most important factor. If you have data governance or regulatory requirements that mandate your data stay within a specific country's borders, you **must** choose a Region within that country.
2. **Proximity to Customers:** To reduce **latency** (the time it takes for data to travel), choose a Region that is physically close to the majority of your user base. This results in a faster, better user experience.
3. **Feature Availability:** AWS is constantly innovating, and new services or features may roll out to different Regions over time. You must choose a Region where all the services your application requires are available.
4. **Pricing:** Costs can vary between Regions due to factors like local taxes and energy costs. While services may be the same, their pricing can differ.

## Building Redundant Architectures

To ensure your application is stable and has minimal downtime, it's crucial to build for redundancy. The two primary benefits of using multiple Regions and AZs are **high availability/fault tolerance** and **low latency for end users**.

* ### <ins>Multi-AZ Deployments</ins>

A **multi-AZ architecture** involves running your application across multiple **Availability Zones** within a single AWS Region. If one AZ experiences an interruption, your application automatically fails over to a backup AZ. This is a foundational practice for achieving **high availability and fault tolerance**.

* ### <ins>Multi-Region Deployments</ins>

For an even higher level of fault tolerance, you can deploy your application in **multiple AWS Regions**. If an entire Region experiences an interruption, you can failover your operations to another. This strategy is also used to place resources closer to global end users, which **reduces latency**.

## The AWS Global Edge Network

Separate from Regions, AWS operates a worldwide network of **edge locations**. Their primary purpose is to **cache content to deliver data with lower latency and higher transfer speeds to end users**.

* **Amazon CloudFront:** This is a **Content Delivery Network (CDN)** that uses edge locations to cache content like images, videos, and APIs closer to users. When a user requests this content, it's delivered from the nearest edge location instead of the main Region, dramatically speeding up load times.

## Infrastructure as Code (IaC) with AWS CloudFormation

When you need to deploy and manage resources across multiple Regions or accounts, doing so manually is slow and prone to human error. **Infrastructure as Code (IaC)** is the best approach for deployments that require **automation, consistency, and repeatability**.

**AWS CloudFormation** is an IaC service where users can **model and set up their AWS resources using code to automate provisioning and the management of infrastructure**.

* **How it Works:** You define all the resources you need (like servers, databases, and message queues) in a text-based document called a **template**. CloudFormation reads this template and automatically builds your entire environment.
* **Key Benefits:** This method helps **reduce errors and maintain consistency across environments**. By deploying the same template in different Regions, you create identical, error-free setups every time.
