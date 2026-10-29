# Module 5: Understand Cloud Threats ☁️🔐

Cloud threats are risks that can damage cloud systems, steal sensitive information, or allow unauthorized people to access cloud resources.

Example: A company stores customer details in AWS, Azure, or Google Cloud. If the storage is accidentally made public, attackers may access those details. This is a cloud security threat.

Let's learn all five topics in simple English, with examples, prevention methods, and exam questions.

## 1. Misconfigurations

Definition: A cloud misconfiguration happens when a cloud service or security setting is configured incorrectly.

In simple words, the cloud system is set up in the wrong way, creating a security weakness.

[Billions of Files at Risk: The Growing Threat of Misconfigured Cloud Storage Buckets | by Siva Gunasekaran | Medium](https://images.openai.com/static-rsc-4/yhVVoKUXwg9uPtYKzPWCPEtVNBLuWgD9IJX7D8gzmG-zwJX7sfKP5LSX2-Y7CYM1nMZwe_UoNVWccS8u98amcDPG8MY4Es7m0KbnhyxpzfqCc2zbbpbCXYc2erfqDLcWUvLSqJcC7BHs8eJcNHKKXDCIXJq4qCKEjG0u6v_tdBo?purpose=inline)

[medium.com](https://medium.com/%40sivagunasekaran/billions-of-files-at-risk-the-growing-threat-of-misconfigured-cloud-storage-buckets-864cffe2d40b?utm_source=chatgpt.com)

Common examples:

- A storage bucket is accidentally made public.
- A database is exposed to the internet.
- A firewall allows connections from everyone.
- Security logging is disabled.
- A server is running with insecure settings.

Real-life scenario:

A company stores customer records in a cloud storage bucket. An employee mistakenly changes the permissions from private to public. Anyone who discovers the public location may be able to access the records.

How to prevent misconfigurations:

1. Review cloud settings regularly.
2. Keep storage private by default.
3. Use secure configuration templates.
4. Enable configuration monitoring and alerts.
5. Apply security policies and automated checks.

Exam point: Misconfiguration is a security weakness caused by incorrect cloud settings.

## 2. Credential Theft

Definition: Credential theft occurs when an attacker steals login information, such as usernames, passwords, access keys, or authentication tokens.

Credentials act like keys to your cloud account. If attackers steal them, they may enter the account as if they were legitimate users.

[Phishing scam, hacker attack](https://images.openai.com/static-rsc-4/cCgCiHczXHk-3Ax3ofacKiwecc8ZstXNrp2adyaieOiKMhPL2JCIAcSSlDApR_9ZjKvhMfcrygVv0NIHtsU0vZLMP_suzXgMSCXavTVl9899naYrwGenscCNyLhcjM3GgXiJkjbOR9Bud_Nkobia02zy2TRAKp3I7h7PqpqwCFwc79waG1s4sld-en4aO2np?purpose=inline)

Common methods:

- Phishing emails and fake login pages.
- Weak or reused passwords.
- Malware that steals saved credentials.
- Access keys accidentally uploaded to public code repositories.
- Stolen session tokens.

Real-life scenario:

A cloud administrator receives a fake email asking them to verify their account. They enter their password on a fake website. An attacker steals the password and attempts to access the company's cloud resources.

How to prevent credential theft:

1. Enable multi-factor authentication (MFA).
2. Use strong, unique passwords and a password manager.
3. Never share passwords or access keys.
4. Store secrets in a secure secrets manager.
5. Rotate exposed credentials and revoke compromised sessions.
6. Monitor unusual login attempts.

Exam point: Credential theft allows attackers to use stolen authentication information to access cloud accounts.

## 3. Excessive Permissions

Definition: Excessive permissions occur when a user, application, or service has more access rights than necessary to perform its tasks.

In simple words, a person gets more power than their job requires.

[Stop Being a Noob: The Real Way to Set Up Your AWS Account (Without Breaking Everything) | by Sai Varaprasad | Medium](https://images.openai.com/static-rsc-4/BR97ou7AhMSPtnlXTYxCGYmYBmaku9qPTrMWf-Tv4bgTRuMBg9oKLXFcfucTETxangMe3SYulYRqPt5TNtU8mrJ7Aofe9FOep8WJ1BA050Lg0pkUMkbaGnl9pPRhk28i-tbYLq2x3bV11ChVgWJuALsd3F4UFr8BCDz_dVkwIx4?purpose=inline)

[medium.com](https://medium.com/%40saivaraprasadb/stop-being-a-noob-the-real-way-to-set-up-your-aws-account-without-breaking-everything-2d8ce9579c17?utm_source=chatgpt.com)

Example of excessive permissions:

Imagine three employees:

| Employee     | Required access           | Excessive access                    |
| ------------ | ------------------------- | ----------------------------------- |
| Data analyst | Read reports              | Delete all databases                |
| Developer    | Manage development server | Change production security settings |
| Intern       | View assigned files       | Access every customer's records     |

Giving unnecessary permissions increases the damage an account can cause if compromised or misused.

How to prevent excessive permissions:

1. Follow the principle of least privilege.
2. Use role-based access control (RBAC).
3. Review permissions regularly.
4. Remove unused accounts and access rights.
5. Give temporary permissions when possible.
6. Separate administrator and everyday accounts.

Important concept: Principle of Least Privilege

Give each user only the minimum access required to do their job.

Exam point: Excessive permissions increase the risk of unauthorized actions and privilege abuse.

## 4. Data Exposure

Definition: Data exposure happens when sensitive information becomes accessible to unauthorized people.

Data exposure can happen accidentally or through a deliberate attack.

[Cloud server data security lock, flat isometric 3d illustration](https://images.openai.com/static-rsc-4/sCnsWlVRAz1FW0CqqIMpSCoif_Q6KMy50EGNz0DU2PmZYSYDl1TiHmTka1Nx1Gq0ibxpFlKU_jpl5TXjlP_qxaWL16byDXANJ5T9EVmc6cbgzNh2v7uWu7TIm-zLoI0XMWcP-xA-lAP__H4xyqyFuGLz59Xmx6gDAaOjblV3q_x1t7WWKDk6WXAdvd5L7tpH?purpose=inline)

Examples:

- Customer records stored in a public cloud folder.
- Personal information sent to the wrong person.
- An exposed database containing financial records.
- Sensitive files downloaded by an unauthorized user.
- An unencrypted backup being accessed by an attacker.

Types of sensitive data:

- Personal information
- Passwords and authentication secrets
- Financial records
- Business documents
- Medical or customer records

How to prevent data exposure:

1. Encrypt data at rest and in transit.
2. Restrict access to authorized users.
3. Classify sensitive data.
4. Keep storage private and verify sharing settings.
5. Use data loss prevention (DLP) controls where appropriate.
6. Back up data securely and monitor access.

Encryption explained simply:

Encryption transforms readable data into an unreadable form using cryptographic methods. An authorized party with the appropriate key can decrypt it.

Remember: Encryption helps protect data, but it does not replace access control. A publicly exposed file may still reveal information if it is unencrypted or its decryption keys are also exposed.

Exam point: Data exposure is the unauthorized disclosure or accessibility of sensitive information.

## 5. Insider Threats

Definition: An insider threat is a security risk caused by someone who has legitimate access to an organization's systems or information.

An insider may be an employee, contractor, administrator, or another trusted user.

[Cuando el enemigo ya está dentro de la empresa: la amenaza cyber de los "insiders" y cómo contenerla - Yahoo Noticias](https://images.openai.com/static-rsc-4/RihZcHFrqOXkDWxVwZXg1-IyBVnr3PkOpN3Nei_PIOHna3aVBRKD_TSPqKZkRstNutPu_MOCuwGbtUV3V5uvt6FvnCe2EVDV2HABcOajMxykYE-sFFCs3KDAYvpdzD5H6aHEbZ-_Xc-bhnf_oN33sdn9fGWFbYdJiViWFm4i0-g?purpose=inline)

[es-us.noticias.yahoo.com](https://es-us.noticias.yahoo.com/enemigo-empresa-amenaza-cyber-insiders-185100884.html?utm_source=chatgpt.com)

Types of insider threats:

- Malicious insider: Intentionally steals or damages information.
- Negligent insider: Accidentally exposes information by making a mistake.
- Compromised insider account: An attacker uses a legitimate employee's stolen account.

Real-life scenario:

An employee who is leaving a company downloads confidential customer information without permission. The employee already had legitimate access to the system but misuses it.

Another example is an employee accidentally sharing a confidential cloud document with the public.

How to prevent insider threats:

1. Apply least-privilege access.
2. Monitor sensitive data access and downloads.
3. Maintain audit logs.
4. Remove access immediately when employees leave or change roles.
5. Separate sensitive duties between different people.
6. Train employees in security awareness.
7. Investigate unusual activity fairly and according to company policy.

Exam point: Insider threats can be intentional, accidental, or caused by compromised legitimate accounts.

## Quick comparison for exams

| Cloud threat          | Main problem                            | Example                                 |
| --------------------- | --------------------------------------- | --------------------------------------- |
| Misconfiguration      | Incorrect settings                      | Public storage bucket                   |
| Credential theft      | Stolen login details                    | Phishing steals an admin password       |
| Excessive permissions | Too much access                         | Analyst can delete production databases |
| Data exposure         | Sensitive data becomes accessible       | Customer records exposed online         |
| Insider threat        | Trusted access is misused or mishandled | Employee copies confidential files      |

## How the five threats can connect

Consider a single attack scenario:

1\. Misconfiguration

A cloud service is set up insecurely.

2\. Data exposure

Sensitive information becomes accessible.

3\. Attacker gains access

Stolen credentials or excessive permissions may help the attacker reach more resources.

4\. Security incident

Information may be stolen, altered, or deleted.

This is one possible scenario, not a sequence that every cloud attack follows.

## Important exam questions and answers

Q1. What is a cloud threat?

A cloud threat is a potential danger that can compromise the confidentiality, integrity, or availability of cloud resources and data.

Q2. What is cloud misconfiguration?

It is an incorrect or insecure cloud setting that may allow unauthorized access or expose resources.

Q3. What is credential theft?

It is the unauthorized acquisition of login information, passwords, access keys, or authentication tokens.

Q4. What is the principle of least privilege?

It means providing users and applications only the minimum permissions needed for their tasks.

Q5. What is data exposure?

It is the unauthorized disclosure or accessibility of sensitive information.

Q6. What is an insider threat?

It is a security risk caused by someone with legitimate access who intentionally or accidentally misuses that access, or whose account is compromised.

Q7. Scenario question: A cloud administrator discovers that an employee can access every database even though the employee only prepares reports. Identify the threat and suggest a solution.

Answer: This is excessive permissions. Apply least privilege, assign a suitable role with read-only access to the required reports, and review permissions regularly.

Q8. Scenario question: A company accidentally makes its cloud storage public. What is the threat, and how can it be prevented?

Answer: The primary threat is misconfiguration, which can lead to data exposure. Keep storage private, review access policies, and use automated configuration monitoring.

## Final revision notes

Remember these five definitions:

- Misconfiguration: Wrong security settings.
- Credential theft: Stolen login information.
- Excessive permissions: More access than necessary.
- Data exposure: Sensitive information becomes accessible to unauthorized people.
- Insider threat: Risk from trusted access being misused, mishandled, or compromised.

Exam tip: For a 5-mark answer, write the definition, explain two or three examples, and include prevention methods. For a 10-mark answer, add a real-life scenario and explain how the threat affects cloud confidentiality, integrity, and availability.
