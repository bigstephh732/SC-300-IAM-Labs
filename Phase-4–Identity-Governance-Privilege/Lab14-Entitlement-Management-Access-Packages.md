## SC-300 — Lab 14: Entitlement Management & Access Packages
### Phase: Phase 4 – Identity Governance & Privilege

### Goal
To understand Entitlement Management and create an Access Package that automates how users request, receive, and lose access across their lifecycle.  


### Why this lab matters
Manual access assignment does not scale.  
Entitlement Management:  
Automates onboarding/offboarding  
Reduces human error  
Enforces time-bound access  
Supports compliance  
This is enterprise IAM design and appears on SC-300 as scenario-based questions.  


### Lab Environment 
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab environment only)
Portal: https://entra.microsoft.com

### Steps

### Step 1 — Navigate to Entitlement Management
Go to:  
Entra ID → Identity Governance → Entitlement management  
Review sections:  
Access packages  
Catalogs  
Requests  
Assignment policies  


### Step 2 — Create a Catalog
Catalogs group access resources.  
Click Catalogs  
Select New catalog  
Name:  
IAM-Lab-Catalog  
Description:  
Catalog for IAM lab access packages  
Create  


### Step 3 — Create an Access Package
Go to Access packages  
Click New access package  
Name:  
IAM-Users-Access-Package  
Catalog:  
IAM-Lab-Catalog  


### Step 4 — Add Resource Roles
Add access resources:  
Groups  
Select: IAM-Users  
Role: Member  
(Optional: Add apps if available.)  
Understand:  
Access packages bundle multiple access resources together.  


### Step 5 — Configure Request Policy
Configure:  
Who can request: Users in this tenant  
Approval required: No (lab simplicity)  
Access duration: 30 days  
Expiration: Remove access automatically  
This enforces time-bound access.  


### Step 6 — Review Assignment & Lifecycle
Understand lifecycle behavior:  
User requests access  
Access is granted automatically  
Access expires after set duration  
No manual cleanup required  
This prevents access creep.  

### What You Learned
-Entitlement Management automates access lifecycle  
-Catalogs organize access resources  
-Access packages bundle permissions  
-Request policies control who gets access  
-Expiration removes access automatically  

### Screenshots Include:
-Entitlement Management overview  
-Catalog created  
-Access package overview  
-Resource roles (IAM-Users group)  
-Assignment policy settings  
