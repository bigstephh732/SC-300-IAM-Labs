## SC-300 — Lab 2: Users & Groups Management



##  Lab Name

Lab 2 – Create and Manage Users & Groups

## Phase

Phase 1: Core Identity Foundation



## Goal

To create cloud-based users and security groups in Microsoft Entra ID and understand how group-based access management is used to scale identity and access control in enterprise environments.



## Lab Environment
	•	Microsoft Entra admin center
	•	URL: https://entra.microsoft.com
	•	Tenant type: Cloud-only lab tenant
	•	Role used: Global Administrator (lab environment only)



## Steps



Step 1: Create Cloud Users
	1.	Navigate to Entra ID → Users
	2.	Select New user → Create new user
Display Name	Username	Purpose
Lab User 1	lab-user1@tenant.onmicrosoft.com	Standard user
Lab User 2	lab-user2@tenant.onmicrosoft.com	Standard user
Lab Admin	lab-admin@tenant.onmicrosoft.com	Admin test user
4.	Record temporary passwords for testing.

Purpose:
Users represent individual identities that authenticate to Entra ID.



Step 2: Verify Users
	1.	Confirm users appear in the Users list
	2.	Select one user and review:
	•	Account status
	•	Assigned roles (none)
	•	Authentication methods

Purpose:
Verify that users were created successfully and are cloud-only identities.

⸻

Step 3: Create Security Groups
	1.	Navigate to Entra ID → Groups
	2.	Select New group
	3.	Create the following groups:

Group 1
	•	Group type: Security
	•	Name: IAM-Users
	•	Membership type: Assigned
	•	Members: lab-user1, lab-user2

Group 2
	•	Group type: Security
	•	Name: IAM-Admins
	•	Membership type: Assigned
	•	Members: lab-admin

Purpose:
Security groups are used to assign access and policies at scale.

⸻

Step 4: Review Group Membership
	1.	Open the IAM-Users group
	2.	Confirm correct users are listed under Members
	3.	Review group overview settings

Purpose:
Group membership determines access and policy scope.

Include:
	1.	Users list showing created users
	2.	Individual user profile page
	3.	Groups list (All groups)
	4.	Group overview page (IAM-Users)
	5.	Group members page

⸻

##  What You Learned
	•	How to create cloud-only users in Microsoft Entra ID
	•	How to verify user identities and account status
	•	How to create and manage security groups
	•	Difference between users and groups
	•	Why group-based access is preferred over direct user assignments
	•	How group membership simplifies identity lifecycle management
