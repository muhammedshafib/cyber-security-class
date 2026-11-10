# Module 3: Understand Secure Coding Principles 🔐



Secure SDLC | Beginner to Advanced

Application Security



Secure coding is one of the most important skills in cybersecurity, especially for Application Security (AppSec), Ethical Hacking and Penetration Testing.

In Module 1, we learned the Secure SDLC process.

In Module 2, we learned how to identify security requirements and risks.

Now, in Module 3, we will learn how developers write code securely and how security professionals identify insecure coding practices.

## What are Secure Coding Principles?

Definition: Secure coding principles are guidelines and practices used when writing software to prevent vulnerabilities, protect sensitive information and reduce security risks.

In simple words:

Secure coding means writing application code in a way that makes it difficult for attackers to exploit weaknesses.

### Example: Login system

Imagine a developer creates a login page.

An insecure application might:

- Store passwords as plain text.
- Accept unsafe user input.
- Allow unlimited login attempts.
- Expose database errors.
- Allow users to access other users' accounts.

A secure application should:

- Hash passwords using a suitable password-hashing algorithm.
- Validate user input.
- Handle errors safely.
- Implement authentication protection.
- Enforce server-side authorization.

## 1. Input Validation

Beginner level

Definition: Input validation is the process of checking user-provided data to ensure it follows the expected format, type, length and allowed values before processing it.

In simple words:

Never trust data received from users.

### 1.1 Why is input validation important?

Imagine a website has a registration form:

- Username
- Email
- Password
- Age

The application expects an email address, but an attacker may submit unexpected data.

Without proper validation, malicious or invalid input could cause:

- SQL Injection.
- Cross-Site Scripting (XSS).
- Application crashes.
- Unexpected application behavior.
- Data corruption.

### 1.2 Types of input validation

A. Client-side validation

Validation performed inside the user's browser.

Example:

- Required fields.
- Email format.
- Password length.
- Input format.

B. Server-side validation

Validation performed by the backend server.

Example:

- Check whether an email address follows the expected format.
- Verify that age is within an allowed range.
- Check whether submitted values are permitted.



Important

&#x20;Client-side validation can be bypassed. Server-side validation is essential.



### 1.3 Validation techniques

| Technique            | Purpose                 | Example                            |
| -------------------- | ----------------------- | ---------------------------------- |
| Type validation      | Check data type         | Age must be an integer             |
| Length validation    | Limit input length      | Username maximum 30 characters     |
| Format validation    | Check expected format   | Email address                      |
| Range validation     | Check allowed range     | Age between 18 and 100             |
| Allowlist validation | Accept permitted values | Country must be from approved list |

### 1.4 Practical Python example

Let's validate a username using Python.

```
username = input("Enter username: ")if username.isalnum() and 3 <= len(username) <= 20:    print("Valid username")else:    print("Invalid username")
```

Line-by-line explanation:

1. `input()` receives the username from the user.
2. `isalnum()` checks whether it contains only letters and numbers.
3. `len(username)` checks its length.
4. The username must contain between 3 and 20 characters.
5. If all conditions are satisfied, the program accepts it.

Note: This is a basic validation example. Production applications need additional checks, such as Unicode handling and server-side business rules.

### 1.5 SQL Injection prevention

Insecure SQL example:

```
query = "SELECT * FROM users WHERE name = '" + username + "'"
```

The problem is that user input is directly combined with SQL code.

Secure approach using parameterized queries:

```
cursor.execute(    "SELECT * FROM users WHERE name = ?",    (username,))
```

Why is this better?

The database treats the supplied username as data rather than executable SQL syntax.

## 2. Error Handling

Beginner to intermediate

Definition: Error handling is the process of detecting, managing and responding to application errors without exposing sensitive information or causing unexpected system failures.

In simple words:

When something goes wrong, the application should handle it safely.

### 2.1 Why is error handling important?

Imagine a user enters an incorrect password.

An insecure application displays:

```
Database error!
Database: company_users
Username: admin
Internal server: 192.168.1.10
```

This reveals internal information that attackers might find useful.

A secure application displays:

```
Invalid username or password.
Please try again.
```

### 2.2 Types of errors

| Error type           | Example                        |
| -------------------- | ------------------------------ |
| Input error          | Invalid email                  |
| Authentication error | Incorrect password             |
| Database error       | Database unavailable           |
| Network error        | Server connection failed       |
| Permission error     | Unauthorized access            |
| System error         | Unexpected application failure |

### 2.3 Python error handling

Python uses `try`, `except`, `else` and `finally`.

Example:

```
try:    number = int(input("Enter a number: "))    result = 100 / numberexcept ValueError:    print("Please enter a valid number.")except ZeroDivisionError:    print("Division by zero is not allowed.")else:    print("Result:", result)finally:    print("Program completed.")
```

Explanation:

- `try`: Executes the main code.
- `except`: Handles errors.
- `else`: Executes if no error occurs.
- `finally`: Executes whether an error occurs or not.

### 2.4 Secure error-handling practices

1. Never expose passwords or API keys in error messages.
2. Avoid displaying database connection details.
3. Log technical errors securely.
4. Show users understandable error messages.
5. Avoid exposing stack traces in production.
6. Ensure errors do not accidentally bypass security checks.

Important concept:

Security principle

Detailed errors should be available to authorized developers through protected logs, not exposed to ordinary application users.

## 3. Authentication Security

Intermediate level

Definition: Authentication security is the process of verifying the identity of a user, device or system before allowing access to an application.

In simple words:

Authentication answers the question: Who are you?

### 3.1 Common authentication methods

| Method                     | Explanation                          |
| -------------------------- | ------------------------------------ |
| Password authentication    | User enters a password               |
| MFA                        | Uses multiple authentication factors |
| OTP                        | One-time password                    |
| Biometric authentication   | Fingerprint or facial recognition    |
| SSO                        | Single Sign-On                       |
| Certificate authentication | Uses digital certificates            |

### 3.2 Important authentication security practices

1\. Secure Password Storage

Never store passwords as plain text.

Bad practice:

```
password = "admin123"
```

Storing this directly in a database is dangerous.

Secure practice:

Use password hashing algorithms such as:

- Argon2id.
- bcrypt.
- scrypt.

Example using Python's bcrypt library:

```
import bcryptpassword = b"mysecret123"hashed = bcrypt.hashpw(    password,    bcrypt.gensalt())print(hashed)
```

Explanation:

- `import bcrypt`: Imports the password hashing library.
- `password`: Contains the original password.
- `gensalt()`: Generates a random salt.
- `hashpw()`: Creates a password hash.
- `print()`: Displays the resulting hash.

For login verification:

```
entered_password = b"mysecret123"if bcrypt.checkpw(entered_password, hashed):    print("Login successful")else:    print("Invalid password")
```

The application verifies the password without storing the original password.

2\. Multi-Factor Authentication (MFA)

MFA requires more than one authentication factor.

Example:

- Something you know: Password.
- Something you have: Authenticator app.
- Something you are: Fingerprint.

Even if an attacker obtains a password, another authentication factor can provide additional protection.

3\. Account Lockout and Rate Limiting

Prevent attackers from repeatedly guessing passwords.

Example:

- Limit login attempts.
- Introduce temporary delays.
- Apply rate limiting.
- Monitor suspicious login activities.

Avoid permanent account lockouts that attackers could abuse to deny service to legitimate users.

4\. Secure Session Management

After successful authentication, applications often create a session to maintain the user's logged-in state.

Security practices:

- Use secure, unpredictable session identifiers.
- Enable HTTPS.
- Set `HttpOnly` and `Secure` cookie attributes.
- Use appropriate `SameSite` settings.
- Expire inactive sessions.
- Regenerate session identifiers after authentication.
- Invalidate sessions during logout.

### 3.3 Authentication attack examples

| Attack              | Explanation                                     |
| ------------------- | ----------------------------------------------- |
| Brute Force         | Repeatedly guesses passwords                    |
| Credential Stuffing | Uses leaked username/password combinations      |
| Password Spraying   | Tries common passwords across multiple accounts |
| Session Hijacking   | Attempts to take over an authenticated session  |
| Phishing            | Tricks users into revealing credentials         |

Red Team connection: When performing an authorized penetration test, authentication security is an important area to assess.

## 4. Authorization Security

Intermediate to advanced

Definition: Authorization is the process of determining what an authenticated user is allowed to access or perform within an application.

In simple words:

Authentication checks who you are.

Authorization checks what you are allowed to do.

### 4.1 Authentication vs Authorization

| Authentication                   | Authorization                        |
| -------------------------------- | ------------------------------------ |
| Verifies identity                | Verifies permissions                 |
| Happens before access is granted | Determines permitted actions         |
| Uses passwords, MFA, biometrics  | Uses roles, permissions and policies |
| Who are you?                     | What can you access?                 |

Example: Online banking application

A customer successfully logs in.

Authentication: The application verifies the customer's identity.

Authorization: The application allows the customer to view their own account but prevents them from accessing another customer's account.

### 4.2 Types of access control

1\. Role-Based Access Control (RBAC)

Permissions are assigned according to user roles.

Example:

| Role          | Permissions                       |
| ------------- | --------------------------------- |
| Customer      | View own account                  |
| Employee      | Manage assigned transactions      |
| Manager       | Approve certain transactions      |
| Administrator | Manage authorized system settings |

2\. Attribute-Based Access Control (ABAC)

Access decisions are based on attributes such as:

- User role.
- Department.
- Location.
- Resource classification.
- Time of access.

Example:

An employee can access a confidential document only if they belong to the finance department and have the required clearance.

3\. Discretionary Access Control (DAC)

The resource owner can decide who gets access.

Example:

A document owner shares a file with selected users.

4\. Mandatory Access Control (MAC)

Access is controlled through centrally enforced security labels and clearance levels.

Example:

A classified system may restrict access based on security classification.

### 4.3 Practical authorization example

Imagine a website has two users:

- User A: ID 101
- User B: ID 102

User A logs in and tries to access:

```
/account/102
```

If the application only checks whether the user is logged in, User A might access User B's account.

This is a Broken Access Control vulnerability.

Secure approach:

The server must verify that the requested account belongs to the authenticated user or that the user has an explicitly authorized permission.

Example Python logic:

```
logged_in_user = 101requested_account = 102if logged_in_user == requested_account:    print("Access granted")else:    print("Access denied")
```

This is a simplified ownership check. Real applications must also handle authorized administrative roles and other permission policies.

### 4.4 Common authorization vulnerabilities

| Vulnerability                   | Meaning                                                        |
| ------------------------------- | -------------------------------------------------------------- |
| IDOR                            | Accessing another user's object by manipulating its identifier |
| Privilege Escalation            | Obtaining higher permissions                                   |
| Broken Access Control           | Accessing restricted resources or actions                      |
| Horizontal Privilege Escalation | Accessing another user's resources at the same privilege level |
| Vertical Privilege Escalation   | Gaining higher-level permissions                               |

