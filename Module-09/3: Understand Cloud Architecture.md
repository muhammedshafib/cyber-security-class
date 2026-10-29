# Module 3: Understand Cloud Architecture ☁️

Complete study notes for exam preparation, explained in simple English with diagrams, examples, comparisons, important points, and exam questions.

## 1. What is Cloud Architecture?

Cloud architecture is the design and arrangement of cloud computing components, such as virtual machines, containers, storage, networks, databases, and security services, that work together to run applications.

In simple words, cloud architecture is the blueprint of how a cloud system is built and how its parts communicate with each other.

### Example

Imagine an online shopping website. It needs:

- Virtual machines or containers to run the website.
- Storage to store product images and files.
- A database to store customer orders.
- Networking to connect users to the website.
- Scalability to handle more visitors during festival sales.

All these components together form the website's cloud architecture.

Users

Customers using a browser or mobile app

Network and Load Balancer

Routes and distributes requests

Application Layer

Virtual machines

Containers

Database

Customer orders

Storage

Images and files

Security, monitoring, backups, and scaling support the entire architecture.

### Main goals of cloud architecture

1. Availability: Keep applications accessible when users need them.
2. Scalability: Handle increases or decreases in workload.
3. Performance: Process requests efficiently.
4. Security: Protect systems, accounts, and data.
5. Reliability: Continue working correctly despite certain failures.
6. Cost efficiency: Use resources without unnecessary expenditure.

## 2. Virtual Machines (VMs)

### What is a virtual machine?

A virtual machine (VM) is a software-based computer that runs an operating system and applications using resources from a physical computer.

A VM can have its own virtual CPU, RAM, storage, network interface, and operating system.

In simple words, one physical computer can behave like several separate computers by using virtualization.

