# Module 4: Understand Cloud Security Fundamentals ☁️🔐

Complete study notes for exam preparation, explained in simple English with examples, diagrams, comparisons, important points, and exam questions.

## 1. Shared Responsibility Model

### What is the shared responsibility model?

The shared responsibility model explains how security responsibilities are divided between the cloud service provider and the customer.

In simple words, the cloud provider protects the cloud infrastructure, while the customer protects their data, accounts, and configurations according to the service being used.

For example, AWS, Microsoft Azure, or Google Cloud protects its underlying data center infrastructure. However, a customer must still configure permissions correctly and protect their cloud accounts.

### How does it work?

Cloud provider responsibility

- Physical data centers and hardware
- Physical security
- Underlying networking infrastructure
- Security of the cloud infrastructure

Customer responsibility

- Protecting data and user accounts
- Managing permissions and access
- Configuring services securely
- Securing applications and operating systems where applicable

The exact division depends on the provider, service model, and configuration.

### Example: Cloud website

Suppose you host a website on a cloud virtual machine.

- Provider: Protects the physical server and data center.
- Customer: Updates the guest operating system, configures the firewall, protects login credentials, and secures the website.
- Both: Have responsibilities that contribute to the overall security of the service.

### How responsibilities differ by service model

| Responsibility               | IaaS             | PaaS             | SaaS                                        |
| ---------------------------- | ---------------- | ---------------- | ------------------------------------------- |
| Physical hardware            | Provider         | Provider         | Provider                                    |
| Underlying infrastructure    | Provider         | Provider         | Provider                                    |
| Operating system maintenance | Usually customer | Usually provider | Provider                                    |
| Application code             | Customer         | Customer         | Mostly provider                             |
| Data and user access         | Customer         | Customer         | Customer retains important responsibilities |

For example, with IaaS, the customer generally has more operating-system responsibilities. With SaaS, the provider manages the application software, but the customer must still manage user access and protect their data.

### Why is it important?

1. Prevents confusion about security duties.
2. Reduces configuration mistakes.
3. Helps protect confidential information.
4. Supports regulatory compliance.
5. Makes security planning more effective.

Exam point: Moving to the cloud does not mean transferring every security responsibility to the provider.

## 2. Identity Management

### What is identity management?

Identity management is the process of creating, maintaining, verifying, and managing digital identities for users, applications, devices, and services.

In simple words, it answers the question: “Who are you?”

For example, when you sign in to a cloud account using your email and password, the cloud identity system helps verify your identity.

### Important identity management concepts

1\. Identity

A digital representation of a user, application, or service.

Example: A developer's cloud account.

2\. Authentication

Verifies that an identity is genuine.

Example: Signing in with a password and a one-time verification code.

3\. Multi-factor authentication (MFA)

Requires two or more different types of verification factors.

Example: A password plus an authenticator-app approval.

4\. Single sign-on (SSO)

Allows a user to access multiple supported applications through one sign-in process.

Example: Signing in once to access several company applications.

5\. Identity lifecycle management

Creates, updates, disables, and removes identities as people's roles and access needs change.

Example: Disabling an employee's account when they leave the organization.

### How identity management works

User enters credentials

Identity system verifies the user

Password, MFA, or another supported method

Identity is authenticated

Access control checks permissions

Determines which actions are allowed

### Examples of cloud identity services

- AWS IAM
- Microsoft Entra ID
- Google Cloud IAM

These services have different features and scopes, but all support aspects of managing identities and access.

### Best practices for identity management

- Enable MFA, especially for administrators.
- Use unique accounts rather than sharing credentials.
- Disable unused accounts promptly.
- Protect passwords and authentication tokens.
- Use temporary credentials for workloads where supported.
- Review identity activity and suspicious sign-ins.

Remember: Authentication verifies identity. Authorization determines what that identity can do.

## 3. Access Control

### What is access control?

Access control is the process of deciding which users, applications, or services can access a resource and what actions they are allowed to perform.

In simple words, it answers two questions:

- Which resources can you access?
- What are you allowed to do with them?

For example, in a college cloud system, a student can view their marks, a teacher can update marks, and an administrator can manage accounts.

### Types of access control

1\. Role-Based Access Control (RBAC)

Permissions are assigned according to a user's job role.

Example:

