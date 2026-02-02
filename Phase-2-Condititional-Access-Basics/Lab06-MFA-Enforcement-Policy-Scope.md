## SC-300 — Lab 6: MFA Enforcement & Policy Scope
### Phase: Phase 2 – Authentication & Conditional Access


### Goal
To understand how Multi-Factor Authentication (MFA) is enforced using Conditional Access, and how policy scope (users, groups, and exclusions) impacts access decisions.


### Why this lab matters
Microsoft no longer recommends per-user MFA.
Conditional Access is the preferred and scalable way to enforce MFA. Microsoft strongly recommends Conditional Access for MFA enforcement due to its flexibility, scalability, and Zero Trust alignment.
This lab teaches:
How MFA is applied dynamically
Why scope and exclusions are critical
How to avoid locking out administrators


### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab environment only)
Portal: https://entra.microsoft.com

### Lab Constraint (Licensing)

Note: Conditional Access policy creation is restricted in this tenant due to licensing limitations.
This lab focuses on analysis, comparison, and intended policy design, not enforcement.


### Steps

### Step 1 — Review Existing Conditional Access Policy
Open your existing policy:
CA-Require-MFA-for-Lab-Users
Review:
Users: IAM-Users group
Cloud apps: All cloud apps
Grant: Require MFA
State: On
Purpose:
Confirm baseline MFA enforcement using Conditional Access.

### Step 2 Understanding MFA Enforcement Models (Analysis)

### Per-User MFA (Legacy)
Characteristics:
	•	Enabled directly on individual users
	•	Always enforced once enabled
	•	No context awareness

Limitations:
	•	Cannot evaluate device state, location, or risk
	•	Difficult to manage at scale
	•	Not aligned with Zero Trust principles

###  Conditional Access MFA (Recommended)
Characteristics:
	•	Enforced via policies
	•	Evaluated dynamically at sign-in
	•	Supports contextual conditions

Benefits:
	•	Scalable
	•	Flexible
	•	Supports Zero Trust architecture
	•	Microsoft-recommended enforcement method



## Step 3 Intended MFA Policy Design (No Enforcement)

### Policy Name (Design Only)

CA-MFA-Conditional-Enforcement

###  Target Users
	•	IAM-Users security group
	•	Administrative accounts excluded (best practice)

(Rationale:
Group-based targeting simplifies management and reduces risk.)

### Target Applications
	•	All cloud applications

(Rationale:
Ensures consistent MFA enforcement across resources.)

### Intended Conditions (Conceptual)
	•	Sign-in risk: Medium or High
	•	Access from untrusted locations
	•	Non-compliant or unmanaged devices

(Rationale:
MFA should be required when risk is detected, not permanently.)

###  Intended Access Control
	•	Grant access
	•	Require multi-factor authentication


### Step 4 — Review Policy Scope Impact
Understand the behavior:
Users in IAM-Users → MFA required
Users in IAM-Admins → MFA excluded
Users outside both groups → Not affected
This demonstrates policy scope control.


### Step 5 — Review Sign-In Evaluation Logic
Understand the Conditional Access flow:
User attempts sign-in
Policy scope is evaluated
Conditions are checked
Grant controls are enforced
Access is allowed or blocked


### What You Learned

-Per-user MFA is a legacy enforcement model
-MFA should be enforced using Conditional Access
-Group-based targeting improves scalability
-Exclusions prevent administrative lockout
-Policy scope directly affects access outcomes
-Conditional Access evaluates decisions at sign-in

### Screenshots Included: These screenshots document feature availability and constraints.

	Per-user MFA settings page
	•	Conditional Access overview page
	•	Conditional Access policies page (policy creation disabled)
	•	Licensing restriction banner
