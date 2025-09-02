# Module 5 — Networking 🔗

Status: 🟡 In Progress

## What is Networking in AWS?

At its core, networking is a system of **interconnected devices that can exchange data and share resources**. In the AWS Cloud, this is primarily managed through the Amazon Virtual Private Cloud.

### Amazon Virtual Private Cloud (VPC)

An **Amazon VPC** is a service that lets you provision a **logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define**. You have complete control over your virtual networking environment, including your own private IP address range.

Within a VPC, you organize your resources into **subnets**. A subnet is a range of IP addresses that you use to group resources. The primary distinction is between private and public:

* **Public Subnets:** Contain resources, like a web server, that need to be accessible from the internet.
* **Private Subnets:** Contain resources, like a backend database, that should be isolated from users on the internet.

### Availability Zones (AZs)

An **Availability Zone** is a physically isolated data center or set of data centers within an AWS Region. Its primary function is to **enhance application availability and fault tolerance** by allowing you to deploy resources across multiple, redundant locations within the same Region.

## Connecting to Your VPC

### Gateways for VPC Access

* **Internet Gateway:** This is the "front door" to your VPC, allowing communication between resources in your public subnets and the internet.
* **Virtual Private Gateway:** This is a private "door" used to establish a secure, private connection between your on--premises network and your VPC. It is the VPN endpoint on the AWS side of the connection.

### Dedicated and VPN Connectivity

* **AWS Direct Connect:** This service establishes a **dedicated private connection** from your on-premises network to an Amazon VPC. It's the best choice when you need a consistent network experience with **increased bandwidth**.
* **AWS Site-to-Site VPN:** This is a cost-effective solution that creates a **secure, encrypted connection** between your on-premises sites (like data centers or branch offices) and your Amazon VPC over the public internet.
* **AWS Client VPN:** A fully managed service for connecting your **remote workforce** to your AWS and on-premises resources. It provides advanced authentication and automatically scales based on user demand.

## Securing Your VPC Network

### Shared Responsibility for Networking

Based on the AWS Shared Responsibility Model, the customer is responsible for **securing network traffic within their VPC**. This is primarily done using Network ACLs and Security Groups.

### Network Access Control Lists (Network ACLs)

* **Role & Scope:** Acts as a firewall for controlling traffic in and out of one or more **subnets**. It's your first line of defense.
* **Rules:** You can set up both **allow and deny** rules for broad traffic control.
* **State:** Network ACLs are **stateless**. They check every packet that crosses the subnet boundary (inbound and outbound) without remembering previous traffic.

### Security Groups

* **Role & Scope:** Acts as a virtual firewall for your **EC2 instances** to control inbound and outbound traffic at the instance level.
* **Rules:** You can only set up **allow** rules. By default, all inbound traffic is denied.
* **State:** Security Groups are **stateful**. If you allow incoming traffic, the corresponding outgoing (return) traffic is automatically allowed, regardless of outbound rules.

## Edge Networking & Content Delivery

### Amazon Route 53

**Amazon Route 53** is a highly available and scalable **Domain Name System (DNS)**. Its primary function is to **translate human-readable domain names** (like `www.mycompany.com`) into machine-readable IP addresses. It can also be used to manage domain registrations and route internet traffic to your resources.

### Amazon CloudFront

**Amazon CloudFront** is a **Content Delivery Network (CDN)** designed to deliver static content (like training videos) and dynamic content with **low latency**. It securely delivers content through a worldwide network of data centers called edge locations.

### AWS Global Accelerator

**AWS Global Accelerator** is a networking service that improves the **availability and performance** of your applications for global users. It provides static IP addresses and directs traffic over the AWS global network to optimal endpoints based on health, user location, and your configured policies. This is the best solution for traffic routing when something goes wrong in one of your application's locations.

## Summary

This module covered AWS networking fundamentals. You learned how to create an isolated network using **Amazon VPC** with **public and private subnets**. You explored various connection methods, including **Virtual Private Gateways**, **Direct Connect**, and **VPN** services. You also learned to secure network traffic using stateless **Network ACLs** at the subnet level and stateful **Security Groups** at the instance level. Finally, you saw how edge networking services like **Route 53**, **CloudFront**, and **Global Accelerator** work to route users and deliver content globally with high performance and availability.
