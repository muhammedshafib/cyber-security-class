Below is a **base-to-advanced revision + interview Q&A note** covering **Task 1 to Task 10**. I’ve kept the answers simple enough to speak in an interview, while adding deeper points for reviewer questions.

# Web Security & Secure Development

## Task 1 to Task 10 — Complete Interview & Reviewer Notes

### Purpose

This note is designed for:

* Beginner revision
* Technical interviews
* Trainer/reviewer questions
* Viva preparation
* GitHub reference
* Practical project discussions
* Moving from basic to advanced concepts

### How to answer in an interview

Use this simple pattern:

> **Definition → How it works → Example → Security point**

Example:

**Question:** What is authentication?

**Answer:**

> Authentication is the process of verifying who a user is. For example, when I enter my username and password, the application verifies my identity. After successful authentication, the application can create a session for me. Authentication answers the question: "Who are you?"

---

# TASK 1 — WEB FUNDAMENTALS

## 1. What is a website?

**Answer:**

A website is a collection of web pages and resources that users access through a web browser.

Example:

```text
Browser
   ↓
Website Server
   ↓
HTML / CSS / JavaScript
   ↓
Browser displays the page
```

---

## 2. How does a website work?

**Answer:**

When I enter a website address:

1. Browser receives the URL.
2. DNS finds the server's IP address.
3. Browser connects to the server.
4. Browser sends an HTTP/HTTPS request.
5. Server processes the request.
6. Server sends a response.
7. Browser displays the webpage.

Simple flow:

```text
User
 ↓
Browser
 ↓
DNS
 ↓
Server
 ↓
Application
 ↓
Database
 ↓
Response
 ↓
Browser
```

---

## 3. What is a URL?

**Answer:**

URL means **Uniform Resource Locator**.

It identifies where a web resource is located.

Example:

```text
https://example.com/products?id=10
```

Parts:

```text
https://       → Protocol
example.com    → Domain
/products      → Path
?id=10         → Query parameter
```

---

## 4. What is DNS?

**Answer:**

DNS means **Domain Name System**.

It converts a domain name into an IP address.

Example:

```text
example.com
     ↓
DNS
     ↓
93.184.216.34
```

The browser uses the IP address to communicate with the server.

---

## 5. What is an IP address?

**Answer:**

An IP address identifies a device or network interface on a network.

Example:

```text
192.168.1.10
```

A website domain is easier for humans to remember, while the IP address is used for network communication.

---

## 6. What is client-server architecture?

**Answer:**

Client-server architecture means the client requests a service and the server provides the service.

```text
Client
  |
  | Request
  ↓
Server
  |
  | Response
  ↓
Client
```

The browser is normally the client.

---

## 7. What is frontend?

**Answer:**

Frontend is the part of a web application that users see and interact with.

Common technologies:

* HTML
* CSS
* JavaScript

Examples:

* Buttons
* Forms
* Navigation bars
* Login pages
* Cards

---

## 8. What is backend?

**Answer:**

Backend is the server-side part of an application.

It handles:

* Business logic
* Authentication
* Authorization
* Database operations
* APIs
* Sessions
* Server-side validation

Example:

```text
Frontend
   ↓
Backend
   ↓
Database
```

---

## 9. What is a database?

**Answer:**

A database stores and manages application data.

Example:

```text
users
products
orders
payments
```

---

## 10. What is an API?

**Answer:**

API means **Application Programming Interface**.

It allows different software components to communicate.

Example:

```text
Frontend
   ↓
GET /api/users
   ↓
Backend
   ↓
Database
   ↓
JSON response
```

---

## 11. What is static content?

**Answer:**

Static content is content that is served without being dynamically generated for each request.

Examples:

* HTML files
* CSS files
* JavaScript files
* Images

Example:

```text
style.css
logo.png
index.html
```

---

## 12. What is dynamic content?

**Answer:**

Dynamic content is generated based on data, user input, authentication, or application logic.

Example:

```text
User logs in
     ↓
Server checks user
     ↓
Server gets user information
     ↓
Dashboard is generated
```

---

## 13. What happens when I click a link?

**Answer:**

Usually:

```text
Click link
   ↓
Browser creates HTTP request
   ↓
Server receives request
   ↓
Server processes request
   ↓
Server sends response
   ↓
Browser displays result
```

---

## 14. What is modern web architecture?

**Answer:**

A modern application can contain multiple layers:

```text
Browser
   ↓
Frontend
   ↓
API
   ↓
Backend
   ↓
Database
   ↓
External Services
```

Security should be considered at every layer.

---

# TASK 1 — ADVANCED INTERVIEW QUESTIONS

## 15. What happens between entering a domain and seeing a webpage?

**Answer:**

A simplified process is:

```text
URL entered
 ↓
DNS resolution
 ↓
IP address obtained
 ↓
TCP connection
 ↓
TLS handshake for HTTPS
 ↓
HTTP request
 ↓
Server processing
 ↓
HTTP response
 ↓
Browser rendering
```

---

## 16. Why do we use HTTPS?

**Answer:**

HTTPS protects communication between the client and server using TLS.

It helps provide:

* Confidentiality
* Integrity
* Server authentication

However, HTTPS does **not** automatically mean the website itself is trustworthy.

---

# TASK 2 — HTML FUNDAMENTALS

## 1. What is HTML?

**Answer:**

HTML means **HyperText Markup Language**.

It defines the structure of a webpage.

Example:

```html
<h1>Hello</h1>
<p>Welcome</p>
```

---

## 2. What is an HTML element?

**Answer:**

An HTML element normally consists of a start tag, content, and an end tag.

Example:

```html
<p>Hello</p>
```

---

## 3. What is an HTML attribute?

**Answer:**

An attribute provides additional information about an HTML element.

Example:

