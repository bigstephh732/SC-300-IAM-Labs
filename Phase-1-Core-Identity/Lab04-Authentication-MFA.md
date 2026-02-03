
# SC-300 — Lab 4: Authentication Methods & MFA

## Phase: Phase 1 – Core Identity Foundation
Goal

To configure authentication methods in Microsoft Entra ID, enable Multi-Factor Authentication (MFA), and understand how strong authentication protects identities.


## Why this lab matters
Strong authentication protects identities and reduces the risk of credential-based attacks.
MFA is the single most effective identity security control.


## Lab Environment
	•	Microsoft Entra ID (cloud-only tenant)
	•	Microsoft Entra Admin Center
	•	Role used: Global Administrator (lab tenant only)
	•	Portal: https://entra.microsoft.com



## Steps


## Step 1 — Review Authentication Methods

Navigate to:

Entra ID → Protection → Authentication methods

Review available methods:
	•	Microsoft Authenticator
	•	SMS
	•	Voice call
	•	Temporary Access Pass (TAP)
	•	FIDO2 security keys
	•	Email OTP (for guests)

*Do NOT disable anything yet.

Purpose:
Understand which methods Entra supports and how authentication is controlled centrally.



## Step 2 — Enable Microsoft Authenticator
	1.	Click Microsoft Authenticator
	2.	Set Enable = Yes
	3.	Target:
	•	All users (lab tenant)
	4.	Save

Purpose:
Allows users to register and use the Authenticator app for MFA.


## Step 3 — Enable Temporary Access Pass (TAP)
	1.	Click Temporary Access Pass
	2.	Enable policy
	3.	Configure:
	•	Lifetime: 1 hour (recommended for lab)
	•	One-time use: Yes
	4.	Target: All users
	5.	Save

Purpose:
Used for onboarding users without passwords.


## Step 4 — Review Authentication Method Policies

Navigate back and observe:  
	•	Each method can be enabled/disabled  
	•	Policies are centrally controlled  
	•	Methods can be targeted by group  

Understand this concept:

Authentication methods define how users authenticate, not when.

(Conditional Access controls when — later labs.)


## Step 5 — Review User Authentication Methods
	1.	Go to Entra ID → Users  
	2.	Select lab-user1  
	3.	Click Authentication methods  

Observe:  
	•	No MFA registered yet  
	•	Methods are allowed but not enforced  

This distinction matters.  


## What You Learned
	•	Authentication methods are managed centrally in Entra ID
	•	MFA provides additional verification beyond passwords
	•	Microsoft Authenticator is the primary MFA method
	•	Temporary Access Pass supports secure onboarding
	•	Authentication methods ≠ Conditional Access
	•	Users can authenticate only using enabled methods

	
## Screenshots Include:
 	1.	Authentication methods overview page
	2.	Microsoft Authenticator enabled
	3.	Temporary Access Pass enabled
	4.	User authentication methods page

