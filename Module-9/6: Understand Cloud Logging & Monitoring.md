# Module 6: Understand Cloud Logging & Monitoring ☁️🔍

Cloud logging and monitoring help organizations understand what is happening inside their cloud systems, identify suspicious activities, and investigate security incidents.

Imagine your cloud account is a large office building:

- Logging is the record book that stores what happened.
- Monitoring is the security guard watching what is happening.
- Alerts are warnings when something unusual occurs.
- Incident investigation is examining the records to understand what went wrong.

## 1. Audit Logs

Definition: Audit logs are records of activities performed by users, applications, and services in a cloud environment.

They help answer questions such as:

- Who performed an action?
- What action was performed?
- When did it happen?
- Which resource was affected?
- Was the action successful or denied?

### Example

A cloud administrator deletes a virtual machine at 10:30 AM.

An audit log might record:

| Field    | Example                |
| -------- | ---------------------- |
| User     | admin-user             |
| Action   | Delete virtual machine |
| Time     | 10:30 AM               |
| Resource | VM-01                  |
| Result   | Success                |

This record helps the security team determine who deleted the virtual machine and when.

### Why are audit logs important?

1. Track user and administrator actions.
2. Investigate unauthorized changes.
3. Support security audits and compliance.
4. Help identify suspicious activity.
5. Provide evidence during incident investigations.

### Common cloud audit-log services

- AWS CloudTrail
- Microsoft Azure Activity Log
- Google Cloud Audit Logs

Exam point: Audit logs provide a historical record of actions performed in a cloud environment.

## 2. Activity Monitoring

Definition: Activity monitoring is the continuous or periodic observation of cloud resources, user actions, network activity, and system performance.

Audit logs tell us what actions were recorded. Activity monitoring helps us observe patterns and detect unusual behavior.

