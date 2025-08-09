# Module 2 — Compute in the Cloud 💻

Status: 🟡 In Progress

## Key Concepts

- **Virtual Machines (Servers):** At its core, cloud compute involves renting virtual servers, known as **instances**, from a cloud provider. This eliminates the need to buy and manage physical hardware.

- **Amazon EC2 (Elastic Compute Cloud):** This is the primary AWS service for providing secure, resizable compute capacity (virtual servers) in the cloud. It's designed to make web-scale cloud computing easier for developers.

## EC2 Components

- **Instance Types:** EC2 offers a wide variety of instance types optimized for different tasks. They are grouped into families:
  - **General Purpose (e.g., T-family, M-family):** Balanced CPU, memory, and networking. Good for web servers and code repositories.
  - **Compute Optimized (e.g., C-family):** High-performance processors. Ideal for compute-intensive tasks like scientific modeling, high-performance computing (HPC), and dedicated gaming servers.
  - **Memory Optimized (e.g., R-family, X-family):** Large memory capacity for processing large datasets in-memory, such as high-performance databases or real-time big data analytics.
  - **Storage Optimized (e.g., I-family, D-family):** High-performance local storage. Suited for data warehousing, distributed file systems, and database workloads that require high sequential read/write access to very large data sets.

- **Amazon Machine Images (AMIs):** An AMI is a pre-configured template required to launch an EC2 instance. It includes the operating system (e.g., Linux, Windows), software packages, and other required settings. You can use AMIs from AWS, the community, or create your own.

## EC2 Pricing Models

- **On-Demand:** Pay a fixed rate by the hour (or second) with no long-term commitment. Ideal for applications with short-term, spiky, or unpredictable workloads.
- **Reserved Instances (RIs) & Savings Plans:** Provide a significant discount (up to 72%) compared to On-Demand pricing in exchange for a commitment to a 1-year or 3-year term. Best for applications with steady-state or predictable usage.
- **Spot Instances:** Request spare EC2 computing capacity for up to 90% off the On-Demand price. These instances can be interrupted by AWS with a 2-minute notice, making them suitable for fault-tolerant and flexible applications, like batch jobs or data analysis.

## Serverless Compute

- **AWS Lambda:** A serverless compute service that lets you run code without provisioning or managing servers. You write your code (a "Lambda function") and Lambda handles the infrastructure to run and scale it. You only pay for the compute time you consume.