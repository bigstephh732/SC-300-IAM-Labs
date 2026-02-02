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


### Steps

### Step 1 — Review Existing Conditional Access Policy
Navigate to:
Entra ID → Protection → Conditional Access
Open your existing policy:
CA-Require-MFA-for-Lab-Users
Review:
Users: IAM-Users group
Cloud apps: All cloud apps
Grant: Require MFA
State: On
Purpose:
Confirm baseline MFA enforcement using Conditional Access.
Step 2 — Understand MFA Enforcement Models
Understand this clearly:
❌ Per-user MFA
Legacy
Hard to scale
Limited control
✅ Conditional Access MFA
Context-aware
Group-based
Microsoft-recommended
Exam concept:
Conditional Access evaluates MFA at sign-in, not permanently on the account.
Step 3 — Add an Exclusion (Admin Safety)
Edit the policy.
Under Users:
Include: IAM-Users
Exclude: IAM-Admins
Save changes.
Purpose:
Prevents accidental admin lockout and demonstrates least-privilege design.
Step 4 — Review Policy Scope Impact
Understand the behavior:
Users in IAM-Users → MFA required
Users in IAM-Admins → MFA excluded
Users outside both groups → Not affected
This demonstrates policy scope control.
Step 5 — Review Sign-In Evaluation Logic
Understand the Conditional Access flow:
User attempts sign-in
Policy scope is evaluated
Conditions are checked
Grant controls are enforced
Access is allowed or blocked
This logic is tested heavily on SC-300.


### Screenshots Included:




### What You Learned
MFA should be enforced using Conditional Access
Group-based targeting simplifies MFA management
Exclusions prevent administrative lockout
Policy scope directly affects access outcomes
Conditional Access evaluates decisions at sign-in
