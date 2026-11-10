# Module 2: Understand Security Requirements 🔐

Secure SDLC | Beginner to Advanced

Security requirements are one of the most important parts of Secure Software Development Life Cycle (SSDLC).

In Module 1, we learned how security is integrated into every stage of software development.

Now, we will learn how to identify what security a software application needs before developers start building it.

### What are Security Requirements?

Security requirements are rules, controls and conditions that an application must follow to protect its users, data, systems and services.

Example: Online Banking Application

Imagine a company wants to build an online banking website.

Before development starts, the security team identifies requirements:

- Users must authenticate before accessing accounts.
- Passwords must be securely hashed.
- Sensitive information must be encrypted.
- Only authorized users can transfer money.
- All important activities must be logged.
- The application must protect against common web attacks.

These are security requirements.

## 1. Security Planning

Beginner level

Definition: Security planning is the process of identifying security needs, protection methods, responsibilities and resources before software development begins.

In simple words:

Before building an application, we decide how to protect it.

### 1.1 What happens during security planning?

1. Identify sensitive data.
2. Identify application assets.
3. Identify possible threats.
4. Define security requirements.
5. Select security controls.
6. Assign security responsibilities.
7. Plan security testing.

### 1.2 Practical example

Imagine developing an e-commerce website.

| Area                | Security planning               |
| ------------------- | ------------------------------- |
| User accounts       | Secure authentication           |
| Passwords           | Password hashing                |
| Payment information | Encryption and payment security |
| Database            | Access restrictions             |
| Admin panel         | Role-based access control       |
| Application         | Vulnerability testing           |
| User activities     | Security logging                |

### 1.3 Important security planning activities

A. Asset identification

Identify what needs protection.

Examples:

- Customer information.
- Login credentials.
- Payment information.
- Database.
- Application source code.
- Server infrastructure.

B. Security control selection

Choose appropriate security measures.

Examples:

- MFA.
- Encryption.
- Firewalls.
- Access control.
- Secure backups.

C. Security responsibility

Assign responsibility to the correct team members.

Example:

- Developers: Secure coding.
- Security engineers: Security controls.
- Penetration testers: Vulnerability assessment.
- DevOps: Secure infrastructure and deployment.

Why is security planning important?

- Reduces security problems.
- Prevents expensive fixes later.
- Protects sensitive information.
- Improves application reliability.

## 2. Threat Awareness

Beginner to intermediate

Definition: Threat awareness means understanding possible attackers, attack methods, security weaknesses and potential damage to an application.

In simple words:

We need to understand what can go wrong and how an attacker might exploit it.

### 2.1 Common application security threats