```html
<a href="https://example.com">Visit</a>
```

Here:

```text
href = attribute
```

---

## 4. What is `<a>`?

**Answer:**

`<a>` creates a hyperlink.

```html
<a href="login.html">Login</a>
```

---

## 5. What is `href`?

**Answer:**

`href` specifies the destination of a link or linked resource.

```html
<a href="login.html">Login</a>
```

---

## 6. What is `<img>`?

**Answer:**

`<img>` displays an image.

```html
<img src="logo.png" alt="Logo">
```

---

## 7. What is `src`?

**Answer:**

`src` specifies the source/path of a resource.

Example:

```html
<img src="logo.png">
```

---

## 8. What is a form?

**Answer:**

A form collects user input.

Example:

```html
<form>
    <input type="text">
    <button>Submit</button>
</form>
```

---

## 9. What is the difference between GET and POST in forms?

**Answer:**

GET generally sends form data as part of the URL.

POST sends the data in the request body.

Example:

```text
GET:
 /search?q=hello

POST:
 Request body contains the data
```

POST is commonly used when submitting data that changes server-side state.

---

## 10. What is `name` in an input?

**Answer:**

The `name` attribute identifies the form field when its value is submitted.

```html
<input type="text" name="username">
```

The server can access:

```text
username = entered value
```

---

## 11. What is semantic HTML?

**Answer:**

Semantic HTML uses meaningful elements that describe their purpose.

Examples:

```html
<header>
<nav>
<main>
<section>
<article>
<footer>
```

It improves:

* Accessibility
* Maintainability
* SEO
* Understanding of page structure

---

# TASK 2 — ADVANCED HTML QUESTIONS

## 12. What is the difference between HTML, CSS and JavaScript?

**Answer:**

```text
HTML       → Structure
CSS        → Appearance
JavaScript → Behavior
```

Example:

```text
HTML       → Button exists
CSS        → Button looks good
JavaScript → Button performs an action
```

---

## 13. What is client-side validation?

**Answer:**

Client-side validation checks user input in the browser.

Example:

```text
Email must contain @
Password must have minimum length
```

It improves user experience but **cannot be trusted as the only security control**.

The backend must validate input again.

---

# TASK 3 — CSS FUNDAMENTALS

## 1. What is CSS?

**Answer:**

CSS means **Cascading Style Sheets**.

It controls the appearance and layout of HTML.

---

## 2. What is a CSS selector?

**Answer:**

A selector tells CSS which HTML elements should be styled.

Example:

```css
p {
    color: red;
}
```

`p` is the selector.

---

## 3. What does `.` mean in CSS?

**Answer:**

A dot selects a class.

HTML:

```html
<div class="container">
```

CSS:

```css
.container {
}
```

So:

```text
. = class selector
# = ID selector
```

---

## 4. What is padding?

**Answer:**

Padding is the space **inside** an element, between the content and border.

```text
+----------------------+
|       padding        |
|    +-----------+     |
|    |  content  |     |
|    +-----------+     |
+----------------------+
```

---

## 5. What is margin?

**Answer:**

Margin is the space **outside** an element.

```text
Element
   ↓
Outside space = margin
```

---

## 6. What is the CSS box model?

**Answer:**

The box model consists of:

```text
Content
Padding
Border
Margin
```

---

## 7. What is Flexbox?

**Answer:**

Flexbox is a CSS layout system mainly used to arrange elements in one direction.

```css
.container {
    display: flex;
}
```

It can arrange items:

```text
→ Row
↓ Column
```

Useful properties:

```css
justify-content
align-items
gap
flex-direction
```

---

## 8. What is Grid?

**Answer:**

CSS Grid is a layout system designed for rows and columns.

```css
.container {
    display: grid;
}
```

Example:

```text
+-----+-----+
|  1  |  2  |
+-----+-----+
|  3  |  4  |
+-----+-----+
```

---

## 9. Flexbox vs Grid

**Answer:**

```text
Flexbox → Mainly one-dimensional
Grid    → Two-dimensional
```

Flexbox is useful for:

```text
Navbar
Buttons
Small layouts
```

Grid is useful for:

```text
Cards
Page layouts
Rows + columns
```

---

## 10. What is responsive design?

**Answer:**

Responsive design means a webpage adjusts to different screen sizes.

Examples:

```text
Desktop
Tablet
Mobile
```

Common techniques:

* Flexible widths
* Media queries
* Flexbox
* Grid
* Responsive images
* `max-width`

---

## 11. What is a media query?

**Answer:**

A media query applies CSS depending on screen/device conditions.

Example:

```css
@media (max-width: 600px) {
    .container {
        width: 90%;
    }
}
```

---

# TASK 3 — ADVANCED QUESTIONS

## 12. Why is `display: flex` useful?

**Answer:**

It makes it easier to arrange elements and control:

* Direction
* Alignment
* Spacing
* Distribution

---

## 13. What is `max-width`?

**Answer:**

`max-width` prevents an element from becoming wider than a specified size.

Example:

```css
.container {
    width: 90%;
    max-width: 500px;
}
```

This is useful for responsive layouts.

---

# TASK 4 — HTTP FUNDAMENTALS

## 1. What is HTTP?

**Answer:**

HTTP means **HyperText Transfer Protocol**.

It is used for communication between clients and servers.

---

## 2. What is an HTTP request?

**Answer:**

A request is a message sent by the client to the server.

Example:

```text
GET /login HTTP/1.1
Host: example.com
```

---

## 3. What is an HTTP response?

**Answer:**

A response is the message sent by the server back to the client.

Example:

```text
HTTP/1.1 200 OK
Content-Type: text/html
```

---

## 4. What are HTTP methods?

**Answer:**

Common methods are:

| Method  | Purpose                             |
| ------- | ----------------------------------- |
| GET     | Read data                           |
| POST    | Create/submit data                  |
| PUT     | Replace data                        |
| PATCH   | Partially update data               |
| DELETE  | Delete data                         |
| HEAD    | Get headers only                    |
| OPTIONS | Ask about supported methods/options |

---

## 5. GET vs POST?

**Answer:**

GET is commonly used to retrieve data.

POST is commonly used to submit data or create/change server-side state.

---

## 6. What are HTTP status codes?

**Answer:**

Status codes tell the client what happened to the request.

```text
1xx → Informational
2xx → Success
3xx → Redirection
4xx → Client/request problem
5xx → Server problem
```

---

## 7. What does 200 mean?

**Answer:**

The request was successful.

---

## 8. What does 201 mean?

**Answer:**

A resource was successfully created.

Example:

```text
POST /users
→ 201 Created
```

---

## 9. What does 400 mean?

**Answer:**

The request is invalid or malformed.

---

## 10. What does 401 mean?

**Answer:**

The request requires authentication or authentication was not successfully provided.

Simple memory:

> **401 = Who are you?**

---

## 11. What does 403 mean?

**Answer:**

The server understood the request but refuses access.

Simple memory:

> **403 = I know who you are, but you cannot do this.**

---

## 12. What does 404 mean?

**Answer:**

The requested resource was not found.

---

## 13. What does 500 mean?

**Answer:**

The server encountered an internal error.

---

## 14. What are HTTP headers?

**Answer:**

Headers provide additional information about a request or response.

Examples:

```text
Content-Type
Authorization
Cookie
Set-Cookie
Cache-Control
Location
Host
```

---

## 15. What is HTTPS?

**Answer:**

HTTPS is HTTP protected using TLS.

It helps protect:

```text
Confidentiality
Integrity
Authentication of the server
```

---

# TASK 4 — ADVANCED QUESTIONS

## 16. What is the difference between authentication and authorization?

**Answer:**

```text
Authentication → Who are you?
Authorization  → What are you allowed to do?
```

Example:

```text
Login
 ↓
Authentication
 ↓
User identified
 ↓
Authorization
 ↓
Can user access admin page?
```

---

## 17. What is a request body?

**Answer:**

The request body contains data sent to the server.

Example:

```http
POST /login
Content-Type: application/json

{
    "username": "admin",
    "password": "example"
}
```

---

# TASK 5 — BACKEND FUNDAMENTALS

# API

## 1. What is an API?

**Answer:**

An API allows different parts of software to communicate.

Example:

```text
Frontend
   ↓
API
   ↓
Backend
   ↓
Database
```

---

## 2. What is REST API?

**Answer:**

REST is an architectural style commonly used for web APIs.

Example:

```text
GET    /users
POST   /users
GET    /users/10
PATCH  /users/10
DELETE /users/10
```

---

## 3. What is JSON?

**Answer:**

JSON is a common data format used between applications.

Example:

```json
{
    "username": "admin",
    "role": "user"
}
```

---

# DATABASES

## 4. What is a database?

**Answer:**

A database stores and manages application data.

---

## 5. What is SQL?

**Answer:**

SQL means **Structured Query Language**.

It is commonly used to work with relational databases.

Example:

```sql
SELECT * FROM users;
```

---

## 6. What is NoSQL?

**Answer:**

NoSQL databases use data models other than traditional relational tables.

MongoDB is a common example.

---

## 7. What is CRUD?

**Answer:**

CRUD means:

```text
C → Create
R → Read
U → Update
D → Delete
```

---

# AUTHENTICATION

## 8. What is authentication?

**Answer:**

Authentication verifies the identity of a user.

Examples:

* Password
* OTP
* MFA
* Biometrics

---

## 9. How should passwords be stored?

**Answer:**

Passwords should normally be stored using a password-hashing algorithm such as:

* Argon2id
* bcrypt
* scrypt

They should **not** be stored as plain text.

---

## 10. What is password hashing?

**Answer:**

Hashing converts a password into a one-way representation.

Example:

```text
Password
   ↓
Password hashing
   ↓
Hash
   ↓
Database
```

During login:

```text
Entered password
   ↓
Password verification
   ↓
Stored hash
```

---

## 11. Hashing vs encryption?

**Answer:**

```text
Hashing    → One-way, mainly verification
Encryption → Reversible with a key
```

Passwords are normally hashed.

Sensitive data that must later be recovered may need encryption.

---

# SESSION MANAGEMENT

## 12. What is a session?

**Answer:**

A session allows the server to remember an authenticated user across multiple requests.

Basic flow:

```text
Login
 ↓
Server verifies user
 ↓
Session created
 ↓
Session identifier sent to browser
 ↓
Browser sends it with later requests
 ↓
Server identifies user
```

---

## 13. What is a cookie?

**Answer:**

A cookie is small data stored by the browser and sent with matching requests.

A session identifier is commonly stored in a cookie.

---

## 14. What is `HttpOnly`?

**Answer:**

`HttpOnly` prevents normal JavaScript from reading the cookie.

This can reduce the impact of some cookie theft through XSS.

---

## 15. What is `Secure`?

**Answer:**

`Secure` tells the browser to send the cookie only over HTTPS connections.

---

## 16. What is `SameSite`?

**Answer:**

`SameSite` controls when cookies are sent in cross-site contexts.

It can help reduce certain cross-site request attacks.

---

# TASK 5 — ADVANCED BACKEND QUESTIONS

## 17. What is middleware?

**Answer:**

Middleware is code that runs between the incoming request and the final application handler.

It can perform:

* Authentication
* Logging
* Request processing
* Security checks
* Error handling

Example:

```text
Request
 ↓
Middleware
 ↓
Authentication
 ↓
Route
 ↓
Response
```

---

