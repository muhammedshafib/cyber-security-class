# AWS Practical Lab 1: Explore the Cloud Environment

I'll guide you through the AWS website as if we are sitting in front of your Windows computer together. We'll cover which website to open, where each menu is located, what buttons to click, what information appears, and what you should write in your practical notebook.

For this first practical, we will inspect four AWS services:

1. IAM: users and permissions
2. S3: cloud storage
3. EC2: virtual machines and network security
4. CloudTrail: activity and audit logs

You do not need to create a server or upload data for this exercise. We'll start with read-only exploration.

## Step 1: Open the AWS website

[Launching a PBX on AWS](https://images.openai.com/static-rsc-4/va1GCdpqxTnASFpiVQ96i4DBueMl_m8DsgBa0RCiCGvYI-9PrQ0GvqwV3LcauuvcbKZj0RyJDXTcLDPIjUmv_96ZLlOIJr5jHUqNtcsOQ5dUMXRQx5IrbIAuoglFP_RT5rABRypcFaJRGBbv8NyJ4lYeTQXkbnR0kntiWvYu-Uw?purpose=inline)

1\. Open Google Chrome

Click the address bar at the top of Chrome.

[How to Set Up and Configure AWS: A Comprehensive Tutorial | DataCamp](https://images.openai.com/static-rsc-4/t5N4d8YtaPLrBalwFqafQdLhsykbJyqs5Y_Yo_0YceUquxNoTFyuO89bcpuBErV8ZYAcL3ApUs3NWdV0eSC1ZXrpxlO9_yiDl_bOAMKZvU565qFbqteuPH0P0qA4j4r-Xz7tu9doNE-qXSvNuynprqMbYHWQvF7tijtxPPUrXt4?purpose=inline)

2\. Visit the official AWS console

Open [https://console.aws.amazon.com/](https://console.aws.amazon.com/?utm_source=chatgpt.com).

This is the AWS Management Console, the website used to manage cloud resources.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS Identity and Access Management

+1



[A programmatic way to create an account in AWS Control Tower. | by Saket Deshpande | Globant | Medium](https://images.openai.com/static-rsc-4/MrtPSkNF5WnutZwye5GFK3dOZv2ufPls68UoaNzupvk2o8QeV4e48ZJTX-D21_peNn3FxZObC1bBXvlqKA3DelGi6V1MX5uCAK7zP58Zz0E9CMqOGVjRg7yrRNJmKM7iljKdHHkAdtsFQRHHLnUBk6R_1dxHzFfJXYNO8q-LZrY?purpose=inline)

3\. Sign in

Use your own AWS account or an account provided by your instructor. Follow the sign-in option appropriate for your account.

If you don't have an account yet, open the [AWS Free Tier page](https://aws.amazon.com/free/?utm_source=chatgpt.com) and review the current terms before registering.

Important: Never share your password, MFA code, secret access key, or other credentials with anyone.

## Step 2: Understand the AWS home page

Once signed in, you'll land on the AWS Console home page. Your layout may look slightly different depending on your account and console settings.

[EmoryAWS_StartGuide_Yang](https://images.openai.com/static-rsc-4/oc7O-EtbICJtKohmGVZiFwIEmE0ZIQcpw_AVul8naAbX-J74xlMqK9RlTF16yLLsEcBqh36JMJ1q5-4B6h2SeudyTQv4od1JOGKwULHo1CW7akJBfDPSjAaINQ6xSeVAcTzHmSPoCS7_sfI0i92OWfho_uylQz_-LxEK8CbSP6s?purpose=inline)

[yanglab-emory.github.io](https://yanglab-emory.github.io/assets/ComputationSlides/EmoryAWS_StartGuide_Yang.html?utm_source=chatgpt.com)

Here are the main areas to identify:

A. Search bar

Usually near the top. Search for services such as `IAM`, `S3`, `EC2`, or `CloudTrail`. This is the easiest way to navigate.

B. Region selector

Usually in the top navigation bar. It lets you select a geographical AWS Region, such as Mumbai (`ap-south-1`).

C. Account or identity menu

Usually at the top right. Use it to identify your current account or sign-in identity.

D. Services and recently visited

These help you open AWS services you've used before. Some panels may be absent or arranged differently.

### What is an AWS Region?

A Region is a geographical area where AWS operates cloud infrastructure.

For this lab, you can select Asia Pacific (Mumbai), `ap-south-1`, if it is available and suitable for your environment.

Remember:

- IAM is largely a global service, although some IAM features and related resources have different scopes.
- S3 is a global service with buckets created in particular Regions.
- EC2 resources are Region-specific.
- CloudTrail Event history is viewed for a selected Region.

Do not create resources just to test the Region selector.

# Step 3: Open IAM and explore users and permissions

[How to Create an AWS S3 Bucket and an IAM User | Vectorize Docs](https://images.openai.com/static-rsc-4/SJPPyy74ucrEe-uVOgVLWw8mvpD3A722jqX_1rak2sdYZs0seY0H1S7oXm46ll6o94dKLGIoZQgVKPoOatwgV4_U4BFeFWq4wzae6utxW2o17ZLrrmCI3zO_O04LHPYAOjLlxX0-ZxDN_qdZUOBQVZMnlgsD8zR4_Xap5q0M6HI?purpose=inline)

## Service 1: IAM

Identity and Access Management

IAM controls who can access AWS and what they can do.

## 3.1 Open the IAM page

1. Go to the AWS home page.
2. Click the top search bar.
3. Type `IAM`.
4. Select IAM, usually shown under Security, Identity, and Compliance.
5. Wait for the IAM dashboard to open.

You can also open IAM directly using this official link:

[Open AWS IAM Console](https://console.aws.amazon.com/iam/?utm_source=chatgpt.com)

## 3.2 Explore each page inside IAM

[Mastering AWS IAM Users: Creating, Managing, and Deleting with Confidence | by Pushpendra | Medium](https://images.openai.com/static-rsc-4/P7xkgppXPCmi_gn5wAsj8ubersTshgUAk_u47D2-dWgNHIwCCg6sKh0MwYWiJPur-ZYlKWbLYpM7z7BA7XQb6wzD3Iom57b619HoKKS5atLOzlMXLMWaPJKYP8POsIiCr0XUzL4QnmAu1YPVR73tVCsRfnhn2_ZfVJh1h7D1zA8?purpose=inline)

Page A: Dashboard

Find the account information and any security recommendations displayed. The exact widgets depend on your account and the current console layout.

Your task: Identify the account-level security information available.

[Introduction to AWS Identity and Access Management (IAM) | Notes by Nisha](https://images.openai.com/static-rsc-4/axl7zBYCJihclLQXj1FDN5XvwBo7q6GKfjTl72-LX62AHaSAkj0MJII5CeRhQdfnqqF-nCWZl-NuZLTh6jjjze3dpvgWZCeSobCrHkNW4fjmfyf8wD_-OtMLuDoI8iK7Iv_E90nESlO32PGZ8E1a2ta98oULS8X5fd3W5Sty7jM?purpose=inline)

Page B: Users

In the left navigation, click Users.

Look for the user list and columns such as user name, groups, and last activity information when available.

Your task: Record how many users are visible and whether you can inspect their permissions. Do not create or delete users.

[Use SSM Instead of SSH to Access EC2 Instances! | by Dorian Ferguson | Medium](https://images.openai.com/static-rsc-4/rrTfFU9JN3H_d3H_p2K7-phoTghTgeAq-oX9JDXWRKORyMBFy4tdcRRXn7m2EQxvUsq0v9YaNL955iNCbwbs0zWy7H-j6uf5PVTErZ-VtDBWX2sVb7fmiArOvOxagQ47LHbMmeWOZox_IX-2a0jD_MUSdgrzO9BMFVGm58peUV0?purpose=inline)

Page C: Roles

Click Roles in the left navigation.

Roles are identities that users, AWS services, or other authorized entities can assume.

Your task: Inspect role names and the permissions attached to a role you are allowed to view.

[Configuring AWS policy - Prerequisites · Wazuh documentation](https://images.openai.com/static-rsc-4/ODSq7DJoEJCsj0CiqfwJcBg6af6iOm4tAuHDNeoyP0SpmISxGFjwZMbApjzR0-s8VQXFDd-N0632Fh1PYAkvo7hofEZDnLRfxPtABpEuXi9FawMer8ATmc3IzMHm4SsTYzDTPVxD7lj1jSuwlbLVuUk7NoEX6Ht6nqQmzLLE2Zk?purpose=inline)

Page D: Policies

Click Policies.

Policies describe which actions are allowed or denied on which resources, subject to applicable conditions and other controls.

Your task: Open a policy that you are permitted to inspect and find its permissions summary or JSON document.

[AWS IAM overview · Hyperskill](https://images.openai.com/static-rsc-4/uXyOTf6_QVxFKVfXpZ1pGUw5iUHr7uflFyKFk2tE1FNRC0JqJ03kBKkwfAxf69fn8aGRaDeKIP2v1RptDfH-4TSHsTlty-hknPjiNlrwLaZZyGTA9rRtm97W5q0CFaVOvrPCo3SGnqsdlCxoxfsVF8DqIpHGZj1f_RR5F4SFEjg?purpose=inline)

Page E: Security credentials or account security settings

Select an authorized identity to inspect its available security information. For your own account, look for MFA and sign-in settings.

Your task: Understand how MFA and credential management help secure an account.

AWS may show different navigation labels or restrict some pages depending on your permissions. IAM users can access only the actions allowed by their permissions.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://aws.amazon.com\&sz=32)

Amazon Web Services, Inc.

+1



### 3.3 What should you understand from IAM?

Suppose you see a policy that grants `s3:GetObject`.

- `s3` refers to Amazon S3.
- `GetObject` means retrieving an object from storage.
- The `Resource` field identifies which resources the permission applies to.
- Other policy statements and conditions can further restrict or deny access.

A permission is not automatically a security problem. You must compare it with the identity's actual job requirements.

Write in your practical notebook:

- Service explored: IAM
- Pages visited: Dashboard, Users, Roles, Policies
- Information observed: User list, roles, policies, permissions
- Security objective: Ensure identities have appropriate access

# Step 4: Open S3 and explore cloud storage

[How to Create an S3 Bucket in AWS Using Terraform · Mike Vu](https://images.openai.com/static-rsc-4/jZqDUzzQUb10BhmSmtsIq4JkYLqCJFNxVTICjssDZoJFY4UTiPDOR9kbdllzsXxTG9DfBsjEngZcm9zdtQS33Fp8F25T6nuDKr_LqN-p5UG54-qjVyCmOEEZXPRy91IGtmB0XIYNQdbMe0xpjXRAqfw6KklmYkIlFYMYf7ZEo_8?purpose=inline)

## Service 2: Amazon S3

Simple Storage Service

S3 stores files and objects such as images, documents, backups, and application data.

## 4.1 Open S3

1. Return to the AWS console home page.
2. Click the search bar at the top.
3. Type `S3`.
4. Select S3.
5. The S3 console should open on the buckets page.

Direct link: [Open Amazon S3 Console](https://s3.console.aws.amazon.com/s3/home?utm_source=chatgpt.com)

## 4.2 Understand the S3 buckets page

[How to Deploy a Static Website with S3 and CloudFront on AWS - DEV Community](https://images.openai.com/static-rsc-4/PeWRrvwdY4hXqxZlwXKqPjvp3zzI4p_ha55inB1ZeA4KDinXg7aROvmfJvRQR0FDF5u0Azb3GMIqx6n7OekCA-mTSwEW2U3Jcw-WCiedJgsjtYWyYrDiCxzL6_txrsjeVPGUVoleVJXrCCAh4Zu-Bg7pkMSwBy4yYvClSM7jQoI?purpose=inline)

[dev.to](https://dev.to/ooluwatobi_o/how-to-deploy-a-static-website-with-s3-and-cloudfront-on-aws-1lnj?utm_source=chatgpt.com)

A bucket is a container for storing objects.

For example, a company could have buckets for application images, backups, or reports.

On the buckets page:

1. Look for the bucket list.
2. Inspect bucket names and Regions, where shown.
3. Open a bucket only if you are authorized to view it.
4. Explore its tabs, such as Objects, Properties, Permissions, and Management, if available.

### What is inside each tab?

Objects

Shows files stored in the bucket, if you have permission. Observe object names, types and other metadata. Do not download private files unnecessarily.

Properties

Contains settings such as bucket versioning, encryption, logging-related configuration, and other bucket properties where supported.

Permissions

Review Block Public Access, bucket policies and other access-control settings.

Management

Review lifecycle rules, replication and other management features if configured.

## 4.3 What if the bucket list is empty?

That is perfectly fine. It may mean your account has no buckets in view or your identity cannot list them.

For this exploration task, do not create a bucket just to make the page look populated. You can document that no buckets were visible and continue to EC2.

If you have a training bucket, inspect its settings without changing permissions or accessing data outside your authorization.

### Your practical notes for S3

Record:

- Service name: Amazon S3
- Main resource: Bucket
- Pages visited: Buckets, Objects, Properties, Permissions
- Security checks: Public access, bucket policy, encryption settings
- Observation: What was visible, or whether you lacked permission

# Step 5: Open EC2 and explore virtual machines

[Jack B. Du - Firewall Log Analysis](https://images.openai.com/static-rsc-4/7DYLvszjaG_J8KojFQ-5N7rmaYQp5c1d8OskzKpCstMFOiYSzcN-4PJ8pTjI0BHS20_bYoJf8xXqVKg_XXSPXf3xQlPFdNrlTOcv8qOSXCoFTtSR0fADiMLzqMNbzC65rVIQHCAvkvkhJ38fo82nNJrlNbNoyziNii_1Z2sPfPc?purpose=inline)

## Service 3: Amazon EC2

Elastic Compute Cloud

EC2 provides virtual servers that run applications, websites and other workloads.

## 5.1 Open EC2

1. Return to the AWS console.
2. Click the search bar.
3. Type `EC2`.
4. Select EC2.
5. The EC2 dashboard opens.

Direct link: [Open Amazon EC2 Console](https://console.aws.amazon.com/ec2/home?utm_source=chatgpt.com)

## 5.2 Explore the Instances page

[Virtual Machines in the Cloud: Amazon EC2 | by Abdul Wassay | Medium](https://images.openai.com/static-rsc-4/HjsWlJ1sbgEt_K0k5hryElPB5eytFgv4SSZy8YQl8fgl1y0KmrcNSF0AjcQZqyl7cU8iR-xc_xCeO0J5G706f-JBHq7XVV1cqfodBbo5ZlpnqQOnzh1JrJjx8SMTHAu2wCgptDpky6p-tRviKcbeBDAH_leu9fyNn6Cr5x1b0Bw?purpose=inline)

[hotplugin.medium.com](https://hotplugin.medium.com/amazon-ec2-101-a-hands-on-guide-89a51d9e6200?utm_source=chatgpt.com)

In the EC2 left navigation, locate Instances and click it.

Look for information such as:

| Field               | Meaning                                             |
| ------------------- | --------------------------------------------------- |
| Instance ID         | Unique identifier for the virtual machine           |
| Instance state      | Whether it is running, stopped, or in another state |
| Instance type       | The virtual machine's compute configuration         |
| Availability Zone   | The specific zone hosting the instance              |
| Public IPv4 address | Publicly routable IPv4 address, if assigned         |
| Security groups     | Network access rules associated with the instance   |

Your account may contain no instances. That is normal for a new or unused account.

## 5.3 Explore the security groups

This is particularly important for cloud security.

1. Select an existing instance you are authorized to inspect, if one exists.
2. Open the Security tab in the instance details pane, or follow the security group link.
3. Select the relevant security group.
4. Open Inbound rules.
5. Examine the protocol, port range and source.
6. Open Outbound rules to understand permitted outbound traffic.

For example, a rule might allow TCP port `443` from `0.0.0.0/0`. This allows IPv4 traffic from any address to reach that port, subject to the rest of the network and service configuration.

Your job is to determine whether the exposure is intentional, not to assume every public rule is dangerous.

Do not click Launch instance, Terminate instance, or modify security group rules during this read-only practical. Creating or running cloud resources may incur charges.

### Your practical notes for EC2

Record:

- Service name: Amazon EC2
- Pages visited: Dashboard, Instances, Security groups
- Information observed: Instance states, types, network rules
- Security objective: Identify unnecessary exposure and understand network access controls

# Step 6: Open CloudTrail and explore activity logs

[Listening To Events By AWS Services | AWS](https://images.openai.com/static-rsc-4/PyvFYSiC53P3IdSRkjLWTT1Cf2zaQc8t8MOGpnw_60WBdbDbS3PVsLuKdWC_KPOe9ctt_EGpEoFib7NtiXI3nKHEap2vaheO7jlSAPgOZrct18uUnEBc6on6IZGn6WTo8zcEJdVgZacr1KsbOxvFkMATZ9BNRHCO6_amdcqh9vw?purpose=inline)

## Service 4: AWS CloudTrail

Audit and activity logging

CloudTrail helps you understand which AWS actions occurred, when they occurred, and which identity was associated with them.

## 6.1 Open CloudTrail

1. Return to the AWS console home page.
2. Click the search bar.
3. Type `CloudTrail`.
4. Select CloudTrail.
5. Find Event history in the left navigation panel.

You can also open [AWS CloudTrail Console](https://console.aws.amazon.com/cloudtrail/?utm_source=chatgpt.com).

## 6.2 Open Event history

[Kiran Thomas | How to use AWS CloudTrail to Audit Infrastructure Changes](https://images.openai.com/static-rsc-4/nKpY_amF-_GtcQng_qRiKXvyKoyhKGgP4q-RgWoT2PIZbP9e0QuiqBm3RRy_mBAYPQP49ObixVvnpMxemkI9i-LX4xPNT81mtpglFj-6TDBKvxgO5AGjJJTWaNCxdfPNcS4dEMavoF3o2c71MGkEWRqDsvptXEAveuT1Rcj_7wI?purpose=inline)

[kiranjthomas.com](https://www.kiranjthomas.com/posts/cloudtrail/?utm_source=chatgpt.com)

The Event history page shows recorded management events for the selected Region.

Follow these steps:

1. Find the event table.
2. Look at the event name and event time columns.
3. Locate the Lookup attributes or filter controls.
4. Choose Event name from the filter options.
5. Type `ConsoleLogin`.
6. Apply the filter if the page requires you to.
7. Open an event to inspect its details.
8. Scroll to Event record to view the JSON event data.

If no login events appear, remove the filter and check the time range and Region. Your account may simply have no matching events.

CloudTrail Event history provides up to 90 days of management-event history in a Region. It does not display all S3 object-level data events, so an empty result does not prove that no activity occurred.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail



## 6.3 Understand the event details page

When you open an event, look for these fields:

| Field                | What you learn                              |
| -------------------- | ------------------------------------------- |
| Event name           | Which action occurred                       |
| Event time           | When it occurred                            |
| Username or identity | Who or what performed the action            |
| Event source         | Which AWS service received the request      |
| Source IP            | Where the request originated, when recorded |
| AWS Region           | Which Region is associated with the event   |
| Error code           | Whether an error was recorded               |

For your first visit, you only need to inspect the existing records. Do not create a CloudTrail trail or change logging settings during this task. Creating a trail that delivers logs to S3 may incur storage charges.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail



### Your practical notes for CloudTrail

- Service name: AWS CloudTrail
- Page visited: Event history
- Information observed: Event names, timestamps, identities and sources
- Security objective: Understand and audit activity in the cloud environment

# Step 7: Complete your practical notebook

You have now explored the four main services. Use this worksheet to record what you actually saw.

## Practical record: Explore AWS

Enter your own observations. If a page was unavailable, record that rather than guessing.

1\. IAM

What user, role or policy information could you view?

2\. S3

Were any buckets visible? Which security settings could you inspect?

3\. EC2

Were any instances visible? What did you learn about security groups?

4\. CloudTrail

Were events visible? Which event fields did you identify?

Copy practical notes

## Step 8: Check your progress

## Completion checklist

0/7

Opened the AWS Management Console

Identified the search bar and Region selector

Explored IAM

Explored S3

Explored EC2 and security groups

Opened CloudTrail Event history

Recorded my observations

## Troubleshooting: If the AWS website looks different

- Access denied: Your AWS identity may not have permission to view the service or resource. Ask your instructor or account administrator for appropriate read-only access.
- No resources found: You may be using a new account, an empty environment, or the wrong Region.
- Cannot find a menu: Use the AWS console's top search bar to find the service directly.
- A page asks you to create something: Stop and return to the existing resources. Creating resources is not required for this first practical.
- A security recommendation appears: Record it and investigate its meaning before changing anything.

Your first practical is complete when you can navigate to all four services, explain their purpose, identify their main pages, and document your observations. You do not need to modify or deploy anything.


# Step 9: Use GuardDuty to examine security findings

CloudTrail tells you about recorded activity. Amazon GuardDuty is a threat-detection service that analyzes supported data sources and generates findings about potentially suspicious activity.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

Amazon GuardDuty



## 9.1 Open GuardDuty

[Amazon GuardDuty EC2 Runtime Monitoring is now generally available | AWS News Blog](https://images.openai.com/static-rsc-4/XUyvxDPX0koOtNoA-ffn4B5XJh5diLiqc70NJGDwxNRiPggDMueyD_fNAoy6BruhfWlvj94-7Ye20ZIWmLkpdtzAWmZzkdBxEOBQ9brhdU0Kcw_e99UQLRtLM6xGfao2jAIIrk1Jh5c7g0vVQfG4eQno5uEyE0Ah1nQyNpwHTDM?purpose=inline)

[aws.amazon.com](https://aws.amazon.com/blogs/aws/amazon-guardduty-ec2-runtime-monitoring-is-now-generally-available/?utm_source=chatgpt.com)

1. Return to the AWS console.
2. Search for `GuardDuty`.
3. Open Amazon GuardDuty.
4. Look at the left navigation panel.
5. Select Findings.
6. Inspect the findings table, if findings are available.

Direct link: [Open Amazon GuardDuty](https://console.aws.amazon.com/guardduty/?utm_source=chatgpt.com)

## 9.2 What should you look for?

| Field             | Meaning                                      |
| ----------------- | -------------------------------------------- |
| Finding type      | The category of detected activity            |
| Severity          | GuardDuty's severity classification          |
| First seen        | When the activity was first observed         |
| Last seen         | When the activity was most recently observed |
| Resource affected | The resource associated with the finding     |
| Description       | The activity or risk GuardDuty identified    |

Click a finding to view its details. Review the affected resource, evidence, description and recommended actions.

If the Findings page is empty: Do not assume that the account is secure. GuardDuty may not be enabled, the activity may not match a detection, or there may be no findings to display.

## 9.3 Optional: Practice using sample findings

AWS supports generating sample GuardDuty findings so you can learn the interface without waiting for an actual threat to occur. These are training examples, not evidence of a real attack.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

Amazon GuardDuty



1. Open GuardDuty.
2. In the left navigation, select Settings.
3. Find the Sample findings section.
4. Select Generate sample findings, if available.
5. Return to Findings.
6. Open a finding marked `[SAMPLE]`.
7. Inspect its finding type, severity and affected resource.
8. Write down the recommended investigation steps.

If you do not see this option, your permissions or console layout may differ. Do not enable additional paid services just to complete the basic practical.

# Step 10: Complete one cloud incident investigation

Now combine CloudTrail and GuardDuty into one exercise.

## Training scenario

Imagine GuardDuty reports a suspicious activity finding involving an IAM identity. You need to investigate whether the activity is legitimate.

## Incident investigation checklist

1\. Open GuardDuty Findings

Record the finding type, severity, affected resource and time.

2\. Open CloudTrail Event history

Search the relevant time range and Region for related management events.

3\. Identify the actor

Inspect userIdentity, user name or role session details.

4\. Check the source

Review sourceIPAddress and compare it with known, approved activity.

5\. Build the timeline

List related actions in chronological order, including failed and successful requests.

6\. Assess the impact

Determine which resources or permissions may have been affected.

7\. Document and escalate

Record evidence and notify the authorized incident-response team if needed.

Completed steps: 0 of 7

### What if you confirm unauthorized activity?

In a real incident, follow your organization's response procedure. An authorized responder may need to restrict the affected identity, revoke compromised credentials, restore safe resource configurations and preserve evidence. Avoid making disruptive changes until the risk, business impact and appropriate response are understood, unless immediate containment is required by your incident-response policy.

## Step 11: Write your incident investigation report

Use this template in your notebook:

# AWS Cloud Security Incident Investigation

**Incident ID:** AWS-IR-001\
**Date:**\
**Investigator:**\
**AWS account / Region:**

## 1. Incident summary

Describe the suspicious activity or finding.

## 2. Detection source

- Service: GuardDuty / CloudTrail / Other
- Finding type or event name:
- Severity:
- First observed:

## 3. Evidence collected

- Identity involved:
- Source IP:
- Event timestamp:
- Affected resource:
- Related events:

## 4. Investigation results

Explain what the evidence establishes and what remains uncertain.

## 5. Impact assessment

Describe the resources, permissions or data potentially affected.

## 6. Recommended response

List containment, remediation and recovery actions.

## 7. Verification

Record how the team will confirm that the issue has been resolved.

## 8. Final status

Open / Under investigation / Contained / Resolved

Use fictional details for your training report unless you have actually examined real account evidence.

## Official AWS references

- [CloudTrail Event History tutorial](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/tutorial-event-history.html?utm_source=chatgpt.com)
- [CloudTrail event filtering and details](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/view-cloudtrail-events-console.html?utm_source=chatgpt.com)
- [GuardDuty Findings page](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_working-with-findings.html?utm_source=chatgpt.com)
- [GuardDuty sample findings tutorial](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_settingup.html?utm_source=chatgpt.com)

Your goal for Practical 2: You should be able to open CloudTrail, search and read events, inspect GuardDuty findings when available, construct a timeline, explain the evidence, and prepare an incident report. You are investigating suspicious activity, not creating an attack or changing production resources.


# Practical 3: Review Cloud Logs in AWS

In this practical, you will learn how to open the AWS logging pages, search for recorded events, inspect the full event details, download logs, and understand what the records tell you.

The main service is AWS CloudTrail. We will also explore CloudWatch Logs, which is used to review logs from applications and other configured sources.

You can perform the basic CloudTrail exercise without launching a server. AWS provides Event history automatically, and viewing that history does not incur a CloudTrail charge.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail



## Step 1: Open the AWS Management Console

[How to Set Up and Configure AWS: A Comprehensive Tutorial | DataCamp](https://images.openai.com/static-rsc-4/t5N4d8YtaPLrBalwFqafQdLhsykbJyqs5Y_Yo_0YceUquxNoTFyuO89bcpuBErV8ZYAcL3ApUs3NWdV0eSC1ZXrpxlO9_yiDl_bOAMKZvU565qFbqteuPH0P0qA4j4r-Xz7tu9doNE-qXSvNuynprqMbYHWQvF7tijtxPPUrXt4?purpose=inline)

1\. Open Chrome

Go to [https://console.aws.amazon.com/](https://console.aws.amazon.com/?utm_source=chatgpt.com).

[Launching a PBX on AWS](https://images.openai.com/static-rsc-4/va1GCdpqxTnASFpiVQ96i4DBueMl_m8DsgBa0RCiCGvYI-9PrQ0GvqwV3LcauuvcbKZj0RyJDXTcLDPIjUmv_96ZLlOIJr5jHUqNtcsOQ5dUMXRQx5IrbIAuoglFP_RT5rABRypcFaJRGBbv8NyJ4lYeTQXkbnR0kntiWvYu-Uw?purpose=inline)

2\. Sign in

Use your own AWS account or an account provided by your instructor.

[Configuring AWS Credentials for .NET Applications - Detailed Guide - codewithmukesh](https://images.openai.com/static-rsc-4/CLLQETdpxEIHGml-jiTCE7sNMmyOtozM7py117LANdQINbGbBSI7zN2-hGO1ZkkFYMAv500khu9uOJapz9UTnSdhNhA4fLJJpsl45l5f0YRZqnnvlfmq0RHDxVeCLiYXiA7pF-ulaz_9DWb44-kkn9pr8Eh7N_zb_y-uG-bfQNc?purpose=inline)

3\. Check the Region

Look at the Region selector in the top navigation. For this practical, select Asia Pacific (Mumbai), `ap-south-1`, if appropriate. CloudTrail Event history is Region-specific.

## Step 2: Open CloudTrail

[Listening To Events By AWS Services | AWS](https://images.openai.com/static-rsc-4/PyvFYSiC53P3IdSRkjLWTT1Cf2zaQc8t8MOGpnw_60WBdbDbS3PVsLuKdWC_KPOe9ctt_EGpEoFib7NtiXI3nKHEap2vaheO7jlSAPgOZrct18uUnEBc6on6IZGn6WTo8zcEJdVgZacr1KsbOxvFkMATZ9BNRHCO6_amdcqh9vw?purpose=inline)

[tusharf5.com](https://tusharf5.com/posts/aws-eventbridge/?utm_source=chatgpt.com)

Follow these exact steps:

1. Click the AWS search bar at the top of the page.
2. Type `CloudTrail`.
3. Click the CloudTrail service result.
4. Wait for the CloudTrail dashboard to open.
5. Find the navigation panel on the left.
6. Click Event history.

You can also open the official console directly:

[Open AWS CloudTrail](https://console.aws.amazon.com/cloudtrail/?utm_source=chatgpt.com)

The Event history page displays recent recorded management events, with newer events generally appearing first.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail

+1



## Step 3: Understand the Event history page

[Securing AWS CloudTrail | Sysdig](https://images.openai.com/static-rsc-4/8u2ztzwYp2g-4TzcuEeUbJb3Vas-XMRq9iGGVOJ1_ktzatvsukCLxbKClSWIIigg63RGiJb2FcDU_V_W5VVJI21TOpfVccxSy77yIQqWsWVvPTkktkoSpAlVQxcXz9-NPXLd9Rsbggk1BWkF1pyp6rrFcfVJ88zIey42LR-PPHo?purpose=inline)

[sysdig.com](https://www.sysdig.com/learn-cloud-native/securing-aws-cloudtrail?utm_source=chatgpt.com)

When the page opens, look at these areas.

A. Lookup attributes

Located above the event table. This area lets you search for events by event name, user name, event source, resource name and other available attributes.

B. Time range

Choose a relative period, such as the last hour or day, or set a custom start and end time.

C. Event table

Displays matching events and columns such as Event name, Event time, User name, Event source, Resource type and Resource name, depending on your settings.

D. Download events

Usually near the top-right area. You can export matching event history as CSV or JSON.

### Important: The default filter

AWS commonly opens Event history with a filter called Read-only = false. This focuses the list on events that are not read-only, so you may initially see fewer events than expected.

To view more types of activity:

1. Look for the `Read-only` filter above the table.
2. Click its X to remove it.
3. Wait for the event list to refresh.

You can then explore both read and write events.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail

+1



## Step 4: Search for specific cloud logs

We will practice three searches. These are safe, read-only searches.

### Practical A: Find login events

[Find the owner of an AWS Access Key | by Fırat DİKMEN | Commits | Medium](https://images.openai.com/static-rsc-4/Qhy4xnby6oEIxcLrrzd9jmb12niB-UYmY0yIRZJAznGid9NqAZammvMoMC9VA8-dfciYnxSqAaL9_DI53Eve2rVPvoffEsLTMp02kLKmNU4hfDIqiFaaWVxcAB6_RI9YnABJt2_ffZU1TyCiUhoNPuDZeeYz4fuhWGdMWcx79oA?purpose=inline)

[medium.com](https://medium.com/commits/find-the-owner-of-an-aws-access-key-68fcb13864b4?utm_source=chatgpt.com)

1. In Lookup attributes, open the attribute dropdown.
2. Select Event name.
3. Enter `ConsoleLogin`.
4. Apply the filter or press Enter, depending on the interface.
5. Review the results.

What does `ConsoleLogin` mean? It is an event name associated with an attempt to sign in to the AWS Management Console.

Look for the user or identity, time, source IP and event result. If the list is empty, widen the time range or check the Region. Do not assume an empty list means nobody has signed in.

### Practical B: Find IAM changes

Repeat the process, but search for:

`CreateAccessKey`

This searches for recorded events associated with creating an IAM access key.

You can also search for these event names individually:

| Event name         | What you are investigating                  |
| ------------------ | ------------------------------------------- |
| `CreateUser`       | Creation of an IAM user                     |
| `CreateAccessKey`  | Creation of an access key                   |
| `AttachUserPolicy` | Attachment of a policy to a user            |
| `PutUserPolicy`    | Creation or update of an inline user policy |
| `DeleteTrail`      | Deletion of a CloudTrail trail              |

These are examples of events to review, not proof of malicious activity. A legitimate administrator may perform them.

### Practical C: Find EC2 changes

In the Event name filter, enter:

`RunInstances`

This searches for recorded EC2 instance-launch activity.

You can also search for `AuthorizeSecurityGroupIngress` to investigate recorded changes to security-group inbound rules.

For every search, write down:

- The event name
- The event time
- The identity
- The source IP, when recorded
- The resource affected
- Whether the activity was expected

A useful limitation: Event history permits one attribute filter at a time, combined with a time range. It is not a full multi-field query tool.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail



## Step 5: Open one event and read its full details

[View event history - AWS CloudTrail](https://images.openai.com/static-rsc-4/qDH76mTo84l0W8IAwRpRw_ilOBtfErgpK4JADVldnmK9OFEdUwLS4u-VuKusvDlE9lLcpmHtGwtxJQdplq2TLDuGu7JIm_TFpPaFbAQp43LW8y8flM_MtCrsKAFQNOHj7HY2jVQkHiAPHRoeEIWezqPcFNTZmlgmJTNu3NfmSPI?purpose=inline)

[docs.aws.amazon.com](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/tutorial-event-history.html?utm_source=chatgpt.com)

Now click an event name in the results table.

The event details page contains information about the event, any referenced resources, and the complete event record when available.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail



### What each field means

| Field               | Explanation                                         |
| ------------------- | --------------------------------------------------- |
| `eventTime`         | The time the event occurred                         |
| `eventName`         | The action recorded                                 |
| `eventSource`       | The AWS service associated with the action          |
| `userIdentity`      | Information about the user, role or other identity  |
| `sourceIPAddress`   | The recorded request source IP                      |
| `awsRegion`         | The Region associated with the event                |
| `requestParameters` | Parameters supplied with the request, when recorded |
| `responseElements`  | Response details, when available                    |
| `errorCode`         | Error information, when the request failed          |
| `eventID`           | A unique identifier for the event                   |

Some fields may be missing or have different structures depending on the event type.

### Your task

1. Open a recorded event.
2. Scroll to Event record.
3. Find `eventTime`.
4. Find `eventName`.
5. Find `userIdentity`.
6. Find `sourceIPAddress`, if present.
7. Look for `errorCode` or `errorMessage`.
8. Record what you learned.

You are now reading the underlying event data rather than just the summary table.

## Step 6: Download cloud logs to your computer

This step helps you save evidence for your practical report.

[Use AWS CloudTrail to See Who Did Something in Your AWS Account - AWS - CloudBank](https://images.openai.com/static-rsc-4/z3cpYsgEC1F5VPZ6R0M6q_4JjvPvupcxYVMwBRLqyaQlQodlCDhNd6KXitk-RCRIgnN_gysMBdK336YxdPhPJ2lxogdYkS9tTuMC5x5yQjdoS6DBTndrVX3_y625zTD2SypgbDSVqgeczFjqF0N89IuC-VjqsHIBUprITmWNVh4?purpose=inline)

[community.cloudbank.org](https://community.cloudbank.org/t/use-aws-cloudtrail-to-see-who-did-something-in-your-aws-account/256?utm_source=chatgpt.com)

Follow these steps:

1. Return to Event history using the page breadcrumb.
2. Choose a relevant time range.
3. Apply an event filter, such as `ConsoleLogin`.
4. Click Download events near the top-right.
5. Choose Download as JSON or Download as CSV.
6. Save the file to your computer if prompted.
7. Open your Downloads folder and locate the file.
8. Open JSON in a code editor or text editor. Open CSV in Excel if needed.

Which format should you use?

- JSON: Better for examining complete event structures and using Python to analyze logs.
- CSV: Convenient for reviewing event summaries in a spreadsheet.

For your first exercise, download a small, filtered set of events. AWS supports downloading up to 200,000 events per file from Event history. Be careful when opening exported CSV files in spreadsheet software because untrusted values can pose spreadsheet-injection risks.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail



## Step 7: Open CloudWatch Logs

CloudTrail is mainly for account and API activity. CloudWatch Logs is a separate service for examining logs that applications, AWS services and other configured sources send to it.

[How to Monitor Databricks with Amazon CloudWatch | AWS Cloud Operations Blog](https://images.openai.com/static-rsc-4/kRalwDeGd8igdYruhb8r1nqnRQ7APgDjRFYX-89d5ApP9O9QO7yWSjmw4MlhIWfSkUji11YtIn6u7MPUQxD9T91t0f0JSeuKfz6u1Yza8D50ywqIl0KzBa7UOhMLdPUmOwmewMKdTJ1afmA_45azfSinXNXFDPQ7vypVH3LzyqI?purpose=inline)

[aws.amazon.com](https://aws.amazon.com/blogs/mt/how-to-monitor-databricks-with-amazon-cloudwatch/?utm_source=chatgpt.com)

### 7.1 Open the CloudWatch website

1. Return to the AWS console.
2. Click the search bar.
3. Type `CloudWatch`.
4. Select CloudWatch.
5. Find Logs in the left navigation.
6. Click Log groups.

Direct link: [Open Amazon CloudWatch](https://console.aws.amazon.com/cloudwatch/?utm_source=chatgpt.com)

### 7.2 Understand the Log groups page

A log group is a container for related log streams.

For example, a web application might send its application logs to a group named `/application/web`.

The page may show:

- Log group name: The name of the collection.
- Retention: How long logs are kept, if a retention policy is configured.
- Stored bytes: The amount of log data stored, when displayed.
- Creation time: When the log group was created, where shown.

These are examples of fields you may see, not a guarantee that every column appears in your account.

### 7.3 Open a log group

If a log group exists and you have permission:

1. Click its name.
2. Find the log streams list.
3. Open a stream.
4. Inspect the timestamps and messages.
5. Look for errors, repeated failures, unexpected access or other events relevant to the investigation.

A log stream is a sequence of log events from a particular source or instance of a source.

If there are no log groups, record that no application log groups were visible. Do not create logging resources just to fill the page. CloudWatch may require additional configuration before logs are delivered.

## Step 8: Understand the difference between CloudTrail and CloudWatch

[AWS CloudTrailでIAMユーザーのサインイン失敗を検出してみる - 協栄情報ブログ](https://images.openai.com/static-rsc-4/KIK3woC5GeTcRHqYWbVHH-e1qHedIzeu7bs2gak57eJ510M6LYE-_-9eS49qjF3VFMAjK7Obj3MtwQySV3gQwqVfDchoE1L44bTN3zQ-QJgohsHmS7DVxRamAg2MV6NsUt_v_KGPz9nP3qy4iiuOLqdhU6TE4e1sEzw4IRX-ACk?purpose=inline)

AWS CloudTrail

Focus: Who performed an AWS action, and what happened?

Example: An identity changed an EC2 security group.

[AWS Entities for Metric Streaming monitoring & observability | Dynatrace Hub](https://images.openai.com/static-rsc-4/iwJkcJ9NTLV9yZpub_pSCuu4iBK45NLU_kt86n2UKnkj_F4iIiVkQt5g1B1k0O96MbKLnDacC3qW_wbRqGhLlgqkA6LWO20fBx6cQ4Cl6za07oH1iLFbeb0d5HkMdRwCTq0NRyyKHVkAFng5xTXa13WrmxuxaJWrXGRmMONSy_w?purpose=inline)

Amazon CloudWatch Logs

Focus: What messages did a configured application or log source produce?

Example: A web application recorded repeated authentication errors.

CloudTrail does not automatically show every application message or every data-access event. Event history covers management events for the last 90 days in the selected Region. S3 object-level data events, for example, require appropriate data-event logging configuration to be captured.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail

+1



## Step 9: Write your cloud log review report

Use this template for your practical notebook.

# AWS Practical 3: Review Cloud Logs

**Date:**\
**Student name:**\
**AWS Region reviewed:**

## 1. Objective

To review AWS account activity and examine available cloud logs.

## 2. Services explored

- AWS CloudTrail
- Amazon CloudWatch Logs

## 3. CloudTrail observations

- Events visible:
- Filters tested:
- Event names reviewed:
- Identity and source information:
- Errors or unusual activity:

## 4. CloudWatch observations

- Log groups visible:
- Log streams reviewed:
- Application messages or errors:
- Any missing log sources:

## 5. Findings

Record each observation and explain whether it is normal, suspicious, or requires further investigation.

## 6. Recommendations

List any justified improvements to logging coverage, monitoring, retention, or incident investigation.

## 7. Conclusion

Summarize what the logs revealed and what additional evidence, if any, is needed.

## Step 10: Final checklist

## Practical completion

0/9

Opened CloudTrail

Opened Event history

Removed the default read-only filter when needed

Searched ConsoleLogin

Searched an IAM or EC2 event

Opened an event and inspected its JSON record

Downloaded a filtered log file

Opened CloudWatch Log groups

Recorded observations in the report

Copy checklist

### Official AWS guides

- [View CloudTrail Event History](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/tutorial-event-history.html?utm_source=chatgpt.com)
- [Filter, inspect and download CloudTrail events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/view-cloudtrail-events-console.html?utm_source=chatgpt.com)
- [CloudTrail overview and logging options](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html?utm_source=chatgpt.com)

Your practical is complete when you can search an event, explain its fields, save a relevant log file, and write a short report about what you observed. No server deployment or security-setting changes are required.


# Practical 4: Identify Cloud Misconfigurations in AWS

The goal of this practical is to inspect an AWS environment, identify security settings that may be unsafe, and document the risks.

A cloud misconfiguration happens when a cloud resource is set up in an insecure or unintended way. For example:

- An S3 bucket allows public access to private files.
- An IAM user has more permissions than necessary.
- An EC2 security group allows internet traffic on sensitive ports.
- Multi-factor authentication (MFA) is not enabled for an important account.
- CloudTrail logging is not configured as expected.

We'll inspect these settings through the AWS Management Console, step by step. You do not need to create resources or change security settings for this exercise. Keep the practical read-only, especially if this is a real account.

## What you will inspect

[Security, Identity & Compliance  | AWS Architecture Center](https://images.openai.com/static-rsc-4/yW4y9F9z2I0-cHTZhSJ6ljYOvdyruAYQGQyRyQo3y8A9C86Yk_mPL-LxWsrWekV5Jx9ZC1_YmSLYtYOcMj-xbMoD48r4bud4c_G4m-8I3-alhYtXAlltXcG61i_yhkEAnF3Q15V0sFk9R1pMP-KcSaKkPJpfZNDMx5PiC1YxdO4?purpose=inline)

1\. IAM (Identity and Access Management)

Check users, permissions, roles, and MFA.

[Amazon S3 Simple Storage Service Logo Vector Png | AWS S3 Bucket Icon  - freepng](https://images.openai.com/static-rsc-4/rB8GMmjRGUBIfO9GRNEL6l37e3jVW1hoDOCdtBff_Wr7VxkdCHtrta2g8EOf4zncP-U_xh6GGgSiEkpH5sASXFUOS_FyAJByqom1RHN_8AH3G2_0e-dOIH9z8H7GWykzTw3-woJ0v9yGGL6R4soSj66bGyOOPAMJOgN_sNVgnU0?purpose=inline)

2\. S3 (Simple Storage Service)

Check bucket public-access controls and permissions.

[Amazon EC2 | Integrations | Opal Security](https://images.openai.com/static-rsc-4/HSk8YHPa6JA14sHlG7c1BIR-AlCKhBxVeJuwjDBuKFv0wCszN1hDGDjwq-Txab19tCqxYoocuiFOhFq8Yhd9R6oP21ruzP6QYOSMHqySIYkoYsG7EC9Pr3DNr6lmz8_MQY4secqbsHxSJ4GQEmd1TqjS70vkl5h_qgmZI58BL4I?purpose=inline)

3\. EC2 (Elastic Compute Cloud)

Check security groups and inbound network rules.

[AWS CloudTrailでIAMユーザーのサインイン失敗を検出してみる - 協栄情報ブログ](https://images.openai.com/static-rsc-4/KIK3woC5GeTcRHqYWbVHH-e1qHedIzeu7bs2gak57eJ510M6LYE-_-9eS49qjF3VFMAjK7Obj3MtwQySV3gQwqVfDchoE1L44bTN3zQ-QJgohsHmS7DVxRamAg2MV6NsUt_v_KGPz9nP3qy4iiuOLqdhU6TE4e1sEzw4IRX-ACk?purpose=inline)

4\. CloudTrail

Check whether account activity logging is available and configured.

[Prepare for consolidated controls view and consolidated control findings in AWS Security Hub | AWS Security Blog](https://images.openai.com/static-rsc-4/d7vT_vFnP5s2e_5n-A6mqKDtVhq5GXsc0AZP-3m4jQwce05iJsE6jRDUq5SaKbrydLcuj6-H4zqaqslwvFF85mAz-7QZ84Ef_kCHbbbT1mOoMBDXNzpv7nGqTvIXJ_RuKeEatODfkBz_epHpGnJQmyOEEIi0BVIXafygN7WET9U?purpose=inline)

5\. Security Hub, if available

Review security findings and configuration checks, if the service is already enabled.

## Step 1: Open the AWS Management Console

[EmoryAWS_StartGuide_Yang](https://images.openai.com/static-rsc-4/oc7O-EtbICJtKohmGVZiFwIEmE0ZIQcpw_AVul8naAbX-J74xlMqK9RlTF16yLLsEcBqh36JMJ1q5-4B6h2SeudyTQv4od1JOGKwULHo1CW7akJBfDPSjAaINQ6xSeVAcTzHmSPoCS7_sfI0i92OWfho_uylQz_-LxEK8CbSP6s?purpose=inline)

[yanglab-emory.github.io](https://yanglab-emory.github.io/assets/ComputationSlides/EmoryAWS_StartGuide_Yang.html?utm_source=chatgpt.com)

1. Open Chrome.
2. Go to [AWS Management Console](https://console.aws.amazon.com/?utm_source=chatgpt.com).
3. Sign in using your AWS account.
4. On the console home page, locate the search bar at the top. This is the easiest way to open each service.
5. If you see a Region selector near the top-right, you can select Asia Pacific (Mumbai), `ap-south-1` for regional services if that is the Region you are using for your practical.
6. Do not create an EC2 instance, S3 bucket, or other resource just to complete this exercise.

Important: Your console may look slightly different depending on your account permissions and AWS's interface updates. If you cannot see a page or setting, record that rather than assuming it is insecure.

## Step 2: Check IAM for identity and permission problems

IAM controls who can access AWS and what actions they can perform. AWS recommends least-privilege permissions, MFA, and regular reviews of unused credentials.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://aws.amazon.com\&sz=32)

Amazon Web Services

+1



[Mastering IAM in AWS: Creating Users and Roles Step-by-Step](https://images.openai.com/static-rsc-4/YM3VGXHSO5amd2dwoepTcT6FxEhrEQKV6sD0nxJmAy-3XFOgXvtJfHTt2ddRxXgWHPYTMmqmMwRnrx6wvIO6x0GEifK78yJ8H1x3O5Fi4gjRzjqLI1p4Jo22_1MkIepJBbw9dgGq10MVcjzUYjZyzM_ttA0sG_sDQQuCwQAUeqM?purpose=inline)

[devsecops-blog.hashnode.dev](https://devsecops-blog.hashnode.dev/mastering-iam-in-aws-creating-users-and-roles-step-by-step?utm_source=chatgpt.com)

### A. Open IAM

1. Click the top search bar.
2. Type `IAM`.
3. Select IAM, usually described as Identity and Access Management.
4. The IAM dashboard opens.
5. In the left navigation panel, locate sections such as Users, User groups, Roles, Policies, and Account settings. The exact list may vary.

### B. Inspect users

1. Click Users in the left navigation.
2. A table should show the IAM users in the account, if any.
3. Click a user name to open that user's details.
4. Look for the Permissions, Security credentials, and Last accessed areas or tabs.

Check for these possible warning signs:

| What to inspect                 | Possible concern                                          |
| ------------------------------- | --------------------------------------------------------- |
| Unfamiliar users                | An account may have been created without authorization.   |
| Administrator-level permissions | A user may have more access than their job requires.      |
| Old or unused credentials       | Credentials may no longer be necessary.                   |
| MFA status                      | Console users without MFA have weaker account protection. |
| Access keys                     | Old or unnecessary keys may increase exposure.            |

How to record your result: Write down the number of users you reviewed, any unexpected users, whether MFA is shown as enabled, and whether permissions appear broader than necessary.

Do not assume an account is misconfigured just because it has administrator permissions. Some administrators legitimately need them. You must compare permissions with the person's actual responsibilities.

### C. Inspect policies

1. Return to the IAM left navigation.
2. Click Policies.
3. Open a policy that is attached to a user or role you are allowed to review.
4. Look at the Permissions or JSON view.
5. Check whether the policy grants broad access, such as `"Action": "*"` combined with `"Resource": "*"`.
6. Record the policy name and why the access might be excessive.

A broad policy can be a warning sign, but the full policy and its conditions must be reviewed before calling it a confirmed problem.

### D. Inspect roles

1. Click Roles in the IAM left navigation.
2. Select a role you are authorized to inspect.
3. Review its permissions policies and Trust relationships.
4. Check whether it grants more permissions than necessary or trusts accounts and identities that should not have access.

Do not edit policies, delete users, deactivate keys, or change trust relationships during this identification exercise.

## Step 3: Check S3 for public storage access

S3 stores objects such as files, backups, images, and logs. An improperly exposed bucket can disclose sensitive data. AWS recommends blocking public access unless public access is explicitly required.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

Amazon Simple Storage Service

+1



[Hosting a Static Website on AWS S3 - #90DaysOfDevOps Day 82](https://images.openai.com/static-rsc-4/bkb7UPC3qnBiPOUl7Y2ndsgpwd8HJPSvto_tPillGFJk9GYmaqyi16U5lcnL4bcz6EbXZvR33vDtin9ASkDnGAAJCjEUXgSk0Nom2dLd5Z8bslJ2s9lswMhbY49mCZ0FhtefX5ZmQCrzRzkMdUb3iswZFLQyQZF2DwDQCfgz-y8?purpose=inline)

[blog.estebanmoreno.link](https://blog.estebanmoreno.link/90daysofdevops-challenge-day-82-devops-project-3-static-website-using-aws-s3?utm_source=chatgpt.com)

### A. Open S3

1. Click the top AWS search bar.
2. Type `S3`.
3. Select S3, or Amazon S3.
4. In the left navigation or main page, open General purpose buckets or Buckets, depending on the console layout.
5. Review the bucket list.

If the list is empty, record: No S3 buckets were available to inspect in this account.

### B. Inspect a bucket

1. Click a bucket name. Do not click Create bucket.
2. Open the Permissions tab.
3. Find Block public access (bucket settings).
4. Inspect whether the four Block Public Access settings are enabled.
5. Review Bucket policy and, if available, Access control list (ACL).
6. Look for warnings that a bucket or its objects may be publicly accessible.

Potential concerns include:

- Block Public Access settings are disabled without a documented reason.
- A bucket policy grants access to `"Principal": "*"`.
- Permissions allow public write access.
- Sensitive data is stored in a bucket intended to be private.

A public bucket is not automatically a misconfiguration. Some websites deliberately serve public images or downloads. The question is whether the exposure matches the intended purpose.

### C. Check encryption

1. While inside the bucket, open Properties.
2. Find Default encryption.
3. Record whether encryption is enabled and which encryption method is displayed.
4. Do not change the encryption configuration.

Write in your notebook: Bucket name, Block Public Access status, any public-access warning, encryption status, and your preliminary risk rating.

Never open, download, or share files that might contain someone else's private information.

## Step 4: Check EC2 for unsafe network rules

EC2 provides virtual servers. A common misconfiguration is allowing anyone on the internet to connect to sensitive administration ports, such as SSH port `22` or Windows Remote Desktop port `3389`. AWS identifies unrestricted access to these ports as a security concern.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS Security Hub

+1



[How to Create an AWS Account, Launch a Windows EC2 Instance, and Install IIS - DEV Community](https://images.openai.com/static-rsc-4/vclFa8hNYGqT3WZHm65LNFQd5Y3aeE_yCT-VInHLMZXpJG5CYII_RsksZ0gstEcy3sTeCJPjDf42them973FPwQruWKi4tf6S7TYN4NTJcdWNXWLQ4AKDuOJ4Ff5tU3Te5uNL6CPajyUfZzmP4GPYpcdVApKZKI0k3pu-ogfLdU?purpose=inline)

[dev.to](https://dev.to/busa/how-to-create-an-aws-account-launch-a-windows-ec2-instance-and-install-iis-5dj1?utm_source=chatgpt.com)

### A. Open EC2

1. Click the top search bar.
2. Type `EC2`.
3. Select EC2, or Amazon Elastic Compute Cloud.
4. In the EC2 dashboard, find the left navigation panel.
5. Under Network & Security, click Security Groups. You might need to scroll down the panel.

### B. Inspect security groups

1. A table of security groups should appear.
2. Select a security group to inspect it. Do not select any action to edit it.
3. In the lower details panel or details page, open Inbound rules.
4. Review the columns for Type, Protocol, Port range, and Source.

Pay special attention to these examples:

| Port   | Purpose                      | Potential warning                   |
| ------ | ---------------------------- | ----------------------------------- |
| `22`   | SSH for Linux administration | Source is `0.0.0.0/0` or `::/0`     |
| `3389` | Remote Desktop for Windows   | Source is `0.0.0.0/0` or `::/0`     |
| `3306` | MySQL database               | Database access is open to everyone |
| `5432` | PostgreSQL database          | Database access is open to everyone |
| `80`   | HTTP web traffic             | May be normal for a public website  |
| `443`  | HTTPS web traffic            | May be normal for a public website  |

`0.0.0.0/0` means all IPv4 addresses. `::/0` means all IPv6 addresses.

For example, if you see:

- Type: SSH
- Port range: 22
- Source: `0.0.0.0/0`

record it as a potential high-risk misconfiguration. It allows connection attempts from any IPv4 address, although other controls may still affect whether access succeeds.

### C. Check outbound rules

1. Keep the security group selected.
2. Open Outbound rules.
3. Record whether outbound traffic is broadly allowed.
4. Do not automatically label all-open outbound access as a confirmed vulnerability. Determine whether the rule is justified for the workload.

### D. Record the finding

Write the security group ID, the rule, the source address range, the risk, and a recommended action. For example, recommend restricting SSH to an approved administration IP range or using a managed access method such as AWS Systems Manager where appropriate.

Do not edit or delete rules during this practical. You could disconnect an active server or disrupt an application.

## Step 5: Check CloudTrail logging

CloudTrail records AWS API activity, including who performed an action, when it happened, and the source IP address. Security reviews commonly check whether a trail is enabled and captures management events across Regions.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS Security Hub



[Better Security: How to Get Notified Immediately When an AWS User Signs Into the Console | by Archit Bidkar | Medium](https://images.openai.com/static-rsc-4/Z2M4qYakuKr77M4q3h7ek05u9LKJmaQPwwJB3Bv0-gTNzLdqMlOIUwA09NzaWbEyUiZcK_JYVBryoupozi_Yv5f2tPD3USrI7_jddQxhq-kLNGRNJ3lxGTb8t3VmWB-PKONCHeXVJ-qbV-8Fla5Py-_hQgIktghj_xrXzZlpa04?purpose=inline)

[medium.com](https://medium.com/%40architbidkar_66467/better-security-how-to-get-notified-immediately-when-an-aws-user-signs-into-the-console-0908a5343b35?utm_source=chatgpt.com)

### A. Open CloudTrail

1. Use the top search bar and type `CloudTrail`.
2. Select CloudTrail.
3. In the left navigation, find Trails.
4. Open Trails to see the configured trails, if any.

### B. Inspect a trail

If a trail is listed:

1. Click its name.
2. Review its status and whether logging is enabled.
3. Look for the multi-Region setting.
4. Review the management event configuration for Read and Write events.
5. Check the available settings for log file validation and the destination S3 bucket.
6. Record what is enabled, disabled, or unavailable to you.

Possible warning signs:

- No suitable trail is configured.
- Logging is stopped.
- The trail does not cover the Regions or events required by the organisation.
- The destination bucket is publicly accessible.

If no trail is listed, record that fact, but do not immediately conclude that no CloudTrail event history exists. CloudTrail Event history can still be available without a separately configured trail.

### C. Open Event history

1. In the CloudTrail left navigation, click Event history.
2. Inspect recent activity.
3. If permitted, open an event and review its event name, timestamp, identity, Region, and source IP.
4. Look for unexpected configuration changes, such as permission updates or security group modifications.

This helps you connect a suspicious configuration to an action that may have created it. Do not create a trail or change logging settings just for the exercise.

## Step 6: Check Security Hub for automated findings, if already available

Security Hub CSPM evaluates AWS resources against security controls and provides findings for settings that deviate from recommended practices. Examples include overly broad IAM permissions, missing MFA, publicly accessible S3 buckets, and unsafe EC2 security group rules.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS Security Hub

+1



[Consolidating controls in Security Hub: The new controls view and consolidated findings | AWS Security Blog](https://images.openai.com/static-rsc-4/biiIsfZz1WXXnEjg5-REWm8eluibUlGYf9hWqD3tBz7CrhjHZA5UrdwHb4glDVTwaI_Irf47TF0BnyGy62ZOdX5lxsC_sh38TsAKN1CrLH77ouySHEcADQEIMgZZT8uuWJbjMn09Nw_0-RF644Qp9gDP6gKCvS56WqRCRbxzAmE?purpose=inline)

[aws.amazon.com](https://aws.amazon.com/blogs/security/consolidating-controls-in-security-hub-the-new-controls-view-and-consolidated-findings/?utm_source=chatgpt.com)

1. Use the top search bar and type `Security Hub`.
2. Select Security Hub.
3. If the service is already enabled, open Findings or Controls, depending on the navigation available.
4. Look for failed controls or findings.
5. Open a finding to inspect its severity, affected resource, description, and remediation guidance.
6. Record the finding ID or control name, the resource, the reason for the finding, and its status.

Examples of useful controls include:

- IAM.1: IAM policies should not allow full administrative privileges without justification.
- IAM.5: MFA should be enabled for IAM users with console passwords.
- S3.1: S3 buckets should have Block Public Access enabled.
- EC2.13: Security groups should not allow unrestricted inbound access to SSH port 22.
- CloudTrail.1: A suitable multi-Region CloudTrail trail should capture management events.

If Security Hub is unavailable or disabled, do not enable it just for this practical. Setup and ongoing use may incur charges depending on the services and features used. Record it as unavailable and continue with the manual checks.

## Step 7: Classify and document what you find

Use this simple guide to rate potential issues.

High

High risk

Public access to sensitive data, or administration ports open to the internet without a valid reason.

Medium

Medium risk

Broad permissions, weak monitoring coverage, or missing safeguards that need further investigation.

Review

Needs review

A setting is disabled or appears unusual, but you do not yet have enough context to confirm it is a security problem.

These are practical assessment labels, not an official AWS severity rating. Consider the data, exposure, business purpose, and other security controls before finalising a rating.

## Practical notebook template

Copy this table into your notes and fill it with your actual observations.

| Service      | What you checked                               | Observation | Risk / status |
| ------------ | ---------------------------------------------- | ----------- | ------------- |
| IAM          | Users, permissions, MFA                        | \_\_\_      | \_\_\_        |
| S3           | Block Public Access, bucket policy, encryption | \_\_\_      | \_\_\_        |
| EC2          | Inbound and outbound rules                     | \_\_\_      | \_\_\_        |
| CloudTrail   | Trails, logging, event history                 | \_\_\_      | \_\_\_        |
| Security Hub | Existing findings, if available                | \_\_\_      | \_\_\_        |

For each confirmed or potential issue, add:

- Finding: What is misconfigured?
- Evidence: Which page and setting did you inspect?
- Impact: What could happen if the setting is unsafe?
- Recommendation: What should an authorised administrator review or change?
- Status: Confirmed issue, potential issue, not observed, or unable to verify.

## Final practical checklist

Practical progress

### 0/6

Opened IAM and inspected users, permissions, and MFA

Opened S3 and inspected Block Public Access and encryption

Opened EC2 and reviewed security group rules

Opened CloudTrail and checked trail status and Event history

Reviewed Security Hub findings, if already available

Recorded evidence and recommendations without changing settings

Official references for your practical:

- [AWS IAM security best practices](https://aws.amazon.com/iam/resources/best-practices/?utm_source=chatgpt.com)
- [Amazon S3 security best practices](https://docs.aws.amazon.com/AmazonS3/latest/userguide/security-best-practices.html?utm_source=chatgpt.com)
- [AWS Security Hub EC2 controls](https://docs.aws.amazon.com/securityhub/latest/userguide/ec2-controls.html?utm_source=chatgpt.com)
- [AWS Security Hub CloudTrail controls](https://docs.aws.amazon.com/securityhub/latest/userguide/cloudtrail-controls.html?utm_source=chatgpt.com)

Expected outcome: You should be able to explain what a cloud misconfiguration is, identify potential examples in AWS, collect evidence from the console, assess the risk, and recommend a corrective action without making unauthorised changes.


# Practical 5: Create Cloud Security Assessment Reports in AWS

In this practical, you will collect information from AWS services, evaluate security settings, and prepare a report that explains the risks and recommended improvements.

There are two ways to complete this task:

- Method A: Manual assessment report. Inspect IAM, S3, EC2, CloudTrail, and any available Security Hub findings, then prepare your own report. This is the best starting point for a student practical.
- Method B: AWS Audit Manager assessment report. If Audit Manager is available and already configured, you can explore its assessment and report-generation workflow. It collects evidence for audit purposes, but it does not automatically decide whether every piece of evidence is compliant.&#x20;

  [image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

  AWS Audit Manager



We'll start with Method A so you can complete the exercise without creating paid resources.

## What you need to produce

Security assessment report

Scope, findings, evidence, risk ratings, and recommendations.

Evidence from AWS

Observed configuration settings, event records, and available security findings.

Final report file

A document you can submit for your practical or coursework.

## Step 1: Open the AWS Console

[EmoryAWS_StartGuide_Yang](https://images.openai.com/static-rsc-4/oc7O-EtbICJtKohmGVZiFwIEmE0ZIQcpw_AVul8naAbX-J74xlMqK9RlTF16yLLsEcBqh36JMJ1q5-4B6h2SeudyTQv4od1JOGKwULHo1CW7akJBfDPSjAaINQ6xSeVAcTzHmSPoCS7_sfI0i92OWfho_uylQz_-LxEK8CbSP6s?purpose=inline)

[yanglab-emory.github.io](https://yanglab-emory.github.io/assets/ComputationSlides/EmoryAWS_StartGuide_Yang.html?utm_source=chatgpt.com)

1. Open Chrome on your computer.
2. Visit [https://console.aws.amazon.com/](https://console.aws.amazon.com/?utm_source=chatgpt.com).
3. Sign in to your AWS account.
4. Locate the search bar at the top of the console.
5. Select the Region you have been using for your lab, such as Asia Pacific (Mumbai), `ap-south-1`, for regional resources.
6. Keep the account and Region consistent when recording your findings.

Safety rule: Do not change security settings or create resources simply to generate findings. If a service is unavailable, a resource does not exist, or your permissions do not allow access, document that limitation.

## Step 2: Define the scope of your assessment

Before collecting evidence, decide what your report covers.

1. In the AWS Console, open the account menu near the top-right.
2. Identify the account you are signed into. Do not include sensitive account details in a report submitted publicly.
3. Record the assessment date.
4. Record the AWS Region being inspected.
5. List the services you will review.

For a student practical, use this scope:

| Assessment area             | Service                    |
| --------------------------- | -------------------------- |
| User access and permissions | IAM                        |
| File storage security       | S3                         |
| Network exposure            | EC2 security groups        |
| Activity logging            | CloudTrail                 |
| Automated security findings | Security Hub, if available |

This scope tells the reader what you examined and prevents the report from claiming that the entire AWS environment was assessed when only a few services were checked.

## Step 3: Collect security evidence from IAM

[Mastering IAM in AWS: Creating Users and Roles Step-by-Step](https://images.openai.com/static-rsc-4/YM3VGXHSO5amd2dwoepTcT6FxEhrEQKV6sD0nxJmAy-3XFOgXvtJfHTt2ddRxXgWHPYTMmqmMwRnrx6wvIO6x0GEifK78yJ8H1x3O5Fi4gjRzjqLI1p4Jo22_1MkIepJBbw9dgGq10MVcjzUYjZyzM_ttA0sG_sDQQuCwQAUeqM?purpose=inline)

[devsecops-blog.hashnode.dev](https://devsecops-blog.hashnode.dev/mastering-iam-in-aws-creating-users-and-roles-step-by-step?utm_source=chatgpt.com)

IAM evidence helps you evaluate account access and permissions.

1. Click the AWS search bar.
2. Type `IAM` and open IAM.
3. In the left navigation, click Users.
4. Open a user and inspect the Permissions and Security credentials sections.
5. Record whether MFA is enabled, whether permissions seem appropriate, and whether unused credentials need review.
6. Return to the navigation and click Roles.
7. Inspect relevant roles and their attached permission policies.
8. If necessary, open Policies to examine the permissions granted.

Record your observations in a small evidence table:

| Field          | What to record                        |
| -------------- | ------------------------------------- |
| Service        | IAM                                   |
| Evidence       | User MFA status or policy permissions |
| Observation    | What the console actually shows       |
| Risk           | Possible consequence                  |
| Recommendation | Suggested corrective action           |

For example, if a user has broad administrator permissions, write that this needs justification against their responsibilities. Do not automatically label it a confirmed vulnerability.

## Step 4: Collect security evidence from S3

[Creating and Configuring a Bucket | Deploying Web Applications on AWS | Steve Kinney](https://images.openai.com/static-rsc-4/nAcxy8wuVA-MN3Ek2qQY1ovcRXU9xF1Y584uxIJdmxVNok2yBaAV6MnEbW609X7_u2Wf8r9P8m0yI4Jk8DEMakfXKsqzOogRJXDrUdXho5F9TvtTzE0vD0XNrZnCgd46W6VJl5UV_poEevPp5NJZ2ek8VehhKommoNFZOsPh4uA?purpose=inline)

[stevekinney.com](https://stevekinney.com/courses/aws/creating-and-configuring-a-bucket?utm_source=chatgpt.com)

1. Search for `S3` in the top bar and open the service.
2. Select Buckets or General purpose buckets.
3. Open a bucket you are authorised to inspect.
4. Select the Permissions tab.
5. Record the four Block public access settings.
6. Review the bucket policy and any available public-access warnings.
7. Open Properties and inspect Default encryption.
8. Record the observed settings and any concerns.

If the account has no buckets, record Not assessed: no buckets available. Do not create one just to generate evidence.

## Step 5: Collect security evidence from EC2

[Securely Deploy a Django App With Gunicorn, Nginx, & HTTPS – Real Python](https://images.openai.com/static-rsc-4/Ynsk825PDPzGZQJHdK_FA1iIIiGiIkgLCbsqNZMu_XYkLBq2gMqKKE1WUKbidXxC2Ie5NNpTxa3sRbV9DNFRMys_nt8CwRPQn73AyxpaF35aJ-kVzGxCq9M5YLhNvhnVKP-1zrnilKO0ZUL8v8OplV6Q_Ar587b0nmwl4nk4WPQ?purpose=inline)

[realpython.com](https://realpython.com/django-nginx-gunicorn/?utm_source=chatgpt.com)

1. Search for `EC2` and open the service.
2. In the left navigation, scroll to Network & Security.
3. Click Security Groups.
4. Select a security group.
5. Open Inbound rules and record the port, protocol, and source.
6. Check for sensitive ports such as SSH `22`, RDP `3389`, and database ports exposed to `0.0.0.0/0` or `::/0`.
7. Open Outbound rules and record any broad rules that require review.
8. Do not modify the rules.

Your evidence should identify the actual rule and explain why it may be risky, rather than simply saying “EC2 is insecure.”

## Step 6: Collect evidence from CloudTrail

[What is AWS CloudTrail and how to use it](https://images.openai.com/static-rsc-4/I7XnVDfEcTJkkHI5O4tlkkgdodynPiEgJq5PYKQHs0aNwfzbNZG8DOjBanAqt4aUbl9eWJ04V4VMt3_XYZgeibyd83_o_uEW2IBzNzHdFgKjty00YiCgXUCW0Ig9fKG6kWX3CVpvzekrCZiofGzuuD15iy__dQEfGwi1mLHiLvg?purpose=inline)

[howtoforge.com](https://www.howtoforge.com/what-is-aws-cloudtrail-and-how-to-use-it/?utm_source=chatgpt.com)

1. Search for `CloudTrail` and open the service.
2. Select Event history from the left navigation.
3. Review the available management events.
4. Use the Lookup attributes filter to search for events such as `ConsoleLogin`, `CreateAccessKey`, or `AuthorizeSecurityGroupIngress`.
5. Click an event name to view its details.
6. Record the event time, event name, identity, Region, source IP when available, and any relevant resource.
7. To save event evidence, select Download events and choose CSV or JSON.

CloudTrail Event history normally covers the last 90 days of management events for the selected Region. It does not include every kind of activity, such as data events, unless those are captured through other configurations.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS CloudTrail

+1



Treat downloaded logs as potentially sensitive. Store them securely and do not enable links or macros in exported files.

## Step 7: Review Security Hub findings, if available

[How to automate SCAP testing with AWS Systems Manager and Security Hub | AWS Security Blog](https://images.openai.com/static-rsc-4/CTTp6wn7DEhPA3uNKkKBN7sAEZGZSOwndCiiEJxv2UfCDt9jeXro7d8mfuA2A1sSVMcN03-nmUnc0TxOPxmFbMa4LlwuYAq5XB_-nTLv05co53cEcsJZlQGJb-a7bgXNUFT5zhC2nRw8j_tNWyV10-d9qxUBKiU09NY7dXgaw3k?purpose=inline)

[aws.amazon.com](https://aws.amazon.com/blogs/security/how-to-automate-scap-testing-with-aws-systems-manager-and-security-hub/?utm_source=chatgpt.com)

1. Search for `Security Hub`.
2. Open the service.
3. If it is already enabled, open Findings or the relevant security findings page.
4. Review the severity, title, affected resource, status, and remediation guidance.
5. Record findings relevant to IAM, S3, EC2, or logging.
6. If the page provides an Export option, you may inspect the export workflow.

Security Hub can export selected findings to S3 as CSV or JSON, but that workflow requires an appropriate destination bucket, encryption key, policies, and permissions. For this beginner practical, simply record the findings on screen unless export is already configured.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

AWS Security Hub

+1



If the service is unavailable, record that it was not available for the assessment. Do not enable new services solely for this exercise because configuration and usage may incur charges.

## Step 8: Turn your observations into findings

Now you have collected the evidence. Convert each observation into a finding that another person can understand and verify.

For each issue, answer these five questions:

1. What did I find? State the setting or event.
2. Where did I find it? Identify the AWS service and page.
3. Why does it matter? Explain the possible impact.
4. What should be done? Recommend a corrective action.
5. How serious is it? Assign a preliminary risk level based on evidence and context.

Example of how to write a finding:

## Finding example: Unrestricted SSH access

Preliminary risk

High, subject to validation

Observation: An EC2 security group allows inbound SSH traffic on port 22 from `0.0.0.0/0`.

Evidence location: AWS Console → EC2 → Network & Security → Security Groups → Inbound rules.

Potential impact: The rule permits connection attempts from any IPv4 address. If the server is reachable and other controls do not prevent access, this may increase the risk of unauthorised login attempts.

Recommendation: Confirm the intended access requirements and restrict SSH to approved source addresses or an approved managed access solution.

Status: Potential misconfiguration, pending validation by the resource owner.

This is an illustrative example, not a claim about your actual AWS account. Use only the findings you really observe.

## Step 9: Create your final report in Word

You can use Microsoft Word on your Windows computer.

1. Open Microsoft Word.
2. Select Blank document.
3. Add the report title.
4. Fill in the sections below.
5. Insert relevant screenshots using Insert → Pictures. Alternatively, use `Win + Shift + S` to capture a screenshot of the AWS page.
6. Before inserting screenshots, hide or redact sensitive account IDs, IP addresses, usernames, and resource details that should not be shared.
7. Add the finding tables and recommendations.
8. Select File → Save As and save the document as `Cloud_Security_Assessment_Report.docx`.
9. To produce a PDF, select File → Save As or Export, then choose PDF if that option is available.

Here is a report template you can copy into Word.

# Cloud Security Assessment Report

## 1. Assessment Details

- **Report title:** Cloud Security Assessment Report
- **Assessment date:** [Enter date]
- **Platform:** Amazon Web Services (AWS)
- **AWS Region reviewed:** [Enter Region]
- **Assessed by:** [Enter your name or student ID, if required]
- **Assessment type:** Manual security configuration review

## 2. Objective

The objective of this assessment is to inspect selected AWS security configurations, identify potential misconfigurations, document supporting evidence, assess potential risks, and recommend corrective actions.

## 3. Scope

The assessment covers the following services:

- IAM: users, permissions, roles, and MFA
- S3: public-access controls and encryption
- EC2: security group inbound and outbound rules
- CloudTrail: activity logging and event history
- Security Hub: existing security findings, if available

This report covers only the resources and settings that were accessible and inspected during the assessment.

## 4. Assessment Methodology

The assessment was performed through the AWS Management Console using read-only inspection wherever possible. Observations were recorded from service pages, configuration settings, available security findings, and relevant event records. No security settings were intentionally changed during the exercise.

## 5. Summary of Results

- **Areas inspected:** [Enter number]
- **Confirmed findings:** [Enter number]
- **Potential issues requiring validation:** [Enter number]
- **Areas not assessed:** [List services or resources]

## 6. Findings

### Finding 1: [Finding title]

- **AWS service:** [IAM / S3 / EC2 / CloudTrail / Security Hub]
- **Evidence location:** [Console navigation path]
- **Observation:** [Describe what was actually observed]
- **Risk level:** [High / Medium / Low / Needs review]
- **Potential impact:** [Explain the possible security consequence]
- **Recommendation:** [Explain the proposed corrective action]
- **Status:** [Confirmed / Potential / Resolved / Not verified]
- **Evidence reference:** [Screenshot or event reference]

### Finding 2: [Finding title]

- **AWS service:** [Service]
- **Evidence location:** [Console navigation path]
- **Observation:** [Actual observation]
- **Risk level:** [Risk level]
- **Potential impact:** [Potential consequence]
- **Recommendation:** [Recommended action]
- **Status:** [Status]
- **Evidence reference:** [Screenshot or event reference]

## 7. Limitations

Some services, resources, security findings, or configuration details may not have been available because of account permissions, resource availability, Region selection, or service configuration. These limitations have been recorded, and unavailable evidence has not been treated as proof of compliance.

## 8. Recommendations and Action Plan

1. Review and reduce excessive permissions where justified.
2. Verify MFA protection for relevant users.
3. Confirm S3 public-access settings match business requirements.
4. Restrict sensitive network ports to approved sources.
5. Review activity logging and monitoring coverage.
6. Assign each validated finding to an authorised owner for remediation.
7. Recheck the affected configuration after approved changes.

## 9. Conclusion

The assessment reviewed selected AWS security configurations and documented observed concerns, potential risks, evidence, and recommendations. The results reflect the resources and settings inspected during the assessment and should not be interpreted as a certification that the entire AWS environment is secure.

## 10. Evidence Appendix

Attach appropriately redacted screenshots, relevant event references, and any authorised exported findings used to support the report.

## Step 10: Optional, use AWS Audit Manager to generate an assessment report

This is a separate, more formal workflow. It is useful if your course specifically expects a report generated by an AWS service rather than a manually prepared Word report.

[AWS Audit Manager launches AWS Best Practices Framework for Generative AI | AWS Cloud Operations Blog](https://images.openai.com/static-rsc-4/pW-7O6uHLmHN-IkfC46cMMz7p4KjDm8Q8kGpBmtSKwogHlrY5CDRqpE4FnNyPS5VRvY_qH49AlMztEdSu2ABu-x_hF4jMBP9BPlWlM22FBg-YobHvDiBDlCd9XgR0FU7wq7btM3nZN3Wkaig6C_C3TIiCi48pUgO-pFDef6nEJs?purpose=inline)

[aws.amazon.com](https://aws.amazon.com/blogs/mt/aws-audit-manager-launches-aws-best-practices-framework-for-generative-ai/?utm_source=chatgpt.com)

1. Search the AWS Console for `Audit Manager`.
2. Open AWS Audit Manager.
3. If the service is available and configured, inspect Assessments in the navigation.
4. Open an existing assessment that you are authorised to review.
5. Review its framework, controls, evidence, and assessment status.
6. Look for the option to generate an Assessment report.
7. If you are authorised and the assessment is ready, follow the prompts to choose the report details and evidence to include.
8. Generate the report only if your lab instructions permit it and any required configuration or costs are understood.
9. When it finishes, locate the report in the download or evidence workflow provided by the console.
10. Open the downloaded ZIP folder and read `README.txt` to understand the contents. The report folder typically includes `AssessmentReportSummary.pdf` and evidence files.&#x20;

    [image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

    AWS Audit Manager



If Audit Manager asks you to create an assessment, enable evidence collection, configure permissions, or set up other services, pause and check with your instructor before proceeding. You do not need to perform that setup to complete the manual-report method.

## Final checklist

Report completion

### 0/9

Defined the assessment scope, date, and Region

Inspected IAM and recorded access-related evidence

Inspected S3 and recorded storage-security evidence

Inspected EC2 security group rules

Reviewed CloudTrail logging and relevant events

Reviewed Security Hub findings if available

Documented observations, risks, and recommendations

Added appropriate evidence and redacted sensitive details

Saved the final report as DOCX or PDF

Expected practical outcome: You will have a structured cloud security assessment report that explains what you checked in AWS, what the evidence showed, which issues need attention, and how an authorised administrator could address them.
