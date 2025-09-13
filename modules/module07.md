# Module 7 — Databases 💾

Status: 🟡 In Progress

## Relational Databases on AWS

A **relational database** stores data in tables with rigid structures, relating different pieces of data to each other. You interact with these databases using **Structured Query Language (SQL)**.

### Ways to Run Relational Databases on AWS

1. **Unmanaged Solution (on EC2):** You can install a database directly onto an Amazon EC2 instance. This approach is preferable when you need **full control over the database and access to its underlying operating system**, including all installations and configurations.
2. **Amazon RDS (Relational Database Service):** This is a **fully managed service that helps set up, operate, and scale relational databases** in the cloud. RDS automates tasks like patching and backups, freeing you from routine maintenance.
3. **Amazon Aurora:** This is a fully managed, MySQL and PostgreSQL-compatible relational database built for the cloud. It is an excellent choice for **replacing high-cost commercial database engines** with a more cost-effective solution that still provides enterprise-level performance and reliability.

### Migrating Databases

**AWS Database Migration Service (DMS)** is a service designed to help you migrate databases to AWS easily and securely. Its key benefit is **minimizing application downtime**, as the source database remains fully operational during the migration process.

## NoSQL Databases: Amazon DynamoDB

**Amazon DynamoDB** is a **fully managed NoSQL key-value and document database that provides fast, predictable performance with seamless scalability**.

* **Flexible Schema:** The primary way NoSQL databases differ from relational databases is their use of **flexible schema designs rather than rigid table structures**. This is ideal for evolving datasets where not every item has the same attributes.
* **Performance:** DynamoDB is designed for high-traffic applications, offering single-digit millisecond performance at any scale.

## In-Memory Caching: Amazon ElastiCache

**In-memory caching** is a technique that stores frequently used data in memory (RAM) to improve application performance and reduce the need to fetch data from slower, disk-based storage.

**Amazon ElastiCache** is a fully managed in-memory caching service.

* **Primary Benefit:** Its core function is **improved application performance through in-memory caching**. By serving frequent read requests from memory, it reduces latency and offloads the primary database.

## Other Purpose-Built Databases

AWS recommends using purpose-built databases designed for specific workloads.

* **Amazon DocumentDB:** A document database service (MongoDB-compatible) that excels at handling semi-structured data. A practical use case is **storing and managing a large product catalog** for an e-commerce application.

* **Amazon Neptune:** A graph database service designed for **managing and querying highly connected datasets efficiently**, making it ideal for social networks, recommendation engines, and fraud detection.