[Hybrid cloud security must be rebuilt for an AI war it was never designed to fight | VentureBeat](https://images.openai.com/static-rsc-4/N2Enw9WJiaGvUlePJYjIu6x7bNtTGhTtGHTwrt9c936J7ZqMuyYqmfrxPLMjNDWqSsURCnHmjpMbMBESiGR6KDod8DGYX0GkkQCfr36pLrPP4Ng-2WSfkNIzQSjDfKL2qZ6oU03hibvoFb80W1NQLAq9nryJOn9-sf1AUCRkFBY?purpose=inline)

[venturebeat.com](https://venturebeat.com/security/hybrid-cloud-security-reinvented-ai-era?utm_source=chatgpt.com)

### What can be monitored?

- Login attempts and account activity
- CPU, memory, and storage usage
- Network traffic
- Application performance
- Changes to cloud resources
- Unusual downloads or data transfers

### Example

A user normally logs in from India during daytime. Suddenly, the account has multiple failed login attempts followed by a successful login from an unfamiliar location.

The monitoring system may flag this activity for investigation.

### How activity monitoring works

1\. Collect activity data

Logins, network traffic, resource usage

2\. Analyze the activity

Compare activity with rules and normal patterns

3\. Detect unusual behavior

Identify suspicious logins or unexpected changes

4\. Alert the security team

Investigate and respond when needed

### Why is activity monitoring important?

- Detect threats earlier.
- Identify performance problems.
- Find unusual account behavior.
- Reduce the time needed to respond to incidents.

Exam point: Activity monitoring observes cloud activity to detect unusual behavior, security threats, and performance issues.

## 3. Security Visibility

Definition: Security visibility is the ability to see and understand the security status of cloud resources, users, applications, and networks.

In simple words, security visibility helps a security team know what is happening, where it is happening, and whether something is dangerous.

### Example

A company uses 50 virtual machines, several databases, and hundreds of employee accounts. If the security team cannot see which accounts are accessing sensitive data, it has poor security visibility.

When logs, alerts, and monitoring dashboards bring this information together, the team has better visibility.

### What improves security visibility?

1. Centralized logging from different cloud services.
2. Dashboards showing important security events.
3. Alerts for suspicious activity.
4. Monitoring user permissions and resource configurations.
5. Integration with security tools such as SIEM systems.

SIEM stands for Security Information and Event Management. It collects and analyzes security events from multiple sources to help identify possible threats.

### Why is security visibility important?

- Helps identify hidden security risks.
- Shows which resources may be affected by an attack.
- Helps security teams make informed decisions.
- Reduces blind spots in cloud security.

Exam point: Security visibility provides an overall view of cloud security activities, risks, and potential threats.

## 4. Event Tracking

Definition: Event tracking is the process of recording and following specific events that occur in a cloud environment.

An event is an occurrence or action, such as a user logging in, a file being deleted, a firewall rule changing, or a virtual machine starting.

### Examples of cloud events

| Event               | What it means                      |
| ------------------- | ---------------------------------- |
| Successful login    | A user signed in                   |
| Failed login        | A sign-in attempt was unsuccessful |
| Permission changed  | Access rights were modified        |
| File deleted        | A file was removed                 |
| Server started      | A virtual machine began running    |
| Large data transfer | A significant amount of data moved |

### How event tracking works

1. A cloud resource or user performs an action.
2. The cloud service records the event.
3. The event is sent to a logging or monitoring system.
4. Rules or analytics check whether it is suspicious.
5. An alert may be generated if the event meets a defined condition.

### Real-life scenario

An employee account suddenly downloads thousands of files from a cloud database.

The event-tracking system records the downloads, their timestamps, and the account involved. Monitoring rules may flag the unusual volume of activity so the security team can investigate.

Exam point: Event tracking records specific activities and helps establish a timeline of what happened in the cloud.

## 5. Incident Investigation

Definition: Incident investigation is the process of examining logs, alerts, and other evidence to determine what happened during a security incident, how it happened, and what was affected.

A security incident could involve a stolen account, unauthorized data access, malware, or the deletion of important resources.

### Example

A company receives an alert that an administrator account has accessed a sensitive database unexpectedly.

The security team investigates to determine whether the access was legitimate or part of an attack.

### Steps in incident investigation

1\. Identify the incident

Review alerts and identify the suspicious activity.

2\. Collect evidence

Examine audit logs, login records, network logs, and related events.

3\. Reconstruct the timeline

Determine which actions occurred first, which account was involved, and what resources were accessed.

4\. Contain the threat

When appropriate, disable compromised credentials, revoke sessions, or isolate affected resources.

5\. Recover and learn

Restore affected services, fix the root cause, and improve security controls.

### Why is incident investigation important?

- Identifies the cause of an attack.
- Determines which accounts and resources were affected.
- Helps limit further damage.
- Supports recovery and future prevention.
- Provides evidence for reporting and compliance.

Important: Logs should be protected against unauthorized modification and retained for an appropriate period. Accurate timestamps and synchronized clocks help investigators reconstruct events reliably.

Exam point: Incident investigation uses security evidence to understand, contain, and recover from security incidents.

## Quick comparison of all five topics

| Topic                  | Main purpose                             | Simple example                             |
| ---------------------- | ---------------------------------------- | ------------------------------------------ |
| Audit logs             | Record actions                           | Who deleted a server?                      |
| Activity monitoring    | Observe activity                         | Is an account behaving unusually?          |
| Security visibility    | Understand overall security status       | Which cloud resources have security risks? |
| Event tracking         | Follow specific events                   | When was a permission changed?             |
| Incident investigation | Find the cause and impact of an incident | How did an attacker access a database?     |

## How they work together

A cloud security team might use all five capabilities during one incident:

1. Event tracking: Records an unusual login.
2. Activity monitoring: Detects repeated logins and unusual downloads.
3. Audit logs: Show which resources the account accessed.
4. Security visibility: Helps identify other potentially affected resources.
5. Incident investigation: Reconstructs the incident, determines its impact, and guides the response.

These are connected capabilities, not necessarily separate tools or a fixed sequence.

## Important exam questions and answers

Q1. What is cloud logging?

Cloud logging is the process of collecting and storing records of activities, events, and errors in cloud systems.

Q2. What is cloud monitoring?

Cloud monitoring is the process of observing cloud resources and activities to identify performance problems, unusual behavior, and potential threats.

Q3. What is an audit log?

An audit log is a record of actions performed by users, applications, or services, including details such as the action, time, and affected resource.

Q4. What is security visibility?

Security visibility is the ability to see and understand the security status and activities of cloud resources and accounts.

Q5. What is the difference between event tracking and incident investigation?

Event tracking records and follows individual events. Incident investigation examines events and other evidence to determine the cause, timeline, and impact of a security incident.

Q6. What is SIEM?

SIEM stands for Security Information and Event Management. It collects and analyzes security events from different sources to help detect and investigate threats.

Q7. Scenario-based question: A cloud company detects a login from an unfamiliar location, followed by a large download of customer records. Explain how logging and monitoring help.

Answer:

- Activity monitoring detects unusual login and download behavior.
- Event tracking records the related events and timestamps.
- Audit logs identify the account and resources accessed.
- Security visibility helps assess the possible scope of the incident.
- Incident investigation determines whether the account was compromised and what data may have been exposed. The security team can then contain the threat and recover safely.

## Final revision notes

Remember these key distinctions:

- Logging: Records what happened.
- Monitoring: Watches for unusual activity.
- Visibility: Provides an overall view of security.
- Event tracking: Follows individual events.
- Investigation: Explains what happened, why it happened, and what was affected.

Cloud providers offer services to support these tasks, such as AWS CloudTrail and CloudWatch, Azure Activity Logs and Azure Monitor, and Google Cloud Audit Logs and Cloud Monitoring.

For your exam, learn each definition, one practical example, and at least two benefits. For longer answers, explain how all five capabilities work together to detect and investigate a cloud security incident.