[What is Privilege Escalation Attack? ⚔️ Techniques & Protection](https://images.openai.com/static-rsc-4/6yMngW_b19mHf7rzAw2WNszxgXxnVGH1B0klOTTL8xokussyKV3nJZWA7gNG_feyzf8w2trsIh9rSZ7Ef2Caank-B3KsTlA3280XQNHI-mCfue6H8iAn16Wk66S3bn30JYPm3MQzgJJl-sKbanSNSaJvQ_clVDCgirI6Tpcrtlc?purpose=inline)

[wallarm.com](https://www.wallarm.com/what/what-is-privilege-escalation-attack?utm_source=chatgpt.com)

Important Red Team concept:

When testing authorization, check whether:

- A customer can access another customer's data.
- A normal user can access administrator functions.
- Restricted API endpoints are protected.
- Permissions are checked on the server, not only in the browser.

### 4.5 Secure authorization practices

1. Apply least privilege.
2. Enforce permissions on the server.
3. Check ownership of requested resources.
4. Deny access by default.
5. Validate authorization on every protected request.
6. Review permissions regularly.
7. Log important access-control events.

## 5. Secure Development Mindset

Beginner to advanced

Definition: A secure development mindset means considering security during every coding and software development decision rather than treating security as a final testing activity.

In simple words:

Think like a developer who builds software and a security professional who understands how attackers might misuse it.

### 5.1 Normal developer mindset vs secure developer mindset

| Normal development thinking   | Secure development thinking           |
| ----------------------------- | ------------------------------------- |
| Does the login work?          | Can attackers bypass login?           |
| Does the form accept input?   | Can malicious input cause harm?       |
| Can the user access the page? | Is the user authorized?               |
| Does the API return data?     | Does it expose sensitive information? |
| Does the application run?     | Does it run securely?                 |

### 5.2 Important secure development habits

1\. Think like an attacker

Ask:

- What happens if someone submits unexpected input?
- Can someone bypass authentication?
- Can one user access another user's information?
- Can an attacker manipulate API requests?

2\. Follow secure coding standards

Use established security guidance such as:

- OWASP Secure Coding Practices.
- OWASP Top 10.
- OWASP Application Security Verification Standard (ASVS).
- CERT Secure Coding Standards.

3\. Perform code reviews

Review code to identify:

- Hardcoded passwords.
- Unsafe database queries.
- Missing input validation.
- Weak authentication.
- Missing authorization checks.

4\. Keep dependencies updated

Third-party libraries can introduce security vulnerabilities.

Check dependencies, remove unnecessary packages and apply security updates.

5\. Protect secrets

Never expose:

- API keys.
- Database passwords.
- Access tokens.
- Private keys.

Use environment variables or dedicated secrets-management systems.

6\. Test security continuously

Integrate security checks into the development process:

- SAST.
- DAST.
- SCA.
- Dependency scanning.
- Security code reviews.
- Penetration testing.

### 5.3 Secure development mindset example

Imagine you are developing a file-upload feature.

A normal developer might ask:

"Can users upload files successfully?"

A secure developer asks:

1. What file types are allowed?
2. Is the file size restricted?
3. Can malicious files be uploaded?
4. Are file names handled safely?
5. Can uploaded files execute on the server?
6. Are files stored outside publicly executable directories?
7. Can one user access another user's uploaded files?

That is the secure development mindset.

## 6. Practical Lab: Secure Coding Vulnerability Investigation



Hands-on lab

Application Security



Now let's connect all five concepts with practical security testing.

[OWASP Juice Shop - Probably the most modern and sophisticated insecure web application](https://images.openai.com/static-rsc-4/B8W7qbpEPRqNA-VDuclof0azZMqohmhx91bi9k22mOB6iBNPijQop7a_S7DZ_LitFA6sBci8RKCRL6geoY-XhMPT47OlqD6NtbO5fwtFrJdGbNNwLut7yKOHkCZYSquHYA2E2qBbuZrJJFJR3Cihf8zjTB5UV5uayD96bNRjSIA?purpose=inline)

[juice-shop.github.io](https://juice-shop.github.io/juice-shop/?utm_source=chatgpt.com)

Practice application: OWASP Juice Shop

Official website: [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/?utm_source=chatgpt.com)

This application is intentionally vulnerable and designed for security education.

### Lab scenario

You are a junior Application Security Tester. Your task is to investigate the application's coding and access-control weaknesses.

### Task 1: Input validation

- Explore registration and login forms.
- Identify what input validation is performed.
- Check whether invalid input is rejected.
- Understand how SQL Injection and XSS can result from insecure input handling.

### Task 2: Error handling

- Observe how the application responds to invalid requests.
- Check whether sensitive technical information is exposed.
- Identify insecure error messages.

### Task 3: Authentication security

- Explore login and registration.
- Understand password security.
- Investigate authentication protection.
- Identify possible authentication weaknesses.

### Task 4: Authorization security

- Explore user-specific functionality.
- Understand how the application restricts access.
- Investigate IDOR and privilege-related weaknesses in the authorized training environment.

### Task 5: Secure development mindset

For every weakness you identify, document:

1. What is the vulnerability?
2. Where did you find it?
3. How could an attacker abuse it?
4. What is the possible impact?
5. How should developers fix it?

### Practical tools

| Tool                    | Purpose                                 |
| ----------------------- | --------------------------------------- |
| Burp Suite              | Inspect and modify HTTP requests        |
| OWASP ZAP               | Web vulnerability testing               |
| Browser Developer Tools | Inspect requests, responses and cookies |
| Python                  | Practise secure coding                  |
| Semgrep                 | Identify insecure coding patterns       |

### Lab completion tracker

Your practical progress

# 0%

Inspect registration and login input validation.

Understand how parameterized queries prevent SQL Injection.

Observe application error responses.

Study password hashing and MFA.

Investigate session and cookie security.

Test authorization boundaries between users.

Write a vulnerability report with remediation recommendations.

## 7. Important Interview and Exam Questions

Prepare these questions for your examination.

1. What is secure coding?
2. What is input validation?
3. Differentiate between client-side and server-side validation.
4. What is SQL Injection and how can it be prevented?
5. What is error handling?
6. Why should applications avoid exposing stack traces?
7. What is authentication?
8. Explain MFA.
9. What is secure session management?
10. Differentiate between authentication and authorization.
11. What is RBAC?
12. What is ABAC?
13. Explain IDOR.
14. What is privilege escalation?
15. What is a secure development mindset?

## 8. Knowledge Check

Test your understanding.

Module 3 Assessment

5 Questions

1\. What is the main purpose of input validation?

Make websites attractive

Check user input before processing

Store passwords



2\. Which approach is recommended to prevent SQL Injection?

String concatenation

Parameterized queries

Plain-text passwords



3\. Which is a suitable password hashing algorithm?

Base64

Argon2id

Plain text



4\. Authentication answers which question?

Who are you?

What can you access?

Where is the server?



5\. What is IDOR?

A network protocol

A broken access control vulnerability

A password hashing method



Submit answers

## 9. Module 3 Quick Revision

| Topic                      | Remember this                          |
| -------------------------- | -------------------------------------- |
| Input Validation           | Never trust user input                 |
| Error Handling             | Handle errors without exposing secrets |
| Authentication             | Verify user identity                   |
| Authorization              | Verify user permissions                |
| Secure Development Mindset | Think about security while coding      |

### Your Secure SDLC learning roadmap

1. Module 1: Secure SDLC Fundamentals

   Covered

   Understand the development lifecycle.
2. Module 2: Security Requirements

   Covered

   Identify security needs and risks.
3. Module 3: Secure Coding Principles

   Covered

   Understand how to write secure code.
4. Module 4: Security Testing and Vulnerability Assessment

   Learn how to discover, analyze, validate and report application vulnerabilities.

My recommendation: Pay special attention to input validation, authentication and authorization. These three areas are particularly important when you move from Nmap and vulnerability discovery into web application penetration testing.

Next, we can build practical vulnerability-testing exercises around these coding principles using Kali Linux, Burp Suite and OWASP Juice Shop.