[How to create a virtual machine - IONOS CA](https://images.openai.com/static-rsc-4/c9DlI-g0xwPlksokYH7RVEsX2Db0afU7A03wysd1bN8p4uaevX4co-II2pTFnRPmmCDLW2hMZuWCu5dsaeK_BAC9GuLCYYqXGCkEOfL_CwOoddSFirqlXokLHuLmBh-T4gFCUMuFZw0nCNUx65JGtvly5Y487JYtcyNaCRPgKts?purpose=inline)

[ionos.ca](https://www.ionos.ca/digitalguide/server/know-how/virtual-machines/?utm_source=chatgpt.com)

### How does a VM work?

1. A physical server provides CPU, RAM, storage, and networking.
2. A software layer called a hypervisor creates and manages virtual machines.
3. Each VM receives allocated resources.
4. Each VM runs its own guest operating system.
5. Applications run inside those operating systems.

### Important VM terms

- Host machine: The physical computer providing resources.
- Guest OS: The operating system installed inside a VM.
- Hypervisor: Software that creates and manages virtual machines.
- Virtual CPU: A share of processing capacity allocated to a VM.
- Virtual RAM: Memory allocated to a VM.
- VM image: A template used to create a virtual machine.
- Snapshot: A point-in-time representation of a VM's disk state, depending on the platform and snapshot type.

### Example

Suppose a company owns one powerful physical server. Using virtualization, it creates three VMs:

- VM 1 runs a web server.
- VM 2 runs a database.
- VM 3 runs a testing environment.

These workloads operate in separate virtual environments while sharing the underlying physical hardware.

### Cloud VM examples

- Amazon EC2
- Azure Virtual Machines
- Google Compute Engine

### Advantages of virtual machines

- Run different operating systems on shared hardware.
- Isolate workloads from one another.
- Provide substantial control over operating systems and software.
- Allow resources to be adjusted and VMs to be created from images.
- Reduce the need for separate physical computers.

### Limitations

- Consume CPU, memory, and storage.
- Need operating-system maintenance and security updates.
- Can be slower to start than lightweight containers.
- Poor resource allocation can increase costs or reduce performance.

### Virtual machines vs physical machines

| Feature             | Physical machine                        | Virtual machine               |
| ------------------- | --------------------------------------- | ----------------------------- |
| Hardware            | Dedicated physical computer             | Uses shared physical hardware |
| Operating system    | Installed directly on hardware, usually | Installed as a guest OS       |
| Resource allocation | Limited by its hardware                 | Allocated from host resources |
| Isolation           | Physical separation                     | Virtual isolation             |
| Example             | Company-owned server                    | Cloud VM                      |

Exam point: Virtualization is a key technology that enables cloud providers to offer many virtual computers using shared physical infrastructure.

## 3. Container Awareness

### What is a container?

A container is a lightweight, isolated environment that packages an application and its required libraries, dependencies, and configuration so it can run consistently across supported environments.

Unlike a traditional VM, a container typically shares the host operating system's kernel rather than running a separate guest operating system.

In simple words, a container carries the application and the essential things it needs to run.

[Enterprise IT Glossary | HPE | HPE](https://images.openai.com/static-rsc-4/GAqZ7e9DOHGRX2_due7-bHJ2pEX6trJr0SZc9HkhX0Ca5r6QM0hZ9V7haBhyqjXTKa8o9THCjGv9iiKwnmu3l_tQrMaPtHLOfhehEFLLpRb8Y3N9pJNyd_6FPHU3pDhD-k1gJaItUCSZ6Voa14DibpubhrTm5jLXpiL5oP_kQs4?purpose=inline)

[juniper.net](https://www.juniper.net/us/en/products-services/what-is/docker-container/?utm_source=chatgpt.com)

### How do containers work?

1. A developer writes an application.
2. The application and its dependencies are packaged into a container image.
3. A container runtime creates a running container from that image.
4. The application runs in an isolated environment.
5. Multiple containers can run on the same host.

### Important container terms

- Container image: A packaged template used to create containers.
- Container: A running instance created from an image.
- Docker: A platform used to build and run containers.
- Container runtime: Software that starts and manages containers.
- Kubernetes: A platform for orchestrating containers across computing resources.
- Orchestration: Automatically managing deployment, scaling, networking, and recovery of containers.

### Example

A developer creates a Python website requiring Python and certain libraries. Packaging the website into a container image helps ensure that the same dependencies are available in development and production environments.

### VM vs container

| Feature          | Virtual machine                                            | Container                       |
| ---------------- | ---------------------------------------------------------- | ------------------------------- |
| Operating system | Separate guest OS                                          | Usually shares host kernel      |
| Size             | Generally larger                                           | Generally smaller               |
| Startup          | Often slower                                               | Often faster                    |
| Isolation        | Virtual hardware and guest OS boundary                     | OS-level isolation              |
| Best suited for  | Different OS environments and stronger OS-level separation | Portable application deployment |
| Example          | Amazon EC2 VM                                              | Docker container                |

### Benefits of containers

- Portable application environments.
- Efficient resource usage.
- Fast application deployment.
- Consistent dependencies across environments.
- Support for microservices and automated deployment.

### Limitations

- Containers sharing a kernel require careful security configuration.
- Persistent data requires suitable storage arrangements.
- Complex applications may need orchestration.
- Container images and dependencies must be updated and scanned for vulnerabilities.

Remember: A VM virtualizes a computer. A container isolates an application environment.

## 4. Storage Architecture

### What is storage architecture?

Storage architecture is the design of how data is stored, organized, accessed, protected, backed up, and recovered in a cloud environment.

In simple words, it describes where data lives, how applications access it, and how the data is kept safe.

### Main types of storage architecture

[Storage Buckets Demystified: How the Cloud Stores Your World - DEV Community](https://images.openai.com/static-rsc-4/oIQSDoxqaD8aWx-EbtZniQbjbwdt31NTQ7DIaxBTWjwfhMfJQuxTKe-G78_mOlMhr-essRZee-1B_4jegE4BFdaoH9ReU61xIJyBVsKpRP--Zn7NFC1XzlWyGcO3jUtzjHlZyt-Ysua2zBFnElXq-pkoR9QD_H8e-s3aXBHJ8jE?purpose=inline)

1\. Object storage

Stores data as objects, each with data, metadata, and a unique identifier.

- Used for: Images, videos, documents, logs, and backups.
- Examples: Amazon S3, Azure Blob Storage, Google Cloud Storage.
- Main benefit: Suitable for large amounts of unstructured data.

[Run a Windows VM on Azure - Azure Architecture Center | Microsoft Learn](https://images.openai.com/static-rsc-4/2xpNoFWvMqwPeL2Kz60Dc7wBL_YukNWa1dK8Gxe9GJj_lbnGFn4kCk-jyHwoF9iO_f3n8O0rOeHdrD22qiBIwvkh-iPAXgn4em1D0LxGL4gPPgKxysrhvORsCd6NdIWrC-JaWU4JqFPry9dZstT_BZgVfYaUd1PJXLY4we0Y7yU?purpose=inline)

2\. Block storage

Stores data in blocks and provides storage volumes that operating systems and applications can use.

- Used for: VM disks, operating systems, and databases.
- Examples: Amazon EBS, Azure Managed Disks.
- Main benefit: Suitable for many workloads that need low-latency disk access.

[应用场景 - 文件存储CFS | 百度智能云文档](https://images.openai.com/static-rsc-4/WzOHy988Ym47Bez7ijs4FJvlI8qf6j0MLgU8B5_n7lQJC7jEQ5UBUTNIJw2JXqVshICCQiiIl6VqEJLihGGn7ZVW5oq4AsYla7zmqu7ergAda1UTTFQsz5KSBi1fNEuSba8HfSgm97V5U5z5ZlVXbaYuNLIkWw4yWcTtVebNt2o?purpose=inline)

3\. File storage

Organizes data using files and directories.

- Used for: Shared folders, documents, and applications requiring file-system access.
- Examples: Amazon EFS, Azure Files.
- Main benefit: Familiar file and folder organization.

[Truncate table sql описание: SQL оператор TRUNCATE TABLE — Oracle PL/SQL •MySQL •MariaDB •SQL Server •SQLite](https://images.openai.com/static-rsc-4/rwgGUl9GU6VeBFHOCjvh8aYVJgbgEUvkhxxvg2u8j7yZQuD4up_x6NlwMvk6BL93lqfjKpMOYiSeSU6TKEYnUhrrxJ5hj2qgFW5qxr_BWQJul4Cnwlv2wAADBqE26viO3lVdmx_de8VmVBnxk7dOyPIaRIWVU7c9Otb6S2o7DJo?purpose=inline)

4\. Database storage

Organizes data for efficient querying, updating, and application use.

- Relational databases: Store structured data in tables with defined relationships.
- NoSQL databases: Support data models such as documents, key-value pairs, or wide-column records.
- Examples: Amazon RDS, Azure SQL Database, Google Cloud SQL.
- Main benefit: Provides structured ways to manage application data.

### Example: Online shopping storage architecture

An online shopping application might use:

- Object storage: Product photographs and downloadable invoices.
- Block storage: Disks for virtual machines.
- File storage: Shared files needed by several application servers.
- Database: Customer accounts, product details, and order records.
- Backup storage: Recovery copies of important data.

### Important storage concepts

1\. Replication: Creating copies of data on other storage resources or locations.

2\. Backup: Creating a recoverable copy of data for use after accidental deletion, corruption, or other failures.

3\. Encryption: Protecting stored data so that unauthorized people cannot easily read it.

4\. Durability: The ability of a storage service to preserve data over time.

5\. Availability: How readily data can be accessed when required.

6\. Lifecycle management: Automatically moving data between storage classes or deleting it according to rules.

7\. Redundancy: Using extra copies or components to reduce the risk of data loss or service interruption.

### Backup vs replication

| Backup                                    | Replication                                        |
| ----------------------------------------- | -------------------------------------------------- |
| Creates recovery copies                   | Copies data between resources                      |
| Helps recover from deletion or corruption | Helps maintain copies and may support availability |
| Often retains historical recovery points  | May copy unwanted changes or deletions as well     |
| Must be configured and tested             | Must also be configured and monitored              |

Important: Replication is not a replacement for backups. If corrupted data is replicated, the corruption can spread to the replica.

## 5. Network Architecture

### What is network architecture?

Network architecture is the design of the network components, connections, rules, and communication paths that allow cloud resources to communicate securely and efficiently.

In simple words, it explains how users, servers, databases, and other resources connect to each other in the cloud.

### Main components of cloud network architecture

[Secure Cloud Architecture - OWASP Cheat Sheet Series](https://images.openai.com/static-rsc-4/u4Tubki2sQirW3v3R6Vv3jlyoa-D-dpFOQhY26cnnRYX-KCTCIKFQoCLeBsVz34gTXcmhCKvKKl9LFWtR0fchf050J686oAAvA_I1mFkJKfZP3veOFnSSrApl0zpUvitZAmTpAoQmR9cmibLHFhlcpYjxxVc5VLcmHLhw5mt1yQ?purpose=inline)

1\. Virtual Private Cloud (VPC)

A logically isolated cloud network in which you organize and connect cloud resources.

Example: Amazon VPC or Google Cloud VPC.

[If AWS Networking Confuses You — This Guide Is Your Missing Map | by Muhammad Shahbaj | Medium](https://images.openai.com/static-rsc-4/yuF0NBA9405e4do5FU7fAW3dvBFHDQ69ZK3P0FaDT_mD886EmJVuvT1Tvi4b4HWen_ipZ1Lba_1bybEvkmxft6WtVGvXE5FG-TKhqPwpAxmz1givpPPALHOYzzII9uVJ0fHCok7uqmHPxhpQ524MnLq0Wb4p_96dlKYM5s9QiKA?purpose=inline)

2\. Subnets

Subnets divide an IP network into smaller networks. Public-facing and private resources can be placed in different subnets according to the architecture.

Example: A public web server and a private database server are placed in appropriately configured subnets.

[Alibaba Cloud ECS Security Groups | by Diyawanna | Medium](https://images.openai.com/static-rsc-4/H55UtZmx5cKlxtXzmUjcmze5zVWjnm1eI6k_6YmktQGOnnXOPnE6C2cpddC3-_9m5yXKwKi-HZGAo3eKbUb10RjfkljRX36UmYWmksq1rfw61z5_gWw9oESFEOD_HzXVIxaJd5QCCxCdA1e1q44kdtZBCbQQwJ5dRfaSTdX1ubM?purpose=inline)

3\. Firewalls and security rules

Control which network connections are permitted or blocked.

Example: Allow HTTPS traffic to a website while restricting direct internet access to its database.

[Beyond Names & Labels: Load Balancer | by Ananya | Medium](https://images.openai.com/static-rsc-4/ZzvVyYsx7MZ0GJOwyCqrsP9MhflpuVJmWYvXfgttF9XhPICJoU_6Jw-R5AVoNqgDUj4JEbjyisxbAX795hR3vI5asVJ6psF1gXTlTDc3w665Fcr61Ms65Pal4opfO4eI_IS57FQL9-GV44gJbw4pEXcp112_EZdEnHzJwNK3nDM?purpose=inline)

4\. Load balancer

Distributes incoming requests across multiple application servers to improve traffic handling and availability.

[Connecting Your On-Premises Network to Your RONIN AWS Cloud Account](https://images.openai.com/static-rsc-4/XJbGUxXGZxJqDPMgXZVN_3IjNg6Ki6xpGPYZmZaGTdzaU-dkwFYomDdqXFYGqzi1owpfvCe8reyOALyhJTZiw_1-ExFaWt8TlcpsyC6WjmMhFZRmG75Ccbf_dI1AZlh0ZDjyRH81LLJdN07KirVS-5G5nLfJzmSvr7VUJ-or9Xc?purpose=inline)

5\. Gateways and routing

Route traffic between networks and connect cloud resources to external networks where permitted.

Examples: Internet gateways, VPN gateways, and route tables.

[Co to jest i jak działa DNS?](https://images.openai.com/static-rsc-4/NbEB3Pd9oIVx45BRRnMavmLl0Fu3tqYb9DjLMHjHkCONiWBddaZ4wcHgAqyCdPlKL59B_RbyGnneI_f3HiQwVTLJnL7RMvmulGXW4bNhM9_ISbf_ELHrQX0w47xCKov3LoI3SELnfyqdlw8vtznENx2KQFkL3v1rIUv_DMQK5v4?purpose=inline)

6\. DNS

Helps translate a domain name, such as `example.com`, into the network information needed to reach the service.

### Example: Secure website network

Suppose you are building an online banking website.

Internet users

Firewall / Web protection

Filters unwanted traffic

Load balancer

Distributes requests

Private application servers

Private database

Accessible only through approved connections

In this design, the database is not directly exposed to the public internet. Security rules permit only the required communication between the application and database.

### Important networking concepts

- IP address: Identifies a network interface.
- Subnet: Divides a network into smaller address ranges.
- Routing: Determines where traffic should travel.
- Latency: Time taken for data to travel between points.
- Bandwidth: The capacity to transfer data over a connection.
- VPN: Creates a private connection over a network, commonly using encryption.
- Load balancing: Distributes traffic among multiple resources.
- Network segmentation: Separates resources into different network zones to limit unnecessary access.

### Benefits of good network architecture

1. Improves security by controlling traffic.
2. Separates public-facing and private resources.
3. Supports application availability.
4. Improves traffic distribution and performance.
5. Allows secure connectivity between cloud and company networks.
6. Helps organizations monitor and troubleshoot communication.

## 6. Scalability Concepts

### What is scalability?

Scalability is the ability of a cloud system to increase or decrease its computing resources to meet changing workloads.

In simple words, scalability means your application can handle more work when demand increases and use fewer resources when demand decreases.

### Example

Imagine an online shopping website normally receives 1,000 visitors per hour. During a major sale, it receives 50,000 visitors per hour.

If the architecture cannot handle the increased traffic, the website may become slow or stop responding.

A scalable architecture can add computing capacity and distribute the traffic to handle the increase.

### Two main types of scalability

[Horizontal vs Vertical Scaling: Which Strategy is Right for You?](https://images.openai.com/static-rsc-4/wM_cwFYaqxjyMT9UH9GXSbYfyp0u1tUP66vEqzv5hmtoiRr5f14Wi4qMOKVwatIZkwc306LJKABYTb6mii5AUo4ApyrF3w4vMrBn_rBjVokCLF0aEkZe4GyYzdXeMTaOn2KJ2Zb7OlOwkQAmXxcGZ7T-EhBae3qfusL6bmJ2dI0?purpose=inline)

1\. Vertical scaling (Scale up or down)

Increase or decrease the resources of a single server, such as CPU and RAM.

Example: Upgrade a VM from 2 CPU cores and 4 GB RAM to 8 CPU cores and 16 GB RAM.

Advantages: Relatively simple for many applications.

Limitations: There are hardware or service limits, and some changes require downtime.

[How to Scale a System from 0 to 10 million+ Users](https://images.openai.com/static-rsc-4/RKm_J6we-MtSWmYt3EAh_sKUxnhLmH-n4KYJMMerxjvEICNOVDIoAiHUjc3Yd7yp_ZskTs4uQuEyz4l-A6E6ZQUPHIK9kmYyRcef7MjCWIOpb68Z0JcVHrZKcDCovJK00s80kP-SwjA8uRsc5xkhP88qSxa1ABLl9SNGFmsXlMk?purpose=inline)

2\. Horizontal scaling (Scale out or in)

Add or remove server instances to distribute the workload across multiple machines.

Example: Increase a website from 2 application servers to 8 application servers behind a load balancer.

Advantages: Can support larger workloads and improve resilience.

Limitations: Requires traffic distribution and applications that can work correctly across multiple instances.

### Vertical vs horizontal scaling

| Feature        | Vertical scaling                                 | Horizontal scaling                        |
| -------------- | ------------------------------------------------ | ----------------------------------------- |
| Method         | Increase resources on one machine                | Add more machines                         |
| Also called    | Scale up                                         | Scale out                                 |
| Example        | Increase VM RAM                                  | Add application servers                   |
| Resource limit | Limited by the machine or service                | Can expand across more instances          |
| Complexity     | Often simpler                                    | Often needs distributed architecture      |
| Resilience     | One machine can remain a single point of failure | Multiple instances can improve resilience |

### Other important scalability concepts

1\. Auto-scaling

Automatically adds or removes resources based on configured rules, schedules, or demand.

Example: Automatically adding web servers when CPU usage or incoming requests increase.

2\. Load balancing

Distributes requests among available resources so that one server does not receive all the traffic.

3\. Elasticity

The ability to adjust resources dynamically as demand changes. Scalability is the ability to handle growth or changes in workload, while elasticity emphasizes adjusting capacity to actual demand.

4\. High availability

Designing a system to remain accessible by using redundancy, health checks, failover, and other measures.

5\. Fault tolerance

The ability of a system to continue operating despite certain component failures.

6\. Distributed architecture

Spreads application work or data across multiple resources instead of relying entirely on one machine.

### How auto-scaling works

Monitor workload

CPU, request rate, queue length, or other metrics

Evaluate scaling rules

Compare metrics with configured thresholds

Scale out

Add resources when demand rises

Scale in

Remove excess resources when demand falls

Auto-scaling requires appropriate limits and policies. Poor configuration can lead to unnecessary costs or insufficient capacity.

### Benefits of scalability

- Handles sudden increases in traffic.
- Helps maintain application performance.
- Reduces the need to permanently provision for peak demand.
- Supports business growth.
- Can improve availability when combined with redundancy.

### Challenges of scalability

- Poor architecture can prevent effective scaling.
- Database bottlenecks may remain even when more application servers are added.
- Additional resources can increase costs.
- Distributed systems require more careful monitoring and coordination.

## Important exam questions

1\. Define cloud architecture and explain its main components.

2\. What is a virtual machine? Explain the role of a hypervisor.

3\. What are containers? Differentiate containers from VMs.

4\. Explain storage architecture and its types.

5\. Explain the main components of cloud network architecture.

6\. Define scalability. Explain vertical and horizontal scaling.

7\. Differentiate scalability and elasticity.

8\. Explain auto-scaling and its benefits.

9\. Differentiate backup and replication.

10\. Design a basic scalable cloud architecture for an online shopping website.

## Quick revision notes

| Topic              | Remember this                                |
| ------------------ | -------------------------------------------- |
| Cloud architecture | Blueprint of the entire cloud system         |
| Virtual machine    | A virtual computer with its own guest OS     |
| Hypervisor         | Creates and manages virtual machines         |
| Container          | Packages an application and its dependencies |
| Docker             | Builds and runs containers                   |
| Kubernetes         | Orchestrates containers                      |
| Object storage     | Stores objects such as images and files      |
| Block storage      | Provides disk-like storage volumes           |
| File storage       | Stores data as files and directories         |
| VPC                | Logically isolated cloud network             |
| Subnet             | Smaller network within an IP network         |
| Load balancer      | Distributes incoming requests                |
| Vertical scaling   | Increases resources on one machine           |
| Horizontal scaling | Adds more machines or instances              |
| Auto-scaling       | Automatically adjusts resources using rules  |
| Elasticity         | Adjusts capacity dynamically with demand     |
| High availability  | Reduces service interruptions                |
| Fault tolerance    | Continues operating despite certain failures |

Exam preparation tip: For a 5-mark question, write the definition, explain four or five points, and give an example. For a 10-mark question, include a labelled architecture diagram, comparisons, advantages, and limitations.
