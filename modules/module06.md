# Module 6 — Storage 🗄️

Status: 🟡 In Progress

## Core AWS Storage Categories

AWS offers different storage solutions because not all data is the same. Just as you'd use different containers for coffee beans and paperwork, you need different digital storage for different data types.

* **Block Storage:** Provides persistent storage volumes for use with Amazon EC2 instances. It's ideal for applications that need consistent, low-latency performance, like a high-performance transactional database.
* **Object Storage:** A scalable service used to store and retrieve any amount of data from anywhere on the web. It's best for files that don't change constantly, like images, videos, backups, and logs.
* **File Storage:** A fully managed service that provides cost-effective, scalable file storage built on widely used file systems. It's ideal for applications that require shared access, like a content management system.

## Block Storage for EC2: Instance Store & Amazon EBS

### Amazon EC2 Instance Store

An **EC2 instance store** provides **temporary** block-level storage that is physically attached to the host computer. This offers the **highest possible I/O performance** but is **ephemeral**, meaning all data is lost when the instance is stopped or terminated. It's best used for temporary datasets, like for model training.

### Amazon Elastic Block Store (EBS)

**Amazon EBS** is a **block-level storage service that provides persistent storage volumes for Amazon EC2 instances**.

* **Persistence:** Data written to an EBS volume persists even if you stop, restart, or terminate the EC2 instance. The volumes can be attached to and detached from instances as needed and resized independently.
* **Performance:** EBS provides consistent low-latency performance, with different volume types optimized for various workloads.
* **EBS Snapshots:** These are point-in-time copies of EBS volumes used for regular data backups. They are a cost-effective solution for a **disaster recovery strategy** and for creating duplicate environments for testing.
