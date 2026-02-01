## SC-300 — Lab 3: Administrative Roles & Least Privilege

## Phase: Phase 1 – Core Identity Foundation

## Goal

To understand Microsoft Entra administrative roles, apply the principle of least privilege, and safely assign limited administrative access without using Global Administrator unnecessarily.


## Why this lab matters

In real environments:
	•	Global Admin should be extremely rare
	•	Most admins use limited roles
	•	Over-permission is one of the biggest causes of breaches


## Lab Environment
	•	Microsoft Entra ID (cloud-only tenant)
	•	Role used: Global Administrator (lab tenant only)
	•	Portal: https://entra.microsoft.com



##  Steps



## Step 1 — Review Administrative Roles

Go to:

Entra ID → Roles & administrators

Review these built-in roles:
	•	Global Administrator
	•	Global Reader
	•	User Administrator
	•	Security Administrator
	•	Authentication Administrator

 Do not assign anything yet!

Purpose:
Understand that roles control administrative power, not application access.


## Step 2 — Assign a Limited Role (Safe)

Go to:

Entra ID → Roles & administrators → User Administrator
	1.	Click User Administrator
	2.	Select Add assignments
	3.	Choose lab-admin
	4.	Assign role

✅ This role allows:
	•	Create users
	•	Reset passwords
	•	Manage groups

❌ It cannot:
	•	Change Conditional Access
	•	Assign Global Admin
	•	Modify security policies

This is least privilege in action.



## Step 3 — Verify Role Assignment
	1.	Go to Entra ID → Users
	2.	Select lab-admin
	3.	Click Assigned roles

Confirm:
	•	User Administrator is listed
	•	No other admin roles exist



## Step 4 — Understand Role Scope

Important concept:

Roles can be assigned globally or scoped using administrative units.

For now:
	•	Your role is tenant-wide


## Step 5 — Review Why Least Privilege Matters

Understand clearly:
	•	Users should only have permissions they need
	•	Admin access should be temporary when possible
	•	Roles reduce blast radius during compromise

This is security fundamentals.



## Screenshots Include:

	1.	Roles & administrators page
	2.	User Administrator role page
	3.	Role assignment screen
	4.	lab-admin assigned roles page



lab03-roles-admins.png
lab03-user-admin-role.png
lab03-role-assignment.png
lab03-user-assigned-roles.png


## What You Learned
	•	Difference between users, groups, and roles
	•	Administrative roles define what actions an admin can perform
	•	Global Administrator should be highly restricted
	•	Least privilege reduces security risk
	•	Roles should match job responsibility


