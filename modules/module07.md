# Module 7 — Databases 💾

Status: 🟡 In Progress

## Relational Databases on AWS

A **relational database** stores data in tables with rigid structures, relating different pieces of data to each other. You interact with these databases using **Structured Query Language (SQL)**.

### Ways to Run Relational Databases on AWS

1. **Unmanaged Solution (on EC2):** You can install a database directly onto an Amazon EC2 instance. This approach is preferable when you need **full control over the database and access to its underlying operating system**, including all installations and configurations.
2. **Amazon RDS (Relational Database Service):** This is a **fully managed service that helps set up, operate, and scale relational databases** in the cloud. RDS automates tasks like patching and backups, freeing you from routine maintenance.
3. **Amazon Aurora:** This is a fully managed, MySQL and PostgreSQL-compatible relational database built for the cloud. It is an excellent choice for **replacing high-cost commercial database engines** with a more cost-effective solution that still provides enterprise-level performance and reliability.
