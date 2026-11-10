# Module 4: Understand Application Security Testing

This module teaches you how to examine an application, discover security weaknesses, and verify whether security controls are working correctly.

For your offensive security learning path, this is an important bridge between understanding vulnerabilities and performing practical web application penetration testing.

[What is Application Security? Solutions & Best Practices](https://images.openai.com/static-rsc-4/IiVvj1I0V4-CQbfivl2qJpOTT6sqd02bjBVMYUuyCb6HQgZ_qRelKJBobKJobFJiE7jcFNU5HVkTWnuPvfdmxue-CL3x7rDx6IRooG8dgFH5yKHMoLywGAJFptfmOxwHFINuX4IjFNPUmwm6o_uKqIGQMuQEWFx0eH9Fu-73too?purpose=inline)

[Web Application Pen Testing: The Essential Guide | Terra Security Blog](https://images.openai.com/static-rsc-4/Yj-kIRoXJTD5ffqTrGby8T2LlGR1lJ4u9FA5MvIKUxauE4W-K8ZQeU00qRaz1-O_cwKMEPh0FvDAiZny3r1v7XqRpR_mqe1FBFWByUBUwrB9uxzYX9EH6-2A7-Jf4jhSO2-MqK-nKZvK-cU49PEjb5rJXHNP_nNGTySMWGM7NBI?purpose=inline)

[Static Source Code Analysis: Getting Started | Xygeni](https://images.openai.com/static-rsc-4/caVWIHvnQdaWp0hHMbfdt5sKJ-lES0nrRMg5iMOtplP9jHWpMY9hChQ6xUr-XJnKZdE0hJKdOc5zCzbdgPv97Xu7z6zqvtwdHZXeOW4uo4vhhNAG5kIfYVJQyjVdpAxDfpHDDmA_w9zFvqJnkkl7ScpxzbGhb-ToWB3Z-eIgClQ?purpose=inline)

9

## 1. Security Reviews

### 1.1 What is a security review?

A security review is the process of examining an application's design, source code, configuration, and functionality to identify possible security weaknesses.

Think of it as inspecting a building before allowing people inside. You check the doors, windows, locks, cameras, and emergency exits.

In application security, we check:

- Authentication: Is the login system secure?
- Authorization: Can users access only permitted resources?
- Input validation: Does the application validate user input?
- Session management: Are sessions protected?
- Data protection: Is sensitive data stored and transmitted securely?
- Error handling: Does the application expose sensitive information?

### 1.2 Types of security reviews

| Type                  | What we examine                              |
| --------------------- | -------------------------------------------- |
| Design review         | Application architecture and security design |
| Code review           | Source code for security mistakes            |
| Configuration review  | Server and application settings              |
| Authentication review | Login and identity controls                  |
| Authorization review  | Access permissions                           |
| API review            | API endpoints and access controls            |

### 1.3 Example

Imagine an online shopping application.

A security reviewer checks:

1. Can users view another user's orders?
2. Can users change product prices through requests?
3. Are passwords securely hashed?
4. Does the application protect payment information?
5. Can an unauthenticated visitor access private pages?

Why is it important?

Security reviews help identify weaknesses before attackers discover them.

## 2. Static Analysis Awareness (SAST)

### 2.1 What is static analysis?

Static Application Security Testing (SAST) examines an application's source code without executing the application.

It searches for potentially unsafe coding patterns.

For example, consider this Python code:

```
username = input("Enter username: ")query = "SELECT * FROM users WHERE name = '" + username + "'"
```

This code builds an SQL query by directly joining user input into the query string. It may introduce SQL injection.

A static analysis tool can flag this risky pattern.

### 2.2 How SAST works

[What Is Static Application Security Testing (SAST)? | Akamai](https://images.openai.com/static-rsc-4/qvj_xji1oaiJS5YZ1ycLrYp_lQXNY_pBYJ1GdHEcV-X6xI2UVLYjJ5srAaomi-gRP6jtGJ10bnwoSTrmp547S5Jpe0xtpmyzdAQ9AGtq8u0PgV-vwTfDsff7i4e9KggH58XLdvfXGCIvNpqk4aN2njDO-72j2bvFBpDeexdtt80?purpose=inline)

[akamai.com](https://www.akamai.com/glossary/what-is-static-application-security-testing-sast?utm_source=chatgpt.com)

1. Developer writes application code.
2. SAST tool scans the source code.
3. Tool identifies suspicious coding patterns.
4. It reports potential vulnerabilities.
5. Developer reviews and fixes the findings.

### 2.3 Popular SAST tools

| Tool      | Purpose                                  |
| --------- | ---------------------------------------- |
| Semgrep   | Finds insecure code patterns             |
| SonarQube | Code quality and security analysis       |
| Bandit    | Python security linting                  |
| CodeQL    | Queries code to discover vulnerabilities |
| Snyk Code | Static code security analysis            |

### 2.4 Practical example: Bandit

Bandit is a security analysis tool for Python code.

Step 1: Install Bandit

```
pip install bandit
```

Step 2: Create a Python file

Save this as `test.py`:

```
import subprocesssubprocess.call("ls", shell=True)
```

Step 3: Scan the file

```
bandit test.py
```

Step 4: Understand the result

Bandit may flag the use of `shell=True` because unsafe handling of shell commands can lead to command injection.

The tool identifies a potential issue. You must investigate whether it is exploitable in the actual application.

Important: SAST does not prove that an application is secure. It can produce false positives and miss vulnerabilities that depend on runtime behavior.

## 3. Dynamic Analysis Awareness (DAST)

### 3.1 What is dynamic analysis?

Dynamic Application Security Testing (DAST) tests an application while it is running.

Unlike SAST, DAST does not need to examine the source code. It interacts with the application through its interfaces, such as web pages and HTTP requests.

For example, imagine a website with a login page:

```
https://example.com/login
```

A DAST tool can examine how the application responds to different inputs and requests.

### 3.2 How DAST works

[Dynamic Application Security Testing (DAST) - GeeksforGeeks](https://images.openai.com/static-rsc-4/7fVTi2pg8UO8PO22oernJLFOtHlFt49_AfwRtpz22kkJ2YSBZEYBL5DuzjmmuJmm5kKagEQtmK8OxrZOIbJPPeXpQM0ZTIbcUhbllYuDgMNJYsIltlRxtAPDPbskSKEAHzVgPCac2lMRmLT-y02RMOSdyHjgeRRPb2DPFtnY3t8?purpose=inline)

[geeksforgeeks.org](https://www.geeksforgeeks.org/ethical-hacking/dynamic-application-security-testing-dast/?utm_source=chatgpt.com)

1. Start the application.
2. Configure the testing target.
3. Discover application pages and endpoints.
4. Send test requests.
5. Analyze responses.
6. Report possible vulnerabilities.

### 3.3 Popular DAST tools

| Tool       | Purpose                               |
| ---------- | ------------------------------------- |
| Burp Suite | Intercepts and tests web traffic      |
| OWASP ZAP  | Web application security scanner      |
| Nikto      | Web server security checks            |
| Nuclei     | Template-based vulnerability scanning |

### 3.4 Practical example: OWASP ZAP

[Securing Web Applications: A Detailed ZAP Scan of DVWA | by Ilerioluwa Ajani | Medium](https://images.openai.com/static-rsc-4/bXGj4-aiYdR4b5MVUja1PZTgH-H9RQ5L8zuHGH5HPjM2uEVWFb_xj1dXqSoHkqeiC2_3f7qe2stOneOIxLRK66daL3XAlZjo7_ETXmQRt1uWboJeiHkMXloBq3kb0XmzEf62W-2wedjTFeQIRSKnc_qJAs7AkmQ1qYRqqlb3pWY?purpose=inline)

[medium.com](https://medium.com/%40IlerioluwaAjani/securing-web-applications-a-detailed-zap-scan-of-dvwa-5d1085f228bf?utm_source=chatgpt.com)

OWASP ZAP can help identify:

- Missing security headers
- Cross-site scripting (XSS) indicators
- Potential SQL injection
- Insecure cookies
- Information disclosure
- Other web application weaknesses

Basic practice:

1. Install OWASP ZAP.
2. Start a local training application such as OWASP Juice Shop.
3. Open ZAP.
4. Configure your browser to use ZAP as its proxy.
5. Browse the training application.
6. Review the Alerts tab.
7. Investigate each finding manually.

Only scan applications you own or have explicit permission to test.

### 3.5 SAST vs DAST

| Feature              | SAST                                | DAST                                 |
| -------------------- | ----------------------------------- | ------------------------------------ |
| Full form            | Static Application Security Testing | Dynamic Application Security Testing |
| Testing              | Source code                         | Running application                  |
| Application running? | Not required                        | Required                             |
| Main focus           | Coding weaknesses                   | Runtime weaknesses                   |
| Example tools        | Bandit, Semgrep                     | ZAP, Burp Suite                      |
| Testing stage        | Usually development                 | Usually testing or staging           |

Remember:

- SAST = Check the code.
- DAST = Test the running application.

## 4. Vulnerability Discovery Concepts

### 4.1 What is vulnerability discovery?

Vulnerability discovery is the process of finding security weaknesses in an application, system, or network.

A vulnerability is a weakness that could allow an attacker to compromise confidentiality, integrity, or availability.

Examples:

| Vulnerability             | Meaning                                                           | Possible impact                    |
| ------------------------- | ----------------------------------------------------------------- | ---------------------------------- |
| SQL Injection             | Unsafe database query handling                                    | Database access or modification    |
| XSS                       | Untrusted input executes as browser script                        | Account or session compromise      |
| IDOR                      | Missing object-level access checks                                | Access to another user's data      |
| CSRF                      | Unwanted actions performed through a user's authenticated session | Unauthorized account actions       |
| Broken authentication     | Weaknesses in login or session controls                           | Account takeover                   |
| Security misconfiguration | Unsafe application or server settings                             | Information exposure or compromise |
| Directory traversal       | Unsafe access to file paths                                       | Unauthorized file access           |
| Sensitive data exposure   | Sensitive information is not adequately protected                 | Data leakage                       |

### 4.2 Vulnerability discovery workflow

[Web Application Penetration Testing Guide (2026 Edition) | DivIHN](https://images.openai.com/static-rsc-4/1MPp9SaU2NbjdlP1qIYhOXsW-5MmdvQk0xdgQ0zBmN23QPz1CphuoN98J1kBUAFxIQshKhQMI0GX1YeO8XCo-GER4Q6riKY1PDNdS5btq86_VSG556lUiww4_z7UsjmjWYUuptq8ItShtJW5zsenGilSqjrWaaVAjVa-rwZeysU?purpose=inline)

[divihn.com](https://divihn.com/perspective/blog/Web-Application-Penetration-Testing-Guide?utm_source=chatgpt.com)

Step 1: Information gathering

Understand the application.

- Identify pages and functions.
- Identify login and registration.
- Discover API endpoints.
- Understand user roles.
- Identify technologies where appropriate.

Tools: Browser Developer Tools, Burp Suite, OWASP ZAP.

Step 2: Attack surface identification

The attack surface is the collection of places where an application can receive input or interact with users and other systems.

Examples:

```
/login
/register
/search
/profile
/api/users
/api/orders
/upload
```

Each endpoint may need different security checks.

Step 3: Vulnerability scanning

Use security tools to identify potential weaknesses.

Examples:

- Nmap: discovers network services and ports.
- Nessus: identifies known vulnerabilities and configuration issues.
- OWASP ZAP: examines running web applications.
- Burp Suite: helps inspect and test HTTP requests.
- Semgrep: identifies potentially insecure code.

Step 4: Manual testing

Automated tools cannot understand every application-specific security rule.

Manually investigate:

- Can one user access another user's information?
- Can a normal user perform administrator actions?
- Does the application validate input on the server?
- Are private API endpoints protected?
- Can a user bypass an important workflow?

Step 5: Document findings

Record the vulnerability, evidence, impact, severity, and recommended fix.

### 4.3 Vulnerability discovery vs exploitation

These are related, but not identical.

| Activity     | Meaning                                                      |
| ------------ | ------------------------------------------------------------ |
| Discovery    | Find a possible vulnerability                                |
| Verification | Check whether the finding is genuine                         |
| Exploitation | Demonstrate the security impact in an authorized environment |
| Reporting    | Document the evidence and remediation                        |

For example:

- Discovery: A scanner reports a possible IDOR.
- Verification: You test with two accounts you control.
- Demonstration: You confirm that Account A can access Account B's test order.
- Reporting: You document the missing authorization check and its impact.

Important: Finding a vulnerability does not automatically mean it can be exploited. Always verify findings carefully.

## 5. Security Validation

### 5.1 What is security validation?

Security validation is the process of confirming that security controls work correctly and that identified vulnerabilities have been fixed.

Finding a problem is only half the job. You must also verify that the solution actually works.

### 5.2 Example: IDOR security validation

Imagine an online shopping application.

Two test accounts exist:

- Account A: `user_id = 101`
- Account B: `user_id = 102`

Suppose Account A can access Account B's order by changing the order ID.

Before the fix

Account A

Logged in as user 101

Account B's order

User 102's private data

Authorization failure

After the fix

Account A

Requests user 102's order

Access denied

Server checks ownership

Authorization working

### 5.3 Security validation process

1. Identify the original vulnerability.
2. Apply the security fix.
3. Repeat the same test.
4. Confirm unauthorized access is blocked.
5. Confirm legitimate users can still access their own data.
6. Check whether the fix introduced another problem.
7. Document the retest result.

### 5.4 Types of security validation

| Type                     | Purpose                                         |
| ------------------------ | ----------------------------------------------- |
| Retesting                | Confirm a reported vulnerability is fixed       |
| Regression testing       | Check that existing features still work         |
| Access-control testing   | Verify permissions and restrictions             |
| Authentication testing   | Verify login and session security               |
| Input validation testing | Check how the application handles invalid input |
| Configuration validation | Confirm security settings are correct           |

### 5.5 Example: Input validation

Suppose a registration form requires an age between 18 and 100.

Test cases:

| Input       | Expected result |
| ----------- | --------------- |
| `25`        | Accepted        |
| `17`        | Rejected        |
| `101`       | Rejected        |
| `hello`     | Rejected        |
| Empty value | Rejected        |
| `-5`        | Rejected        |

The server should validate the input even if the browser already has validation.

## 6. Practical Lab: Application Security Testing

Beginner-friendly authorized lab

For this module, use OWASP Juice Shop. It is deliberately designed for learning web application security.

[OWASP JUICE SHOP — WALKTHROUGH. Dive into the world of real-world web… | by Eleanor | Medium](https://images.openai.com/static-rsc-4/HzbgGH5r8JpiXf-HG6_mROrNJX6XZcFuD_0afcvwJB4J9zRr84wAzNlRFyHzXwOmK5mD63K6uPlu_dAfvBtvO9xx2HnIHQAJzFnjef0xLkLVa-7HMlAKLiu6kRR8lk4fm1gDcZ0wvrRC_9flmzt5jE_sytPL_MAN-DRtVsJqGpM?purpose=inline)

[TryHackMe | OWASP Juice Shop](https://images.openai.com/static-rsc-4/lxFx1_5wzZNmQmqkMajneYTeXA66sriPNlbLTMc7ICd5kSlA3l11apeIW0NhvgXn2XfTWWYJXjUQW813tN2FcWujKnaUVkf412cFKbA05ONxbQHf3CC2vjv7AXjL8weKg-862U9io0KJsb1QHl9QBg0LmjOuiV7WmbT1i42N4mA?purpose=inline)

[OWASP Foundation](https://images.openai.com/static-rsc-4/UMl9fSMNrbmaOOmeR8HPZKlLm9m9RX3yncID8rhKYF0McP-TkAMn_-o8o2dFBkCD8Mc5lpetD4R4WjU6AHnGbzIZrwAAR21MnyleBivs2xnFRxLuMYVqJZHvNw2mV9565clHVu8gv-2D7amKxlA-XO2QggnLRf1hepqVsR2eSM0?purpose=inline)

Official resources:

- [OWASP Juice Shop project](https://owasp.org/www-project-juice-shop/?utm_source=chatgpt.com)
- [Juice Shop GitHub repository](https://github.com/juice-shop/juice-shop?utm_source=chatgpt.com)

### Lab objective

Practice the complete application security testing process:

1. Understand the application.
2. Discover its attack surface.
3. Observe HTTP requests and responses.
4. Identify potential vulnerabilities.
5. Verify findings safely.
6. Document the results.

### Step 1: Start Juice Shop

If you have Docker installed on Kali Linux:

```
docker run --rm -p 3000:3000 bkimminich/juice-shop
```

Open this in your browser:

```
http://localhost:3000
```

### Step 2: Perform a security review

Explore the application and record:

- Login page
- Registration page
- Search function
- Product pages
- Shopping basket
- User profile
- Available API requests

Do not assume every feature is vulnerable. Your task is to understand how it works.

### Step 3: Perform DAST

1. Open OWASP ZAP.
2. Configure your browser to proxy traffic through ZAP.
3. Browse your local Juice Shop application.
4. Review the discovered URLs and alerts.
5. Select one alert and read its evidence.
6. Decide whether it is a confirmed vulnerability or only a potential issue.

Start with passive scanning. Use active scanning only against your own local training application.

### Step 4: Inspect requests with Burp Suite

[Burp Suite Tutorial (Part 1): Introduction to The  Burp Suite Proxy | Cybrary](https://images.openai.com/static-rsc-4/bHwIbZbIRLJDkbuzP4k_oBb4g9XdtvQZE-9TlhhKrjfVU2ujBvlQni2RYlTxYJ-7JoBHnb3JP07oM0mBmLq_0BkcJo1WvqCC7W6oYTrm5cSavOGb12I4XbvGMxEeVjvenTMzbk2UhG6z_jMA3woyc-hRcHneMK3TmBgQNrym1E0?purpose=inline)

[cybrary.it](https://www.cybrary.it/blog/burp-suite-tutorial-part-1-introduction-to-the-burp-suite-proxy?utm_source=chatgpt.com)

1. Open Burp Suite.
2. Configure the browser proxy.
3. Visit Juice Shop.
4. Open Proxy → HTTP history.
5. Select a request.
6. Examine the method, URL, headers, cookies, parameters, and response.

Example request:

```
GET /rest/user/whoami HTTP/1.1
Host: localhost:3000
```

Understand what the application sends and what the server returns.

### Step 5: Write a vulnerability report

Use this structure:

| Field            | Example                                    |
| ---------------- | ------------------------------------------ |
| Vulnerability    | Broken access control                      |
| Affected feature | User order access                          |
| Severity         | Based on verified impact                   |
| Evidence         | Request and response                       |
| Impact           | Unauthorized access to another user's data |
| Recommendation   | Enforce server-side ownership checks       |
| Status           | Open / Fixed / Retested                    |

Do not report a scanner alert as a confirmed vulnerability until you have verified it.

## 7. Important Concepts for Revision

| Term                | Simple meaning                                        |
| ------------------- | ----------------------------------------------------- |
| Security review     | Examining an application for security weaknesses      |
| SAST                | Testing source code without running the application   |
| DAST                | Testing an application while it is running            |
| Vulnerability       | A security weakness                                   |
| False positive      | A reported issue that is not actually a vulnerability |
| False negative      | A real vulnerability that a tool fails to detect      |
| Attack surface      | All possible entry points into an application         |
| Security validation | Confirming security controls work correctly           |
| Retesting           | Testing again after a vulnerability is fixed          |
| Regression testing  | Checking that a fix has not broken existing features  |

## 8. Important Exam and Interview Questions

Q1. What is application security testing?

Application security testing is the process of identifying and verifying security weaknesses in an application.

Q2. What is the difference between SAST and DAST?

SAST examines source code without executing the application. DAST tests the running application.

Q3. Name three SAST tools.

- Semgrep
- Bandit
- SonarQube

Q4. Name three DAST tools.

- Burp Suite
- OWASP ZAP
- Nikto

Q5. What is vulnerability discovery?

It is the process of identifying potential security weaknesses in an application.

Q6. What is a false positive?

A security tool reports a possible vulnerability, but investigation shows that the issue is not actually present.

Q7. Why is manual testing important?

Because automated tools cannot identify every application-specific security weakness.

Q8. What is security validation?

It is the process of checking whether security controls work correctly and vulnerabilities have been fixed.

Q9. What is regression testing?

Testing existing functionality after a change to ensure it still works correctly.

Q10. Why do we use Burp Suite?

To intercept, inspect, modify, and test HTTP requests and responses during authorized web application security testing.

## 9. Module 4 Quick Revision

## Application Security Testing Workflow

1. Security Review

   Examine application design, code, and configuration.
2. Static Analysis (SAST)

   Check source code for potential security weaknesses.
3. Dynamic Analysis (DAST)

   Test the running application.
4. Vulnerability Discovery

   Identify and investigate possible vulnerabilities.
5. Security Validation

   Verify findings and confirm that fixes work.

## 10. Test Your Knowledge

Module 4 Quiz

0/5 answered

1\. Which testing method examines source code without executing the application?

DAST

SAST

Regression testing



2\. Which tool is commonly used for intercepting HTTP requests?

Burp Suite

Bandit

SonarQube



3\. What is a false positive?

A real vulnerability

A fixed vulnerability

A reported issue that is not actually present



4\. What should you do after fixing a vulnerability?

Ignore it

Retest it

Delete the application



5\. Which application is intentionally vulnerable for security training?

OWASP Juice Shop

Google Search

Microsoft Word



Submit answers

Your practical target: Complete the Juice Shop review, inspect traffic with Burp Suite, and investigate at least one ZAP alert. Document what you discovered and how you verified it.

I can also prepare a short application-security testing practice challenge for you each day, progressing from SAST and DAST to manual vulnerability verification.

🛡️Daily application security challengeTap to set up
