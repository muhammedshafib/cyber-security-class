# Module 5: Understand DevSecOps Fundamentals

This module explains how security is integrated into the software development and deployment process.

For your cybersecurity learning path, DevSecOps is important because modern security professionals do not just find vulnerabilities after an application is developed. They help identify and prevent security problems throughout development, testing, and deployment.

[DevSecOps Roadmap 2026 | by Dashrath Purohit | Feb, 2026 | Medium](https://images.openai.com/static-rsc-4/9BldtY2Go1LlspHfxfn8px9jVAr9YdsQ2XjOlt31R86AqkyozFkPNIlKlzLBAeAg8srCSurvFlnHEQ31Vx5ErOFGj1MHQBgdda-iLW_iSDOrlyH5Ifos1enywWWhM_ywb3tT39iGMTehyqHx-gg02VnIbtFO077yf7r3hEBBhLM?purpose=inline)

[medium.com](https://medium.com/%40dashpurohit6/devsecops-roadmap-2026-08784c4b89ba?utm_source=chatgpt.com)

## 1. What is DevSecOps?

### 1.1 Definition

DevSecOps = Development + Security + Operations

DevSecOps is a software development approach that integrates security into every stage of the software development lifecycle.

Traditionally:

- Developers build the application.
- Security teams test it later.
- Operations teams deploy and maintain it.

The problem is that security issues may be discovered very late.

DevSecOps solves this by making security everyone's responsibility and integrating security checks throughout the process.

### 1.2 Understanding the three components

| Component         | Responsibility                             |
| ----------------- | ------------------------------------------ |
| Dev (Development) | Write and maintain application code        |
| Sec (Security)    | Identify risks and protect applications    |
| Ops (Operations)  | Deploy, monitor, and maintain applications |

### 1.3 Traditional DevOps vs DevSecOps

| Traditional DevOps                        | DevSecOps                          |
| ----------------------------------------- | ---------------------------------- |
| Focuses on development and operations     | Includes security throughout       |
| Security may happen later                 | Security starts early              |
| Vulnerabilities may be found late         | Problems can be identified earlier |
| More manual security checks               | Automated security checks          |
| Security can be a separate responsibility | Shared security responsibility     |

### 1.4 Example

Imagine a company is developing an online banking application.

Without DevSecOps:

1. Developers write the application.
2. Operations deploy it.
3. Security team tests it afterward.
4. Critical vulnerabilities are discovered.
5. Developers must fix and redeploy.

With DevSecOps:

1. Developers write secure code.
2. Code is automatically scanned.
3. Dependencies are checked for vulnerabilities.
4. Application security tests run.
5. Deployment checks enforce security requirements.
6. The application is monitored after deployment.

Why is DevSecOps important?

- Detects vulnerabilities earlier.
- Reduces security risks.
- Improves software quality.
- Reduces the cost of fixing security issues.
- Helps maintain security during frequent deployments.

## 2. Shift-Left Security

### 2.1 What is shift-left security?

Shift-left security means performing security activities earlier in the software development lifecycle instead of waiting until the application is completed.

Think about a house: it is easier to include strong locks and secure doors in the design than to rebuild the entire house after discovering security problems.

[DevSecOps 101: Shifting Security Left](https://images.openai.com/static-rsc-4/3jAp40TrcKCvEY_NTQfzJm2D9ujrivJwXMc7C0jZlaGl_-N4n15pnZxWiylEm3YRP3jqAaxG-Dm6fAWUBz_7V2z9oXb7Ia3Sflc8R3FO9sOGVmggsF2H1-HAsQY2CxtjaFG3APfEcp7ZoB4RyshRBgsB1O1TfbV21sW0vElt1jU?purpose=inline)

[linkedin.com](https://www.linkedin.com/pulse/devsecops-101-shifting-security-left-nitin-bharadwaj-9qgpc?utm_source=chatgpt.com)

### 2.2 Traditional security approach

```
Planning → Development → Testing → Deployment → Security
```

Security happens late.

### 2.3 Shift-left security approach

```
Security planning
       ↓
Secure design
       ↓
Secure coding
       ↓
Code scanning
       ↓
Security testing
       ↓
Secure deployment
```

Security is included from the beginning.

### 2.4 Practical examples

Example 1: SQL Injection

Without shift-left:

- Application is completed.
- Security tester discovers SQL injection.
- Developers must redesign the database query.

With shift-left:

- Developers learn secure SQL practices.
- Code scanning identifies unsafe query patterns.
- Developers use parameterized queries before deployment.

Example 2: Weak passwords

Without shift-left:

- Application is deployed.
- Security review identifies weak password handling.

With shift-left:

- Password requirements are included in security requirements.
- Developers implement secure password hashing.
- Authentication tests run before deployment.

### 2.5 Shift-left security activities

| Development stage | Security activity               |
| ----------------- | ------------------------------- |
| Planning          | Identify security requirements  |
| Design            | Threat modeling                 |
| Coding            | Secure coding practices         |
| Code review       | SAST                            |
| Testing           | DAST and penetration testing    |
| Deployment        | Configuration and secret checks |

Remember: Shift-left = Move security earlier.

## 3. Automation in Security

### 3.1 What is security automation?

Security automation means using tools, scripts, and workflows to perform security tasks automatically instead of doing everything manually.

For example, instead of asking a security engineer to inspect every code change manually, a development pipeline can automatically scan the code whenever a developer uploads a change.

### 3.2 Why do we need automation?

- Saves time.
- Reduces repetitive manual work.
- Finds vulnerabilities earlier.
- Makes security checks consistent.
- Supports frequent software releases.

### 3.3 Common security automation activities

| Activity                | What automation does                              |
| ----------------------- | ------------------------------------------------- |
| SAST scanning           | Checks source code                                |
| Dependency scanning     | Finds vulnerable libraries                        |
| Secret scanning         | Detects exposed passwords and API keys            |
| DAST                    | Tests a running application                       |
| Container scanning      | Checks container images for vulnerabilities       |
| Infrastructure scanning | Identifies insecure infrastructure configurations |
| Security monitoring     | Detects suspicious events                         |

### 3.4 Tools used for security automation

[¿Qué es GitHub Actions?. La clave para automatizar tu flujo de… | by María Claudia Pérez Escalante | Medium](https://images.openai.com/static-rsc-4/xg-DO-ZEEBnTj4eHiAO5xQWhqgvPR1RoAxLD46SpujyPGsJEF8kZcclnniBAt7V-Jrt9c64Vr0mA9a6D111LzlZS3NjuLKAx2OIIgf-H5H8x7gl3YbR1r9oPEu72toeARKpJIt_OMsO1SiQL1aOzBaE9qj-zmVBso0FgusAwZDw?purpose=inline)

GitHub Actions

Automates build, testing, and security workflows when code is pushed or a pull request is opened.

Example: Automatically run a security scan after a code change.

[How to Start, Stop, Restart or Reload Jenkins - Mac OSx | Damien Saunders](https://images.openai.com/static-rsc-4/O9sCRdZ8mryGpaZmbdlgeRB9JlFoXysllCrJ8nV-ni3iYU-IXsb6Wc1896bY8Uo-vwQecYU9K6C4KL_wX1ClcD3lLyozLcFSqb97CxpLgjY-vbq4VkJObynZut9O0Skfsbqy2QuAX2ukR_hRo812akmjHD9wby1WBJ-lH2e0W9I?purpose=inline)

Jenkins

Automates software development and deployment pipelines.

Example: Run tests and security checks before deployment.

[Top 10 Open-Source Kubernetes Security Tools Every DevOps Engineer Needs in 2025 | by Baivab Mukhopadhyay | devdotcom | Medium](https://images.openai.com/static-rsc-4/UOg0-8RHJ4MTblX-465wxHhBmRqh2Yds6W2NA1Y0UK5KY34mmo5JwKnU4t6gQmMlMLPllZQFl5iVpM7iyAFTDi07Ks_dEEmLqglvNSfMp1_l9cuW1GEPvmzy7cnbHcUXSgdpkWlO8Gbi4M4k4f5XcK4m1H3pN_fnKGy4pT_APzo?purpose=inline)

Trivy

Scans container images, filesystems, repositories, and configurations for security issues.

Example: Find vulnerable packages in a Docker image.

[dependabot-bot (Dependabot) · GitHub](https://images.openai.com/static-rsc-4/tA9x4l9VbvDJ8DURuBjWhlOVB1csW7dB9A45sL4ob800O3nOPW9v1FwdJkR1yiJCFbiZwnk9I2CMfHE8XiYi5VnrsWAlRy91Xa-EO0aTFQDOEbyS7pYdxAaVYvTwsk9D7ef5cGsuHXw3bDR9WQmZLcS0LFtc3PPIu7uw-PB3nQU?purpose=inline)

Dependabot

Identifies dependency vulnerabilities and helps keep dependencies updated.

Example: Alert developers about an outdated vulnerable library.

### 3.5 Practical example: Automating a Python security scan

Suppose you have a Python project and want to check it automatically.

Install Bandit:

```
pip install bandit
```

Run a security scan:

```
bandit -r .
```

Explanation:

- `bandit`: Runs the Python security scanner.
- `-r`: Scans recursively.
- `.`: Scans the current directory.

You can also scan dependencies with:

```
pip-audit
```

This checks installed Python packages for known vulnerabilities.

Important: Automated tools identify potential issues. A security professional must review and validate their findings.

## 4. Security Integration

### 4.1 What is security integration?

Security integration means connecting security tools and checks directly into the software development workflow.

Instead of treating security as a separate activity, it becomes part of coding, testing, building, and deployment.

### 4.2 Where is security integrated?

[DevSecOps Toolchain: SAST, DAST, SCA and Container Security | by Alfatah Jalalludin | Mar, 2026 | Medium](https://images.openai.com/static-rsc-4/4eQVxwpzqRM21uZNkDSxhB7PcX50Tw-39n2WwhrNdPsG64cQP51KOJAzfx0Du4kYCYrKcPJnZDnM2_1OURDO97I5AgVfRyHdc9kyzTMpH89gM-X11GYn8IgtvgeuPn7czBBOSR1CRe-JN3bJvtSiv2WdoIYX9sXjjsLl-dyN6is?purpose=inline)

[al-fatah.medium.com](https://al-fatah.medium.com/devsecops-toolchain-explained-sast-dast-sca-and-container-security-6e00d9bd7025?utm_source=chatgpt.com)

| Pipeline stage     | Security integration              |
| ------------------ | --------------------------------- |
| Code creation      | Secure coding guidelines          |
| Code upload        | Secret scanning                   |
| Code review        | SAST                              |
| Build              | Dependency scanning               |
| Testing            | DAST and security testing         |
| Container creation | Container image scanning          |
| Deployment         | Configuration and access checks   |
| Production         | Monitoring and incident detection |

### 4.3 What is CI/CD?

You should understand these two terms:

CI = Continuous Integration

Developers frequently add their code changes to a shared project. Automated processes build and test those changes.

CD = Continuous Delivery or Continuous Deployment

- Continuous Delivery: Software is prepared for release, with deployment typically requiring approval.
- Continuous Deployment: Changes that pass the required checks can be deployed automatically.

### 4.4 Example of a DevSecOps pipeline

Imagine you are a developer working on an online shopping application.

1. You write Python code.
2. You upload the code to GitHub.
3. GitHub Actions starts the workflow.
4. Bandit scans the Python code.
5. Dependency scanning checks third-party packages.
6. Automated tests run.
7. The application is built.
8. Container scanning checks the image.
9. Deployment occurs only after the required checks pass.

This is an example of integrating security into CI/CD.

### 4.5 Example GitHub Actions workflow

Create this file inside your project:

```
.github/workflows/security.yml
```

Add:

```
name: Python Security Scan

on:
  push:
  pull_request:

jobs:
  security:
    runs-on: ubuntu-latest

    steps:
      - name: Get source code
        uses: actions/checkout@v4

      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.12"

      - name: Install Bandit
        run: pip install bandit

      - name: Run security scan
        run: bandit -r .
```

What happens?

Whenever code is pushed or a pull request is created, GitHub Actions runs Bandit against the repository.

This is a simple example of DevSecOps integration. For production, you should also pin third-party actions to verified versions or commit SHAs, manage permissions carefully, and define which findings should block a release.

## 5. Continuous Security

### 5.1 What is continuous security?

Continuous security means checking, monitoring, and improving security throughout the entire application lifecycle.

Security is not a one-time activity. New vulnerabilities, software updates, configuration changes, and new threats can appear at any time.

### 5.2 Continuous security lifecycle

[Uday👨‍💻 (@uday_devops) on X](https://images.openai.com/static-rsc-4/ynOr-B6EhWL47aNMFCZ9zR8pDj1D0jiJ5YAZ5PVf6jJf4n26Brpc6wCAjTTo8pda2cuAo4SsYmbZrcMhwW1SnYlrZZLQGMSpEQogAJxm1-A-Ob_FuB0w3hsg_n0Fy4WkjChWERA1Sf6CklKe1AkC22boAQdvUQySVFy2CLH74jo?purpose=inline)

[x.com](https://x.com/uday_devops/status/2044619289378849040?utm_source=chatgpt.com)

1. Plan: Define security requirements.
2. Develop: Follow secure coding practices.
3. Test: Perform automated and manual security testing.
4. Deploy: Apply secure deployment configurations.
5. Monitor: Observe logs, events, and suspicious activity.
6. Respond: Investigate and handle security incidents.
7. Improve: Fix weaknesses and update security controls.

### 5.3 Continuous security examples

| Situation                       | Continuous security activity    |
| ------------------------------- | ------------------------------- |
| New code is uploaded            | Automatically scan the code     |
| A dependency becomes vulnerable | Identify and update it          |
| A secret is exposed             | Detect, revoke, and rotate it   |
| A suspicious login occurs       | Generate a security alert       |
| A server configuration changes  | Check against a secure baseline |
| A vulnerability is fixed        | Retest the application          |

### 5.4 Continuous monitoring

Security monitoring is an important part of continuous security.

Examples of what teams monitor:

- Failed login attempts.
- Unusual user activity.
- Privileged account usage.
- Unexpected network connections.
- Changes to important files.
- Suspicious API requests.
- Security alerts from cloud platforms.

Tools include SIEM platforms, cloud audit logs, endpoint detection systems, and application monitoring tools.

Remember: Continuous security = Security checks throughout development and after deployment.

## 6. Hands-on Practical: Build a Mini DevSecOps Pipeline



Beginner practical

Kali Linux / Windows / GitHub



Objective: Build a small Python project and automatically scan it for security weaknesses whenever you push code to GitHub.

### Step 1: Create a project

Create a folder:

```
devsecops-lab/
│
├── app.py
├── requirements.txt
└── .github/
    └── workflows/
        └── security.yml
```

### Step 2: Create a Python application

Inside `app.py`:

```
def welcome(username):    print("Welcome", username)welcome("student")
```

This is a simple application for practising the security pipeline.

### Step 3: Create requirements.txt

```
bandit
pip-audit
```

### Step 4: Install the tools

Open the terminal inside your project:

```
python -m venv venv
```

Activate the environment.

Windows:

```
venv\Scripts\activate
```

Kali Linux:

```
source venv/bin/activate
```

Install dependencies:

```
pip install -r requirements.txt
```

### Step 5: Run security checks manually

Run Bandit:

```
bandit -r .
```

Run dependency auditing:

```
pip-audit
```

Understand the output and investigate any findings.

### Step 6: Add GitHub Actions

Create:

```
.github/workflows/security.yml
```

Paste the workflow from Section 4.5.

### Step 7: Upload your project to GitHub

```
git init
git add .
git commit -m "feat: add DevSecOps security lab"
```

Create a new empty GitHub repository, then connect it:

```
git branch -M main
git remote add origin YOUR_REPOSITORY_URL
git push -u origin main
```

Replace `YOUR_REPOSITORY_URL` with your own repository URL.

### Step 8: Verify the automated workflow

1. Open your GitHub repository.
2. Select the Actions tab.
3. Find the Python Security Scan workflow.
4. Open the latest run.
5. Inspect the Bandit scan output.
6. Confirm whether the workflow passed or failed.

[Getting Started With GitHub Actions - DZone Refcards](https://images.openai.com/static-rsc-4/c7ixJfrUdrlWlx_hSmjJA0lL4hgrji-QVa_lbGy7ha3hFlIKAnK4Tvfzy9SqYMQh-hrbfvG5k-mTlud-sKvGinABvGyLSXv8lp6TSJGVWRzaHkLz5mKup38KlT-sVK2cGFl0ycXAf0LpmrsofILouRrAcOIBdLO5UT84bqFZzH8?purpose=inline)

[dzone.com](https://dzone.com/refcardz/getting-started-with-github-actions?utm_source=chatgpt.com)

Practical completed

You have now practised a basic DevSecOps pipeline: source code → automated security scan → workflow result.

Advanced improvement: Add secret scanning, dependency review, unit tests, container scanning, and a deployment approval step.

## 7. Important DevSecOps Tools

| Tool           | Main purpose                         |
| -------------- | ------------------------------------ |
| Git            | Version control                      |
| GitHub Actions | CI/CD automation                     |
| Jenkins        | Pipeline automation                  |
| Bandit         | Python SAST                          |
| Semgrep        | Static code analysis                 |
| SonarQube      | Code quality and security            |
| OWASP ZAP      | Dynamic application testing          |
| Trivy          | Container and configuration scanning |
| Dependabot     | Dependency vulnerability alerts      |
| Docker         | Containerization                     |
| Terraform      | Infrastructure as Code               |
| Splunk         | Security monitoring and log analysis |

## 8. Important Exam and Interview Questions

Q1. What is DevSecOps?

DevSecOps integrates security into development and operations throughout the software development lifecycle.

Q2. What does shift-left security mean?

It means performing security checks early in the development process.

Q3. What is security automation?

Using scripts and tools to automatically perform security tasks.

Q4. What is CI/CD?

CI means Continuous Integration. CD means Continuous Delivery or Continuous Deployment.

Q5. What is a security pipeline?

A workflow that includes automated security checks during software development and deployment.

Q6. What is the purpose of GitHub Actions?

It automates workflows such as building, testing, and scanning code.

Q7. What is continuous security?

Continuously checking, monitoring, and improving application security throughout its lifecycle.

Q8. What is the difference between DevOps and DevSecOps?

DevSecOps adds security as an integrated responsibility throughout the DevOps workflow.

Q9. Why do we use Trivy?

To identify vulnerabilities and misconfigurations in container images, filesystems, repositories, and infrastructure configurations.

Q10. Why is automation important in DevSecOps?

It makes security checks repeatable, consistent, and faster.

## 9. Module 5 Quick Revision

## Remember these five concepts

1. DevSecOps: Development + Security + Operations.
2. Shift-left: Start security early.
3. Automation: Let tools perform repeatable security checks.
4. Integration: Connect security tools to development and CI/CD pipelines.
5. Continuous security: Check and improve security throughout the lifecycle.

## 10. Test Your Knowledge

Module 5 Quiz

0/5 answered

1\. What does DevSecOps stand for?

Development, Security, Operations

Development, Server, Operating System

Design, Security, Operations



2\. What is shift-left security?

Security after deployment

Security early in development

Removing security testing



3\. Which tool is used for Python security scanning?

Bandit

Wireshark

Nmap



4\. What does CI stand for?

Continuous Inspection

Continuous Integration

Code Installation



5\. What is the main idea of continuous security?

Test security once

Only scan after deployment

Continuously check and improve security



Submit answers

Your next practical goal: Build the mini DevSecOps pipeline in your own GitHub repository and document the workflow screenshot, tools used, scan results, and security improvements.

Would you like a fresh hands-on DevSecOps challenge every evening, progressing from basic CI/CD security to advanced pipeline security?

🔐Daily DevSecOps practice challengeTap to set up
