## SC-300 — Lab 7: Sign-In Logs & Conditional Access Troubleshooting

### Phase: 
Phase 2 – Authentication & Conditional Access

### Goal
To review Microsoft Entra sign-in logs in order to understand how to troubleshoot authentication and Conditional Access decisions.

### Why this lab matters
In real environments, users don’t say “Conditional Access failed.”
They say “I can’t log in.”
IAM administrators must be able to:
Interpet sign-in logs,
Identify why access was blocked or challenged,
Explain Conditional Access decisions,
Fix misconfigured policies


### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Conditional Access policies enabled
Portal: https://entra.microsoft.com


### Steps

### Step 1 - Navigate to sign-in Logs
Entra ID → Monitoring → Sign-in logs  

You should see a list of recent authentication attempts.  

### Step 2 — Review a Sign-In Event

Click a sign-in record and review:  
	•	User  
	•	Application  
	•	Status (Success / Failure)  
	•	Authentication details  
	•	Conditional Access tab  

Purpose:  
Understand what information is available for each authentication attempt.  


## Step 3 — Review Conditional Access Details

Inside a sign-in event, click the Conditional Access tab.  

Observe:  
	•	Whether Conditional Access was applied  
	•	Policy name (if applicable)  
	•	Result (Success, Failure, Not applied)  

Important concept:  
Even if no policy is enforced, the log still records the evaluation.


## Step 4 — Review Authentication Details

Click the Authentication Details tab.  

Observe:  
	•	Authentication method used  
	•	MFA requirement status  
	•	Step-by-step authentication flow  

Purpose:  
Understand how Microsoft records MFA usage and authentication methods.


## Step 5 — Understand Troubleshooting Flow

When a user reports access issues, administrators typically:  
	1.	Check sign-in logs  
	2.	Review Conditional Access evaluation  
	3.	Review authentication details  
	4.	Identify failure reason or applied control  

This is the standard troubleshooting workflow.  

### What You Learned
-How to access and interpret sign-in logs  
-How Conditional Access decisions are recorded  
-How to identify why MFA was required or skipped  
-How to troubleshoot login issues  
-Why logs are essential for IAM operations  

## Screenshots Include:
-Signin-logs  
-Signin-overview  
-Ca-tab  
-Auth-details  


