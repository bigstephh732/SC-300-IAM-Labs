## SC-300 — Lab 5: Conditional Access Basics
## Phase: 
Phase 2 – Authentication & Conditional Access


## Goal
To understand how Conditional Access works in Microsoft Entra ID and create a basic policy that controls access based on conditions rather than static permissions.

 
 ## Why this lab matters
Conditional Access is the core enforcement engine of Zero Trust.
Instead of trusting users by default, access decisions are made dynamically based on identity, risk, and context. Conditional Access evaluates context such as user, application, and risk at sign-in time to determine whether additional controls, such as MFA, are required.


## Lab Note
Note: Conditional Access policy creation was restricted in this tenant due to licensing limitations.
Policy configuration and enforcement logic were documented based on Conditional Access structure and Zero Trust best practices.



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

### Policy Design Overview

Intended Policy Name:
CA-Require-MFA-for-IAM-Users

### Policy Objective

Require Multi-Factor Authentication for all users in the IAM-Users group when accessing any cloud application.

### Policy Design Details

### Assignments — Users
	•	Include:
	•	Security group: IAM-Users
	•	Exclude:
	•	Administrative accounts (best practice, not enforced in lab)

(Rationale: Group-based targeting allows policies to scale and simplifies onboarding and offboarding.)



### Assignments — Cloud Apps
	•	Include:
	•	All cloud apps

(Rationale:
Ensures MFA is enforced consistently across Microsoft 365 and third-party applications.)


### Conditions
	•	No additional conditions applied in this basic policy design.

(Rationale:
This lab focuses on foundational Conditional Access enforcement before introducing advanced conditions such as device compliance, location, or sign-in risk.)


## Access Controls (Grant)
	•	Grant access
	•	Require multi-factor authentication

(Rationale:
MFA significantly reduces the risk of credential-based attacks while maintaining user access.)


### Policy State
	•	Enabled

(Rationale:
In a production environment, policies may be deployed in report-only mode first.  
For this lab, the intended state is enabled to demonstrate enforcement logic.)


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


## What You Learned
-Conditional Access evaluates access at sign-in  
-Policies are based on conditions and controls  
-Group-based targeting is best practice  
-MFA can be enforced dynamically  
-Conditional Access supports Zero Trust principles  


## Screenshots Include:
Conditional Access Overview page  
Conditional Access policies page (policy creation restricted)  






