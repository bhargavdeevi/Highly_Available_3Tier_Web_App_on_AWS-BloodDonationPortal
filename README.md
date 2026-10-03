# Highly Available 3-Tier Web App on AWS-Blood Donation Portal
Deploying website using AWS Services


**Overview**
This project demonstrates the deployment of a scalable, fault-tolerant 3-tier web application on Amazon Web Services (AWS). The infrastructure supports a PHP-based Blood Donation platform, designed with strict security and high-availability best practices using a custom VPC, elastic compute, and a managed relational database.

*   **Application Source Code:** [bhargavdeevi/ltibbhackathon](https://github.com/bhargavdeevi/ltibbhackathon)

**Architecture Highlights**
*   **Networking Tier:** A custom VPC configured across multiple Availability Zones for redundancy. The network topology utilizes public and private subnets, custom route tables, an Internet Gateway, and a NAT Gateway to secure internal resources while allowing necessary outbound internet access.
*   **Compute & Application Tier:** The application logic is hosted on EC2 instances. Incoming user traffic is distributed across these instances using an Application Load Balancer to ensure responsiveness and fault tolerance without exposing backend servers directly to the internet.
*   **Database Tier:** User and donor data is securely stored in a highly available Amazon RDS MySQL database utilizing the `db.t3.micro` instance class. The database is isolated within a private subnet to prevent direct internet access and integrated securely with the application tier.

**Application Features**
*   Secure user registration and authentication workflows.
*   Interactive blood donation scheduling and data entry forms.
*   Real-time donor search and filtering interface displaying donor availability and blood groups.

**Deployment Steps**
1. Clone the repository:
   ```bash
   git clone [https://github.com/bhargavdeevi/ltibbhackathon.git](https://github.com/bhargavdeevi/ltibbhackathon.git)