[What is Cyber Security? | Types of Threats | Challenges - Scaler Topics.](https://images.openai.com/static-rsc-4/XB7kZSv9oFjlrXSvw5ZLcbhYyRO_z0FggF77kcGKrBSkpfSsC9USWBD18Gf-XqHGbAcD9qF5s0NdpeEu6wosgR7HNg-_g8bYZW4ZDGAGjE_zIzRbLjiHUuLYQGC3rcmQL-zr0ZrW4BhXhA_zvZ9DUixpAIRBmMMgEBoE-xmaxkE?purpose=inline)

1\. SQL Injection

An attacker manipulates database queries through unsafe user input.

Possible impact: Unauthorized database access.

[XSS (Cross-Site Scripting) :: PM Expert](https://images.openai.com/static-rsc-4/xxijgJO5u4K_EkC39oGf8damrlebcZBM8W467THcgmjVKu0QnzF-XmH-NqnMWqlUC_9LEQUGt_vSGyIB12ScKU52BmFzQxoZs9gjXh8dNWPtuVZnKbC5fhqrHOstcXESsJd2gPkzBEntIMv6jnkcIFPL8Lvck9n3k0vMJiQSPF4?purpose=inline)

2\. Cross-Site Scripting (XSS)

An attacker injects malicious scripts into web pages.

Possible impact: User session compromise or malicious actions in a user's browser.

[New hires are your weakest link when it comes to phishing attacks – here's how you can build a strong security culture that doesn't judge victims | IT Pro](https://images.openai.com/static-rsc-4/EWS3AfxefdSYM7tU7R_BgonyaumHTPZVnhJonqXk86Eg7QC0DGQfSSwIWL5uSjh4_XFyL3pPeI7owXO3dPEANHg4n2ZGMPYkIWpXGzB5tziz2R4t4qlYdhrumYWwP9fvvNoQqefeRj6WhilM13Lb27E5PBWMo6m7gT0M9QWJGOs?purpose=inline)

3\. Phishing

Attackers trick users into revealing credentials or sensitive information.

Possible impact: Account compromise.

[The OWASP Top 10 Explained with Real Code Examples | TechWayFit](https://images.openai.com/static-rsc-4/xAZkeFpRuaHx1NFpOySEm0zUiK4XqmPr-EV7ri3vrzxSYPdz-yKA_N30_si5ZucU0fjq4at9rKIETjWBKe2FrRgQbDoyQBFkB5YGODTiu3hfkwP0Em4m7hEEKv31y6MjJ7gMq1thzYkAw35ZaS4UHe6zI14--2cAq4fP_hILTr4?purpose=inline)

4\. Broken Access Control

Users can access resources or perform actions they should not be authorized to access.

Possible impact: Unauthorized access to another user's data.

[Understanding the Modern-day DoS Attacks Landscape](https://images.openai.com/static-rsc-4/nmrVeNFPlUHB08bXERJNN86fhxkDGRdlAaxuPXtBHQgSy0Zha2oheqp4CqPCo8FUk5Ll-HNieUv_XYG5SDy0WEWxqsmk3aX4xQIqUKo7SF3ealW-S4optc6hiOXjyxMPrbwuh6s1Ze0cwmnYjxG-41l_3vrpcc02sd4zGMdoMck?purpose=inline)

5\. Denial of Service (DoS)

An attacker overwhelms a service with requests or other resource-consuming activity.

Possible impact: Application becomes unavailable.

### 2.2 Threat awareness concepts

| Concept        | Meaning                                    |
| -------------- | ------------------------------------------ |
| Threat         | Something capable of causing harm          |
| Vulnerability  | A weakness in a system                     |
| Exploit        | A method of taking advantage of a weakness |
| Attack Vector  | The path used to conduct an attack         |
| Attack Surface | All exposed points that could be attacked  |
| Impact         | The damage caused by an attack             |

Understand the relationship:

Threat → Vulnerability → Exploit → Impact

Example:

- Threat: Malicious attacker.
- Vulnerability: Weak authentication.
- Exploit: Abuse of the login mechanism.
- Impact: Unauthorized account access.

### 2.3 How security teams identify threats

- Review application architecture.
- Analyze user input and authentication.
- Review network exposure.
- Study previous security incidents.
- Perform threat modeling.
- Review OWASP security guidance.

One important reference is the OWASP Top 10.

Official resource: [OWASP Top 10](https://owasp.org/www-project-top-ten/?utm_source=chatgpt.com)

## 3. Compliance Awareness

Intermediate level

Definition: Compliance awareness means understanding the security laws, regulations, industry standards and policies that an organization must follow when developing and managing software.

In simple words:

Companies must follow certain security rules to protect user information and maintain legal and industry requirements.

### 3.1 Why is compliance important?

Imagine an online banking company stores customer information.

The company cannot simply collect and store everything without following applicable privacy and security requirements.

It must consider:

- How customer information is collected.
- How personal information is stored.
- Who can access sensitive data.
- How information is protected.
- How security incidents are handled.
- Whether information can be shared with third parties.

### 3.2 Important security standards and regulations

| Standard / Regulation        | Main purpose                                           |
| ---------------------------- | ------------------------------------------------------ |
| GDPR                         | Protection of personal data in the EU                  |
| PCI DSS                      | Protection of payment card information                 |
| HIPAA                        | Protection of certain healthcare information in the US |
| ISO/IEC 27001                | Information Security Management System                 |
| NIST Cybersecurity Framework | Guidance for managing cybersecurity risks              |
| India's DPDP Act, 2023       | Protection of digital personal data in India           |

### 3.3 Understand each one

1\. GDPR

General Data Protection Regulation.

It establishes requirements for processing personal data within its scope.

Example: A website collecting information from EU users must consider applicable GDPR requirements.

Official website: [European Commission Data Protection](https://commission.europa.eu/law/law-topic/data-protection_en?utm_source=chatgpt.com)

2\. PCI DSS

Payment Card Industry Data Security Standard.

It provides security requirements for organizations that store, process or transmit payment card data.

Example:

- Protect cardholder data.
- Restrict access to payment systems.
- Monitor security activities.
- Maintain secure configurations.

Official website: [PCI Security Standards Council](https://www.pcisecuritystandards.org/?utm_source=chatgpt.com)

3\. ISO 27001

An international standard for establishing and maintaining an Information Security Management System (ISMS).

Example: A company creates policies for:

- Information security.
- Risk management.
- Access control.
- Incident management.

Official website: [ISO/IEC 27001](https://www.iso.org/standard/27001?utm_source=chatgpt.com)

4\. HIPAA

A US law that includes requirements for protecting certain health information.

Example: A healthcare application must protect electronic protected health information when HIPAA applies.

5\. India's DPDP Act

The Digital Personal Data Protection Act, 2023 establishes a framework for processing digital personal data in India.

Example: A company developing an Indian customer application must understand applicable personal-data protection obligations.

Official resource: [Ministry of Electronics and Information Technology](https://www.meity.gov.in/?utm_source=chatgpt.com)

### 3.4 Compliance vs Security

These two terms are related but not identical.

| Security                     | Compliance                                   |
| ---------------------------- | -------------------------------------------- |
| Protects systems and data    | Ensures applicable requirements are followed |
| Focuses on reducing risks    | Focuses on rules and obligations             |
| Uses technical controls      | Uses technical and organizational controls   |
| Continuous security activity | Requires ongoing compliance monitoring       |

Important: Passing a compliance audit does not automatically mean an application is completely secure.

## 4. Secure Design Principles

Intermediate to advanced

Definition: Secure design principles are fundamental rules used when designing software and systems to prevent vulnerabilities and reduce security risks.

In simple words:

Before developers write code, the application should be designed with security in mind.

### 4.1 Important secure design principles

1\. Principle of Least Privilege (PoLP)

Give users and systems only the permissions they need.

Example:

- Customer: View their own orders.
- Employee: Manage assigned orders.
- Administrator: Manage authorized system settings.

A normal customer should not have administrator access.

2\. Defense in Depth

Use multiple layers of security instead of relying on one security mechanism.

[Introduction to Defense in Depth: A Layered Approach to Cybersecurity](https://images.openai.com/static-rsc-4/Fh1ju_qCy81T4qXTNH3wqcQ4FtP5HFHI6Hvb4hA52pVxhgh7SS1YQGhYqH7MPmxizIvp-YwTmvpT5OV0ueMo8kuwoABJh6Hp4zhIZthA3Lp6DZInpZZQQNT25iAg5ltwwKi13_krU3TKScMBjzY9nIzjRsaDULAHFbTF4X6Wuaw?purpose=inline)

[natsar.com](https://www.natsar.com/blog/introduction-to-defense-in-depth-a-layered-approach-to-cybersecurity?utm_source=chatgpt.com)

Example:

An online banking application uses:

1. Firewall.
2. Secure authentication.
3. MFA.
4. Access control.
5. Database encryption.
6. Security monitoring.

If one layer fails, other layers can still provide protection.

3\. Secure by Default

Applications should use secure settings by default.

Example:

- Disable unnecessary services.
- Use secure authentication settings.
- Do not expose sensitive information.
- Restrict access unless explicitly authorized.

4\. Fail-Safe Defaults

When an authorization decision cannot be made, access should be denied by default.

Example:

If the application cannot verify whether a user has permission to access an administrator page, it should deny access.

5\. Separation of Duties

Divide sensitive responsibilities between different people or roles.

Example:

One employee initiates a financial transaction, while another authorized employee approves it.

6\. Minimize Attack Surface

Reduce the number of exposed services, interfaces and entry points.

Example:

- Remove unnecessary application features.
- Disable unused ports and services.
- Remove default accounts.
- Restrict unnecessary API endpoints.

7\. Complete Mediation

Check authorization every time a user accesses a protected resource.

Example:

A user must be authorized every time they request another customer's account information, not just when they initially log in.

8\. Secure Error Handling

Error messages should not expose sensitive internal information.

Bad example:

```
Database connection failed:
Username: admin
Password: admin123
Server: internal-db-01
```

Better example:

```
An internal error occurred.
Please try again later.
```

Log technical details securely for authorized administrators.

9\. Privacy by Design

Protect personal information during the entire application lifecycle.

Example:

- Collect only necessary information.
- Restrict access to personal data.
- Define retention periods.
- Protect stored information.

### 4.2 Quick revision table

| Principle               | Key idea                             |
| ----------------------- | ------------------------------------ |
| Least Privilege         | Minimum permissions                  |
| Defense in Depth        | Multiple security layers             |
| Secure by Default       | Safe initial configuration           |
| Fail-Safe Defaults      | Deny access when uncertain           |
| Separation of Duties    | Divide sensitive responsibilities    |
| Minimize Attack Surface | Reduce exposed entry points          |
| Complete Mediation      | Check every protected access         |
| Secure Error Handling   | Do not expose internal details       |
| Privacy by Design       | Protect personal data from the start |

## 5. Risk Identification

Intermediate to advanced

Definition: Risk identification is the process of discovering possible security risks that could affect an application's confidentiality, integrity, availability or business operations.

In simple words:

Identify what can go wrong, how it can happen and what damage it could cause.

### 5.1 Understand the difference

| Term          | Meaning                                            | Example                             |
| ------------- | -------------------------------------------------- | ----------------------------------- |
| Asset         | Something valuable                                 | Customer database                   |
| Threat        | Potential source of harm                           | Malicious attacker                  |
| Vulnerability | Security weakness                                  | Weak database permissions           |
| Risk          | Potential loss from a threat exploiting a weakness | Unauthorized customer data exposure |
| Impact        | Damage caused                                      | Customer privacy breach             |

### 5.2 Risk identification process

## Risk Identification Workflow

1. Identify Assets

   Find valuable information, systems and services.
2. Identify Threats

   Identify possible attackers, incidents and accidental events.
3. Identify Vulnerabilities

   Discover weaknesses in the application or infrastructure.
4. Analyze Likelihood

   Estimate how likely the risk is to occur.
5. Analyze Impact

   Estimate how serious the damage would be.
6. Evaluate and Prioritize Risks

   Decide which risks need attention first.
7. Plan Risk Treatment

   Select appropriate actions to reduce, avoid, transfer or accept the risk.

### 5.3 Risk assessment example

Imagine an online shopping application.

| Identified risk      | Likelihood | Impact   | Priority |
| -------------------- | ---------- | -------- | -------- |
| SQL Injection        | High       | Critical | Critical |
| Weak passwords       | High       | High     | High     |
| Information exposure | Medium     | High     | High     |
| Outdated software    | Medium     | Medium   | Medium   |
| Website downtime     | Low        | High     | Medium   |

These ratings are illustrative. A real assessment must use evidence and the organization's risk criteria.

### 5.4 Risk calculation

A simple qualitative risk model is:

\\[ Risk = Likelihood \times Impact \\]

For example, using a scale from 1 to 5:

- Likelihood = 4
- Impact = 5

\\[ Risk = 4 \times 5 = 20 \\]

High risk

This is a simplified prioritization technique, not a universal risk calculation standard.

### 5.5 Four risk treatment strategies

| Strategy | Meaning                              | Example                               |
| -------- | ------------------------------------ | ------------------------------------- |
| Avoid    | Stop the risky activity              | Remove an unnecessary exposed service |
| Mitigate | Reduce the risk                      | Implement MFA                         |
| Transfer | Shift certain financial consequences | Appropriate cyber insurance           |
| Accept   | Formally tolerate the risk           | Accept a low residual risk            |

### 5.6 Tools used for security risk identification

| Tool          | Main purpose                         |
| ------------- | ------------------------------------ |
| Nmap          | Discover hosts, ports and services   |
| Nessus        | Identify known vulnerabilities       |
| Burp Suite    | Investigate web application security |
| OWASP ZAP     | Identify web vulnerabilities         |
| Wireshark     | Analyze network traffic              |
| Threat Dragon | Create threat models                 |

These tools support different parts of an assessment. They do not replace security planning or risk analysis.

## 6. Practical Lab: Security Requirements Assessment



Hands-on practice

Red Team foundation



Now let's apply all five topics to one real training application.

Target: OWASP Juice Shop

Website: [Official OWASP Juice Shop](https://owasp.org/www-project-juice-shop/?utm_source=chatgpt.com)

### Lab scenario

You are working as a junior security analyst in a company.

The company wants to launch an e-commerce website. Your responsibility is to identify its security requirements before deployment.

### Task 1: Security planning

Identify these assets:

- Customer accounts.
- Login credentials.
- Customer personal information.
- Product database.
- Payment functionality.

### Task 2: Threat awareness

Identify five possible threats:

- SQL Injection.
- Cross-Site Scripting.
- Broken Access Control.
- Authentication weaknesses.
- Sensitive information exposure.

### Task 3: Compliance awareness

Identify which standards or regulations may apply to the application's data and business operations.

### Task 4: Secure design

Recommend:

- MFA for sensitive accounts.
- Least privilege.
- Encryption.
- Secure authentication.
- Server-side authorization.

### Task 5: Risk identification

Prepare a risk assessment table.

| Vulnerability           | Impact              | Recommendation                   |
| ----------------------- | ------------------- | -------------------------------- |
| Weak authentication     | Account compromise  | MFA and secure authentication    |
| SQL Injection           | Database compromise | Parameterized queries            |
| Broken access control   | Unauthorized access | Server-side authorization        |
| Sensitive data exposure | Privacy breach      | Encryption and data minimization |

Your final deliverable: Create a document called `Security-Requirements-Assessment.md` and include your findings, risk ratings and recommendations.

Use an authorized Juice Shop training instance for practical testing.

## 7. Important Interview and Exam Questions

Prepare these questions for your cybersecurity course.

1. What are security requirements?
2. What is security planning?
3. What is threat awareness?
4. Differentiate between threat, vulnerability and risk.
5. What is compliance awareness?
6. Explain GDPR and PCI DSS.
7. What is ISO 27001?
8. Explain the principle of least privilege.
9. What is defense in depth?
10. What is secure by default?
11. What is attack surface?
12. Explain risk identification.
13. What are the four risk treatment strategies?
14. How does threat modeling help secure software?
15. Why should security requirements be identified before development?

## 8. Knowledge Check

Test your understanding with these five questions.

Module 2 Assessment

5 Questions

1\. What is the main purpose of security planning?

Writing application code

Identifying security needs before development

Deploying the application



2\. What is a vulnerability?

A system weakness

An attacker

A security standard



3\. Which standard focuses on payment card security?

GDPR

HIPAA

PCI DSS



4\. Which principle provides multiple layers of protection?

Least privilege

Defense in depth

Separation of duties



5\. What are the four common risk treatment strategies?

Avoid, mitigate, transfer, accept

Scan, exploit, attack, delete

Plan, code, test, deploy



Submit answers

## 9. Module 2 Quick Revision

| Topic                | Remember this                               |
| -------------------- | ------------------------------------------- |
| Security Planning    | Decide how to protect software              |
| Threat Awareness     | Understand possible attacks                 |
| Compliance Awareness | Understand applicable security requirements |
| Secure Design        | Build security into architecture            |
| Risk Identification  | Discover and prioritize risks               |

The complete learning connection:

Module 1: Secure SDLC Fundamentals

Understand the secure development lifecycle

Module 2: Security Requirements

Identify what needs protection and why

Next: Security Architecture and Threat Modeling

Design the security controls and analyze attack paths

My recommendation: Don't just memorize these concepts. Practise identifying assets, threats, vulnerabilities and risks in applications. This builds the foundation needed for application security assessment and penetration testing.
