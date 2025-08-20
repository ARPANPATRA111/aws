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