## 18. What is business logic?

**Answer:**

Business logic contains the rules of the application.

Example:

```text
User requests withdrawal
 ↓
Check balance
 ↓
Check withdrawal limit
 ↓
Approve or reject
```

---

## 19. Why should authorization be checked on the backend?

**Answer:**

Because the frontend can be modified or bypassed by an attacker.

For example, hiding an Admin button does not prevent someone from directly sending an admin request.

The server must enforce authorization.

---

# TASK 6 — SECURE DEVELOPMENT PRINCIPLES

# INPUT VALIDATION

## 1. What is input validation?

**Answer:**

Input validation checks whether received data is acceptable before using it.

Examples:

```text
Age → number
Email → valid format
Username → allowed characters
Password → minimum length
```

---

## 2. Why is input validation important?

**Answer:**

It helps prevent unexpected and malicious input from reaching application logic.

It can reduce risks such as:

* Injection
* Invalid data
* Application errors
* Abuse

---

## 3. Is frontend validation enough?

**Answer:**

No.

Frontend validation improves user experience, but attackers can bypass it.

Backend validation is mandatory.

---

# OUTPUT HANDLING

## 4. What is output encoding?

**Answer:**

Output encoding converts data into a safe representation for the context where it is displayed.

It helps prevent untrusted data from being interpreted as code.

---

## 5. What is XSS?

**Answer:**

XSS means **Cross-Site Scripting**.

It occurs when untrusted data is incorrectly treated as executable HTML/JavaScript.

Example dangerous pattern:

```javascript
element.innerHTML = userInput;
```

For plain text, a safer approach is often:

```javascript
element.textContent = userInput;
```

---

# AUTHENTICATION AWARENESS

## 6. How can authentication be made safer?

**Answer:**

Use:

* Strong password hashing
* HTTPS
* MFA
* Rate limiting
* Secure password reset
* Secure sessions
* Generic login errors
* Session expiration

---

# AUTHORIZATION AWARENESS

## 7. What is authorization?

**Answer:**

Authorization determines what an authenticated user is allowed to do.

Example:

```text
User → View own profile
Admin → Manage users
```

---

## 8. What is least privilege?

**Answer:**

Least privilege means giving a user, process, or service only the permissions it actually needs.

Example:

```text
Normal user
→ Read own data

Admin
→ Manage users
```

---

# SECURE CODING MINDSET

## 9. What does "never trust user input" mean?

**Answer:**

Any data coming from outside the trusted application boundary should be treated as untrusted until properly validated and handled.

Input can come from:

* Forms
* URLs
* APIs
* Cookies
* Headers
* Uploaded files
* JSON
* Query parameters

---

# TASK 6 — ADVANCED REVIEW QUESTIONS

## 10. What is defense in depth?

**Answer:**

Defense in depth means using multiple security controls instead of depending on one control.

Example:

```text
Input validation
      +
Authentication
      +
Authorization
      +
Parameterized queries
      +
Output encoding
      +
Logging
      +
Monitoring
```

If one control fails, other controls can still provide protection.

---

## 11. What does fail securely mean?

**Answer:**

When something goes wrong, the application should fail in a way that does not accidentally grant access or expose sensitive information.

Example:

Bad:

```text
Database error:
SELECT * FROM users WHERE password...
```

Better:

```text
Something went wrong. Please try again.
```

---

# TASK 7 — COMMON WEB SECURITY RISKS

# INJECTION

## 1. What is injection?

**Answer:**

Injection occurs when untrusted input is interpreted as part of a command or query.

Examples:

* SQL injection
* Command injection
* LDAP injection
* Some forms of XSS

---

## 2. What is SQL injection?

**Answer:**

SQL injection occurs when user input is incorrectly included in an SQL query.

Unsafe idea:

```python
query = "SELECT * FROM users WHERE username='" + username + "'"
```

The input can change the meaning of the query.

---

## 3. How do we prevent SQL injection?

**Answer:**

Use parameterized queries/prepared statements.

Concept:

```text
User input
   ↓
Parameter
   ↓
SQL query
```

The database treats the input as data rather than SQL code.

---

## 4. What is command injection?

**Answer:**

Command injection occurs when attacker-controlled input becomes part of an operating system command.

Safer development includes:

* Avoiding unnecessary shell execution
* Using argument lists
* Validating input
* Least privilege

---

# BROKEN AUTHENTICATION

## 5. What is broken authentication?

**Answer:**

It means weaknesses in authentication allow attackers to bypass or abuse the login/account system.

Examples:

* Weak passwords
* No rate limiting
* Poor password reset
* Session problems
* Authentication bypass
* Poor MFA implementation

---

## 6. What is session fixation?

**Answer:**

Session fixation is an attack where an attacker causes a victim to use a session identifier known or controlled by the attacker, and the application fails to replace it after authentication.

A common defense is to regenerate the session identifier after login or privilege changes.

---

# SENSITIVE DATA EXPOSURE / CRYPTOGRAPHIC FAILURES

## 7. What is sensitive data?

**Answer:**

Sensitive data is information that should be protected from unauthorized access.

Examples:

* Passwords
* API keys
* Session tokens
* Personal information
* Financial information
* Private keys

---

## 8. Where should secrets NOT be stored?

**Answer:**

Avoid putting secrets in:

```text
Source code
Git repositories
Frontend JavaScript
URLs
Logs
Public configuration
```

Use appropriate secret-management mechanisms.

---

# SECURITY MISCONFIGURATION

## 9. What is security misconfiguration?

**Answer:**

It occurs when systems or applications are configured insecurely.

Examples:

* Default passwords
* Debug mode in production
* Unnecessary services
* Weak permissions
* Public sensitive files
* Detailed error messages
* Incorrect CORS settings
* Missing security headers

---

# OWASP

