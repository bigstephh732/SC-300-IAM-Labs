## SC-300 — Lab 8: Identity Protection & Risk-Based Policies
## Phase: 
Phase 2 – Authentication & Conditional Access

### Goal
To understand Microsoft Entra Identity Protection, including user risk and sign-in risk, and to review how risk-based policies automatically protect identities.

### Why this lab matters
Not all sign-ins are equal.
Identity Protection allows Entra ID to detect risky behavior (impossible travel, leaked credentials, unfamiliar sign-ins) and respond automatically.

### Lab Environment
Microsoft Entra ID (cloud-only tenant)
Microsoft Entra Admin Center
Role used: Global Administrator (lab environment only)
Portal: https://entra.microsoft.com

### Steps
### Step 1 — Navigate to Identity Protection
Go to:
Entra ID → Protection → Identity Protection
Review available sections:
Overview
Risky users
Risky sign-ins
Risk policies


### Step 2 — Understand Risk Types
Understand these clearly:
Sign-in risk
Risk detected during a specific sign-in attempt (e.g., unfamiliar location).
User risk
Risk associated with the user account itself (e.g., leaked credentials).
*Sign-in risk is event-based; user risk is identity-based.


### Step 3 — Review Risky Sign-Ins
Navigate to:
Identity Protection → Risky sign-ins
Observe:
Risk level (Low, Medium, High)
Detection type
Status
Even if empty, understand what would appear here in production.


### Step 4 — Review Risky Users
Navigate to:
Identity Protection → Risky users
Observe:
User risk level
Risk state
Remediation status
Understand:
User risk can persist across multiple sign-ins.


### Step 5 — Review Risk Policies
Navigate to:
Identity Protection → Risk policies
Review default or available policies, such as:
Sign-in risk policy
User risk policy
Understand typical actions:
Require MFA
Require password change
Block access


### Step 6 — Understand Identity Protection Integration
Key concept:
Identity Protection feeds risk signals into Conditional Access to enforce automated security responses.
This is a core Zero Trust principle.

