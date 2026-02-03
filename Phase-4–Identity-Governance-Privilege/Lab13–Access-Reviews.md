## SC-300 — Lab 13: Access Reviews
### Phase: Phase 4 – Identity Governance & Privilege

### Goal
To create and review Access Reviews in Microsoft Entra ID in order to regularly validate user access and remove unnecessary permissions.


### Why this lab matters
Over time, users accumulate access they no longer need.  
Access Reviews:  
Identify excess permissions  
Enforce least privilege  
Support audits and compliance  
SC-300 tests how Access Reviews are configured and why they exist.  


### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab environment only)
Portal: https://entra.microsoft.com


### Steps

### Step 1 — Navigate to Access Reviews  
Go to:  
Entra ID → Identity Governance → Access reviews  
Click New access review.  


### Step 2 — Choose Review Type  
Select:  
Teams + Groups  
Click Next.  
*Exam note:  
Access Reviews can target groups, apps, or privileged roles.  


### Step 3 — Configure Scope  
Scope: Selected groups  
Group: IAM-Users  
Click Next.  


### Step 4 — Reviewers  
Choose:  
Self-review  
(Users review their own access for lab simplicity.)  
Understand other options:  
Group owners  
Selected reviewers  


### Step 5 — Review Settings 
Configure:  
Duration: 7 days  
Upon completion: Automatically apply results  
If reviewers don’t respond: Remove access  
This demonstrates automated governance.  


### Step 6 — Start the Review  
Review settings and click Create.  


### Step 7 — Understand Review Outcomes  
Possible outcomes:  
Access approved → retained  
Access denied or no response → removed  
This is access cleanup.  

### Screenshots Include:  
Access reviews overview  
New access review configuration  
Group selection screen  
Review settings  
Active access review  