- Student: View marks.
- Teacher: Update marks.
- Administrator: Manage users and system settings.

2\. Attribute-Based Access Control (ABAC)

Access decisions are based on attributes such as the user's department, resource classification, location, or time.

Example: Only employees in the finance department can access financial records, provided the other access rules are satisfied.

3\. Discretionary Access Control (DAC)

The resource owner can decide who receives access, within the system's rules.

Example: A file owner shares a document with selected coworkers.

4\. Mandatory Access Control (MAC)

Access is determined by centrally enforced security policies and classifications. Individual users generally cannot override those policies.

Example: A system allows access to classified documents only when a user's clearance and the document's classification meet policy requirements.

### Comparison table

| Type | Access is based on      | Example                               |
| ---- | ----------------------- | ------------------------------------- |
| RBAC | User's role             | Teacher can edit marks                |
| ABAC | Attributes and policies | Finance staff can access finance data |
| DAC  | Owner's permissions     | Owner shares a file                   |
| MAC  | Central security policy | Classified information access         |

### Principle of least privilege

The principle of least privilege means giving a user or service only the minimum permissions needed to perform its task.

For example, a Python script that only reads security logs should not receive permission to delete every file on the server.

Why is this important?

- Reduces unauthorized access.
- Limits damage if an account is compromised.
- Helps prevent accidental deletion or modification.
- Makes auditing easier.

### Other important access control concepts

- Permissions: Allowed actions, such as read, write, delete, or administer.
- Policies: Rules that determine whether an action is allowed.
- IAM roles: Sets of permissions or identities used to grant access, depending on the platform.
- Access reviews: Periodically checking whether existing permissions are still necessary.
- Zero Trust: A security approach that avoids automatically trusting a user or device simply because it is inside a network.

Exam point: Authentication asks, “Who are you?” Access control asks, “What are you allowed to do?”

## 4. Security Monitoring

### What is security monitoring?

Security monitoring is the continuous or periodic collection and analysis of system activity, logs, network events, and alerts to detect suspicious behavior, security threats, and policy violations.

In simple words, security monitoring helps an organization notice when something unusual or potentially dangerous happens in its cloud environment.

### What does cloud security monitoring check?

- Failed and successful login attempts.
- Unusual account activity.
- Changes to permissions and security settings.
- Unexpected network traffic.
- Access to sensitive data.
- Malware or suspicious application behavior.
- Resource changes and service availability.
- Potential data leaks or unauthorized access.

### How does security monitoring work?

1\. Collect events and logs

Cloud accounts, applications, networks, and servers

2\. Analyze activity

Rules, patterns, thresholds, and threat detection

3\. Generate an alert

Notify the security team of suspicious events

4\. Investigate and respond

Validate the alert and contain confirmed threats

### Important monitoring concepts

1\. Logs

Records of events occurring in a system.

Example: A log records a login attempt, the time, the account involved, and whether the attempt succeeded.

2\. Metrics

Numerical measurements of system performance or activity.

Examples: CPU usage, network traffic, request counts, and error rates.

3\. Alerts

Notifications generated when specified rules or detection systems identify a condition that needs attention.

Example: An alert triggers after repeated failed administrator logins.

4\. Audit trails

Records that help determine who performed an action, what happened, and when it happened.

Example: An audit event shows that a user changed a storage bucket's permissions.

5\. SIEM (Security Information and Event Management)

A platform that collects and correlates security events from different sources to help analysts identify suspicious activity.

Example: A SIEM correlates repeated failed logins with a successful login from an unusual location.

6\. Incident response

The process of investigating and handling security incidents, including containment, recovery, and learning from the event.

### Examples of cloud monitoring tools

| Cloud platform  | Monitoring and logging examples   |
| --------------- | --------------------------------- |
| AWS             | Amazon CloudWatch, AWS CloudTrail |
| Microsoft Azure | Azure Monitor, Microsoft Sentinel |
| Google Cloud    | Cloud Monitoring, Cloud Logging   |

These tools have different functions. For example, performance monitoring helps identify slow services, while audit logging helps track actions taken within an environment.

### Example: Detecting a suspicious login

Imagine a cloud administrator's account experiences 100 failed login attempts in a short period.

