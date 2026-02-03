### SC-300 — Lab 12: Privileged Identity Management (PIM)
### Phase: Phase 4 – Identity Governance & Privilege


### Goal
To understand Privileged Identity Management (PIM) and configure just-in-time (JIT) administrative access to reduce standing privilege risk.


### Why this lab matters
Permanent admin access is one of the biggest security risks.
PIM:
Removes always-on admin privileges
Requires elevation only when needed
Adds approval, MFA, and auditing
This is Zero Trust for admins and heavily tested on SC-300.



### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab environment only)
Portal: https://entra.microsoft.com


### Steps

### Step 1 — Access Privileged Identity Management
Navigate to:
Entra ID → Identity Governance → Privileged Identity Management
Review sections:
My roles
Roles
Assignments
Alerts


### Step 2 — Understand Eligible vs Active Roles (Critical)
Understand this clearly:
  Eligible role
  User can activate the role
  No permissions until activated
  Active role
  User currently has permissions
  Time-limited
  *Exam tip:
PIM replaces permanent admin access.


### Step 3 — Make a User Eligible for an Admin Role
Go to:
PIM → Roles → Azure AD roles → User Administrator  
Click Add assignments  
Select user: lab-admin  
Assignment type: Eligible  
Duration: Permanent  
Save  
You have NOT given admin access yet — only eligibility.  


### Step 4 — Activate the Role (Just-in-Time Access)
Sign in as lab-admin.  
Go to:  
PIM → My roles
Select User Administrator
Click Activate
Provide:
Reason
MFA (if prompted)
Set duration (e.g., 1 hour)
Activate
The role becomes temporarily active.


### Step 5 — Verify Role Activation
While active:
lab-admin can manage users
Role expires automatically
After expiration:
Access is removed
No manual cleanup required
This is JIT privilege.


### Step 6 — Review Audit & Security Benefits
Understand:  
-All activations are logged  
-Approval can be required  
-MFA can be enforced  
-Alerts flag risky behavior  
-This is enterprise-grade security.

### What You Learned
-Standing admin access is dangerous  
-PIM enables just-in-time admin access  
-Eligible ≠ Active roles  
-Admin privileges can be time-limited  
-PIM supports auditing and compliance  

### Screenshots Include:
-PIM overview page  
-Azure AD roles list  
-Eligible role assignment  
-Role activation screen  
-Active role confirmation  
