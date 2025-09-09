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

## Object Storage: Amazon S3

**Amazon Simple Storage Service (S3)** is a **scalable object storage service that is used to store and retrieve any amount of data from anywhere on the web**.

* **Use Cases:** Ideal for storing and distributing large collections of media files (images, videos), hosting static websites, and managing backups. It offers high durability, easy file sharing through URLs, and security controls.
* **S3 Storage Classes:** The primary function of S3 storage classes is to **provide different storage options optimized for different use cases and access patterns**. Their pricing varies based on storage costs, retrieval fees, and minimum storage durations.

## Shared File Systems: Amazon EFS & Amazon FSx

### Amazon Elastic File System (EFS)

**Amazon EFS** is a **fully managed, elastic file system that scales automatically as files are added and removed**. It is a centralized storage solution that allows **multiple EC2 instances to access the same file system simultaneously**, making it perfect for Linux-based applications that need shared, low-latency access.

### Amazon FSx

**Amazon FSx** is a **fully managed service that provides cost-effective, scalable file storage built on widely used file systems** like Windows File Server, Lustre, and OpenZFS.

* **Amazon FSx for Windows File Server** is the best choice for migrating existing file shares for Windows applications. It supports the SMB protocol, offers Active Directory integration, and provides features like data deduplication.

## Hybrid Cloud & Disaster Recovery

### AWS Storage Gateway

**AWS Storage Gateway** is a **hybrid cloud storage solution that provides on-premises applications with access to virtually unlimited cloud storage**.

* **File Gateway** is a specific configuration that provides a seamless path to cloud storage without disrupting current operations. It maintains low-latency local access to frequently used files by caching them on-premises.

### AWS Elastic Disaster Recovery

This is a service that **minimizes downtime and data loss by providing fast, reliable recovery of on-premises and cloud-based applications**. It uses affordable storage, minimal compute, and point-in-time recovery to protect your critical workloads.

## Summary

This module covered AWS's core storage services. You learned the difference between **block (EBS)**, **object (S3)**, and **file (EFS, FSx)** storage. You explored how **EBS** provides persistent block storage for EC2 instances and can be backed up with **snapshots**. You saw how **S3** offers durable, scalable object storage with different **storage classes** for cost optimization. You also learned how **EFS and FSx** provide managed shared file systems, and how **Storage Gateway** bridges on-premises environments with AWS cloud storage.

## Resources

| Resource link | Description |
| :--- | :--- |
| [Amazon EC2 Instance Store User Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) | A temporary storage option that is directly attached to the host computer of an EC2 instance. |
| [Amazon Elastic Block Store (Amazon EBS)](https://aws.amazon.com/ebs/) | A scalable block storage service that provides persistent, high-performance volumes for EC2 instances. |
| [Amazon Elastic Block Store (Amazon EBS) FAQ](https://aws.amazon.com/ebs/faqs/) | Frequently asked questions about Amazon EBS. |
| [Amazon EBS Snapshots User Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html) | Point-in-time backups of your cloud storage volumes for data protection and restoration. |
| [Amazon Data Lifecycle Manager User Guide](https://docs.aws.amazon.com/dlm/latest/userguide/what-is-dlm.html) | A service that streamlines the creation, retention, and deletion of Amazon EBS snapshots. |
| [Amazon Simple Storage Service (Amazon S3)](https://aws.amazon.com/s3/) | A scalable cloud storage service that can store and retrieve any amount of data from anywhere. |
| [Amazon Simple Storage Service (Amazon S3) FAQ](https://aws.amazon.com/s3/faqs/) | Frequently asked questions about Amazon S3. |
| [Amazon S3 Storage Classes](https://aws.amazon.com/s3/storage-classes/) | Various storage classes tailored to different data retrieval needs and budget constraints. |
| [Amazon S3 Versioning User Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html) | Keeps multiple variants of objects, offering recovery from unintended deletions or modifications. |
| [Amazon S3 Buckets User Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBuckets.html) | Cloud storage containers that securely hold various types of data. |
| [Amazon Elastic File System (Amazon EFS)](https://aws.amazon.com/efs/) | A scalable, fully-managed file storage service for shared data access. |
| [Amazon Elastic File System (Amazon EFS) FAQ](https://aws.amazon.com/efs/faqs/) | Frequently asked questions about Amazon EFS. |
| [Amazon FSx](https://aws.amazon.com/fsx/) | A fully managed file storage service for file systems like Windows File Server, Lustre, and more. |
| [Amazon FSx for Windows File Server](https://aws.amazon.com/fsx/windows/) | Provides reliable, high-performance file storage compatible with Windows applications. |
| [Amazon FSx for NetApp ONTAP](https://aws.amazon.com/fsx/netapp-ontap/) | File storage with advanced data management capabilities for Windows and Linux workloads. |
| [Amazon FSx for OpenZFS](https://aws.amazon.com/fsx/openzfs/) | High-performance, scalable storage using the popular open-source ZFS file system. |
| [Amazon FSx for Lustre](https://aws.amazon.com/fsx/lustre/) | Designed to accelerate workloads by providing fast data access for compute-intensive applications. |
| [AWS Storage Gateway](https://aws.amazon.com/storagegateway/) | A hybrid cloud storage service for seamless on-premises and cloud integration. |
| [Amazon S3 File Gateway](https://aws.amazon.com/storagegateway/file/) | Provides local file access to S3 objects while caching frequently accessed data locally. |
| [Tape Gateway](https://aws.amazon.com/storagegateway/tape/) | Used for backing up data to Amazon S3 while maintaining compatibility with tape-based backup applications. |
| [Volume Gateway](https://aws.amazon.com/storagegateway/volume/) | Provides iSCSI block storage volumes to on-premises applications. |
