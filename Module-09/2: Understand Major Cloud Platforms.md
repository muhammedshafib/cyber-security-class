# Module 2: Understand Major Cloud Platforms ☁️

Complete study notes for exam preparation, explained in simple English with examples, comparisons, important points, and exam questions.

## 1. Cloud Ecosystem Overview

### What is a cloud ecosystem?

A cloud ecosystem is a collection of cloud providers, computing resources, services, tools, developers, customers, and technologies that work together to build, run, and manage applications over a network.

In simple words, a cloud ecosystem is the complete environment that helps a business build and operate its applications without managing every physical computer itself.

### Major cloud platforms

[Amazon Web Services International Admissions – Global Admissions](https://images.openai.com/static-rsc-4/0rQcC42SpGzIZ4x_9S_kmX_8SUFk0MtLf7nSdeII-EzN-3M7An3E3dTLSrDBsajnhNSFLPuLUn3eSeq2Z0_WGNP5hdgqy_y0QWEC1c2cDp_YjZIWb8T95da2NYHq7c18pC5M5MS47GV7jBPlnHfl_hYNe38_vHKIBzDN17ZFQ74?purpose=inline)

1\. Amazon Web Services (AWS)

A widely used cloud platform offering computing, storage, networking, databases, security, analytics, and many other services.

- Compute: Amazon EC2
- Storage: Amazon S3
- Networking: Amazon VPC
- Managed database: Amazon RDS

[Cloudbizz - Votre Partenaire Cloud Global](https://images.openai.com/static-rsc-4/fabJ2nNUuTBse-DEG0vwKt5ic--g7aEix7PzEsuiK7fmV6aSnjZr4f9-4-3ZwocckzPOWTozgA9hdeCeME7-1RkQ_G5MomMaqRXQe1lWRESTrifgxCC9kt0RxWuJ8kCTF3UU8AgFdk4o3yhpzbzfkAC9x804jxcw5FUJfn6N0aQ?purpose=inline)

2\. Microsoft Azure

A cloud platform that integrates with Microsoft technologies and supports enterprise applications, virtual machines, networking, databases, and AI.

- Compute: Azure Virtual Machines
- Storage: Azure Blob Storage
- Networking: Azure Virtual Network
- Managed database: Azure SQL Database

[Spain’s CaixaBank partners Google Cloud to drive digitalisation](https://images.openai.com/static-rsc-4/0zPM0jKMDAUUgrocNQVKdPhj1Ua2atgQ5AghbZVejV9e1SuHshSXw88P3cZk--7F7GOl_izaOR_W8vX8XRx2M6Hh6FNciREXQrqj8zcnbF2r9BBtyjR_DRxo-IbXWBWgGAvPhDPbb0Zzto6IZ79rzKBtxM7fZPf1TDzOvaA16Yk?purpose=inline)

3\. Google Cloud

A cloud platform known for services covering computing, data analytics, machine learning, application hosting, and networking.

- Compute: Compute Engine
- Storage: Cloud Storage
- Networking: Virtual Private Cloud (VPC)
- Managed database: Cloud SQL

### Main components of a cloud ecosystem

Users and applications

Websites, mobile apps, business systems

Cloud services

Compute · Storage · Networking · Managed services

Cloud infrastructure

Physical servers, disks, networks, and data centers

Security, identity management, monitoring, and billing support all these layers.

### Why are cloud platforms important?

- They provide computing resources on demand.
- They allow businesses to deploy applications quickly.
- They provide storage for large amounts of data.
- They help organizations manage security and access.
- They support backup, recovery, and global access.
- They offer tools for monitoring costs and performance.

Example: An online shopping website may use cloud computing to run its website, cloud storage to store product images, a managed database to store orders, and cloud networking to connect the components securely.

### Cloud platform service comparison

The following table helps you remember the main services across the three major platforms. These service categories and equivalents are documented by Google Cloud.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.cloud.google.com\&sz=32)

Google Cloud Documentation

+2



| Service category            | AWS    | Microsoft Azure        | Google Cloud        |
| --------------------------- | ------ | ---------------------- | ------------------- |
| Virtual machines            | EC2    | Azure Virtual Machines | Compute Engine      |
| Object storage              | S3     | Blob Storage           | Cloud Storage       |
| Private networking          | VPC    | Virtual Network (VNet) | VPC                 |
| Managed relational database | RDS    | Azure SQL Database     | Cloud SQL           |
| Serverless functions        | Lambda | Azure Functions        | Cloud Run functions |

Exam point: The platforms provide similar types of services, but their features, pricing, configuration, and management tools differ.

## 2. Compute Services

### What are compute services?

Compute services provide the processing power required to run applications, websites, programs, and operating systems.

In simple words, compute is the part of the cloud that does the actual work of running your software.

For example, when you open an online shopping website, compute resources process your requests, execute application code, and communicate with databases.

### Types of compute services

[What is Server Virtualization and How Does it Work? | Cherry Servers](https://images.openai.com/static-rsc-4/aFBl8tunfnevFP98xvcsH4R0Ypi6vMUTXZzWD625HKFLuPJIiBF68WUkxw9WN2qeXgKweAEI6orKbdL7F-Ve_p14UTtYKCkcW2u13dtDtjl7bICjql25jEo3gBHYrWinrbIVH4VVir0zWt7jon7D9ga0pEaoT4VSAQIwaVW7W1U?purpose=inline)

1\. Virtual machines (VMs)

A virtual machine is a software-based computer with its own operating system and allocated resources.

- Examples: Amazon EC2, Azure Virtual Machines, Google Compute Engine.
- Uses: Hosting websites, running applications, and managing custom operating systems.
- Main advantage: High control over the operating system and software.

[Introduction to Docker, Containers, and Virtualization | by Michael Maurice | Medium](https://images.openai.com/static-rsc-4/0C6pRkOiruzFU-aF5wu1zrLPCgBFt4rwSWhDSR5CmSdDalEi24RBhJDbKekycnB0F7__LxBa-0FIHAlKuu-vrSsZ0CX2_iSSDMXC0FYz7yFbYq5KiTA9tgc88Oa-YDXGTYdAapC4B90G-H4Q4bPukA3lMslPAt4s5V7Gz7CfjaE?purpose=inline)

2\. Containers

Containers package an application and its dependencies into an isolated, portable environment.

- Examples: Docker containers managed using Amazon ECS, Amazon EKS, or Azure Kubernetes Service.
- Uses: Microservices, application deployment, and consistent development environments.
- Main advantage: Lightweight and portable compared with running a separate full operating system for each application.

[Serverless Computing Explained: Event-Driven Architecture with AWS Lambda & Azure Functions | by Alfatah Jalalludin | Mar, 2026 | Medium](https://images.openai.com/static-rsc-4/eQzChaDjb_vXn3opu-eT1GPiHQbARk291xe24oISGm1pGYYlV6M-UX7Vfzi1fwayx0NjeZQc5xbbaHh_Ozghxevbg3cmUohViHExA2B-eQr5E2_lCy8W2leK4QYvv5QYDOM7RTqLPmJDFej0rX1Rwq5pe_LLwwaPIyFJOks6Z8k?purpose=inline)

3\. Serverless computing

Serverless lets developers run code without directly managing the underlying servers.

- Examples: AWS Lambda, Azure Functions, Google Cloud Run functions.
- Uses: Processing uploaded files, responding to web requests, and automating tasks.
- Main advantage: The provider manages much of the infrastructure; pricing is often based on requests and resource usage.

[From Localhost to Production: The Fastest Way to Ship Your Web App | by Dr. Fadi Shaar | TechSync | Apr, 2026 | Medium](https://images.openai.com/static-rsc-4/oapD02vqSpuQePcl3HqEjeLw-wGqrI64NJucGIL5jVskqyvvOSvRKhG4UgRxJOlbt4oHGQ-JSM5ucgh6JfVATfd6pkVRtH_V0roPeBOOCoFxmRyD1Y5QbJOdirHKdLfND6dXmw1JTOYaNAVZ11gLactXOTRNuLS_qaiCqpvumDA?purpose=inline)

4\. Managed application platforms

These services provide a managed environment for deploying and scaling applications.

- Examples: Azure App Service, Google App Engine, AWS Elastic Beanstalk.
- Uses: Hosting websites and web applications.
- Main advantage: Less infrastructure management for developers.

### How compute services work

1. A user sends a request to an application.
2. The cloud compute service runs the required program.
3. The program processes the request and may access a database or storage service.
4. The result is returned to the user.

### Important compute concepts

- CPU: Executes program instructions.
- RAM: Temporarily holds data that programs need while running.
- Virtualization: Creates virtual computing environments on physical hardware.
- Auto-scaling: Automatically adds or removes resources according to demand and configured rules.
- Load balancing: Distributes incoming traffic among multiple servers or application instances.
- High availability: Uses appropriate redundant resources and architecture to reduce service interruptions.

### VM vs containers vs serverless

| Feature       | Virtual machines | Containers                                          | Serverless                      |
| ------------- | ---------------- | --------------------------------------------------- | ------------------------------- |
| Main unit     | Virtual computer | Packaged application                                | Function or managed workload    |
| OS management | Usually customer | Host infrastructure managed by provider or operator | Mostly provider                 |
| Startup       | Often slower     | Usually faster                                      | Depends on service and workload |
| Control       | High             | Moderate to high                                    | Lower infrastructure control    |
| Example       | Amazon EC2       | Amazon ECS                                          | AWS Lambda                      |

Remember: VMs provide control, containers provide portability, and serverless reduces infrastructure management. Serverless does not mean that physical servers do not exist.

## 3. Storage Services

### What are cloud storage services?

Cloud storage services allow users and organizations to store, retrieve, manage, and protect data using cloud infrastructure instead of relying only on local hard disks.

Examples of stored data include photos, documents, videos, databases, application files, and backups.

### Types of cloud storage

[Storage Buckets Demystified: How the Cloud Stores Your World - DEV Community](https://images.openai.com/static-rsc-4/oIQSDoxqaD8aWx-EbtZniQbjbwdt31NTQ7DIaxBTWjwfhMfJQuxTKe-G78_mOlMhr-essRZee-1B_4jegE4BFdaoH9ReU61xIJyBVsKpRP--Zn7NFC1XzlWyGcO3jUtzjHlZyt-Ysua2zBFnElXq-pkoR9QD_H8e-s3aXBHJ8jE?purpose=inline)

1\. Object storage

Stores data as individual objects containing data, metadata, and a unique identifier.

- Best for: Photos, videos, documents, backups, and large datasets.
- Examples: Amazon S3, Azure Blob Storage, Google Cloud Storage.
- Easy example: A bucket containing thousands of product images.

[SQL Cluster Issues with Storage Spaces Direct - (S2D)](https://images.openai.com/static-rsc-4/Js8RlMKB03AWJtJwctyho269Dn0nkDQUGRc26XeS7P1QU_pObjzb0y5yKU2oVZtervC-pIzNltpRkek8t_vC5TwueFrdtHO5Na9IZ5D2b_Gj8lehvUhZS0sBp8l9xTtnT31iCNMG-706qx4-x7U1dNe_Ej3KPKu7ieB_U3wkXE4?purpose=inline)

2\. Block storage

Divides data into blocks and presents them as storage volumes that computers or virtual machines can use.

- Best for: Operating systems, virtual machine disks, and high-performance databases.
- Examples: Amazon EBS, Azure Managed Disks, Google Persistent Disk.
- Easy example: A virtual server's main hard disk.

[Network File System (NFS) in Linux](https://images.openai.com/static-rsc-4/nRJ_6JKuATy_a0RazZNE-EmpFb2nkUK2eCw-7AK3a15Dmo2OCvR_PICdL_wp4k7unytp0mcc9sofPoRI2skUwEPqU9-e06UESobvS3cciEvuJS7ZFGWMnd_TyNHDNCz1XwyAUb6GE-QHRJGEcbkaZc6dR3hbhCH8xcANrfVCP3c?purpose=inline)

3\. File storage

Organizes data into files and folders, similar to a computer's file system.

- Best for: Shared documents, team folders, and applications that need shared file access.
- Examples: Amazon EFS, Azure Files, Google Filestore.
- Easy example: A shared company folder accessed by multiple servers.

[Why Data Backup Matters for Business Continuity](https://images.openai.com/static-rsc-4/tVV4sG491QDfDj6276llp7w4Z8G8ibMfjX3-Zd1jXz8uDlKsPZ70ToyAj7enAO-4HciTIGBxgW9yndM71CVjmXareh3q-lOrF0YZVZ0fpVJzM_YiTDMn6shKpLdwIgcmtBeCfjnFcpHyB8acsoB26Ypq_TsElrcSm5fFjanhwZg?purpose=inline)

4\. Backup and archive storage

Protects data for recovery or keeps it for long-term retention. Archive options are often designed for data that is rarely accessed.

- Best for: Disaster recovery, old records, and long-term backups.
- Examples: Amazon S3 Glacier storage classes and Azure Blob Archive.
- Easy example: Keeping copies of company records in case the original data is lost.

These storage types serve different purposes and are supported by the major cloud platforms.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://cloud.google.com\&sz=32)

Google Cloud

+2



### Comparison of storage types

| Feature      | Object               | Block                       | File                 |
| ------------ | -------------------- | --------------------------- | -------------------- |
| Organization | Objects and metadata | Data blocks                 | Files and folders    |
| Common use   | Media and backups    | VM disks and databases      | Shared folders       |
| Main benefit | Large-scale storage  | Performance and low latency | Familiar file access |
| Example      | Amazon S3            | Amazon EBS                  | Amazon EFS           |

### Important storage concepts

- Durability: How well data is protected against loss over time.
- Availability: How readily data can be accessed when needed.
- Redundancy: Keeping additional copies or using multiple storage resources to improve resilience.
- Replication: Copying data to another location or resource.
- Encryption: Protecting stored data so unauthorized parties cannot easily read it.
- Lifecycle management: Automatically changing storage tiers or deleting data according to defined rules.
- Versioning: Keeping multiple versions of a file or object to help recover from accidental changes or deletions.

### Example

A college stores student photographs in object storage, runs its student management system on virtual machines, uses block storage for the servers' disks, and keeps backups for disaster recovery.

Security reminder: Cloud storage is not automatically safe just because a provider hosts it. Correct permissions, encryption, backup policies, and access monitoring are important.

## 4. Networking Services

### What are cloud networking services?

Cloud networking services connect cloud resources to each other, to users, and to external networks. They help control traffic, improve performance, and protect applications.

In simple words, networking is the system of roads that lets data travel between cloud computers and users.

### Major networking services

[Secure Cloud Architecture - OWASP Cheat Sheet Series](https://images.openai.com/static-rsc-4/u4Tubki2sQirW3v3R6Vv3jlyoa-D-dpFOQhY26cnnRYX-KCTCIKFQoCLeBsVz34gTXcmhCKvKKl9LFWtR0fchf050J686oAAvA_I1mFkJKfZP3veOFnSSrApl0zpUvitZAmTpAoQmR9cmibLHFhlcpYjxxVc5VLcmHLhw5mt1yQ?purpose=inline)

1\. Virtual Private Cloud (VPC)

A logically isolated network environment where cloud resources can communicate according to configured network rules.

- AWS: Amazon VPC
- Azure: Azure Virtual Network (VNet)
- Google Cloud: Virtual Private Cloud
- Purpose: Organize resources into private networks and control connectivity.

[Load Balancing in Cloud Computing | by Preeti Raul | Medium](https://images.openai.com/static-rsc-4/AE-fOmeqvWsJgFsa35P_qCNDB9pUC25PuQjy-S1G00AXDGLlELOCSwHgDItJ0oLvAoeNGeaFoR6-BmULfWzj8n2GKzcfhjFT2tE70QqOZOj2anX63FfGYnFqys5QlKCsOGc-uqhG2v6Bedfn92fT9PimTtCHjGu2VnVtZi2UdiM?purpose=inline)

2\. Load balancing

Distributes incoming requests across multiple servers or application instances.

- AWS: Elastic Load Balancing
- Azure: Azure Load Balancer
- Google Cloud: Cloud Load Balancing
- Purpose: Improve availability and distribute workloads.

[How the Internet Actually Works: From Browser to Server (Beginner-Friendly) | by Rishab Nitin Tiwari | Medium](https://images.openai.com/static-rsc-4/mUEmfONF8EKLOPHI6GSl1P3M8lP-L-WbPPSQVwsK7ZchngnCv6Abl8GDaGppKibsc_ijJ87w2Onp4IJNcSx3ZTOgUfsuxSP0kvvZlaeV76bpX0VpTT-jPkRMPigdpl_y1FzYMjsTKXQviTeu_qJxKpOvSLzCJ4GVGnjYJKjHwdM?purpose=inline)

3\. DNS (Domain Name System)

Translates domain names into the network information needed to locate services.

- AWS: Amazon Route 53
- Azure: Azure DNS
- Google Cloud: Cloud DNS
- Purpose: Help users reach websites through domain names instead of remembering IP addresses.

[What Is a CDN and How Does It Work?](https://images.openai.com/static-rsc-4/g5SPo4omk6uscSzCQQAlfyUHXNyTI5JbKZ_Wi5aYGZweDL8pcEhqy8hr96b6DztE8a-JdoUEVYwlI7Qjubwd39q_G5sdOyQf4132wsNF8xVlrJiFfnOAzwZlRjqRFKVm751xosjyv8mESQJL4H8Q8BsHsT1T6kq0iFTMyhjqOus?purpose=inline)

4\. Content Delivery Network (CDN)

Delivers cached content through distributed locations closer to users.

- AWS: Amazon CloudFront
- Azure: Azure Front Door
- Google Cloud: Cloud CDN
- Purpose: Reduce loading times for supported content and improve delivery performance.

[Cloud Firewalls Explained for Cloud Security](https://images.openai.com/static-rsc-4/zks2D6qSaE2l9MjytKuP9Q0M9muresYnaLBiU8fmOskQS-puJotm00T4W45Cqd9cdG3WAyfHmBtb75mTBXfeFyMWYR2ke4TeyAoXKGZOtqefsJtlEp7cCgP35zGseL4IXe3IdJSkaPavkV3W2c8bqqmcSp4UgxqGeLpBABlJWeU?purpose=inline)

5\. Firewalls and network security

Control permitted network traffic using security rules and policies.

- AWS: Security groups, network ACLs, AWS Network Firewall
- Azure: Network Security Groups, Azure Firewall
- Google Cloud: VPC firewall rules, Cloud NGFW
- Purpose: Reduce unauthorized access and protect network resources.

[6 Types of VPN: What They Are and How to Choose](https://images.openai.com/static-rsc-4/itXsqZxj5cGgNV-BUVUTkhVUkpSIaq0MNsNu7178H9-oEohvvEcla5qcML1lGPSqR0cnSoOGOrYFk6W_eY17e24O76zJGi5yDBYSrmI4NtjOn3IF4HA--P-og_qbedOCWrzM3fXgfkQR8Hku5jdU8WK2lHgZDjuT8FBq28c0F90?purpose=inline)

6\. VPN and private connectivity

Connects company networks to cloud environments through encrypted tunnels or dedicated network connections.

- AWS: AWS Site-to-Site VPN, Direct Connect
- Azure: Azure VPN Gateway, ExpressRoute
- Google Cloud: Cloud VPN, Cloud Interconnect
- Purpose: Connect offices and on-premises systems to cloud resources.

These services correspond to documented networking categories across the major providers.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://learn.microsoft.com\&sz=32)

Microsoft Learn

+2



### How cloud networking works

User's browser

Requests a website

DNS and CDN

Resolves the name and may serve cached content

Firewall and load balancer

Applies traffic rules and distributes requests

Application servers inside a cloud network

Processes the request and returns a response

This is a simplified example. Actual network paths depend on the application's architecture and configuration.

### Important networking terms

- IP address: A numerical address used to identify a network interface.
- Subnet: A smaller network division within a larger IP network.
- Routing: Deciding where network traffic should go.
- Latency: The time taken for data to travel between points.
- Bandwidth: The capacity of a connection to transfer data.
- Firewall: A security control that filters network traffic.
- VPN: A virtual private network that can create an encrypted connection over an untrusted network.
- DDoS attack: An attempt to overwhelm a service with excessive traffic from multiple sources.

### Why cloud networking is important

1. Connects users to applications.
2. Allows servers and databases to communicate.
3. Separates network environments.
4. Helps control unauthorized traffic.
5. Improves application availability and performance.
6. Connects cloud infrastructure to company offices.

## 5. Managed Services

### What are managed cloud services?

Managed services are cloud services in which the provider operates and maintains significant parts of the underlying technology, allowing customers to focus more on their applications and business requirements.

In simple words, the cloud provider takes care of many routine technical tasks so that you do not have to manage everything yourself.

### Types of managed services

[What is Google Cloud SQL, its Features | Net Solutions](https://images.openai.com/static-rsc-4/Odr4HTDvQnAAFfxdQD7MjelD3jUGaG-xswkxXBeU0Dh4HnVQE3ZpXuadD1AHTDdUEef3zB5_ZguSYDEeKumQZEDpweiiQKRrbzoFvmGvyvMhAUyUs7A1CCcaseSKkGIm7sHTfADsz_-VgI-K_4boaPT9RghJgc2m8h00lhT5Y2k?purpose=inline)

1\. Managed databases

The provider handles tasks such as infrastructure maintenance and, depending on the service, backups, patching, and recovery options.

- AWS: Amazon RDS
- Azure: Azure SQL Database
- Google Cloud: Cloud SQL

Example: An online store saves customer orders in a managed database without manually maintaining its database server hardware.

[Medium](https://images.openai.com/static-rsc-4/YEpDfWuNar8o-S7hdXa5b7_ILoiFqWibM8rszN9QHzz7aqvlFj1v3T4g63AIs0BQ9a-bW-u8QDXNGgdjPoxh5TsNxUHAblb6f2is5q6mIJlbTKdEPUgfGsUaWBx8R4Wvzvzdj-BFja8cRqfG9iq5eXbxO2KXGuPSKRWSM_6Nc4o?purpose=inline)

2\. Monitoring and logging

Collects performance metrics, logs, and alerts to help detect problems.

- AWS: Amazon CloudWatch
- Azure: Azure Monitor
- Google Cloud: Cloud Monitoring and Cloud Logging

Example: An administrator receives an alert when a server's CPU usage remains unusually high.

[Cloud Access Control Explained: Users, Roles, and Permissions](https://images.openai.com/static-rsc-4/lHuMCDqIGxSYD_f1ldRU6UyBFZ7vhJDBUeVueQwKCqwKJFKG7gI_7LEGbxpPc9LcXEz0u8lQaxuRkuIMaf8x2ndp14E4KlD0YD19ouTXxPrdl7TR3xNbyoAkSrHReoEO06TeDZm_huTTCzORb7N9MsNyRfSUN4HLUKH-9EKsCOY?purpose=inline)

3\. Identity and access management (IAM)

Controls who can sign in and what resources they are allowed to access.

- AWS: AWS IAM
- Azure: Microsoft Entra ID and Azure role-based access control
- Google Cloud: Cloud IAM

Example: A developer can manage test servers but cannot access confidential production records.

[data migration tools list: 10 Powerful Picks for 2025 Success](https://images.openai.com/static-rsc-4/Uab3hY26MrQQe3Vchary5jj_SVsLU9rwSKQFcE3rQNP8x2n4Fc5knPhtcd7iN-UxG1RlcR009KW2d5Ng9yjBCx1mEyzN3Mb83GRkJZi1effZF-L3ap3kEWuuj26my2DfInt8I6WXhgUTDXr_XV8NwlhFJiJXOGHwfs78eXAZ7-s?purpose=inline)

4\. Backup and disaster recovery

Provides tools for copying data, creating recovery points, and restoring supported resources.

Example: A business restores a database from a suitable backup after an accidental deletion.

Important: Backups and recovery must be configured, tested, and protected from unauthorized deletion.

[What is container orchestration? | Google Cloud](https://images.openai.com/static-rsc-4/SFOkHyvj_LQQjW8yYak4Fr_IRY0ejAc0d6UVxi2O3d9vL-dzB6SLyTlEahWghzvQIDHsjyDNZSL32Y3GFn0gHOPkRxLN2Mzr_T0n9I2XMU9RRCGu8Q-S7SuetyGqvTijdSCXSHQCuxozBoGrWBC33NNReGXt2IcbRXyV1HGMZ_4?purpose=inline)

5\. Managed container and application platforms

Provide environments for deploying and operating applications with less infrastructure administration.

- AWS: Amazon EKS and AWS Fargate
- Azure: Azure Kubernetes Service
- Google Cloud: Google Kubernetes Engine

Example: A development team deploys a containerized application using a managed Kubernetes service instead of building an entire cluster from scratch.

### Benefits of managed services

- Less routine infrastructure maintenance.
- Faster deployment of applications.
- Access to provider-supported monitoring and automation.
- Easier scaling for supported services.
- More time to focus on application development.
- Access to backup, recovery, and security capabilities.

### Limitations of managed services

- Less control over some infrastructure settings.
- Service charges can increase as usage grows.
- Dependence on the provider's supported features.
- Migration to another provider may require changes.
- Customers still need to manage permissions, data protection, and their own configurations.

### Managed vs self-managed services

| Feature                    | Managed service                                    | Self-managed service            |
| -------------------------- | -------------------------------------------------- | ------------------------------- |
| Infrastructure maintenance | Provider handles much of it                        | Customer handles more           |
| Administrative workload    | Usually lower                                      | Usually higher                  |
| Configuration control      | Depends on the service                             | Often greater                   |
| Patching and updates       | Provider handles some or all, depending on service | Customer handles more           |
| Example                    | Amazon RDS                                         | Database installed on an EC2 VM |

Important: Managed does not mean responsibility-free. The exact division of duties depends on the service and provider.

## Important exam questions

1\. What is a cloud ecosystem? Name three major cloud platforms.

2\. Explain the major types of compute services.

3\. Explain object, block, and file storage.

4\. What are cloud networking services? Explain five examples.

5\. What are managed cloud services? Give examples.

6\. Compare AWS, Azure, and Google Cloud.

7\. Explain the benefits and limitations of managed services.

8\. Explain how compute, storage, networking, and managed services work together.

## Quick revision notes

- Cloud ecosystem: The complete environment of cloud providers, services, infrastructure, and users.
- Compute: Runs applications and programs.
- Storage: Saves files, application data, and backups.
- Networking: Connects users, servers, and cloud resources.
- Managed services: Reduce the customer's infrastructure-management workload.
- VM: A virtual computer with an operating system.
- Container: A portable application package with its dependencies.
- Serverless: Runs code or applications without requiring the customer to manage the underlying servers directly.
- Object storage: Best suited to large collections of files and unstructured data.
- Block storage: Commonly used for virtual machine disks and performance-sensitive workloads.
- File storage: Organizes data into files and folders.
- VPC: A logically isolated cloud network.
- Load balancer: Distributes network traffic.
- DNS: Helps resolve domain names.
- CDN: Delivers cached content closer to users.
- IAM: Controls identities and permissions.

### Official references for further study

- [Cloud service comparison: AWS, Azure, and Google Cloud](https://docs.cloud.google.com/docs/get-started/aws-azure-gcp-service-comparison?utm_source=chatgpt.com)
- [AWS compute services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html?utm_source=chatgpt.com)
- [Google Cloud storage services](https://cloud.google.com/docs/storage?utm_source=chatgpt.com)
- [Azure networking fundamentals](https://learn.microsoft.com/en-us/azure/networking/fundamentals/networking-overview?utm_source=chatgpt.com)

Exam tip: For a 5-mark question, write the definition, explain the main types, and give examples. For a 10-mark question, add a labelled diagram, a comparison table, advantages, and limitations.
