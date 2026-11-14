# Secure SDLC, Application Security & DevSecOps

**Learning Level:** Beginner to Advanced  
**Category:** Cybersecurity | Application Security | DevSecOps  
**Purpose:** Theory, Practical Learning, Interview Preparation and Hands-on Assessment

---

# Table of Contents

1. [Secure SDLC Fundamentals](#1-secure-sdlc-fundamentals)
2. [Security Requirements](#2-security-requirements)
3. [Secure Coding Principles](#3-secure-coding-principles)
4. [Application Security Testing](#4-application-security-testing)
5. [DevSecOps Fundamentals](#5-devsecops-fundamentals)
6. [CI/CD Security](#6-cicd-security)
7. [Software Supply Chain Security](#7-software-supply-chain-security)
8. [Advanced Security Concepts](#8-advanced-security-concepts)
9. [Hands-on Practical Tasks](#9-hands-on-practical-tasks)
10. [Fundamental Interview Questions](#10-fundamental-interview-questions)
11. [Scenario-Based Interview Questions](#11-scenario-based-interview-questions)
12. [DevSecOps Tools](#12-devsecops-tools)
13. [Technical Vocabulary](#13-technical-vocabulary)
14. [Final Examination Practice](#14-final-examination-practice)
15. [21-Day Study Roadmap](#15-21-day-study-roadmap)
16. [Final Portfolio Project](#16-final-portfolio-project)
17. [Official Learning Resources](#17-official-learning-resources)

---

# 1. Secure SDLC Fundamentals

## 1.1 What is SDLC?

**SDLC stands for Software Development Life Cycle.**

SDLC is a structured process used to develop software applications.

It explains how software is planned, designed, developed, tested, deployed and maintained.

### Seven Common SDLC Stages

1. **Planning:** Decide what software to build, its purpose, budget and resources.
2. **Requirement Analysis:** Understand what users and the business need.
3. **Design:** Create application architecture, database design and workflows.
4. **Development:** Developers write the application code.
5. **Testing:** Check functionality, quality and security.
6. **Deployment:** Release the application to production.
7. **Maintenance:** Monitor, update and fix the application.

### Why is SDLC Important?

- Organizes software development.
- Reduces development mistakes.
- Improves software quality.
- Helps manage development costs.
- Establishes clear responsibilities.
- Ensures software meets requirements.

## 1.2 What is Secure SDLC?

**Secure SDLC means integrating security into every stage of the Software Development Life Cycle.**

Traditional SDLC focuses mainly on making software work correctly.

Secure SDLC focuses on making software work correctly and securely.

### Example: Banking Application

Traditional development asks:

- Does login work?
- Can users access their dashboard?
- Can users transfer money?

Secure development additionally asks:

- Are passwords stored securely?
- Can attackers bypass authentication?
- Is SQL injection possible?
- Can one user access another user's account?
- Is sensitive information protected?

### SDLC vs Secure SDLC

| Traditional SDLC | Secure SDLC |
|---|---|
| Focuses on functionality | Focuses on functionality and security |
| Security may be tested late | Security starts during planning |
| Fixes problems after discovery | Prevents problems early |
| Mainly functional testing | Functional and security testing |
| Security may be separate | Security is integrated |

## 1.3 Security Throughout Development

Security must be included in every SDLC stage.

| SDLC Stage | Security Activity |
|---|---|
| Planning | Identify security goals |
| Requirements | Define security requirements |
| Design | Threat modelling |
| Development | Secure coding |
| Testing | SAST, DAST and penetration testing |
| Deployment | Secure configuration |
| Maintenance | Monitoring and patching |

### Real-World Example

An organization develops an online banking application.

- **Planning:** Identify customer financial data as sensitive.
- **Requirements:** Require MFA and access control.
- **Design:** Design secure authentication and encrypted communication.
- **Development:** Apply secure coding practices.
- **Testing:** Check SQL injection, broken access control and authentication weaknesses.
- **Deployment:** Apply HTTPS and secure configurations.
- **Maintenance:** Monitor security logs and patch vulnerabilities.

## 1.4 Security Responsibilities

Security is a shared responsibility.

| Role | Security Responsibility |
|---|---|
| Business Analyst | Identify security requirements |
| Software Architect | Design secure architecture |
| Developer | Write secure code |
| Security Engineer | Define security controls |
| AppSec Tester | Discover application vulnerabilities |
| DevOps Engineer | Secure infrastructure and pipelines |
| SOC Analyst | Monitor security events |
| Project Manager | Ensure security activities are completed |

## 1.5 Risk Reduction Strategies

Risk reduction means taking actions to decrease the possibility or impact of security incidents.

### Common Application Risks

- SQL injection
- Password theft
- Brute-force attacks
- Account takeover
- Session hijacking
- Sensitive data exposure

### Risk Reduction Methods

1. Input validation.
2. Parameterized SQL queries.
3. Multi-factor authentication.
4. Password hashing.
5. Rate limiting.
6. Secure session management.
7. Security testing.
8. Regular updates.
9. Access control.
10. Security monitoring.

### Four Risk Treatment Methods

| Method | Meaning | Example |
|---|---|---|
| Avoid | Stop the risky activity | Remove an unnecessary exposed feature |
| Mitigate | Reduce the risk | Implement MFA |
| Transfer | Transfer some financial impact | Cyber insurance |
| Accept | Accept remaining risk | Accept a low-impact issue with approval |

### Interview Questions

**Q1. What is SDLC?**

SDLC is a structured process used to develop software through planning, requirements, design, development, testing, deployment and maintenance.

**Q2. What is Secure SDLC?**

Secure SDLC integrates security activities into every stage of software development to prevent vulnerabilities.

**Q3. Why should security testing start early?**

Early testing helps identify weaknesses before they become deeply integrated into the application. Early fixes are generally less expensive.

**Q4. Who is responsible for application security?**

Everyone involved in developing, testing, deploying and maintaining the application.

### Scenario-Based Questions

**Scenario 1:** A company performs security testing only after deployment. A vulnerability exposes customer information.

- What went wrong?
- Which approach was missing?
- How could the company prevent this?

**Answer:** Security was not integrated throughout development. Secure SDLC should include security requirements, threat modelling, secure coding, pre-deployment testing and monitoring.

**Scenario 2:** A developer says security is only the cybersecurity team's responsibility.

**Answer:** This is incorrect. Developers, testers, security engineers and DevOps engineers all have security responsibilities.

---

# 2. Security Requirements

Security requirements define what an application must do to protect users, information and infrastructure.

## 2.1 Security Planning

Security planning means deciding what protections an application needs before development.

### Example: Healthcare Application

Security planning should identify:

- How patient information is protected.
- Who can access patient records.
- How users authenticate.
- How information is encrypted.
- How incidents are detected.
- How backups are protected.

### Important Planning Activities

1. Identify sensitive information.
2. Identify possible attackers.
3. Identify application assets.
4. Define security requirements.
5. Select security controls.
6. Assign responsibilities.
7. Plan security testing.
8. Establish incident response procedures.

### What is an Asset?

An asset is anything valuable that must be protected.

Examples:

- User accounts
- Passwords
- Customer information
- Payment information
- Source code
- Databases
- Cloud servers
- API keys

## 2.2 Threat Awareness

A threat is a potential danger that can exploit a weakness and cause damage.

### Important Terminology

| Term | Meaning |
|---|---|
| Asset | Something valuable |
| Threat | Potential danger |
| Vulnerability | Security weakness |
| Exploit | Method of taking advantage of a vulnerability |
| Risk | Possibility and impact of harm |
| Attack Surface | All possible entry points into a system |
| Threat Actor | Person or group behind an attack |

### What is Threat Modelling?

Threat modelling is the process of identifying possible attacks against an application and deciding how to prevent them.

### STRIDE Threat Modelling

| STRIDE | Meaning | Example |
|---|---|---|
| S | Spoofing | Attacker impersonates a user |
| T | Tampering | Unauthorized modification of data |
| R | Repudiation | User denies performing an action |
| I | Information Disclosure | Sensitive data exposure |
| D | Denial of Service | Application becomes unavailable |
| E | Elevation of Privilege | Normal user obtains admin privileges |

### What is DFD?

DFD stands for Data Flow Diagram.

It represents how information moves through an application.

Example:

`User → Web Application → API → Database`

Threat modelling examines components and communication paths to identify weaknesses.

## 2.3 Compliance Awareness

Compliance means following applicable laws, regulations, standards and organizational security requirements.

### Important Standards and Regulations

| Standard / Regulation | Main Purpose |
|---|---|
| ISO/IEC 27001 | Information Security Management |
| PCI DSS | Payment Card Data Security |
| GDPR | Personal Data Protection within its scope |
| HIPAA | Protection of health information within its scope |
| SOC 2 | Trust-related organizational controls |
| NIST CSF | Cybersecurity Risk Management |

Important distinction:

- ISO 27001 is a standard.
- PCI DSS is an industry security standard.
- GDPR is a legal regulation.
- SOC 2 is an attestation framework.

## 2.4 Secure Design Principles

1. **Least Privilege:** Give users only the permissions they need.
2. **Defense in Depth:** Use multiple layers of security.
3. **Fail Securely:** Deny access when security verification fails.
4. **Secure by Default:** Default settings should be secure.
5. **Separation of Duties:** Divide sensitive responsibilities.
6. **Complete Mediation:** Check authorization whenever protected resources are accessed.
7. **Minimize Attack Surface:** Remove unnecessary services and exposed endpoints.
8. **Keep Security Simple:** Avoid unnecessarily complicated designs.
9. **Open Design:** Do not depend on hiding system design for security.
10. **Zero Trust:** Verify access instead of automatically trusting users or devices.

## 2.5 Risk Identification

Risk identification means discovering possible security problems before they cause damage.

### Risk Assessment

A basic risk assessment considers:

- **Likelihood:** How likely is the incident?
- **Impact:** How serious would the damage be?

Simple model:

`Risk Score = Likelihood × Impact`

Example:

| Likelihood | Impact | Score |
|---:|---:|---:|
| 5 | 5 | 25 |
| 4 | 3 | 12 |
| 2 | 2 | 4 |

This is a simplified model. Organizations may use more detailed methodologies.

### Interview Questions

1. What is a security requirement?
2. What is threat modelling?
3. Difference between threat and vulnerability?
4. Explain STRIDE.
5. What is an attack surface?
6. What is a DFD?
7. What is least privilege?
8. Explain defense in depth.
9. What is Zero Trust?
10. What is compliance?
11. What is risk assessment?
12. Difference between likelihood and impact?

### Scenario-Based Questions

**Scenario 1:** A healthcare application allows all employees to access patient records.

**Answer:** This is broken access control and excessive permissions. Implement role-based access control and least privilege.

**Scenario 2:** A company plans a payment application without identifying possible threats.

**Answer:** Perform threat modelling, identify assets, map data flows, assess threats and define security requirements before development.

**Scenario 3:** An application has a firewall, but its database is publicly accessible.

**Answer:** Defense in depth and secure configuration have failed. A firewall alone does not provide complete protection.

---

# 3. Secure Coding Principles

Secure coding means writing software code in a way that prevents common security vulnerabilities.

## 3.1 Input Validation

Input validation means checking user-provided data before accepting or processing it.

### Types of Validation

1. **Type Validation:** Check the data type.
2. **Length Validation:** Check the number of characters.
3. **Range Validation:** Check allowed values.
4. **Format Validation:** Check expected format.
5. **Allowlist Validation:** Accept only explicitly permitted values.

### Validation vs Sanitization

- Validation checks whether input is acceptable.
- Sanitization or context-appropriate encoding transforms data to make it safe for a particular use.

### SQL Injection Example

Unsafe code:

```python
query = "SELECT * FROM users WHERE username = '" + username + "'"
```

Problem: User input is directly combined with SQL code.

Safer code:

```python
cursor.execute(
    "SELECT * FROM users WHERE username = ?",
    (username,)
)
```

Parameterized queries treat user input as data instead of executable SQL syntax.

## 3.2 Error Handling

Error handling means managing unexpected situations without exposing sensitive information or crashing insecurely.

Unsafe error:

```text
Password incorrect.
Database: production_users
SQL query: SELECT ...
```

Safer error:

```text
Invalid username or password.
```

### Secure Error Handling Practices

- Do not expose passwords.
- Do not expose database credentials.
- Do not display stack traces to public users.
- Log technical details securely.
- Return generic external error messages.
- Ensure failures do not grant unauthorized access.
- Monitor repeated failures.

## 3.3 Authentication Security

Authentication means verifying the identity of a user or system.

### Authentication Methods

| Method | Explanation |
|---|---|
| Password | Something the user knows |
| OTP | One-time password |
| MFA | Multiple authentication factors |
| Biometrics | Fingerprint or facial verification |
| Security Key | Hardware-backed authentication |
| Certificate | Digital identity verification |
| Passkey | Passwordless public-key authentication |

### What is MFA?

MFA requires two or more different authentication factors.

Three common factor categories:

1. Something you know: Password.
2. Something you have: Security key or authenticator device.
3. Something you are: Fingerprint or facial recognition.

Two passwords do not count as two different factors.

### Secure Password Storage

Passwords should never be stored in plain text.

Use dedicated password hashing algorithms:

- Argon2id
- bcrypt
- scrypt
- PBKDF2

Do not use plain SHA-256 as a password-storage replacement.

### Common Authentication Weaknesses

- Weak passwords
- Brute-force attacks
- Credential stuffing
- Password reset weaknesses
- Insecure session handling
- Missing MFA
- Authentication bypass

## 3.4 Authorization Security

Authorization determines what an authenticated user is allowed to access or perform.

### Authentication vs Authorization

| Authentication | Authorization |
|---|---|
| Verifies identity | Checks permissions |
| Who are you? | What can you do? |
| Login | Access control |
| Identity verification | Permission enforcement |

### Important Authorization Concepts

**RBAC:** Role-Based Access Control. Permissions are assigned to roles.

**ABAC:** Attribute-Based Access Control. Decisions use attributes such as department, location, resource and context.

**Least Privilege:** Give only necessary permissions.

**IDOR / BOLA:** A vulnerability where an application allows unauthorized access to another user's object or resource.

Example:

```text
/account/1001
/account/1002
```

If a user can access another person's account simply by changing the identifier, and the server does not check authorization, the application has a broken access-control vulnerability.

## 3.5 Secure Development Mindset

Developers should ask:

- Can an attacker misuse this feature?
- Can users access another user's information?
- Is the input trusted?
- Are secrets exposed?
- Are errors leaking information?
- Can functionality be abused?
- Is authorization checked on the server?

### Secure Coding Checklist

- Validate untrusted input.
- Use parameterized SQL queries.
- Encode output in the correct context.
- Use secure password hashing.
- Implement proper authentication.
- Enforce authorization on the server.
- Protect session cookies.
- Avoid hardcoded secrets.
- Handle errors securely.
- Keep dependencies updated.

### Interview Questions

1. What is secure coding?
2. What is input validation?
3. Difference between validation and sanitization?
4. What is SQL injection?
5. What are parameterized queries?
6. Why should passwords be hashed?
7. What is MFA?
8. What is authentication?
9. What is authorization?
10. Difference between authentication and authorization?
11. What is RBAC?
12. What is ABAC?
13. What is IDOR?
14. Why should error messages be generic?
15. What is secure session management?

### Scenario-Based Questions

**Scenario 1:** A user can access another user's profile by changing a URL identifier.

**Answer:** Broken access control, commonly called IDOR or BOLA depending on the application context.

**Scenario 2:** A developer stores passwords directly in a database.

**Answer:** Use dedicated password hashing such as Argon2id or bcrypt with unique salts and appropriate parameters.

**Scenario 3:** An application exposes database connection details when incorrect input is submitted.

**Answer:** This is improper error handling and information disclosure.

---

# 4. Application Security Testing

Application Security Testing (AST) is the process of identifying security weaknesses in software applications.

## 4.1 Security Reviews

A security review examines an application's design, code, configuration or security controls.

### Types of Security Reviews

1. **Architecture Security Review:** Examines application architecture and communication.
2. **Code Security Review:** Examines source code for security mistakes.
3. **Configuration Security Review:** Checks application and server settings.
4. **API Security Review:** Checks API authentication, authorization and data exposure.

### Manual vs Automated Reviews

| Manual Review | Automated Review |
|---|---|
| Human examines application | Tools analyze application |
| Can identify complex logic flaws | Quickly scans many patterns |
| Requires expertise | Requires correct configuration |
| Can understand business logic | May produce false positives |

Both methods are important.

## 4.2 Static Application Security Testing (SAST)

SAST analyzes application source code or supported code representations without executing the application.

### SAST Workflow

1. Developer writes application code.
2. SAST tool scans the code.
3. Suspicious patterns are identified.
4. Security findings are generated.
5. Developers review findings.
6. Vulnerabilities are fixed.
7. Code is scanned again.

### Popular SAST Tools

| Tool | Main Purpose |
|---|---|
| Semgrep | Static code analysis |
| SonarQube | Code quality and security analysis |
| Checkmarx | Application security testing |
| CodeQL | Semantic code analysis |

### Advantages

- Finds weaknesses early.
- Does not require a running application.
- Can integrate into development workflows.
- Helps identify insecure coding patterns.

### Limitations

- May produce false positives.
- May miss runtime vulnerabilities.
- May not identify complex business logic problems.
- Requires manual review.

## 4.3 Dynamic Application Security Testing (DAST)

DAST tests a running application from the outside without requiring source code.

### DAST Workflow

1. Start the application.
2. Configure the scanner.
3. Identify pages and endpoints.
4. Test application responses.
5. Identify possible vulnerabilities.
6. Validate findings.
7. Fix vulnerabilities.

### Popular DAST Tools

| Tool | Main Purpose |
|---|---|
| OWASP ZAP | Web application security testing |
| Burp Suite | HTTP traffic inspection and penetration testing |
| Invicti | Automated web vulnerability scanning |

### Advantages

- Tests actual running applications.
- Does not require source code.
- Can discover runtime issues.
- Tests externally observable behavior.

### Limitations

- Cannot see all internal code paths.
- May miss complex business logic vulnerabilities.
- Some findings require manual verification.

## 4.4 Vulnerability Discovery Concepts

### Common Web Application Vulnerabilities

| Vulnerability | Simple Explanation |
|---|---|
| SQL Injection | Unsafe input manipulates database queries |
| XSS | Untrusted content executes as script in a browser |
| CSRF | Tricks a logged-in browser into performing an unwanted action |
| IDOR | Allows access to another user's resource |
| SSRF | Server makes attacker-influenced requests |
| Path Traversal | Accesses files outside the intended directory |
| Security Misconfiguration | Insecure application or server settings |
| Broken Authentication | Weaknesses in identity verification |
| Broken Access Control | Unauthorized actions or resource access |
| Sensitive Data Exposure | Confidential information becomes accessible |

### OWASP Top 10 (2025)

OWASP is a community-driven organization that publishes application security resources.

The 2025 OWASP Top 10 categories are:

1. Broken Access Control.
2. Security Misconfiguration.
3. Software Supply Chain Failures.
4. Cryptographic Failures.
5. Injection.
6. Insecure Design.
7. Authentication Failures.
8. Software or Data Integrity Failures.
9. Security Logging and Alerting Failures.
10. Mishandling of Exceptional Conditions.

## 4.5 Security Validation

Security validation verifies that security controls work as expected.

### Validation Process

1. Identify the security issue.
2. Understand the root cause.
3. Develop a test case.
4. Test the original vulnerability.
5. Apply the security fix.
6. Repeat the test.
7. Perform regression testing.
8. Document results.

### SAST vs DAST

| SAST | DAST |
|---|---|
| Static testing | Dynamic testing |
| Examines source code | Examines running application |
| Does not require execution | Requires running application |
| Finds insecure code patterns | Finds runtime weaknesses |

### What is IAST?

Interactive Application Security Testing uses instrumentation or agents inside a running application to analyze execution and data flows during testing.

### What is SCA?

Software Composition Analysis examines third-party and open-source dependencies for known vulnerabilities, licensing issues and supply-chain risks.

### Interview Questions

1. What is application security testing?
2. What is a security review?
3. What is SAST?
4. What is DAST?
5. Difference between SAST and DAST?
6. What is IAST?
7. What is SCA?
8. What is a false positive?
9. What is a false negative?
10. What is vulnerability validation?
11. What is regression testing?
12. What is OWASP Top 10?
13. What is the purpose of Burp Suite?
14. What is OWASP ZAP?
15. Can automated scanners identify all vulnerabilities?

**Important Answer:** No. Automated tools identify many known patterns and technical weaknesses, but they may miss complex business-logic vulnerabilities and context-specific security problems. Manual testing is also necessary.

---

# 5. DevSecOps Fundamentals

## 5.1 What is DevSecOps?

DevSecOps stands for:

- Dev: Development
- Sec: Security
- Ops: Operations

DevSecOps integrates security into software development and operations.

### Example

A developer uploads code to GitHub.

The DevSecOps pipeline automatically:

1. Scans the code.
2. Checks dependencies.
3. Detects exposed secrets.
4. Runs security tests.
5. Builds the application.
6. Deploys it if required checks pass.

### DevOps vs DevSecOps

| DevOps | DevSecOps |
|---|---|
| Development + Operations | Development + Security + Operations |
| Focuses on collaboration and delivery | Adds integrated security |
| Automates building and deployment | Automates building, deployment and security checks |
| Security may be separate | Security is shared and continuous |

## 5.2 Shift-Left Security

Shift-left security means performing security activities earlier in the development lifecycle.

### Shift-Left Activities

- Security requirement analysis.
- Threat modelling.
- Secure code review.
- SAST.
- Dependency scanning.
- Secret detection.
- Security-focused developer training.

### Shift-Left vs Continuous Security

- Shift-left means moving security earlier.
- Continuous security means maintaining security throughout the lifecycle.

Both work together.

## 5.3 Automation in Security

Security automation uses software tools and workflows to perform security activities automatically.

Examples:

- Source code scanning.
- Dependency scanning.
- Secret detection.
- Container scanning.
- Cloud configuration scanning.
- Security alert generation.
- Automated ticket creation.
- Blocking unsafe builds.

### Popular DevSecOps Tools

| Tool | Main Use |
|---|---|
| Git | Version control |
| GitHub Actions | Workflow automation |
| Jenkins | CI/CD automation |
| Semgrep | Static code analysis |
| SonarQube | Code quality and security analysis |
| Trivy | Vulnerability and configuration scanning |
| Gitleaks | Secret detection |
| OWASP ZAP | Dynamic web security testing |
| Dependency-Check | Dependency vulnerability analysis |
| Checkov | Infrastructure-as-code security scanning |

## 5.4 Security Integration

Security integration means adding security tools and checks to development workflows.

Example:

A developer commits code to GitHub.

The workflow automatically performs:

- Code scanning.
- Secret scanning.
- Dependency scanning.
- Unit testing.
- Build validation.

Serious security findings can prevent deployment according to organizational policy.

## 5.5 Continuous Security

Continuous security means continuously checking and improving application security.

### Continuous Security Activities

1. Continuous vulnerability scanning.
2. Security log monitoring.
3. Dependency monitoring.
4. Configuration monitoring.
5. Patch management.
6. Incident detection.
7. Access reviews.
8. Periodic penetration testing.
9. Security regression testing.

### Interview Questions

1. What is DevSecOps?
2. What does DevSecOps stand for?
3. Difference between DevOps and DevSecOps?
4. What is shift-left security?
5. What is security automation?
6. What is a security pipeline?
7. Why is continuous security important?
8. What is a CI/CD workflow?
9. What is the developer's role in DevSecOps?
10. What happens if a security scan fails?

---

# 6. CI/CD Security

## 6.1 What is CI/CD?

CI/CD is an important part of modern software development.

**CI = Continuous Integration**

Developers regularly combine code changes into a shared repository. Automated tests and checks run to identify problems.

**CD = Continuous Delivery or Continuous Deployment**

- Continuous Delivery keeps software ready for release, usually with approval before production deployment.
- Continuous Deployment automatically releases qualifying changes after required checks pass.

### Basic CI/CD Pipeline

1. Source Code
2. Build
3. Security Scanning
4. Testing
5. Release
6. Deployment
7. Monitoring

## 6.2 Secure Pipelines

A secure pipeline is a CI/CD workflow protected against unauthorized changes, credential exposure and malicious modifications.

### Common CI/CD Security Risks

- Unauthorized pipeline modification.
- Exposed credentials.
- Malicious dependencies.
- Compromised build agents.
- Untrusted build artifacts.
- Insecure deployment configurations.
- Excessive permissions.

### How to Secure a Pipeline

1. Protect important branches.
2. Require code reviews.
3. Restrict workflow permissions.
4. Use trusted dependencies.
5. Scan code automatically.
6. Protect build environments.
7. Verify build artifacts.
8. Require approvals for sensitive deployments.
9. Monitor pipeline activity.
10. Secure deployment credentials.

### What is a Build Agent?

A build agent is a machine or execution environment that performs pipeline tasks such as compiling code, running tests and building application packages.

## 6.3 Secrets Management

A secret is sensitive information used to access a system or service.

Examples:

- API keys.
- Database passwords.
- Cloud credentials.
- SSH private keys.
- Access tokens.
- Signing keys.

### Problem with Hardcoded Secrets

Unsafe example:

```python
API_KEY = "my-secret-api-key"
```

If this code is uploaded to a public GitHub repository, attackers may obtain the key.

### Secure Alternatives

- Environment variables.
- GitHub Actions Secrets.
- AWS Secrets Manager.
- Azure Key Vault.
- HashiCorp Vault.
- Google Cloud Secret Manager.

### Secrets Management Best Practices

1. Never commit secrets to Git.
2. Restrict secret access.
3. Rotate credentials regularly.
4. Avoid printing secrets in logs.
5. Use short-lived credentials where possible.
6. Revoke exposed credentials immediately.
7. Monitor secret usage.

**Important:** Deleting a leaked key from the latest Git commit is not enough. The key must be considered compromised, revoked or rotated, and its exposure investigated.

## 6.4 Dependency Security

A dependency is an external software package or library that an application uses.

Python example:

```python
import requests
import flask
import pandas
```

### Dependency Risks

- Known vulnerabilities.
- Outdated packages.
- Malicious packages.
- Compromised maintainers.
- Risky transitive dependencies.

### What is a Transitive Dependency?

A transitive dependency is a package required by another package.

Example:

Your application installs Package A.

Package A requires Package B.

Your application now indirectly depends on Package B.

### Dependency Security Tools

- OWASP Dependency-Check.
- Dependabot.
- Snyk.
- Trivy.
- npm audit.
- pip-audit.

Python audit command:

```bash
pip-audit
```

## 6.5 Build Security

Build security protects the process that transforms source code into a deployable software artifact.

Examples of artifacts:

- Executable files.
- Container images.
- Application packages.
- Deployment bundles.

### Common Build Security Risks

- Malicious build scripts.
- Compromised dependencies.
- Unauthorized build modifications.
- Exposed credentials.
- Untrusted build environments.
- Modified artifacts.

### Security Measures

- Use trusted build environments.
- Restrict build permissions.
- Scan dependencies.
- Verify artifact integrity.
- Secure build logs.
- Protect signing keys.
- Generate provenance information.

### What is Software Provenance?

Software provenance provides information about where software came from and how it was built.

## 6.6 Deployment Security

Deployment security ensures that software is released into a secure environment.

### Common Deployment Weaknesses

- Default passwords.
- Debug mode enabled.
- Unnecessary open ports.
- Public databases.
- Overprivileged service accounts.
- Missing HTTPS.
- Insecure cloud permissions.

### Secure Deployment Checklist

- Use HTTPS.
- Disable production debug mode.
- Apply least privilege.
- Restrict network access.
- Secure database connections.
- Protect configuration files.
- Apply security patches.
- Enable security logging.
- Use approved deployment artifacts.

### Interview Questions

1. What is CI/CD?
2. What is Continuous Integration?
3. What is Continuous Delivery?
4. What is Continuous Deployment?
5. What is a CI/CD pipeline?
6. What is a build agent?
7. What is a build artifact?
8. What is secrets management?
9. Why are hardcoded credentials dangerous?
10. What is a dependency?
11. What is a transitive dependency?
12. What is software provenance?
13. What is artifact integrity?
14. How do you secure a deployment?
15. What is GitHub Actions?

---

# 7. Software Supply Chain Security

## 7.1 Third-Party Software Risks

Third-party software means software developed or maintained by another organization or individual and used by your application.

Examples:

- Python packages.
- JavaScript libraries.
- Java frameworks.
- Database drivers.
- Cloud SDKs.
- Open-source tools.
- External APIs.

### Common Risks

1. **Known Vulnerabilities:** A package contains a publicly documented weakness.
2. **Malicious Packages:** A package is designed to steal credentials or execute malicious code.
3. **Abandoned Packages:** The maintainer stops updating the software.
4. **Compromised Maintainers:** An attacker gains control of a maintainer's account.
5. **Dependency Confusion:** Package resolution causes an unintended package to be downloaded.
6. **Typosquatting:** A malicious package has a name similar to a legitimate package.
7. **License Risks:** Dependencies have licensing conditions that conflict with organizational requirements.

## 7.2 Dependency Management

Dependency management means controlling external libraries and packages used by an application.

### Dependency Management Activities

- Installing dependencies.
- Tracking versions.
- Updating packages.
- Removing unused packages.
- Identifying vulnerabilities.
- Reviewing package sources.
- Managing licenses.

### Package Managers

| Ecosystem | Package Manager |
|---|---|
| Python | pip |
| JavaScript | npm |
| Java | Maven |
| PHP | Composer |
| Ruby | Bundler |
| .NET | NuGet |

### Important Dependency Files

| File | Purpose |
|---|---|
| requirements.txt | Python dependency list |
| package.json | JavaScript project metadata and dependencies |
| package-lock.json | Locks resolved npm dependency versions |
| pom.xml | Maven project configuration |
| Gemfile | Ruby dependency declaration |
| Cargo.toml | Rust project dependencies |

### Python Dependency Management Lab

Create a project:

```bash
mkdir secure-app
cd secure-app
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

Install a package:

```bash
pip install flask
```

Save dependencies:

```bash
pip freeze > requirements.txt
```

Audit dependencies:

```bash
pip install pip-audit
pip-audit
```

### What is Dependency Pinning?

Dependency pinning means specifying a particular package version.

Example:

```text
flask==3.1.2
```

Pinning improves reproducibility, but pinned versions must still be monitored and updated.

## 7.3 Software Integrity

Software integrity means ensuring that software and its components have not been unexpectedly modified or corrupted.

### What is a Hash?

A hash is a fixed-length output produced from input data using a hash function.

Linux:

```bash
sha256sum application.zip
```

Windows PowerShell:

```powershell
Get-FileHash application.zip -Algorithm SHA256
```

The result can be compared against a digest obtained through a trusted channel.

A hash alone does not prove who created a file.

### What is a Digital Signature?

A digital signature uses asymmetric cryptography to help verify:

- Who signed the software.
- Whether signed content has been modified.

### Hash vs Digital Signature

| Hash | Digital Signature |
|---|---|
| Produces a digest | Creates a cryptographic signature |
| Helps detect changes when compared with a trusted digest | Helps verify authenticity and integrity |
| Does not establish signer identity | Can establish signer identity through trusted public-key verification |
| Does not require a private signing key | Requires the signer's private key |

### What is an SBOM?

SBOM stands for Software Bill of Materials.

It is a structured inventory of software components and dependencies included in a software product.

Think of it as an ingredient list for software.

An SBOM helps organizations identify which applications use a vulnerable library.

### What is SLSA?

SLSA stands for Supply-chain Levels for Software Artifacts.

It is a security framework that provides guidance for improving software build and distribution integrity.

## 7.4 Security Monitoring

Security monitoring means continuously observing systems and software for suspicious activities or security weaknesses.

### What Should Organizations Monitor?

- New dependency vulnerabilities.
- Package changes.
- Unauthorized repository modifications.
- Build failures.
- Unexpected deployment activities.
- Exposed credentials.
- Suspicious API requests.
- Unauthorized access.
- Security alerts.

### Important Logs

| Log Type | Purpose |
|---|---|
| Application Logs | Record application activity and errors |
| System Logs | Record operating system events |
| Authentication Logs | Record login and authentication activity |
| CI/CD Logs | Record pipeline and deployment events |
| Cloud Audit Logs | Record cloud account and resource activity |

## 7.5 Risk Mitigation

Risk mitigation means applying security measures to reduce software supply chain risks.

| Risk | Mitigation |
|---|---|
| Vulnerable packages | Dependency scanning and patching |
| Malicious packages | Verify package sources and publishers |
| Abandoned packages | Replace unsupported dependencies |
| Exposed API keys | Secret management and rotation |
| Package tampering | Verify signatures and hashes |
| Unknown dependencies | Maintain an SBOM |
| Compromised build system | Secure and isolate build environments |
| Unauthorized code changes | Branch protection and code reviews |
| Outdated software | Continuous monitoring |

### Supply Chain Security Workflow

1. Identify software components.
2. Scan dependencies.
3. Verify package integrity.
4. Fix security issues.
5. Monitor continuously.

### Interview Questions

1. What is software supply chain security?
2. What is third-party software?
3. What is a dependency?
4. What is a transitive dependency?
5. What is dependency confusion?
6. What is typosquatting?
7. What is a malicious package?
8. What is dependency pinning?
9. What is software integrity?
10. What is a cryptographic hash?
11. What is a digital signature?
12. What is an SBOM?
13. What is SLSA?
14. Why is dependency scanning important?
15. How do you manage vulnerable third-party libraries?

---

# 8. Advanced Security Concepts

## 8.1 Security Gates

A security gate is a rule that determines whether a development pipeline can proceed.

Example organizational policy:

- Critical vulnerabilities: Build must fail.
- High vulnerabilities: Approval required.
- Medium vulnerabilities: Remediation ticket.
- Low vulnerabilities: Track and review.

Security gates prevent unacceptable known risks from silently reaching production.

## 8.2 Vulnerability Severity

CVSS stands for Common Vulnerability Scoring System.

CVSS v4.0 qualitative severity levels:

| Score | Severity |
|---|---|
| 0.0 | None |
| 0.1–3.9 | Low |
| 4.0–6.9 | Medium |
| 7.0–8.9 | High |
| 9.0–10.0 | Critical |

CVSS is a technical severity measure. Remediation priority should also consider business impact, exploitability and exposure.

## 8.3 Vulnerability Lifecycle

1. Discovery.
2. Initial validation.
3. Risk assessment.
4. Assignment.
5. Remediation.
6. Retesting.
7. Closure.
8. Monitoring.

## 8.4 Security Documentation

Important documents:

- Security requirements document.
- Threat model.
- Architecture security review.
- Vulnerability assessment report.
- Penetration testing report.
- Dependency inventory.
- SBOM.
- Risk register.
- Remediation report.
- Security testing evidence.

## 8.5 Important Frameworks

| Framework / Resource | Purpose |
|---|---|
| OWASP Top 10 | Common application security risks |
| OWASP ASVS | Application security verification requirements |
| OWASP SAMM | Software assurance maturity model |
| NIST SSDF | Secure software development practices |
| NIST CSF | Cybersecurity risk management |
| MITRE ATT&CK | Adversary tactics and techniques |
| SLSA | Software supply chain security |
| CWE | Common Weakness Enumeration |
| CVE | Common Vulnerabilities and Exposures |
| CVSS | Vulnerability severity scoring |

### CWE vs CVE vs CVSS

- **CWE:** Describes a type of software weakness.
- **CVE:** Identifies a publicly disclosed vulnerability.
- **CVSS:** Measures vulnerability severity.

Example:

A program contains an SQL injection weakness.

- CWE describes the weakness category.
- CVE identifies a particular publicly documented vulnerable product or component, when one exists.
- CVSS provides a severity score for a specific vulnerability.

---

# 9. Hands-on Practical Tasks

**Objective:** Convert theoretical knowledge into practical application security skills.

Perform all testing only on your own applications, local labs or explicitly authorized environments.

## Practical Task 1: Review Application Architecture

### Objective

Understand how a web application is structured and identify security risks.

Example e-commerce architecture:

1. Frontend: Website users interact with.
2. Backend: Processes user requests.
3. API: Allows frontend and backend communication.
4. Database: Stores customer and order information.
5. Authentication Service: Verifies user identity.

### Architecture Review Checklist

| Question | What to Examine |
|---|---|
| Where is authentication performed? | Login mechanism |
| Where is authorization checked? | Backend/API |
| Where is sensitive data stored? | Database |
| Is communication encrypted? | HTTPS/TLS |
| Are API endpoints protected? | Authentication and authorization |
| Are secrets exposed? | Application configuration |
| Is database access restricted? | Network and identity controls |

### Expected Findings

- Publicly accessible database.
- Missing authorization.
- Insecure communication.
- Hardcoded API credentials.
- Excessive permissions.
- Unprotected administrative endpoints.

**Deliverable:** Architecture Security Review Report.

## Practical Task 2: Analyze Security Weaknesses

### Recommended Practice Target

**OWASP Juice Shop**

Official project:

https://owasp.org/www-project-juice-shop/

OWASP Juice Shop is a deliberately vulnerable web application designed for security training.

Use a local instance or explicitly authorized training environment.

### Tools

- Kali Linux.
- Burp Suite Community Edition.
- OWASP ZAP.
- Browser Developer Tools.
- Nmap for authorized network discovery.

### Testing Process

1. Understand the application.
2. Identify pages, functionality and APIs.
3. Study HTTP requests and responses.
4. Inspect requests using Burp Suite.
5. Identify possible security weaknesses.
6. Validate findings.
7. Recommend remediation.

### Important HTTP Concepts

- GET
- POST
- PUT
- PATCH
- DELETE
- HTTP Status Codes
- Headers
- Cookies
- Request Body
- Response Body

### Security Testing Checklist

- [ ] Authentication weaknesses
- [ ] Broken access control
- [ ] IDOR / BOLA
- [ ] SQL injection indicators
- [ ] Cross-site scripting indicators
- [ ] CSRF protections
- [ ] Security misconfiguration
- [ ] Sensitive information exposure
- [ ] Insecure session management
- [ ] API security weaknesses

**Deliverable:** Application Vulnerability Assessment Report.

## Practical Task 3: Assess Software Supply Chain Risks

### Objective

Examine application dependencies and identify potential risks.

Create a Python project:

```bash
mkdir supply-chain-lab
cd supply-chain-lab
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

Install a dependency:

```bash
pip install requests
```

Check installed packages:

```bash
pip list
```

Generate dependency information:

```bash
pip freeze > requirements.txt
```

Install the auditing tool:

```bash
pip install pip-audit
```

Scan dependencies:

```bash
pip-audit
```

### Understand the Results

The tool may report:

- Package name.
- Installed version.
- Vulnerability identifier.
- Affected version range.
- Fixed version, if available.

### Assessment Questions

1. Is the dependency maintained?
2. Is its version outdated?
3. Are known vulnerabilities present?
4. Does it have unnecessary permissions?
5. Is the package from a trusted source?
6. Is there a safer replacement?

**Deliverable:** Software Supply Chain Risk Assessment.

## Practical Task 4: Design a Secure Development Workflow

### Objective

Design a CI/CD pipeline with security integrated into important stages.

### Tools

- GitHub.
- GitHub Actions.
- Semgrep.
- Gitleaks.
- Trivy.
- OWASP ZAP.

### Suggested Workflow

```text
Developer Commits Code
        |
        v
GitHub Repository
        |
        v
Semgrep - SAST
        |
        v
Gitleaks - Secret Detection
        |
        v
Trivy - Dependency Scanning
        |
        v
Automated Testing
        |
        v
Build Application
        |
        v
OWASP ZAP - DAST
        |
        v
Security Approval
        |
        v
Approved Deployment
        |
        v
Security Monitoring
```

### Security Conditions

- Critical issues should block release according to policy.
- Exposed secrets must be investigated and revoked.
- Vulnerable dependencies must be reviewed.
- Failed tests should be investigated.
- Deployment permissions must be restricted.
- Findings should be documented.

**Deliverable:** Secure CI/CD Workflow Design.

## Practical Task 5: Create a DevSecOps Assessment Report

### Objective

Document the security assessment professionally.

### Report Structure

1. Project Information.
2. Assessment Objective.
3. Application Architecture.
4. Testing Methodology.
5. Tools Used.
6. Security Findings.
7. Risk Severity.
8. Evidence.
9. Recommendations.
10. Final Conclusion.

### Example Finding

**Finding 01: Hardcoded API Key**

**Severity:** High (illustrative; confirm actual impact).

**Description:** A sensitive API key was discovered in application source code.

**Affected Component:** Configuration file.

**Risk:** Unauthorized access to the associated service if the key is valid and exposed.

**Evidence:** Source-code review identified a credential-like value.

**Impact:** Possible unauthorized service access, data exposure or financial impact depending on key permissions.

**Recommendations:**

- Revoke and rotate the exposed key.
- Remove secrets from source code.
- Use a secrets manager.
- Introduce automated secret scanning.
- Investigate possible misuse.

---

# 10. Fundamental Interview Questions

| No. | Question | Simple Answer |
|---:|---|---|
| 1 | What is SDLC? | Software Development Life Cycle. |
| 2 | What is Secure SDLC? | Integrating security throughout software development. |
| 3 | What is DevSecOps? | Integrating security into DevOps. |
| 4 | What is application security? | Protecting applications against security weaknesses. |
| 5 | What is a vulnerability? | A weakness that can be exploited. |
| 6 | What is a threat? | A potential danger to a system. |
| 7 | What is an exploit? | A method of taking advantage of a vulnerability. |
| 8 | What is risk? | Potential loss or damage from a threat exploiting a weakness. |
| 9 | What is threat modelling? | Identifying potential threats before development. |
| 10 | What is STRIDE? | A threat modelling methodology. |
| 11 | What is least privilege? | Giving only necessary permissions. |
| 12 | What is defense in depth? | Using multiple security layers. |
| 13 | What is secure coding? | Writing code that prevents security weaknesses. |
| 14 | What is input validation? | Checking user input before processing. |
| 15 | What is authentication? | Verifying identity. |
| 16 | What is authorization? | Checking permissions. |
| 17 | What is MFA? | Multi-Factor Authentication. |
| 18 | What is SAST? | Static Application Security Testing. |
| 19 | What is DAST? | Dynamic Application Security Testing. |
| 20 | What is SCA? | Software Composition Analysis. |

---

# 11. Scenario-Based Interview Questions

## Scenario 1: Vulnerable Login Application

A developer creates a login system. The application stores passwords in plain text.

**Questions:**

1. What is the security weakness?
2. What could an attacker do?
3. How would you fix it?

**Answer:**

- Weakness: Insecure password storage.
- Risk: Attackers can read passwords if the database is exposed.
- Fix: Use a dedicated password hashing algorithm such as Argon2id or bcrypt, with unique salts and appropriate parameters.

## Scenario 2: Exposed Database

A company accidentally exposes its database to the public internet.

**Recommended Actions:**

- Restrict database network access.
- Review firewall and security group rules.
- Enforce authentication.
- Apply least privilege.
- Encrypt sensitive data.
- Review database access logs.
- Investigate possible unauthorized access.

## Scenario 3: Vulnerable Open-Source Library

A company discovers a critical vulnerability in a library used by its application.

**Recommended Actions:**

1. Identify affected applications.
2. Determine affected versions.
3. Assess exposure and impact.
4. Find a fixed version or safe alternative.
5. Upgrade the dependency.
6. Perform security and regression tests.
7. Document remediation.

## Scenario 4: Unauthorized Administrator Access

A normal user can access the administrator dashboard.

**Answer:** This is likely broken access control. The backend must enforce authorization on every protected operation.

## Scenario 5: CI/CD Secret Leakage

A GitHub repository contains a cloud access key.

**Recommended Actions:**

1. Revoke or deactivate the exposed credential.
2. Create replacement credentials if needed.
3. Investigate whether the key was used.
4. Review cloud audit logs.
5. Remove the secret from repository history where appropriate.
6. Add secret scanning.
7. Use secure secrets management.

## Scenario 6: Security Testing After Deployment

An organization performs security testing only after releasing software.

**Answer:** Introduce Secure SDLC and shift-left practices. Add threat modelling, secure code review, SAST, dependency scanning and pre-release security validation.

## Scenario 7: SAST Reports Hundreds of Vulnerabilities

**Recommended Actions:**

1. Group findings by type.
2. Validate possible false positives.
3. Prioritize based on severity and context.
4. Identify root causes.
5. Fix high-risk weaknesses.
6. Re-run scans.
7. Track remaining issues.

## Scenario 8: Malicious Package Discovered

**Recommended Actions:**

1. Stop using the package.
2. Identify affected applications and environments.
3. Isolate compromised systems if necessary.
4. Investigate possible execution and credential exposure.
5. Remove or replace the package.
6. Rotate affected secrets.
7. Verify software integrity.
8. Document the incident.

## Scenario 9: Deployment Bypass

A developer bypasses security approval and deploys an untested application.

**Answer:** Implement protected deployment environments, least-privilege access, mandatory approvals, pipeline enforcement and audit logging.

## Scenario 10: New Vulnerability Discovered in Production

**Recommended Actions:**

1. Understand the vulnerability.
2. Identify affected systems.
3. Assess exposure and business impact.
4. Apply temporary mitigation if needed.
5. Develop and deploy a fix.
6. Retest.
7. Monitor for exploitation.
8. Document the incident and lessons learned.

---

# 12. DevSecOps Tools

Learn these tools in a logical order.

## Stage 1: Application Fundamentals

| Tool | Purpose |
|---|---|
| Git | Version control |
| GitHub | Code hosting and collaboration |

## Stage 2: Application Security Testing

| Tool | Purpose |
|---|---|
| Burp Suite | HTTP interception and web penetration testing |
| OWASP ZAP | Automated and manual web security testing |

## Stage 3: Code Security

| Tool | Purpose |
|---|---|
| Semgrep | SAST and secure coding checks |
| SonarQube | Code quality and security analysis |
| CodeQL | Semantic code analysis |

## Stage 4: Supply Chain Security

| Tool | Purpose |
|---|---|
| Trivy | Dependency, container and configuration scanning |
| Gitleaks | Secret detection |
| pip-audit | Python dependency auditing |
| Dependabot | Dependency update management |

## Stage 5: DevSecOps Automation

| Tool | Purpose |
|---|---|
| Jenkins | CI/CD pipeline automation |
| GitHub Actions | Development and security workflow automation |
| Checkov | Infrastructure-as-code security scanning |

---

# 13. Technical Vocabulary

| Word | Simple Meaning |
|---|---|
| Application | Software designed for users |
| Repository | Storage location for source code |
| Source Code | Human-readable program instructions |
| Framework | Structure used to develop software |
| Library | Reusable code |
| API | Interface for communication between software |
| Endpoint | Specific API or service access point |
| Payload | Data sent in a request |
| Request | Message sent to a server |
| Response | Message returned by a server |
| Token | Data representing authorization or identity |
| Session | Information maintaining a user's interaction |
| Patch | Software update fixing an issue |
| Build | Process of creating software artifacts |
| Pipeline | Automated sequence of development activities |
| Artifact | Produced software package |
| Container | Isolated environment for running applications |
| Image | Template used to create a container |
| Sandbox | Isolated testing environment |
| Misconfiguration | Incorrect or insecure settings |
| Remediation | Correcting a security problem |
| Mitigation | Reducing risk or impact |
| Regression | Previously working behavior breaks after a change |
| Provenance | Record of where software came from and how it was produced |
| Attestation | Verifiable statement about a process or artifact |

---

# 14. Final Examination Practice

Test your understanding of the complete syllabus.

## Multiple-Choice Questions

**1. What does Secure SDLC integrate into software development?**

- A. Only functionality
- B. Security throughout the lifecycle
- C. Only deployment
- D. Only maintenance

**Answer:** B

**2. Which methodology is used for threat modelling?**

- A. STRIDE
- B. HTTP
- C. DNS
- D. SMTP

**Answer:** A

**3. Which testing method examines source code without running the application?**

- A. DAST
- B. SAST
- C. Penetration Testing
- D. Network Monitoring

**Answer:** B

**4. Which testing method examines a running application?**

- A. SAST
- B. SCA
- C. DAST
- D. Code Formatting

**Answer:** C

**5. What is authentication?**

- A. Checking permissions
- B. Verifying identity
- C. Encrypting files
- D. Building software

**Answer:** B

**6. What does shift-left security mean?**

- A. Testing only after release
- B. Moving security earlier in development
- C. Removing security tests
- D. Disabling automation

**Answer:** B

**7. What does SBOM stand for?**

- A. Software Build Operating Method
- B. Software Bill of Materials
- C. Secure Backup of Modules
- D. Software Browser Object Model

**Answer:** B

**8. Which tool detects exposed secrets in Git repositories?**

- A. Gitleaks
- B. Nmap
- C. Wireshark
- D. Ping

**Answer:** A

**9. What is the best immediate response to an exposed valid API key?**

- A. Ignore it
- B. Only delete the source file
- C. Revoke or rotate it and investigate
- D. Rename the variable

**Answer:** C

**10. What does authorization check?**

- A. Who a user is
- B. What a user can access
- C. Which programming language is used
- D. Which server is running

**Answer:** B

---

# 15. 21-Day Study Roadmap

| Days | Study Topic | Practical Activity |
|---|---|---|
| 1–2 | SDLC and Secure SDLC | Draw SDLC lifecycle |
| 3–4 | Security Requirements | Threat modelling using STRIDE |
| 5–7 | Secure Coding | Review Python login code |
| 8–10 | Application Security Testing | Burp Suite and OWASP ZAP |
| 11–12 | SAST and DAST | Scan a practice application |
| 13–14 | DevSecOps | Understand GitHub Actions |
| 15–16 | CI/CD Security | Design a secure pipeline |
| 17–18 | Supply Chain Security | Run dependency scanning |
| 19 | Software Integrity | Hash verification and SBOM |
| 20 | Security Assessment | Perform an authorized assessment |
| 21 | Final Report | Prepare professional documentation |

---

# 16. Final Portfolio Project

## Secure Application Development Assessment

**Project Category:** Application Security and DevSecOps

**Objective:** Demonstrate practical understanding of Secure SDLC, application security testing, CI/CD security and software supply chain risk management.

### Project Components

| Component | What It Demonstrates |
|---|---|
| Application Architecture | Understanding application components |
| Threat Modelling | STRIDE and risk identification |
| Secure Coding Review | Identifying insecure code |
| SAST Assessment | Static code analysis |
| DAST Assessment | Dynamic security testing |
| Dependency Assessment | Third-party vulnerability discovery |
| Secrets Management | Credential protection |
| CI/CD Workflow | Security automation |
| Vulnerability Report | Findings and remediation |
| Final Assessment | Security recommendations |

### Suggested GitHub Folder Structure

```text
Secure-SDLC-DevSecOps/
│
├── README.md
│
├── 01-SDLC-Fundamentals/
│   └── SDLC-Notes.md
│
├── 02-Security-Requirements/
│   ├── Security-Requirements.md
│   └── Threat-Model.md
│
├── 03-Secure-Coding/
│   └── Code-Review.md
│
├── 04-Application-Security/
│   ├── SAST-Results.md
│   └── DAST-Results.md
│
├── 05-DevSecOps/
│   └── Security-Workflow.md
│
├── 06-CICD-Security/
│   └── Pipeline-Assessment.md
│
├── 07-Supply-Chain/
│   ├── Dependency-Report.md
│   └── SBOM.md
│
├── 08-Assessment-Report/
│   ├── Findings.md
│   └── Recommendations.md
│
└── screenshots/
```

---

# 17. Official Learning Resources

## OWASP

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/)
- [OWASP SAMM](https://owasp.org/www-project-samm/)

## NIST

- [NIST Secure Software Development Framework](https://csrc.nist.gov/pubs/sp/800/218/final)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

## GitHub

- [GitHub Code Security](https://docs.github.com/en/code-security)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

## Software Supply Chain

- [SLSA Framework](https://slsa.dev/)
- [CISA SBOM Resources](https://www.cisa.gov/sbom)

## Practical Application Security

- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)

---

# Final Knowledge Checklist

Before completing this syllabus, make sure you can explain:

- [ ] Every SDLC stage.
- [ ] Why security must be integrated throughout SDLC.
- [ ] Assets, threats, vulnerabilities and risks.
- [ ] STRIDE threat modelling.
- [ ] Least privilege and defense in depth.
- [ ] Common secure coding mistakes.
- [ ] Authentication and authorization.
- [ ] SAST, DAST, IAST and SCA.
- [ ] OWASP Top 10.
- [ ] DevSecOps and shift-left security.
- [ ] Secure CI/CD pipeline design.
- [ ] Secrets management.
- [ ] Third-party dependency risks.
- [ ] SBOM, hashes and digital signatures.
- [ ] Authorized application security assessment.
- [ ] Professional security assessment reporting.

---

## Conclusion

Secure SDLC and DevSecOps help organizations develop software that is functional, reliable and secure.

The most important areas to understand are:

1. Secure coding.
2. Application vulnerability discovery.
3. Security testing.
4. CI/CD pipeline security.
5. Software supply chain security.
6. Vulnerability assessment and remediation.

**Learning Approach:** Understand the concept → Study the security risk → Learn the tools → Practise in an authorized lab → Document findings → Explain the result in an interview.

**Learning Status:** Theory and practical preparation in progress.
