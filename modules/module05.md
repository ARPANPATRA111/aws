# Module 5 — Networking 🔗

Status: 🟡 In Progress

## What is Networking in AWS?

At its core, networking is a system of **interconnected devices that can exchange data and share resources**. In the AWS Cloud, this is primarily managed through the Amazon Virtual Private Cloud.

### Amazon Virtual Private Cloud (VPC)

An **Amazon VPC** is a service that lets you provision a **logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define**. You have complete control over your virtual networking environment, including your own private IP address range.

Within a VPC, you organize your resources into **subnets**. A subnet is a range of IP addresses that you use to group resources. The primary distinction is between private and public:

* **Public Subnets:** Contain resources, like a web server, that need to be accessible from the internet.
* **Private Subnets:** Contain resources, like a backend database, that should be isolated from users on the internet.
