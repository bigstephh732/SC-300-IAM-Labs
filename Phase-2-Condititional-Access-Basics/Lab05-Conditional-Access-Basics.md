## SC-300 — Lab 5: Conditional Access Basics
## Phase: 
Phase 2 – Authentication & Conditional Access


## Goal
To understand how Conditional Access works in Microsoft Entra ID and create a basic policy that controls access based on conditions rather than static permissions.

 
 ## Why this lab matters
Conditional Access is the core enforcement engine of Zero Trust.
Instead of trusting users by default, access decisions are made dynamically based on identity, risk, and context.

## Lab Environment

Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab tenant only)
Portal: https://entra.microsoft.com

 
 
 ## Steps

## Step 1 — Navigate to Conditional Access
Go to:
Entra ID → Conditional Access
Observe:
Policies list (likely empty)
Report-only option
What-if tool (important later)


## Step 2 — Understand Conditional Access Logic
Before creating a policy, understand the flow:
IF a user tries to access a resource
AND conditions match (user, app, location, device, risk)
THEN enforce controls (MFA, block, require compliant device)
This logic is critical for the exam.


## Step 3 — Create a Basic Conditional Access Policy
Click Create new policy
Policy Name
CA-Require-MFA-for-Lab-Users
Assignments — Users
Include:
Select users and groups
Choose group: IAM-Users
Exclude:
None (for lab simplicity)
✅ Best practice: Always target groups, not individual users.
Assignments — Cloud Apps
Select: All cloud apps
This means:
Policy applies to any app the user accesses
Conditions
Skip all conditions for now (leave defaults).
📘 This lab focuses on basic enforcement, not advanced logic.
Access Controls
Grant access
Require multi-factor authentication
Select Require MFA
Save
Enable Policy
Set:
Enable policy: On
⚠️ In production you might use Report-only first, but for lab we enable it.



## Step 4 — Review Policy
Open the policy and confirm:
Users = IAM-Users
Apps = All cloud apps
Grant = Require MFA
State = On



## Step 5 — Understand the Impact
Now understand clearly:
Users in IAM-Users must use MFA
Users NOT in the group are unaffected
Access decisions are evaluated at sign-in
This is dynamic security.



## Screenshots Include:
Save under:
screenshots/lab05/
Take the following:
Conditional Access policies list
Policy assignments (Users & groups)
Cloud apps selection
Grant controls (Require MFA)
Policy overview page
Suggested filenames:
lab05-ca-policies.png
lab05-ca-users-groups.png
lab05-ca-cloud-apps.png
lab05-ca-grant-controls.png
lab05-ca-policy-overview.png


## What You Learned
Conditional Access evaluates access at sign-in
Policies are based on conditions and controls
Group-based targeting is best practice
MFA can be enforced dynamically
Conditional Access supports Zero Trust principles




