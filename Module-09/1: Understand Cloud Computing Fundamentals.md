# Module 1: Understand Cloud Computing Fundamentals ☁️

Complete study notes for exam preparation, explained in simple English with examples, important points, differences, and exam questions.

## 1. What Is Cloud Computing?

### Definition

Cloud computing is the delivery of computing services over the internet, such as servers, storage, databases, networking, software, and security, without needing to own and maintain all the physical hardware yourself.

In simple words, cloud computing means using another company's computers and services through the internet whenever you need them.


### Example

Suppose you want to store your photos.

- Without cloud computing: You save photos on your computer's hard disk or a pen drive.
- With cloud computing: You upload your photos to Google Drive and access them through the internet from different devices.

Other examples include Gmail, Google Photos, Microsoft OneDrive, and online applications.

### How does cloud computing work?

Step 1: User's device

A computer or mobile sends a request.

Internet connection

Step 2: Cloud provider

Remote servers process the request and store or retrieve data.

Step 3: Result

The user receives the requested data or service.

### Main characteristics of cloud computing

1. On-demand self-service: Users can access resources whenever required without waiting for manual setup by the provider.
2. Broad network access: Services are available over networks, typically the internet, using supported devices.
3. Resource pooling: Providers share computing resources among multiple customers while keeping their data logically separated.
4. Rapid elasticity: Resources can increase or decrease according to demand.
5. Measured service: Resource usage can be monitored and billed according to consumption.

### Important terms

- Cloud provider: A company that offers cloud services, such as AWS, Microsoft Azure, or Google Cloud.
- Virtualization: Technology that allows one physical computer to run multiple virtual machines.
- Scalability: The ability to increase or decrease computing capacity as needs change.
- Pay-as-you-go: Paying according to the resources you use, depending on the service's pricing model.

### Advantages

- Access data from different locations.
- Reduce the need to purchase physical servers.
- Scale resources as demand changes.
- Improve backup and disaster recovery options.
- Deploy applications quickly.

### Disadvantages

- Requires reliable network access for many services.
- Costs can grow if usage is not monitored.
- Misconfiguration can expose sensitive data.
- Provider outages can interrupt services.
- Moving between providers can be difficult or expensive.

## 2. Cloud Service Models

A cloud service model describes what the cloud provider manages and what the customer manages.

There are three main service models: IaaS, PaaS, and SaaS.

