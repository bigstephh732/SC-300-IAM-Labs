## SC-300 — Lab 11: Single Sign-On (SSO) Concepts & Configuration
### Phase: Phase 3 – Application Access


### Goal
To understand how Single Sign-On (SSO) works in Microsoft Entra ID, review common SSO methods, and recognize when each method is used.


### Why this lab matters
SSO reduces:
Password fatigue
Credential exposure
Authentication complexity
SC-300 focuses on:
Which SSO method to choose
Where SSO is configured
How identity is validated
You must understand flows, not just clicks.


### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Enterprise application created (Lab 10)
Portal: https://entra.microsoft.com


### Steps

### Step 1 — Navigate to Single Sign-On
Go to:
Entra ID → Enterprise applications → Lab-App-Registration → Single sign-on  
You’ll see SSO options:
SAML
OpenID Connect / OAuth 2.0
Password-based
Linked
Disabled


### Step 2 — Understand SSO Methods (Exam Critical)
SAML  
Claims-based authentication
Common with enterprise SaaS apps
Uses certificates
Browser-based

OAuth 2.0 / OpenID Connect  
Token-based authentication
Modern apps and APIs
Used with app registrations
Preferred for new applications

Password-based  
Stores credentials in Entra
Least secure
Legacy apps only

*Exam tip:
Microsoft prefers OIDC/OAuth over SAML for modern apps.


### Step 3 — Review Claims & Attributes (Conceptual)
If SAML is selected, you’ll see:
Claims mapping
Attributes sent to the app
Understand:
Claims are how identity information is passed to applications.
(No configuration required.)


### Step 4 — Understand SSO Authentication Flow
Understand this flow:
User attempts to access app
App redirects to Entra ID
Entra authenticates user
Token or assertion issued
App grants access
This flow is frequently tested.


### Step 5 — Review Where SSO Is Controlled
Key distinction:
App registrations → Identity & permissions
Enterprise applications → Access & SSO
This difference matters on the exam.


### What You Learned
SSO allows users to authenticate once and access multiple apps
Entra ID supports multiple SSO methods
OAuth/OIDC is preferred for modern apps
SAML is common for enterprise SaaS
SSO is configured in Enterprise Applications
Claims pass identity information to apps
