# **Module 7: Understand Supply Chain Security**

This module teaches you how to protect software from security risks that come from external libraries, tools, vendors, and other third-party components.

**Simple meaning:** Supply Chain Security means protecting all the components and services used to create, build, and deliver software.

Imagine you develop a website using Python, Flask, a database, Docker, and external APIs. Even if your own code is secure, one vulnerable or malicious external component could put the entire application at risk.

[An Overview of Software Supply Chain Security](https://images.openai.com/static-rsc-4/Uk2YRrNXRGuaqZY4TELuz7CRQ3x3OHPDbIdo-b4fW7sK1XtdG0ibSes2JmgwLzCT0CccJTdxmopbJhReZl8junFi7HVeDFYEftrYnQ9LjE5r6AWmr2oB2ijngN6GjB_kKZsIBcGYQ30tpiHcRoNyLvCahjy2-CgbkRdcYgG3c9s?purpose=inline)

[tldrsec.com](https://tldrsec.com/p/supply-chain-security-overview?utm_source=chatgpt.com)

## **1. Third-Party Software Risks**

### **1.1 What is third-party software?**

Third-party software is software, libraries, tools, or services developed by someone other than the organization using them.

Examples:

- Python libraries such as Flask and Requests.
- JavaScript packages such as Express.
- External APIs.
- Docker base images.
- Cloud services.
- Software development tools.

**Example:**

You develop an application and install a third-party package:

```
pip install requests
```

Your application now depends on software created and maintained by another developer or organization.

### **1.2 What are third-party software risks?**

These are security problems that can enter your application through external software or services.

### **1.3 Common third-party risks**

| Risk                  | Simple meaning                                                                     |
| --------------------- | ---------------------------------------------------------------------------------- |
| Vulnerable dependency | An external package contains a security weakness                                   |
| Malicious package     | A package is intentionally designed to harm users                                  |
| Outdated software     | Old software may contain known vulnerabilities                                     |
| Compromised vendor    | An external provider gets hacked                                                   |
| Dependency confusion  | An unintended package is installed because of package-name or repository confusion |
| Unmaintained software | A package no longer receives security updates                                      |
| Software tampering    | Software is modified by an unauthorized party                                      |

### **1.4 Real-world example**

Imagine your company uses a Python library in its banking application.

1. Developers install the library.
2. The library contains a security vulnerability.
3. The vulnerability is discovered.
4. Attackers create attempts to exploit affected applications.
5. Your banking application may become vulnerable because it uses that library.

**Important:** Your own application code may be secure, but an insecure third-party component can still create risk.

### **1.5 How to reduce third-party risks**

- Use trusted software repositories.
- Check package maintainers and project activity.
- Avoid unnecessary packages.
- Check dependencies for known vulnerabilities.
- Update vulnerable packages.
- Verify package integrity and provenance.
- Monitor vendor security advisories.

## **2. Dependency Management**

### **2.1 What is a dependency?**

A dependency is an external package or library that an application needs to function.

Example Python project:

```
import requestsimport flask
```

Here, Requests and Flask are dependencies.

### **2.2 What is dependency management?**

Dependency management means controlling which external packages an application uses, which versions are installed, and when they are updated.

For example, instead of installing random versions every time, a developer records the required packages and versions.

### **2.3 Why is dependency management important?**

- Prevents vulnerable packages.
- Avoids unexpected updates.
- Improves application stability.
- Makes builds more reproducible.
- Helps identify outdated libraries.
- Reduces the risk of malicious packages.

### **2.4 Python dependency management example**

Install Flask:

```
pip install flask
```

Check installed packages:

```
pip list
```

Save dependencies:

```
pip freeze > requirements.txt
```

Example `requirements.txt`:

```
Flask==3.1.0
requests==2.32.3
```

These are illustrative version pins, not a guarantee that these versions are the latest or suitable for every project.

Install the recorded dependencies:

```
pip install -r requirements.txt
```

### **2.5 Dependency security scanning**

Install:

```
pip install pip-audit
```

Scan the project environment:

```
pip-audit
```

This checks installed Python packages against known vulnerability information.

### **2.6 Important dependency management tools**

| Tool                   | Purpose                                              |
| ---------------------- | ---------------------------------------------------- |
| pip                    | Python package installation                          |
| pip-audit              | Python vulnerability checking                        |
| Dependabot             | Dependency vulnerability alerts and update proposals |
| Snyk                   | Dependency security analysis                         |
| OWASP Dependency-Check | Known vulnerability detection                        |
| Renovate               | Dependency update automation                         |

**Remember:** Dependency management = Control, update, and secure external libraries.

## **3. Software Integrity**

### **3.1 What is software integrity?**

Software integrity means ensuring that software has not been secretly changed, damaged, or tampered with by unauthorized people.

In simple words:

**Software integrity = Making sure the software you receive is the genuine, unchanged software you expect.**

### **3.2 Example**

Imagine you download a software package from the internet.

An attacker modifies the package and adds malicious code before you download it.

If you install that modified package, your computer or application could be compromised.

Software integrity checks help detect unexpected changes.

### **3.3 How do we verify software integrity?**

Three important methods:

**1. Hash verification**

A hash is a unique-looking fixed-length value calculated from data.

Example:

```
sha256sum application.zip
```

This generates a SHA-256 hash.

If the file changes, its hash will normally change too.

**2. Digital signatures**

A digital signature helps verify that software or a package came from the expected signing identity and has not been modified since it was signed.

**3. Checksums**

A checksum is a value used to detect accidental or unexpected changes in a file.

### **3.4 Practical example: Compare file hashes**

Linux / Kali:

```
sha256sum application.zip
```

Windows PowerShell:

```
Get-FileHash application.zip -Algorithm SHA256
```

Compare the calculated hash with a trusted hash provided by the software publisher.

**Example**

Illustrative hash values

Original file hash

ABC123

Downloaded file hash

ABC123

Hashes match. No change detected by this comparison.

Trusted hash

ABC123

Downloaded file hash

XYZ789

Hashes differ. Investigate the file before installing it.

**Important:** A matching hash only provides meaningful assurance when the reference hash comes from a trusted, independent source. A hash alone does not prove that software is safe.

### **3.5 Software Bill of Materials (SBOM)**

An SBOM is a list of the software components and dependencies included in an application.

For example:

```
Shopping Application
│
├── Python
├── Flask
├── Requests
├── Database Driver
└── Other Libraries
```

An SBOM helps security teams understand what software is inside their application and identify affected components when a vulnerability is discovered.

Two common SBOM formats are:

- SPDX
- CycloneDX

**Remember:** Software integrity = Verify that software is genuine and has not been tampered with.

## **4. Security Monitoring**

### **4.1 What is security monitoring?**

Security monitoring means continuously observing software, systems, dependencies, and activities to identify suspicious behaviour and security threats.

**Simple meaning:** Watch your software and its components to detect security problems.

### **4.2 What should we monitor?**

| Monitoring area      | What we check                          |
| -------------------- | -------------------------------------- |
| Dependencies         | New vulnerabilities in packages        |
| Software updates     | Unexpected or suspicious changes       |
| Vendor activity      | Security incidents affecting providers |
| Build systems        | Unauthorized build changes             |
| Access logs          | Suspicious login activity              |
| Package repositories | Malicious or compromised packages      |
| Software integrity   | Unexpected file or artifact changes    |

### **4.3 Example**

Imagine your application uses a third-party library called `requests`.

A new security advisory reports a vulnerability in the version you use.

Security monitoring helps your team:

1. Receive the vulnerability alert.
2. Identify affected applications.
3. Check the installed package version.
4. Assess the risk.
5. Update to a safe version when available.
6. Verify that the application works after the update.

### **4.4 Tools used for security monitoring**

| Tool       | Purpose                                  |
| ---------- | ---------------------------------------- |
| Splunk     | Collects and analyzes security logs      |
| Wazuh      | Security monitoring and threat detection |
| Dependabot | Dependency vulnerability alerts          |
| Trivy      | Vulnerability and configuration scanning |
| Snyk       | Software dependency and code security    |

### **4.5 Security monitoring workflow**

[Semgrep Supply Chain | Protect Dependencies with Software Composition Analysis (SCA) | Semgrep](https://images.openai.com/static-rsc-4/snFfmxbZt6VL5tu43F1BkirXobIMwuL14NXPampWfu6ekz3r0pWkaNKqgirSEPoIKVxAxd4mZ_c08RdplML_FUXE_PxVmvfI2be36Fypnx8lQOpLAkRfSJNCHu8ysCyUgadrJDxuFbA-l4ve2EZVruMbEO-4s9tAUJYPrwhT-KI?purpose=inline)

[semgrep.dev](https://semgrep.dev/products/semgrep-supply-chain/?utm_source=chatgpt.com)

1. Monitor software and dependencies.
2. Detect suspicious changes or vulnerability alerts.
3. Investigate the affected component.
4. Assess the risk.
5. Fix or isolate the affected component.
6. Verify the fix.
7. Document the incident.

**Remember:** Security monitoring = Continuously watch for security problems.

## **5. Risk Mitigation**

### **5.1 What is risk mitigation?**

Risk mitigation means taking steps to reduce the possibility or impact of a security problem.

**Simple meaning:** Identify the risk and take action to make it less dangerous.

### **5.2 Example**

Imagine your website uses an outdated third-party package with a known critical vulnerability.

Risk:

An attacker may exploit the vulnerable package and compromise your application.

Mitigation:

1. Identify the affected package.
2. Check whether your application is affected.
3. Update to a fixed version.
4. Test the application.
5. Deploy the update safely.
6. Monitor for further issues.

### **5.3 Common supply chain risks and mitigation**

| Risk                       | Mitigation                                     |
| -------------------------- | ---------------------------------------------- |
| Vulnerable packages        | Scan and update dependencies                   |
| Malicious packages         | Use trusted repositories and verify packages   |
| Outdated libraries         | Maintain an update process                     |
| Compromised vendors        | Assess vendors and monitor security advisories |
| Tampered software          | Verify hashes and digital signatures           |
| Exposed credentials        | Use secrets management                         |
| Unmaintained dependencies  | Replace with maintained alternatives           |
| Unauthorized modifications | Restrict access and review changes             |

### **5.4 Four common risk treatment approaches**

| Approach | Meaning                                   | Example                                 |
| -------- | ----------------------------------------- | --------------------------------------- |
| Avoid    | Stop the risky activity                   | Stop using an unsafe package            |
| Mitigate | Reduce the risk                           | Update a vulnerable library             |
| Transfer | Shift some financial or contractual risk  | Cyber insurance                         |
| Accept   | Understand and formally tolerate the risk | Accept a low-risk issue with monitoring |

**Remember:** Risk mitigation = Reduce security risks before they cause damage.

## **6. Hands-on Practical: Software Supply Chain Security Lab**

Beginner practical

**Objective:** Practise dependency checking, software integrity verification, SBOM generation, and vulnerability monitoring.

You can perform this lab using Kali Linux or Windows.

### **Step 1: Create a project**

```
supply-chain-lab/
│
├── app.py
├── requirements.txt
└── README.md
```

Create `app.py`:

```
import requestsresponse = requests.get("https://example.com", timeout=5)print(response.status_code)
```

This is a simple Python application that uses an external library.

### **Step 2: Install the dependency**

```
pip install requests
```

Check installed packages:

```
pip list
```

### **Step 3: Perform dependency security scanning**

Install the scanner:

```
pip install pip-audit
```

Run:

```
pip-audit
```

Observe:

- Package name
- Installed version
- Vulnerability details
- Fixed version, if available

Record any findings.

### **Step 4: Generate an SBOM**

Install CycloneDX for Python:

```
pip install cyclonedx-bom
```

Generate an SBOM:

```
cyclonedx-py environment -o sbom.json
```

This creates a software component inventory in CycloneDX JSON format.

Open `sbom.json` and examine the listed packages and versions.

### **Step 5: Verify software integrity**

Create a sample file:

```
echo "Supply chain security lab" > sample.txt
```

Generate its SHA-256 hash:

```
sha256sum sample.txt
```

Now modify the file:

```
echo "File modified" >> sample.txt
```

Generate the hash again:

```
sha256sum sample.txt
```

Compare both hashes. They should be different.

### **Step 6: Enable GitHub dependency monitoring**

1. Upload your project to GitHub.
2. Open the repository.
3. Go to **Settings → Advanced Security** if available.
4. Enable the supported dependency security features.
5. Configure Dependabot alerts or dependency update features where available.
6. Review alerts if any are generated.

### **Step 7: Document your results**

Use this report structure:

| Practical activity     | What to document           |
| ---------------------- | -------------------------- |
| Dependency scanning    | pip-audit output           |
| SBOM generation        | Generated sbom.json        |
| Integrity verification | Before and after hashes    |
| Security monitoring    | GitHub dependency alerts   |
| Risk mitigation        | Recommended security fixes |

Use a project you control. A clean scan does not guarantee that every dependency or software component is safe.

## **7. Important Exam and Interview Questions**

**Q1. What is supply chain security?**

Supply chain security is the process of protecting software components, dependencies, vendors, and tools used to develop and deliver software.

**Q2. What is third-party software?**

Software developed by an external organization or developer and used by another application.

**Q3. What is dependency management?**

Managing the packages, libraries, versions, and updates used by an application.

**Q4. What is software integrity?**

Ensuring software has not been modified or tampered with by unauthorized parties.

**Q5. What is a software hash?**

A hash is a fixed-length value generated from data and can be used to detect changes in files.

**Q6. What is an SBOM?**

A Software Bill of Materials is an inventory of software components and dependencies used in an application.

**Q7. What is security monitoring?**

Continuously observing software and systems to detect vulnerabilities and suspicious activities.

**Q8. What is risk mitigation?**

Taking actions to reduce the likelihood or impact of security risks.

**Q9. What is Dependabot?**

A GitHub tool that identifies vulnerable dependencies and can suggest dependency updates.

**Q10. Why is supply chain security important?**

Because vulnerable or malicious third-party components can compromise an otherwise secure application.

## **8. Module 7 Quick Revision**

## **Five concepts to memorize**

1. **Third-party software risks:** External software can introduce vulnerabilities.
2. **Dependency management:** Control and update external libraries.
3. **Software integrity:** Verify software is genuine and unchanged.
4. **Security monitoring:** Continuously watch for security threats.
5. **Risk mitigation:** Reduce the possibility and impact of security problems.

## **9. Test Your Knowledge**

**Module 7 Quiz**

0/5 answered

**1. What is third-party software?**

Software developed by an external provider

Only your own source code

A computer operating system



**2. Which tool checks Python packages for known vulnerabilities?**

Nmap

pip-audit

Wireshark



**3. What does SBOM stand for?**

Secure Build Operating Method

Software Bill of Materials

System Backup Operating Mode



**4. What is the purpose of SHA-256 hash verification?**

Install dependencies

Detect file changes by comparing hashes

Deploy an application



**5. What is risk mitigation?**

Ignoring risks

Increasing vulnerabilities

Reducing security risks



Submit answers

**Portfolio task:** Save your `sbom.json`, dependency scan results, and hash comparison evidence in your GitHub cybersecurity repository. This is a useful beginner supply chain security project.

You can continue with a daily practical challenge to build your supply chain security skills.

🔐Daily supply chain security challengeTap to set up