1. Authentication logs record the failed attempts.
2. A detection rule identifies the unusual pattern.
3. The monitoring system generates an alert.
4. The security team investigates the source and account activity.
5. If an attack is confirmed, the team takes appropriate action, such as blocking the activity, revoking compromised credentials, and reviewing other actions performed by the account.

Important: An alert does not always mean an attack has occurred. Security teams must investigate and validate alerts.

## 5. Cloud Security Best Practices

Cloud security best practices are methods used to protect cloud accounts, infrastructure, applications, networks, and data from unauthorized access, attacks, and accidental damage.

### A. Identity and access security

- Enable MFA for privileged accounts and, where possible, all users.
- Follow the principle of least privilege.
- Avoid shared administrator accounts.
- Use strong authentication and secure credential storage.
- Remove unused accounts and unnecessary permissions.
- Review access regularly.

### B. Data security

- Encrypt sensitive data at rest and in transit.
- Use secure key management and restrict key access.
- Classify data according to its sensitivity.
- Configure storage permissions carefully.
- Maintain protected backups and test restoration.
- Apply appropriate data retention and deletion policies.

### C. Network security

- Separate public-facing services from private resources.
- Configure firewalls and security groups using restrictive rules.
- Avoid exposing databases and administration interfaces directly to the internet.
- Use secure connections such as HTTPS and appropriate VPN configurations.
- Monitor network traffic and investigate suspicious connections.

### D. System and application security

- Patch operating systems, applications, and dependencies.
- Scan virtual machine images and container images for vulnerabilities.
- Use trusted software sources.
- Store API keys and secrets in appropriate secrets-management services.
- Test applications for common security weaknesses.
- Use secure development practices and code reviews.

### E. Monitoring and incident response

- Enable relevant audit logging.
- Monitor important security events.
- Configure meaningful alerts.
- Protect logs from unauthorized alteration or deletion.
- Prepare an incident response plan.
- Regularly test recovery procedures.

### F. Cost, governance, and compliance

- Apply organizational security policies.
- Understand applicable privacy and regulatory requirements.
- Monitor cloud spending and resource usage.
- Tag and inventory cloud resources.
- Remove unused resources and public exposure.
- Regularly assess configurations against security standards.

### Cloud security best-practice checklist

### Revision checklist

0/10

Enable multi-factor authentication (MFA).

Apply least-privilege access permissions.

Encrypt sensitive data at rest and in transit.

Configure firewalls and storage permissions securely.

Patch systems and scan for vulnerabilities.

Enable audit logs and security alerts.

Maintain protected backups and test recovery.

Store credentials and API keys securely.

Review permissions and cloud configurations regularly.

Prepare and test an incident response plan.

Reset checklist

## Important exam questions and answers

1\. What is the shared responsibility model?

2\. Define identity management and explain its importance.

3\. Differentiate authentication and authorization.

4\. Explain RBAC and ABAC.

5\. What is the principle of least privilege?

6\. What is cloud security monitoring?

7\. What are logs, alerts, and SIEM?

8\. Explain five cloud security best practices.

9\. What is MFA, and why is it important?

10\. What should an organization do after detecting suspicious cloud activity?

## Quick revision notes

| Topic                 | Key point                                     |
| --------------------- | --------------------------------------------- |
| Shared responsibility | Provider and customer share security duties   |
| Identity management   | Manages digital identities                    |
| Authentication        | Verifies identity                             |
| Authorization         | Determines permitted actions                  |
| MFA                   | Uses multiple authentication factors          |
| RBAC                  | Access based on roles                         |
| ABAC                  | Access based on attributes and policies       |
| Least privilege       | Grant minimum necessary permissions           |
| Security monitoring   | Detects suspicious activities                 |
| Logs                  | Records system events                         |
| SIEM                  | Collects and correlates security events       |
| Encryption            | Protects data confidentiality                 |
| Incident response     | Investigates and handles security incidents   |
| Backup                | Enables recovery from data loss               |
| Zero Trust            | Does not automatically trust users or devices |

### Final exam tip

For a 5-mark answer, write a definition, explain four or five important points, and provide an example.

For a 10-mark answer, include the definition, a labelled diagram, the working process, advantages, security best practices, and a real-world scenario.

The most important distinction to remember is: the cloud provider protects the cloud infrastructure, identity management verifies who you are, access control determines what you can do, and security monitoring helps detect suspicious activity.