[What is Cloud Computing? Definition & Models Explained | STACKIT](https://images.openai.com/static-rsc-4/0Et3i393Y-ibngmG7ILuLYbDuPiGTQdJFFxnO57u6a6wmzEXbKYIDHi5B3D8CSGZCKxXh4KnNLU_S4mVIaxfRSUc4O98ftDgAJ9-6a_T52JPl2iQeetAGpGcFCT6ldavSI_F3ba2GGGwt4R2JcwgM_bF930OJTA-DmLrr1sXgHo?purpose=inline)

## 1. IaaS: Infrastructure as a Service

Meaning: Renting computing infrastructure, such as virtual machines, storage, and networking.

Provider manages: Physical servers, data centers, and underlying infrastructure.

Customer manages: Operating system, applications, configurations, and data.

Example: Amazon EC2, Azure Virtual Machines.

Use case: A company wants control over its server operating system without buying physical servers.

[Itac PaaS Solutions | Comprehensive Platform as a Service](https://images.openai.com/static-rsc-4/tyPHSTRpbzMpzTgm3S6tDz670Ansddlz3U7wqfwI0zWmSb5P-1G3gGBiqjCN6MeB3E8xDpogVMmcrXxJaW55EU8FYfQVkv-s_dTVVqPkLNLgUM7Cmwb51AuaFG9JFKldOouRztbDat3j1OKllsEnD3tP2pP2lCEjGkbpLZH0Ckc?purpose=inline)

## 2. PaaS: Platform as a Service

Meaning: A ready-to-use platform for developing, testing, and deploying applications.

Provider manages: Infrastructure, operating system, and supported runtime environment.

Customer manages: Application code, application settings, and data.

Example: Google App Engine, Azure App Service.

Use case: A developer wants to build a website without managing the underlying servers.

[Saas Illustrations - Free Download in SVG, PNG](https://images.openai.com/static-rsc-4/X91FP_QqoGdopn5440hm-V1HHdhlAZsALJwTZxgSFa495SwCNppJRAliFvh6_QGA2oV4sYMlEDh_9Gg7JqhsEYoYttcloFymnK7B70JkKTpVZNXLW99QeeKwzBr0EfmOcDdJsyZJ7Z4tiCdv0rQ8bAz6ExLFIV2eb0V1Db8zY1s?purpose=inline)

## 3. SaaS: Software as a Service

Meaning: Using ready-made software over the internet.

Provider manages: Infrastructure, platform, application software, and maintenance.

Customer manages: User access, their own data, and available application settings.

Example: Gmail, Microsoft 365, Salesforce.

Use case: A business wants to use email software without installing and maintaining its own email servers.

### Difference between IaaS, PaaS, and SaaS

| Feature           | IaaS                        | PaaS                  | SaaS                  |
| ----------------- | --------------------------- | --------------------- | --------------------- |
| Full form         | Infrastructure as a Service | Platform as a Service | Software as a Service |
| Provides          | Virtual infrastructure      | Development platform  | Ready-made software   |
| Customer control  | High                        | Medium                | Lower                 |
| Server management | Mostly provider             | Provider              | Provider              |
| Main users        | IT administrators           | Developers            | End users             |
| Example           | Amazon EC2                  | Google App Engine     | Gmail                 |

Easy way to remember:

- IaaS = Rent a computer.
- PaaS = Get a platform to build software.
- SaaS = Use finished software.

The provider's responsibilities vary by service, and customers remain responsible for appropriate data protection, access control, and secure configuration.

## 3. Cloud Deployment Models

A deployment model explains where cloud infrastructure is hosted, who can use it, and how it is managed.

[Public Cloud - Evolution IT](https://images.openai.com/static-rsc-4/R7hDnO2G8ENzVJIm9UJ7PXEdZzLluet9SEif3wIHNr8DIwNfDVEE1_UyPyNBWVyLK0hN91mfTAamLQwg-dS2U3yki4LvRB5EmbBLO3pN4BmL5TjYCgjq6pvJqDujq8G6gIxS594hMQev0xl2TggvBoDcoN7oZeTmFwy_4xCt2jo?purpose=inline)

1\. Public Cloud

Cloud infrastructure is provided by a third-party provider and serves multiple customers.

- Cost: Often lower initial cost.
- Management: Mainly handled by the provider.
- Best for: Startups, websites, and applications with changing demand.
- Examples: AWS, Microsoft Azure, Google Cloud.

[VPC. Private cloud within a company icon of secure data store hand managing. Vector illustration.](https://images.openai.com/static-rsc-4/6Zgk20xqtOgZ5Rfs9al3B8PThJ0cRs-UEGDpJEj9rgMUQEZWBJOrfhFIR_d0X8VzLzOyeTKjBUy6eQEOsz4TprM94X6TpjmgNAgb1fgrhuffAc8VpWhiDU1yEZbVvaXTBLQNP93lWs_smQSklhx8rWbZwNZA85dV6jnl9OLdpP7tikXeFUZZ0uJ-yjvIjBK0?purpose=inline)

2\. Private Cloud

Cloud infrastructure is dedicated to a single organization. It can be hosted internally or by a third party.

- Cost: Often higher due to dedicated resources and management.
- Management: Organization or service provider.
- Best for: Organizations needing greater control over infrastructure.
- Example: A bank's dedicated cloud environment.

[Hybrid Cloud Architecture This diagram will illustrate the core components of a hybrid cloud: your on-premises data center, a public cloud provider, and the secure connection between them. Key… | Sukhen Tiwari](https://images.openai.com/static-rsc-4/Kcb7Zs8qchtPfdY8NIH40hOH-xHbUzopHjtmJbNbQSG7VnO-ot18ymK18-4eGA79cyYKIndFXs6P4i2aaK47eVIxDQb5KHHuMYXpiilZ1JrzeTf4YMF225wTvG4TaDOMrQYPpfKmI3XCrSALAkmNRZck0WJ0Mzx_Xz-84HqppWM?purpose=inline)

3\. Hybrid Cloud

Combines private cloud infrastructure with public cloud infrastructure, allowing data and applications to be shared or moved between them where configured.

- Cost: Depends on the combined environment.
- Management: Requires coordination between environments.
- Best for: Businesses that need both control and flexibility.
- Example: A hospital keeps sensitive systems in a private environment and uses public cloud services for less-sensitive workloads.

[Community Cloud là gì? Hiểu về đám mây cộng đồng | VNPT Cloud](https://images.openai.com/static-rsc-4/MdbYVBfUJzQp-9Xy1zRk3kEOduNEdbVjhez8r48StliH_FdCBC_BblDn5d-vSPLhTySpasu-hY6BOSORLKDaogJgtwxd7BoPCIQGBVXQFekTuKnLPE-OVLBos3d1HyvDCYhssS8WaVgfsvTT_YCTPCGvYg4w2mqhWOHNciLguxs?purpose=inline)

4\. Community Cloud

Cloud infrastructure is shared by organizations with common requirements, such as security policies, regulations, or mission.

- Cost: Shared among participating organizations.
- Management: One or more participating organizations or a provider.
- Best for: Organizations with similar needs.
- Example: Several government departments sharing a cloud environment.

### Difference between deployment models

| Model     | Who uses it?                                 | Main advantage                     | Main limitation                    |
| --------- | -------------------------------------------- | ---------------------------------- | ---------------------------------- |
| Public    | Multiple customers                           | Flexibility and easy access        | Less direct infrastructure control |
| Private   | One organization                             | Greater control                    | Higher management responsibility   |
| Hybrid    | One organization using combined environments | Balance of control and flexibility | More complex integration           |
| Community | Organizations with shared requirements       | Shared costs and common policies   | Coordination can be difficult      |

Exam tip: Do not confuse service models with deployment models.

- Service models describe what services are provided.
- Deployment models describe how the cloud environment is organized and made available.

## 4. Benefits of Cloud Computing

Cloud computing helps individuals and businesses use computing resources efficiently.

1\. Cost savings

Reduces the need to purchase and maintain physical servers. Many services charge according to usage.

2\. Scalability

Resources can be increased or decreased to match workload requirements.

3\. Speed and agility

New servers and services can often be provisioned in minutes instead of waiting to buy physical hardware.

4\. Global accessibility

Authorized users can access services from different locations using supported devices and network connections.

5\. Security capabilities

Providers may offer encryption, identity management, logging, monitoring, and other security tools. Customers must configure and use them correctly.

6\. Backup and disaster recovery

Cloud-based backup and replicated systems can help restore services after data loss or failures, if properly configured and tested.

7\. Collaboration

Teams can share files, access common applications, and work together from different locations.

### Challenges of cloud computing

1. Internet dependency: Some cloud services become unavailable when network access fails.
2. Security risks: Weak passwords, exposed storage, and incorrect permissions can cause data breaches.
3. Privacy and compliance: Organizations must protect personal and confidential information and follow applicable laws.
4. Vendor lock-in: Moving applications and data to another provider may require significant work.
5. Unexpected costs: Unused resources, data transfer, and poor cost monitoring can increase bills.
6. Service outages: Provider or regional failures can interrupt applications.

### Shared responsibility in cloud security

Cloud security is a shared responsibility between the provider and the customer.

- The provider protects the underlying infrastructure according to the service agreement.
- The customer protects their accounts, access permissions, data, and application configurations, along with other responsibilities depending on the service model.

For example, a cloud provider can secure its physical data center, but a customer who accidentally makes a storage bucket public can still expose confidential files.

## 5. Enterprise Cloud Adoption

### Definition

Enterprise cloud adoption is the process by which an organization begins using cloud computing services or moves its existing IT systems, applications, and data to cloud environments.

In simple words, it means a company changes from relying mainly on its own IT infrastructure to using cloud services for some or all of its computing needs.

### Why do enterprises adopt cloud computing?

- Reduce the cost of purchasing and maintaining hardware.
- Scale applications during periods of high demand.
- Improve employee collaboration.
- Develop and release software faster.
- Support remote work and global operations.
- Improve backup and disaster recovery capabilities.
- Access modern services such as analytics, AI, and managed databases.

### Enterprise cloud adoption process

1. Assess business needs

   Identify the business problems, existing IT systems, costs, and expected benefits.
2. Choose a cloud strategy

   Decide whether public, private, hybrid, or a combination of cloud services is appropriate.
3. Plan security and compliance

   Define identity access, encryption, backup, monitoring, privacy, and regulatory requirements.
4. Migrate applications and data

   Move selected workloads to the cloud, or redesign applications where needed.
5. Test and validate

   Check performance, functionality, security, data integrity, and recovery procedures.
6. Monitor and optimize

   Track costs, availability, security alerts, and performance. Improve the environment continuously.

### Common cloud migration strategies

These are often called the “6 Rs” of cloud migration.

| Strategy                | Simple meaning                                                     |
| ----------------------- | ------------------------------------------------------------------ |
| Rehost                  | Move an application with minimal changes.                          |
| Replatform              | Move it with a few optimizations.                                  |
| Refactor / Re-architect | Change its design to take better advantage of cloud capabilities.  |
| Repurchase              | Replace the existing application with another product, often SaaS. |
| Retire                  | Stop using applications that are no longer needed.                 |
| Retain                  | Keep applications where they are for now.                          |

### Challenges during enterprise adoption

- Migrating large amounts of data.
- Training staff in new technologies.
- Integrating older systems with cloud services.
- Meeting security and compliance requirements.
- Controlling cloud expenditure.
- Managing outages and business continuity.
- Avoiding excessive dependence on one provider.

### Example of enterprise cloud adoption

Suppose an online shopping company has its own physical servers.

Initially, the company purchases servers and installs its shopping website on them. During festival sales, thousands of extra customers visit the website, and the servers may become overloaded.

After adopting cloud computing, the company can use cloud infrastructure that scales according to demand, managed databases, monitoring tools, and backup services.

Result: The company can respond to changing traffic more effectively, reduce some hardware-management tasks, and improve resilience when its cloud architecture is designed properly.

## Important exam questions

1\. Define cloud computing and explain its main characteristics.

2\. Explain IaaS, PaaS, and SaaS with examples.

3\. Explain the four cloud deployment models.

4\. Discuss the benefits and challenges of cloud computing.

5\. What is enterprise cloud adoption? Explain its stages.

6\. Differentiate service models and deployment models.

7\. Explain the shared responsibility model.

8\. What are the 6 Rs of cloud migration?

## Quick revision notes

Memorize these before your exam:

- Cloud computing: Computing services delivered over a network.
- IaaS: Infrastructure.
- PaaS: Development platform.
- SaaS: Ready-made software.
- Public cloud: Shared provider infrastructure.
- Private cloud: Dedicated to one organization.
- Hybrid cloud: Combination of private and public cloud environments.
- Community cloud: Shared by organizations with common requirements.
- Five characteristics: On-demand self-service, broad network access, resource pooling, rapid elasticity, and measured service.
- Enterprise cloud adoption: Assess, plan, secure, migrate, test, and optimize.
- Shared responsibility: Both provider and customer have security responsibilities.

Exam preparation tip: Practise writing the definitions first, then explain each concept with one example. For a 5-mark question, include a definition, four or five key points, and an example. For a 10-mark question, add a diagram, advantages, disadvantages, and a comparison table where relevant.
