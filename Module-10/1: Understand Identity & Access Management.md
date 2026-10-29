# Module 1: Understand Identity & Access Management (IAM)

Cloud Computing and Cybersecurity Study Notes ☁️🔐

IAM is one of the most important topics in cloud security. It helps organizations control who can access a system, how they prove their identity, and what they are allowed to do.

## 1. What is IAM?

IAM (Identity and Access Management) is a security system used to manage digital identities and control access to resources such as applications, servers, databases, and cloud services.

In simple words, IAM decides who you are and what you can access.

[Workforce Identity and Access Management (IAM) Explained](https://images.openai.com/static-rsc-4/8fxfBSArzyIs69icotRiPd87cmvmMlJM_yuoxuCEOyPvRRT7Fu_azYU9FBB4oE81Qh6kEdYW76XuF8HT5KUi4O_Ez5MbX-sF5gavCnz90f9QZmavzuppFLCLaGSQ1Ea80in_gnFypRBSjQ5iHo0gbwQNY3A_XHJ8mONy40JwitM?purpose=inline)

[strongdm.com](https://www.strongdm.com/blog/workforce-identity-and-access-management?utm_source=chatgpt.com)

Example:

Imagine a company uses AWS cloud.

- An administrator can create users and manage cloud resources.
- A developer can access application servers.
- An employee can access only their work application.
- An unauthorized person cannot access the system.

IAM ensures that each person receives the correct level of access.

### Why is IAM important?

1. Prevents unauthorized access.
2. Protects confidential data.
3. Reduces the risk of cyberattacks.
4. Ensures users have only the permissions they need.
5. Helps organizations track and audit user activities.

### Main components of IAM

| Component      | Meaning                                     |
| -------------- | ------------------------------------------- |
| Identity       | A user, application, device, or service     |
| Authentication | Verifying who you are                       |
| Authorization  | Deciding what you can do                    |
| Permissions    | Specific actions you are allowed to perform |
| Policies       | Rules that control access                   |
| Audit logs     | Records of access and activity              |

## 2. Authentication concepts

Authentication is the process of verifying a user's identity.

In simple words, it answers: "Are you really who you claim to be?"

[Multi-Factor Authentication: How It Works and Why It Matters](https://images.openai.com/static-rsc-4/St-yF0i-LVrHCUr9AvQ7ttOwNB4_c511Lo748t1ChuUdNwVbCFqB_OJyp7Y78AF7gaINqsKrFPkQ_nTBX38tpUQXn1NEiqHh-bWCDPCKtC3YDAxoZNNM46SyIiA7mW_VnaOlv4Lbhr4RTIWA2mN9dcydTBGf13MUITJz-8g1oR4?purpose=inline)

[aratek.co](https://www.aratek.co/news/multi-factor-authentication-how-it-works-and-why-it-matters?utm_source=chatgpt.com)

### Common authentication methods

1\. Password authentication

The user enters a username and password.

Example: Logging into your email account.

2\. Multi-factor authentication (MFA)

The user provides two or more different types of verification.

Example:

- Something you know: password.
- Something you have: phone or security key.
- Something you are: fingerprint or face recognition.

Even if an attacker steals your password, MFA can help prevent account access.

3\. One-time password (OTP)

A temporary code used to verify identity.

Example: Entering a code received through an authenticator app or SMS.

4\. Biometric authentication

Uses physical characteristics such as fingerprints or facial recognition.

5\. Single sign-on (SSO)

Allows a user to sign in once and access multiple approved applications without separately logging in to each one.

Example: Using one company account to access email, an HR portal, and a work application.

### Authentication vs. Authorization

| Authentication                  | Authorization                                            |
| ------------------------------- | -------------------------------------------------------- |
| Verifies identity               | Checks permissions                                       |
| Answers "Who are you?"          | Answers "What can you do?"                               |
| Uses passwords, MFA, biometrics | Uses roles, policies, permissions                        |
| Happens before access decisions | Determines allowed actions after identity is established |

Easy example: A security guard checks your ID to verify who you are. Then the guard checks your access pass to determine which rooms you can enter.

## 3. Authorization concepts

Authorization determines which resources and actions an authenticated identity is allowed to access.

For example, after logging into a cloud platform, a user may be permitted to view files but not delete them.

### Common authorization models

[Announcing Advanced RBAC in Superblocks: Unify, centralize, and simplify governance](https://images.openai.com/static-rsc-4/-V2sO7BQkhfeE_tUbEnocA3MHlghDpIrX6ns4wCIImO81MEClGPvtYItiPskeLP3x1NXJHsAuc0hid1UmQnZNEtMLwbr7W2qVV9pezvWqisKNr184HQ8bn7gv7CGHIYnT8vMn7ZhKcoe2rTHXAE1AH_rOEd5OnwHmNG3XalAqc0?purpose=inline)

1\. RBAC: Role-Based Access Control

Permissions are assigned to roles, and users receive access through those roles.

Example: A cloud administrator manages resources, while a developer deploys applications.

[RBAC vs ABAC vs PBAC: Key Access Control Differences](https://images.openai.com/static-rsc-4/8Aq78aZoIVHCzfWBhfCmxCFsAbKAu-CI5UHU97K9sImU7pzdXWHkIRcTlQ95nW6Tg3S43q1NMdH4y9B_nW6yJrilSik0z3OIo-ks4NTIr6yebMi7xiC3P_ZuW4JY63aBD1mamgb-Ff1S6jSCompP_KSdA-3WlSRG3iVPiRvZJG0?purpose=inline)

2\. ABAC: Attribute-Based Access Control

Access depends on attributes such as department, device security, location, or resource classification.

Example: An employee can access a confidential document only from an approved device.

[What Is the Principle of Least Privilege (PoLP)?  | Wiz](https://images.openai.com/static-rsc-4/-wUos8i0zxR23Doj6RYK3TMx2oC2N_L35ZRxrOXOXf2ux5aASk4dsmc8i8HFmoaZIVXipMDfMCAdvx0uuN6g_hdnajhy7ZZPIZvQJiXR8__NE-ufnRj9DZdkapksdRb2mqM6lEsLU1rZpuEI-uZzK2HG_gBDimVvYbic5RMjuz8?purpose=inline)

3\. Least privilege

Users receive only the minimum permissions needed to perform their jobs.

Example: A report viewer can read reports but cannot modify or delete them.

### Important authorization terms

- Permission: An allowed action, such as reading a file.
- Role: A collection of permissions associated with a job or function.
- Policy: A rule that allows or denies access.
- Privilege escalation: When a user gains permissions beyond those they should have.
- Separation of duties: Dividing sensitive tasks among different people to reduce misuse.

Exam tip: Authentication verifies identity; authorization controls access.

## 4. Identity lifecycle

The identity lifecycle is the process of managing a digital identity from its creation until its access is removed.

1\. Provisioning

Create an account and grant required access.

2\. Modification

Update roles and permissions when responsibilities change.

3\. Review

Check whether existing access is still appropriate.

4\. Deprovisioning

Disable accounts and revoke access when it is no longer needed.

### Real-world example

A company hires a new cloud engineer.

1. The IT team creates the engineer's account.
2. The engineer receives access to approved development resources.
3. The engineer changes teams, so their permissions are updated.
4. The engineer leaves the company, so the account is disabled and access is revoked.

### Why is identity lifecycle management important?

- Prevents former employees from accessing company systems.
- Avoids unnecessary permissions.
- Reduces orphaned accounts, which are accounts no longer owned or needed.
- Helps maintain accurate access records.
- Supports security audits and compliance.

Important: Deprovisioning should also cover active sessions, access keys, tokens, and other credentials where applicable. Simply disabling a login may not revoke every existing form of access.

## 5. Access governance

Access governance is the process of ensuring that access rights are appropriate, approved, reviewed, and compliant with security policies.

IAM provides the mechanisms to control access. Access governance ensures those mechanisms are being used correctly.

### Main activities

| Activity             | Explanation                                            |
| -------------------- | ------------------------------------------------------ |
| Access reviews       | Check whether users still need their permissions       |
| Approval workflows   | Require authorization before granting sensitive access |
| Least privilege      | Limit access to what is necessary                      |
| Separation of duties | Prevent one person from controlling conflicting tasks  |
| Audit and monitoring | Review access records and suspicious activity          |
| Policy enforcement   | Ensure access follows company rules                    |
| Compliance           | Help meet applicable legal and regulatory requirements |

### Example: Access review

Suppose an employee moves from the finance department to the marketing department.

Their old finance permissions should be reviewed and removed if no longer needed. They should receive only the permissions required for their new role.

Without access governance, the employee might retain access to sensitive financial information unnecessarily.

### Important principle: Zero Trust

Zero Trust follows the principle "Never trust automatically; verify explicitly."

It means access decisions should consider identity, permissions, device or session risk, and other relevant signals rather than assuming a user is safe simply because they are inside the company network.

## 6. Practical cloud security scenario

Scenario: A company discovers that a former employee can still access its cloud storage.

What should the security team do?

1. Disable the former employee's account.
2. Revoke active sessions, access tokens, and credentials as appropriate.
3. Review access logs to identify activity after departure.
4. Check for other inactive or unnecessary accounts.
5. Review the identity lifecycle and employee departure process.
6. Implement automated deprovisioning and periodic access reviews.

Lesson: Strong IAM combines authentication, authorization, lifecycle management, and governance.

## 7. Exam revision questions

## IAM knowledge check

6/6 answered

1\. What does IAM stand for?

Internet Access Monitoring

Identity and Access Management

Internal Account Method

Identity Application Module

Correct! IAM manages digital identities and their access to resources.

2\. Which process verifies a user's identity?

Authorization

Provisioning

Authentication

Access review

Correct! Authentication checks whether the user is who they claim to be.

3\. A user can log in but cannot delete a file. Which concept controls this?

Authentication

Authorization

Identity creation

Deprovisioning

Correct! Authorization determines which actions an authenticated user may perform.

4\. What should happen when an employee leaves a company?

Keep all permissions active

Share their password

Disable access and revoke relevant credentials

Give them administrator access

Correct! Deprovisioning prevents continued unauthorized access.

5\. Which model assigns permissions based on job roles?

MFA

ABAC

RBAC

SSO

Correct! RBAC means Role-Based Access Control.

6\. What is the purpose of access governance?

Create stronger passwords only

Ensure access is appropriate and reviewed

Increase all users' permissions

Replace authentication

Correct! Access governance oversees approvals, reviews, policies, and compliance.

### Score: 6/6

Try again

## 8. Final quick revision

Remember these five concepts:

1. IAM: Manages identities and access.
2. Authentication: Verifies who you are.
3. Authorization: Determines what you can do.
4. Identity lifecycle: Creates, updates, reviews, and removes access.
5. Access governance: Ensures access is appropriate, approved, and monitored.

These fundamentals apply across AWS, Microsoft Azure, and Google Cloud, although each platform uses its own services and terminology.