## 10. What is OWASP?

**Answer:**

OWASP stands for **Open Worldwide Application Security Project**.

It provides security guidance, tools, standards, projects, and educational resources for application security.

---

## 11. What is OWASP Top 10?

**Answer:**

OWASP Top 10 is a widely used awareness document covering important categories of web application security risks.

Examples include:

* Broken Access Control
* Cryptographic Failures
* Injection
* Insecure Design
* Security Misconfiguration
* Vulnerable/Outdated Components
* Identification and Authentication Failures
* Software/Data Integrity Failures
* Security Logging and Monitoring Failures
* SSRF

---

## 12. How does OWASP help developers?

**Answer:**

OWASP can be used as a security checklist.

Example:

```text
Build application
      ↓
Check OWASP risks
      ↓
Find weaknesses
      ↓
Fix weaknesses
      ↓
Test again
```

---

# TASK 7 — ADVANCED SECURITY QUESTIONS

## 13. What is the difference between vulnerability, threat and risk?

**Answer:**

```text
Vulnerability → Weakness
Threat         → Something that can exploit a weakness
Risk           → Potential impact/probability of harm
```

Example:

```text
Weak password
    ↓
Vulnerability

Attacker attempting login
    ↓
Threat

Account compromise
    ↓
Risk
```

---

## 14. What is attack surface?

**Answer:**

Attack surface is the collection of possible entry points an attacker could interact with.

Examples:

* Login
* APIs
* File uploads
* Admin panels
* Network services
* User inputs

Reducing unnecessary entry points can reduce attack surface.

---

# TASK 8 — SECURITY LOGGING & MONITORING

## 1. What is logging?

**Answer:**

Logging means recording events that happen in an application or system.

Example:

```text
2026-10-07 LOGIN_FAILED user=admin
```

---

## 2. Why is logging important?

**Answer:**

Logging helps with:

* Debugging
* Troubleshooting
* Security investigations
* Detecting suspicious activity
* Auditing
* Incident response

---

## 3. What is an application log?

**Answer:**

An application log records events generated by an application.

Examples:

```text
Application started
User logged in
Database error
Payment failed
File uploaded
```

---

## 4. What is an access log?

**Answer:**

An access log records requests made to a web server/application.

Example:

```text
IP
Method
URL
Status
Timestamp
```

---

## 5. What is an error log?

**Answer:**

An error log records application or system failures.

Example:

```text
Database connection failed
File not found
Internal application error
```

---

## 6. What is an audit trail?

**Answer:**

An audit trail records important actions so that we can determine:

```text
Who did what?
When?
To which resource?
```

Example:

```text
Admin
Changed user role
10:30 AM
```

---

## 7. What is security monitoring?

**Answer:**

Security monitoring means continuously observing logs and system activity to identify suspicious behavior.

---

## 8. Logging vs monitoring?

**Answer:**

```text
Logging   → Record events
Monitoring → Watch/analyze events
```

---

## 9. What should we log?

**Answer:**

Useful security events include:

* Login success/failure
* Logout
* Password changes
* Password reset
* MFA failures
* Authorization failures
* Role changes
* Admin actions
* Sensitive resource access
* Configuration changes
* Important errors

---

## 10. What should we not log?

**Answer:**

Avoid logging:

* Passwords
* Session tokens
* API keys
* Private keys
* Authentication secrets
* Unnecessary sensitive personal information

---

# LOG ANALYSIS PROJECT

## 11. How can Python analyze logs?

**Answer:**

Python can:

1. Open the log file.
2. Read each line.
3. Find important events.
4. Extract values.
5. Count events.
6. Detect suspicious activity.
7. Generate a report.

Example:

```text
Log file
   ↓
Python
   ↓
Find LOGIN_FAILED
   ↓
Count IP addresses
   ↓
Detect repeated failures
   ↓
Alert
```

---

## 12. How can repeated failed logins be detected?

**Answer:**

We can count failed login attempts for each IP address.

Example:

```text
192.168.1.20 → 3 failures
```

If the defined threshold is reached, the system can mark it as suspicious.

---

# TASK 8 — ADVANCED QUESTIONS

## 13. What is security visibility?

**Answer:**

Security visibility means having enough information to understand what is happening in an application, system, or network.

Simple flow:

```text
Event
 ↓
Log
 ↓
Collect
 ↓
Monitor
 ↓
Detect
 ↓
Alert
 ↓
Investigate
 ↓
Respond
```

---

## 14. Why are logs important during an incident?

**Answer:**

Logs can help determine:

* What happened
* When it happened
* Which account was involved
* Which resource was accessed
* What actions occurred
* What systems were affected

---

# TASK 9 — AI-ASSISTED SECURE DEVELOPMENT

## 1. How can AI help developers?

**Answer:**

AI can help with:

* Code review
* Security review
* Debugging
* Architecture discussions
* Secure coding suggestions
* Documentation
* Test-case generation
* Explaining code

---

## 2. Can AI replace a security professional?

**Answer:**

No.

AI is an assistant.

Security recommendations and generated code must be reviewed, verified, and tested.

---

## 3. How can AI help with code review?

**Answer:**

We can provide code to an AI system and ask it to identify:

* Bugs
* Security weaknesses
* Poor practices
* Error-handling problems
* Authentication issues
* Injection risks

Then the developer reviews the suggestions.

---

## 4. How can AI help with security reviews?

**Answer:**

AI can help identify possible:

* Injection
* Authentication problems
* Authorization problems
* Session weaknesses
* Sensitive data exposure
* Hard-coded secrets
* Input validation issues

---

## 5. How can AI help with architecture?

**Answer:**

AI can help discuss architecture such as:

```text
Frontend
   ↓
API
   ↓
Backend
   ↓
Database
```

We can ask questions about:

* Authentication
* Authorization
* API security
* Database security
* Session management
* Logging
* Rate limiting
* Network separation

---

## 6. What is AI hallucination?

**Answer:**

An AI hallucination is when AI generates information that sounds correct but is actually incorrect, invented, or unsupported.

Examples:

* Fake functions
* Incorrect configuration
* Non-existent libraries
* Wrong security recommendations
* Outdated practices

---

## 7. How should we validate AI-generated security advice?

**Answer:**

Use:

```text
AI suggestion
 ↓
Understand it
 ↓
Review it
 ↓
Check trusted documentation
 ↓
Implement carefully
 ↓
Test
 ↓
Security validation
```

---

## 8. Should we give passwords or API keys to AI?

**Answer:**

We should not casually share secrets with AI.

Avoid sharing:

* Passwords
* API keys
* Private keys
* Session tokens
* Database credentials
* Confidential information

Use placeholders:

```text
API_KEY = "<REDACTED>"
```

when discussing examples.

---

# TASK 9 — ADVANCED AI QUESTIONS

## 9. What is AI-assisted development?

**Answer:**

AI-assisted development means using AI as a tool to help developers design, write, review, debug, and improve software.

The developer remains responsible for understanding and validating the result.

---

## 10. What is the biggest danger of blindly using AI-generated code?

**Answer:**

The code may contain:

* Security vulnerabilities
* Incorrect assumptions
* Bugs
* Outdated methods
* Poor error handling
* Hard-coded secrets

Therefore:

> Never blindly copy AI-generated security-sensitive code into production.

---

# TASK 10 — HANDS-ON PROJECTS

## Project 1 — Simple Web Application

### 1. What did you build?

**Answer:**

I built a simple Flask web application that accepts a user's name through a form and returns a response.

---

## 2. What is Flask?

**Answer:**

Flask is a lightweight Python web framework used to build web applications and APIs.

---

## 3. What is a route?

**Answer:**

A route connects a URL/path to a Python function.

Example:

```python
@app.route("/")
def home():
    return "Hello"
```

The `/` route calls the `home()` function.

---

## 4. What is `request.form`?

**Answer:**

It is used to access form data submitted by the client.

Example:

```python
name = request.form["name"]
```

---

## 5. What is `render_template()`?

**Answer:**

It is used in Flask to render an HTML template.

Example:

```python
return render_template("index.html")
```

---

## 6. What is `url_for()`?

**Answer:**

`url_for()` generates URLs for Flask routes or static files.

Example:

```html
<link rel="stylesheet"
      href="{{ url_for('static', filename='style.css') }}">
```

---

# PROJECT 2 — AUTHENTICATION WORKFLOW

## 1. What happens during registration?

**Answer:**

A simple workflow is:

```text
User enters username/password
        ↓
Server receives input
        ↓
Validate input
        ↓
Check existing user
        ↓
Hash password
        ↓
Store user information
        ↓
Registration complete
```

---

## 2. What happens during login?

**Answer:**

```text
User enters credentials
        ↓
Server receives credentials
        ↓
Find user
        ↓
Verify password hash
        ↓
Authentication successful
        ↓
Create session
        ↓
User accesses protected page
```

---

## 3. What happens during logout?

**Answer:**

```text
Logout request
 ↓
Session invalidated
 ↓
Session cookie cleared/expired
 ↓
User returns to login/home
```

---

## 4. How should a real application store passwords?

**Answer:**

Passwords should be stored using a suitable password-hashing algorithm such as Argon2id, bcrypt, or scrypt, with appropriate configuration.

The application should verify passwords using the password-hash verification mechanism.

---

## 5. What is a protected route?

**Answer:**

A protected route is a route that requires the user to be authenticated or authorized.

Example:

```text
/dashboard
```

If the user has no valid session:

```text
→ Redirect to login
```

---

# PROJECT 3 — LOG ANALYZER

## 1. What did you build?

**Answer:**

I created a simple Python log analyzer that reads security logs, finds failed login attempts, counts attempts by IP address, and identifies suspicious repeated failures.

---

## 2. Why use `Counter`?

**Answer:**

`Counter` makes it easy to count how many times each value appears.

Example:

```text
IP1 → 1
IP2 → 3
IP3 → 2
```

---

## 3. What is the security purpose?

**Answer:**

It can help identify suspicious authentication activity such as repeated failed login attempts.

---

# PROJECT 4 — SECURITY WEAKNESS IDENTIFICATION

## 1. How do you review a web application for security weaknesses?

**Answer:**

I would review areas such as:

```text
Input validation
Authentication
Authorization
Session management
Injection
XSS
Sensitive data
Error handling
Secrets
Configuration
Logging
Dependencies
```

---

## 2. What is a security vulnerability?

**Answer:**

A vulnerability is a weakness that could potentially be exploited to cause harm or gain unauthorized access.

---

## 3. How would you fix SQL injection?

**Answer:**

I would use parameterized queries or prepared statements instead of building SQL queries through string concatenation.

---

## 4. How would you protect against XSS?

**Answer:**

I would:

* Safely handle untrusted output
* Use context-appropriate encoding
* Avoid unsafe HTML injection
* Use safer DOM APIs for plain text
* Apply an appropriate Content Security Policy as an additional layer

---

# PROJECT 5 — SECURITY REPORT

## 1. What should a security report contain?

**Answer:**

A basic security report can contain:

```text
Project information
Scope
Finding
Description
Risk
Severity
Evidence
Recommendation
Fix
Retest result
```

---

## 2. What is severity?

**Answer:**

Severity describes how serious a vulnerability is.

A simple classification can be:

```text
Critical
High
Medium
Low
Informational
```

Severity should be based on factors such as impact and exploitability.

---

## 3. What is remediation?

**Answer:**

