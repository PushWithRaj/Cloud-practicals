# Practical 1: Introduction to Cloud Platforms

## Aim
To familiarize students with the major Public Cloud Service Providers (CSPs)—Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP)—and to navigate their management consoles, core services, and pricing models.

## Theory
- Cloud computing platforms provide on-demand delivery of IT resources via the internet with pay-as-you-go pricing.
- Instead of buying and maintaining physical data centers, users access technology services such as computing power, storage, and databases.

### Leading Cloud Providers
* **AWS (Amazon Web Services):** The most mature platform, offering a vast array of global services.
* **Microsoft Azure:** Deeply integrated with Microsoft software and enterprise environments.
* **GCP (Google Cloud Platform):** Known for high-performance computing, data analytics, and machine learning.

## Account screenshot
<img width="1347" height="427" alt="a1" src="https://github.com/user-attachments/assets/67d164d0-609c-4cec-a78b-ab198b31ac1d" />

## Core Service Categories
* **Compute:** Virtual servers that process data (e.g., EC2, Virtual Machines).
* **Storage:** Systems to save and retrieve data (e.g., S3, Blob Storage).
* **Networking:** Tools to connect cloud resources (e.g., VPC, Virtual Networks).
* **Identity and Access Management (IAM):** Security frameworks for user permissions.

### Resource Identification Table
| Service Category | AWS Service | Azure Service | GCP Service |
| :--- | :--- | :--- | :--- |
| Virtual Servers | Amazon EC2 | Azure Virtual Machines | Compute Engine |
| Object Storage | Amazon S3 | Azure Blob Storage | Cloud Storage |
| Database (SQL) | Amazon RDS | Azure SQL Database | Cloud SQL |
| Networking | Amazon VPC | Azure Virtual Network | VPC Network |
| Serverless | AWS Lambda | Azure Functions | Cloud Functions |


## Operational Flowchart
```mermaid
graph TD
    A[Start] --> B[Create Free Tier Account]
    B --> C{Account Verification}
    C -->|Success| D[Access Management Console/Dashboard]
    C -->|Failure| B
    D --> E[Navigate to Service Menu]
    E --> F[Explore Compute, Storage & Network]
    F --> G[Access Pricing Calculator]
    G --> H[Estimate Resource Costs]
    H --> I[End/Documentation]
```

### Configuration Parameters for Free Tier

| Platform | Validation Method | Key Free Tier Limit |
| :--- | :--- | :--- |
| AWS | Credit/Debit Card | 12 Months (750 hours EC2/mo) |
| Azure | Credit/Debit Card | 12 Months + Initial Credits |
| GCP | Credit/Debit Card | 90 Days + $300 Credit |
## Conclusion
The fundamental interfaces and service hierarchies of AWS, Azure, and GCP were successfully explored. The exercise established an understanding of how to manage cloud resources and utilize cost-estimation tools to maintain budget compliance.  
