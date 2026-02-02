## SC-300 — Lab 10: Enterprise Applications (Access & SSO)
### Phase: Phase 3 – Application Access

### Goal
To understand how enterprise applications represent applications in use within a tenant, and how users and groups are assigned access for authentication and Single Sign-On (SSO).


### Why this lab matters
App registrations define what an app is.
Enterprise applications define how that app is used in a tenant.


### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab environment only)
Portal: https://entra.microsoft.com


### Steps

### Step 1 — Navigate to Enterprise Applications
Go to:
Entra ID → Enterprise applications
Review:
All applications list
App type filters (Enterprise / Gallery / Non-gallery)


### Step 2 — Locate Your App’s Service Principal
In the Enterprise applications list, search for:
Lab-App-Registration
Click the app.
Understand:
This entry is the service principal created automatically when the app registration was created.


### Step 3 — Review Enterprise Application Overview
On the app overview page, review:
Application ID
Object ID
Assignment required (Yes/No)
Sign-in status
Understand:
Enterprise applications control access, not application identity.


### Step 4 — Configure User & Group Assignment
Navigate to:
Users and groups
Click Add user/group
Select group: IAM-Users
Assign
Understand:
Assigning users or groups controls who can sign in to the app.


### Step 5 — Review Access Control Behavior
Understand this clearly:
If Assignment required = Yes
Only assigned users/groups can access the app
If Assignment required = No
All users can access the app
This is a common exam scenario.


### Step 6 — Review Single Sign-On (SSO)
Navigate to:
Single sign-on
Review available options:
SAML
OpenID Connect / OAuth
Password-based
Linked
Understand:
Enterprise applications manage SSO configuration.
(No configuration required for this lab.)


### Screenshots Included:
Enterprise applications list
Enterprise application overview
Users and groups assignment page
Assigned group (IAM-Users)
Single Sign-On options page

Suggested filenames:
lab10-enterprise-apps.png
lab10-enterprise-app-overview.png
lab10-users-groups.png
lab10-group-assigned.png
lab10-sso-options.png


### What You Learned
Enterprise applications represent apps in use within a tenant
Service principals are created automatically from app registrations
User and group assignments control access
Assignment required setting restricts access
Enterprise applications manage SSO