Remediation means fixing or reducing the security weakness.

Example:

```text
Finding:
SQL Injection

Remediation:
Use parameterized queries.
```

---

# COMMON INTERVIEW QUESTIONS — ALL TASKS

## 1. Explain a web application from beginning to end.

**Answer:**

A user opens a browser and requests a website.

```text
Browser
 ↓
DNS
 ↓
Server
 ↓
Frontend
 ↓
API
 ↓
Backend
 ↓
Database
```

The backend processes the request and returns a response. The browser then displays the result.

---

## 2. Explain login from a security perspective.

**Answer:**

```text
User enters credentials
 ↓
HTTPS request
 ↓
Server validates input
 ↓
Find user
 ↓
Verify password hash
 ↓
Authentication successful
 ↓
Create secure session
 ↓
Authorization checks access
 ↓
User accesses protected resources
```

Important protections include:

* HTTPS
* Password hashing
* Rate limiting
* Secure session cookies
* Authorization
* Secure logout

---

## 3. Authentication vs authorization?

**Answer:**

> Authentication tells us **who the user is**. Authorization tells us **what the user is allowed to do**.

---

## 4. What is the most important security principle you learned?

**Answer:**

> Never trust untrusted input, and always enforce security controls on the server.

---

## 5. Why is backend validation important?

**Answer:**

Because attackers can bypass frontend controls by directly sending requests to the server.

Therefore, security validation must happen on the backend.

---

## 6. Why is HTTPS important?

**Answer:**

HTTPS protects data while it travels between the client and server using TLS.

It helps protect against:

* Eavesdropping
* Tampering
* Certain man-in-the-middle attacks

---

## 7. Why should passwords not be stored in plain text?

**Answer:**

If the database is compromised, plain-text passwords are immediately exposed.

Password hashing provides a safer way to store passwords so the original password is not directly stored.

---

## 8. Why should we not hard-code API keys?

**Answer:**

Because source code may be exposed through:

* Git repositories
* Logs
* Backups
* Screenshots
* Shared files

Secrets should be stored using appropriate secret-management mechanisms.

---

## 9. Why is authorization important?

**Answer:**

Authentication only proves identity.

Authorization prevents authenticated users from accessing resources or performing actions they are not permitted to use.

---

## 10. Why are logs important?

**Answer:**

Logs provide visibility into application and security events.

They help with:

```text
Detection
Investigation
Debugging
Auditing
Incident response
```

---

# SCENARIO-BASED REVIEW QUESTIONS

## Scenario 1

**Reviewer:** A user changes the URL from:

```text
/user/10
```

to:

```text
/user/11
```

and can see another user's information. What is the problem?

**Answer:**

This is an authorization/access-control problem.

The application is not properly checking whether the current user is allowed to access user 11's data.

---

## Scenario 2

**Reviewer:** The login page has frontend validation, but an attacker sends requests directly using a tool. What should happen?

**Answer:**

The backend should validate the input again.

Frontend validation cannot be treated as a security boundary.

---

## Scenario 3

**Reviewer:** Passwords are stored like this:

```text
admin,password123
```

What is wrong?

**Answer:**

The password is stored in plain text.

A real application should use secure password hashing such as Argon2id, bcrypt, or scrypt.

---

## Scenario 4

**Reviewer:** A website displays this user input directly using unsafe HTML insertion. What could happen?

**Answer:**

It could create an XSS vulnerability if the untrusted input is interpreted as HTML or script.

The application should safely handle the output according to its context.

---

## Scenario 5

**Reviewer:** An application returns a database error containing SQL details to the user. What is the problem?

**Answer:**

It may expose sensitive technical information.

The user should receive a safe error message while detailed information is kept in protected server-side logs.

---

## Scenario 6

**Reviewer:** The application allows unlimited login attempts. What risk exists?

**Answer:**

An attacker may perform password guessing or credential-stuffing attacks.

Possible protections include:

* Rate limiting
* Account protections
* MFA
* Monitoring
* Alerting

---

## Scenario 7

**Reviewer:** A developer says, "The Admin button is hidden, so users cannot access the admin page."

**Answer:**

That is not sufficient security.

An attacker can directly send a request to the admin endpoint.

Authorization must be enforced on the server.

---

# IMPORTANT SECURITY DIFFERENCES

| Concept        | Meaning                                            |
| -------------- | -------------------------------------------------- |
| Authentication | Who are you?                                       |
| Authorization  | What can you do?                                   |
| Validation     | Is the input acceptable?                           |
| Encoding       | How should data be safely represented?             |
| Hashing        | One-way transformation                             |
| Encryption     | Reversible protection using keys                   |
| Logging        | Record events                                      |
| Monitoring     | Observe/analyze events                             |
| Session        | Server-side state/identity context across requests |
| Cookie         | Browser-stored data sent with requests             |
| API            | Interface for software communication               |
| Database       | Stores application data                            |
| Vulnerability  | Security weakness                                  |
| Threat         | Potential source of attack/harm                    |
| Risk           | Potential impact/likelihood                        |
| OWASP          | Application security guidance/resources            |

---

# IMPORTANT SECURITY CHECKLIST

When reviewing a web application, ask:

### Input

```text
[ ] Is input validated?
[ ] Are types checked?
[ ] Are length/range limits applied?
[ ] Is untrusted input handled safely?
```

### Authentication

```text
[ ] Are passwords securely hashed?
[ ] Is HTTPS used?
[ ] Is MFA considered?
[ ] Is brute-force protection implemented?
[ ] Is password reset secure?
```

### Authorization

```text
[ ] Are permissions checked server-side?
[ ] Can users access other users' data?
[ ] Are admin functions protected?
[ ] Is least privilege applied?
```

### Sessions

