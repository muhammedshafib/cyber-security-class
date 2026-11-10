# Module 6: Understand CI/CD Security

This module teaches you how to protect the software development pipeline from attackers.

Simple meaning: CI/CD security means protecting the process that takes application code from a developer's computer to a production server.

Imagine a developer builds an online shopping website. The code is uploaded to GitHub, tested, built, and deployed. If an attacker compromises any step in this process, they may be able to steal secrets, modify code, or deploy malicious software.

That's why CI/CD security is important.

[Secure CI/CD Pipelines: Automating Security in DevOps | by Alfatah Jalalludin | Mar, 2026 | Medium](https://images.openai.com/static-rsc-4/ahQB0Uaxa4GYUMOFNRrZhQQc9FmucaG_X3yDSv4t--idEsNvPFLQENPq6XZEUmcbSREg2Fys-THorNheGoluPk2VxX38izcgSxjvpE0lMiSXccgTf4RK2BFaW_zMtUQLxZ6Jev78rzduvtev_VwKQ9mG4WFmR3gtjw5EVNUaXQk?purpose=inline)

[al-fatah.medium.com](https://al-fatah.medium.com/secure-ci-cd-pipelines-automating-security-in-devops-249e22a3fabd?utm_source=chatgpt.com)

## 1. Secure Pipelines

### 1.1 What is a pipeline?

A pipeline is an automated sequence of steps used to build, test, and deploy software.

Example:

```
Developer writes code
        ↓
Code uploaded to GitHub
        ↓
Automated testing
        ↓
Security scanning
        ↓
Application build
        ↓
Deployment
```

### 1.2 What is a secure pipeline?

A secure pipeline means protecting every stage of this process using security controls.

Simple example:

A developer uploads Python code to GitHub.

Before the application is deployed:

1. The pipeline checks the code.
2. It scans for vulnerabilities.
3. It checks dependencies.
4. It verifies security requirements.
5. It allows deployment only if required checks pass.

### 1.3 Common pipeline security risks

| Risk                | Meaning                                          |
| ------------------- | ------------------------------------------------ |
| Unauthorized access | Someone accesses the pipeline without permission |
| Malicious code      | An attacker inserts harmful code                 |
| Exposed secrets     | Passwords or API keys become visible             |
| Insecure plugins    | A vulnerable pipeline plugin is exploited        |
| Weak permissions    | Users or workflows have excessive privileges     |
| Pipeline tampering  | An attacker changes pipeline instructions        |

### 1.4 How to secure pipelines

- Use strong authentication and MFA.
- Give users only necessary permissions.
- Protect important GitHub branches.
- Review code changes before merging.
- Use trusted pipeline actions and plugins.
- Scan code automatically.
- Keep CI/CD tools updated.
- Protect deployment credentials.

Remember: Secure pipeline = Protect the entire software delivery process.

## 2. Secrets Management

### 2.1 What are secrets?

Secrets are confidential values used by applications and systems to authenticate or access resources.

Examples:

- Passwords
- API keys
- Database credentials
- Access tokens
- SSH private keys
- Cloud credentials

Example of an exposed secret:

```
API_KEY = "my-secret-api-key-123"
```

This is dangerous because anyone who can access the source code may be able to obtain the key.

### 2.2 What is secrets management?

Secrets management means securely storing, accessing, using, rotating, and protecting sensitive credentials.

Instead of writing passwords directly in the source code, applications should retrieve secrets from a secure storage system.

### 2.3 Bad practice vs good practice

Bad practice

Hardcoding a password

```
DB_PASSWORD = "admin123"
```

The password is directly inside the source code.

Better practice

Reading from an environment variable

```
import osDB_PASSWORD = os.getenv("DB_PASSWORD")
```

The application reads the password from its environment instead of storing it in the code.

### 2.4 Popular secrets management tools

| Tool                   | Purpose                                  |
| ---------------------- | ---------------------------------------- |
| HashiCorp Vault        | Securely stores and manages secrets      |
| AWS Secrets Manager    | Manages application secrets in AWS       |
| Azure Key Vault        | Protects keys, secrets, and certificates |
| GitHub Actions Secrets | Stores secrets for GitHub workflows      |

### 2.5 What if a secret is exposed?

Suppose an API key accidentally gets uploaded to GitHub.

You should:

1. Revoke the exposed key.
2. Generate a new key.
3. Update the secure secret store.
4. Check logs for unauthorized usage.
5. Remove the exposed value from the repository history where appropriate.
6. Investigate how the exposure happened.

Remember: Secrets management = Keep passwords, API keys, and credentials safe.

## 3. Dependency Security

### 3.1 What is a dependency?

A dependency is an external library or package that your application uses to perform specific tasks.

For example, a Python application may use:

- `requests` for HTTP requests.
- `flask` for web applications.
- `django` for web development.
- `numpy` for numerical operations.

These packages are developed by other people or organizations.

### 3.2 What is dependency security?

Dependency security means checking third-party libraries for vulnerabilities, outdated versions, and unsafe packages.

Simple example:

Imagine your application uses an old version of Flask.

A security vulnerability is discovered in that version. An attacker may exploit it if your application is affected.

Dependency security helps identify and fix such problems.

### 3.3 Common dependency risks

| Risk                  | Meaning                                                                          |
| --------------------- | -------------------------------------------------------------------------------- |
| Outdated packages     | Using old versions with known vulnerabilities                                    |
| Vulnerable libraries  | Packages containing security weaknesses                                          |
| Malicious packages    | Packages designed to steal data or execute harmful code                          |
| Dependency confusion  | Installing an unintended package because of package-name or repository confusion |
| Unmaintained packages | Libraries that no longer receive security updates                                |

### 3.4 Dependency security tools

| Tool                   | Purpose                                                  |
| ---------------------- | -------------------------------------------------------- |
| Dependabot             | Detects vulnerable dependencies and suggests updates     |
| pip-audit              | Checks Python packages against known vulnerability data  |
| Snyk                   | Finds vulnerabilities in dependencies and code           |
| OWASP Dependency-Check | Identifies known vulnerabilities in project dependencies |

### 3.5 Practical example: pip-audit

Step 1: Install

```
pip install pip-audit
```

Step 2: Check installed packages

```
pip-audit
```

Step 3: Understand the result

The tool may show:

- Package name
- Installed version
- Vulnerability ID
- Fixed version, if available

Step 4: Fix the issue

Update the affected package to a safe compatible version, then run the audit again.

```
pip install --upgrade package-name
```

Replace `package-name` with the actual affected package.

Remember: Dependency security = Check the libraries your application uses.

## 4. Build Security

### 4.1 What is a build?

A build is the process of converting source code into software that can be tested or deployed.

For example:

```
Python / Java / JavaScript source code
                 ↓
            Build process
                 ↓
        Application package
                 ↓
           Ready to deploy
```

### 4.2 What is build security?

Build security means protecting the process that creates the application package from unauthorized changes, malicious code, and compromised tools.

Imagine an attacker changes the build process so that the final application contains malicious code even though the original source code looked safe.

Build security helps prevent this.

### 4.3 Common build security risks

| Risk                    | Meaning                                  |
| ----------------------- | ---------------------------------------- |
| Malicious build scripts | Scripts perform harmful actions          |
| Compromised build tools | Attackers manipulate build software      |
| Tampered artifacts      | Final application packages are modified  |
| Unauthorized changes    | Someone changes build configurations     |
| Untrusted dependencies  | Unsafe external packages enter the build |

### 4.4 How to secure builds

1. Use trusted build tools.
2. Restrict access to build systems.
3. Scan source code before building.
4. Verify dependencies.
5. Protect build configurations.
6. Store build artifacts securely.
7. Use digital signatures to verify artifact integrity.

### 4.5 What is an artifact?

A build artifact is a file produced by the build process.

Examples:

- `.jar` files
- `.zip` application packages
- Docker images
- Compiled executables
- Deployment packages

Example: A developer builds an application and produces `shopping-app.zip`. The file is a build artifact.

If an attacker modifies this file, the deployed application may no longer be trustworthy.

### 4.6 What is artifact integrity?

Artifact integrity means ensuring that a build artifact has not been unexpectedly modified.

One way to check integrity is using a cryptographic hash.

Linux:

```
sha256sum shopping-app.zip
```

Windows PowerShell:

```
Get-FileHash shopping-app.zip -Algorithm SHA256
```

Compare the hash against a trusted recorded value. If the values differ, investigate the change.

Remember: Build security = Protect the process that creates your application.

## 5. Deployment Security

### 5.1 What is deployment?

Deployment means releasing an application to an environment where people can use it.

Examples:

- Deploying a website to a cloud server.
- Releasing a mobile application.
- Publishing an API.
- Deploying a Docker container.

### 5.2 What is deployment security?

Deployment security means protecting the application and its environment during and after release.

It ensures that the application is deployed with secure configurations and appropriate access controls.

[Open Source Dependency Management](https://images.openai.com/static-rsc-4/0KHTl2WzWxeGELt7k_mOErKd2JxwzWugJJMkiGYeXtUEspXvCemzI7uvdrqZpGykDbQWmADzNbOcGMUUDdjlhBuykZBnLtmc3iEWpNe-OHVIKU0tz0MLM0xocnZMbVNdM3Eti9lApZaOOvPTmBKq2LYSrfvlPE6lJkBMbLurKKo?purpose=inline)

[mediusware.com](https://mediusware.com/blog/open-source-dependency-management?utm_source=chatgpt.com)

### 5.3 Common deployment security risks

| Risk                      | Meaning                                                 |
| ------------------------- | ------------------------------------------------------- |
| Default credentials       | Leaving default usernames and passwords unchanged       |
| Open ports                | Exposing unnecessary network services                   |
| Misconfiguration          | Using insecure server or cloud settings                 |
| Excessive permissions     | Giving applications or users too much access            |
| Unencrypted communication | Sending sensitive information without proper encryption |
| Exposed secrets           | Leaving API keys or passwords in deployment settings    |

### 5.4 How to secure deployment

- Use HTTPS/TLS.
- Enable MFA for administrative accounts.
- Apply least privilege.
- Remove default credentials.
- Disable unnecessary services and ports.
- Secure environment variables and secrets.
- Use secure server configurations.
- Monitor application logs.
- Keep software updated.

### 5.5 Example: Cloud deployment

Imagine you deploy a website on AWS.

Before making it publicly accessible, check:

1. Is the server properly configured?
2. Are only required ports exposed?
3. Is SSH access restricted?
4. Are IAM permissions limited?
5. Is HTTPS enabled?
6. Are database credentials stored securely?
7. Are logs and monitoring enabled?

Remember: Deployment security = Protect the application when releasing it to users.

## 6. Understand the Difference Between All Five Topics

This is the most important table for remembering Module 6.

| Topic               | What are we protecting?     | Easy meaning                 |
| ------------------- | --------------------------- | ---------------------------- |
| Secure pipelines    | CI/CD workflow              | Protect the whole pipeline   |
| Secrets management  | Passwords and API keys      | Protect credentials          |
| Dependency security | External libraries          | Protect packages             |
| Build security      | Build process and artifacts | Protect application creation |
| Deployment security | Released application        | Protect application release  |

### Easy real-world example

Imagine you are building an online shopping website.

## One application, five security layers

1. Secure pipeline

   Protect your GitHub Actions workflow from unauthorized changes.
2. Secrets management

   Protect your database password and API keys.
3. Dependency security

   Check whether Flask and other Python libraries have known vulnerabilities.
4. Build security

   Ensure the generated application package has not been tampered with.
5. Deployment security

   Ensure the website is released with HTTPS, secure permissions, and proper configurations.

## 7. Hands-on Practical: CI/CD Security Mini Lab

Beginner practical

Objective: Practise secrets management, dependency security, and pipeline security using your own GitHub repository.

### Step 1: Create your project

```
cicd-security-lab/
│
├── app.py
├── requirements.txt
└── .github/
    └── workflows/
        └── security.yml
```

### Step 2: Create app.py

```
import osdef welcome():    username = os.getenv("USERNAME", "student")    print("Welcome", username)welcome()
```

### Step 3: Create requirements.txt

```
requests
flask
```

### Step 4: Check dependencies

```
pip install -r requirements.txt
```

Run:

```
pip-audit
```

Investigate any reported vulnerabilities.

### Step 5: Check secrets

Run a simple search for suspicious hardcoded credentials:

```
grep -RniE "password=|api_key=|secret=" .
```

This is only a basic search, not a complete secret scanner.

### Step 6: Add GitHub Actions security workflow

Create `.github/workflows/security.yml`:

```
name: CI CD Security Check

on:
  push:
  pull_request:

jobs:
  security:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.12"

      - name: Install dependencies
        run: pip install -r requirements.txt

      - name: Check dependencies
        run: pip-audit

      - name: Scan Python code
        run: |
          pip install bandit
          bandit -r .
```

### Step 7: Push your project to GitHub

```
git init
git add .
git commit -m "feat: add CI CD security lab"
git branch -M main
git remote add origin YOUR_REPOSITORY_URL
git push -u origin main
```

### Step 8: Check the result

Open your GitHub repository:

1. Click Actions.
2. Open `CI CD Security Check`.
3. Select the latest workflow run.
4. Inspect the dependency audit.
5. Inspect the Bandit results.
6. Investigate any failures.

Note: This is a learning pipeline. A real production pipeline also needs protected branches, carefully restricted workflow permissions, trusted dependencies, secret scanning, artifact verification, and controlled deployment.

## 8. Important Exam and Interview Questions

Q1. What is CI/CD security?

CI/CD security is the process of protecting software development, building, testing, and deployment pipelines from security threats.

Q2. What is a secure pipeline?

A secure pipeline protects the automated software delivery process using access controls, security scanning, and verification.

Q3. What is secrets management?

It is the secure storage and management of passwords, API keys, tokens, and other sensitive credentials.

Q4. What is dependency security?

It means identifying and managing vulnerabilities in third-party libraries and packages used by an application.

Q5. What is build security?

Build security protects the process of converting source code into application packages.

Q6. What is a build artifact?

A build artifact is a file generated during the application build process, such as a Docker image or ZIP package.

Q7. What is deployment security?

Deployment security protects applications and their environments during release and operation.

Q8. Name three secrets management tools.

- HashiCorp Vault
- AWS Secrets Manager
- Azure Key Vault

Q9. What is pip-audit?

It is a Python tool used to identify known vulnerabilities in installed Python packages.

Q10. Why is CI/CD security important?

It prevents attackers from compromising the software delivery process and helps ensure secure application releases.

## 9. Module 6 Quick Revision

## Five points to memorize

1. Secure pipelines = Protect the workflow.
2. Secrets management = Protect passwords and API keys.
3. Dependency security = Protect external libraries.
4. Build security = Protect application creation.
5. Deployment security = Protect application release.

## 10. Test Your Knowledge

Module 6 Quiz

0/5 answered

1\. What does a CI/CD pipeline do?

Only stores passwords

Automates building, testing, and releasing software

Only monitors networks



2\. Which tool manages secrets in AWS?

AWS Secrets Manager

Nmap

Wireshark



3\. Which tool checks Python dependencies for known vulnerabilities?

pip-audit

Burp Suite

Hydra



4\. What is a build artifact?

A user password

A file produced during a build

A firewall rule



5\. What is deployment security?

Protecting application release and environment

Writing source code only

Installing a text editor



Submit answers

Your practical target: Build the CI/CD security lab and document the pipeline, dependency scan, secrets handling, and workflow results in your cybersecurity GitHub portfolio.

🔐Daily CI/CD security practiceTap to set up
