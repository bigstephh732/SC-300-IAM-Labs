## SC-300 — Lab 9: App Registrations (Application Identity)
## Phase: Phase 3 – Application Access

### Goal
To create an application registration in Microsoft Entra ID, understand application identities, and learn how permissions and consent are used to secure application access.


### Why this lab matters
Applications don’t log in like users — they authenticate using application identities.
This lab teaches:
How apps are represented in Entra ID
Difference between app objects and service principals
How permissions and consent control access


### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab environment only)
Portal: https://entra.microsoft.com

 
 ### Steps

 ### Step 1 — Navigate to App Registrations
Go to:
Entra ID → App registrations
Review:
All applications list
Owned applications tab


### Step 2 — Create a New App Registration
Click New registration and configure:
Name: Lab-App-Registration
Supported account types:
Single tenant (this organizational directory only)
Redirect URI: Leave blank
Click Register.


### Step 3 — Review Application Overview
On the app’s Overview page, observe:
Application (client) ID
Directory (tenant) ID
Object ID
Understand:
The app registration represents the application’s identity in Entra ID.


### Step 4 — Review App Authentication Options
Navigate to:
Certificates & secrets
Observe:
Client secrets
Certificates
⚠️ Do NOT create a secret for this lab.
Understand:
Applications authenticate using secrets or certificates, not passwords.


### Step 5 — Review API Permissions
Navigate to:
API permissions
Observe:
Delegated permissions
Application permissions
Consent status
Understand:
Delegated permissions → App acts on behalf of a user
Application permissions → App acts independently


### Step 6 — Understand Service Principals
Key concept (exam critical):
An app registration defines the application.
A service principal represents the app inside a tenant.


### Screenshots Include:
App registrations list,
App overview page,
Certificates & secrets page,
API permissions page


### What You Learned
Applications have identities in Entra ID,
App registrations define application identity,
Apps authenticate using secrets or certificates,
Permissions control what apps can access,
Service principals represent apps in tenants