```text
[ ] Are session IDs unpredictable?
[ ] Is Secure used?
[ ] Is HttpOnly used where appropriate?
[ ] Is SameSite configured appropriately?
[ ] Are sessions invalidated on logout?
[ ] Are sessions regenerated after authentication/privilege changes?
```

### Data

```text
[ ] Are passwords protected?
[ ] Are sensitive data fields protected?
[ ] Are secrets outside source code?
[ ] Is unnecessary sensitive data avoided?
```

### Injection

```text
[ ] Parameterized SQL queries?
[ ] Safe command execution?
[ ] Safe output handling?
[ ] Appropriate input validation?
```

### Configuration

```text
[ ] No default passwords?
[ ] Debug disabled in production?
[ ] Unnecessary services disabled?
[ ] Correct permissions?
[ ] Secure error handling?
[ ] Dependencies maintained?
```

### Logging

```text
[ ] Login failures logged?
[ ] Authorization failures logged?
[ ] Important admin actions logged?
[ ] Sensitive secrets excluded?
[ ] Logs protected?
[ ] Monitoring/alerting available?
```

---

# BASE → INTERMEDIATE → ADVANCED LEARNING PATH

## Level 1 — Base

Understand:

```text
HTML
CSS
HTTP
Frontend
Backend
Database
API
Authentication
Authorization
```

---

## Level 2 — Intermediate

Learn:

```text
REST APIs
CRUD
Sessions
Cookies
Password hashing
Input validation
Output encoding
SQL injection
XSS
Logging
OWASP
```

---

## Level 3 — Advanced

Learn:

```text
Access control
Session security
Secure architecture
Threat modeling
Security headers
Rate limiting
Secure API design
Dependency security
Secrets management
Security monitoring
Incident response
Security testing
```

---

# INTERVIEW ANSWER FORMULA

When a reviewer asks a technical question:

### Step 1 — Define it

> "Authentication is the process of verifying a user's identity."

### Step 2 — Explain how it works

> "The user provides credentials, the server verifies them, and a session can be created after successful authentication."

### Step 3 — Give an example

> "For example, a username and password login."

### Step 4 — Add security

> "The password should be securely hashed, communication should use HTTPS, and the session should be protected."

This makes the answer sound much stronger than giving only a definition.

---

# 20 VERY IMPORTANT QUESTIONS TO PREPARE

### 1. What is a website?

A collection of web resources accessed through a browser.

### 2. How does a website work?

Browser → DNS → Server → Application → Database → Response → Browser.

### 3. What is frontend?

The user-facing part of an application.

### 4. What is backend?

The server-side logic and processing.

### 5. What is an API?

An interface that allows software components to communicate.

### 6. What is HTTP?

A protocol used for communication between clients and servers.

### 7. What is HTTPS?

HTTP protected using TLS.

### 8. What is authentication?

Verifying identity.

### 9. What is authorization?

Checking permissions.

### 10. What is a session?

A mechanism that allows the application to maintain authenticated state across requests.

### 11. What is input validation?

Checking whether received input is acceptable.

### 12. What is SQL injection?

Injecting unintended SQL through unsafe query construction.

### 13. What is XSS?

Causing untrusted data to be interpreted as executable web content.

### 14. What is OWASP?

An organization/project providing application security resources, guidance, and tools.

### 15. What is logging?

Recording application/system events.

### 16. What is monitoring?

Observing and analyzing events for problems or suspicious behavior.

### 17. Why hash passwords?

To avoid storing passwords directly.

### 18. Why use parameterized queries?

To keep user input separate from SQL instructions.

### 19. Why is authorization checked on the server?

Because client-side controls can be bypassed.

### 20. Can AI guarantee secure code?

No. AI can assist, but generated code must be reviewed, verified, and tested.

---

# FINAL SECURITY MINDSET

Remember this complete flow:

```text
BUILD
  ↓
VALIDATE INPUT
  ↓
AUTHENTICATE USERS
  ↓
AUTHORIZE ACTIONS
  ↓
PROTECT DATA
  ↓
HANDLE OUTPUT SAFELY
  ↓
SECURE SESSIONS
  ↓
PREVENT INJECTION
  ↓
CONFIGURE SYSTEM SECURELY
  ↓
LOG IMPORTANT EVENTS
  ↓
MONITOR ACTIVITY
  ↓
TEST SECURITY
  ↓
FIX WEAKNESSES
  ↓
REPORT FINDINGS
```

## Most important rules to remember

1. **Never trust user input.**
2. **Validate on the server.**
3. **Use parameterized queries.**
4. **Store passwords using secure password hashing.**
5. **Use HTTPS.**
6. **Authentication is not authorization.**
7. **Authorization must be enforced server-side.**
8. **Protect session cookies.**
9. **Do not expose secrets.**
10. **Do not expose sensitive information in errors.**
11. **Log important security events.**
12. **Do not log passwords or secrets.**
13. **Use least privilege.**
14. **Keep dependencies updated.**
15. **Use OWASP guidance.**
16. **Test security after making changes.**
17. **AI can assist but must not be blindly trusted.**
18. **Security is a continuous process, not a one-time task.**

# ONE-LINE REVISION

```text
Web → HTML → CSS → HTTP → API → Backend → Database
     → Authentication → Authorization → Sessions
     → Validation → Output Security → Injection Prevention
     → OWASP → Logging → Monitoring → AI Assistance
     → Testing → Reporting
```

# FINAL INTERVIEW STATEMENT

> "I understand the basic web application architecture from frontend to backend and database. I understand HTTP, APIs, authentication, authorization, sessions, input validation, output handling, common web vulnerabilities such as SQL injection and XSS, OWASP security concepts, logging and monitoring, and AI-assisted secure development. I also understand that security controls must be implemented and enforced on the server, tested properly, and continuously reviewed."
