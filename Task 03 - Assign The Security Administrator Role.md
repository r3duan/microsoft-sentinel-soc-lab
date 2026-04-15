# 🧪 Lab Walkthrough – Task 3: Assign the Security Administrator Role

**Course:** Modernize and Optimize Your SOC Deployment with Microsoft Sentinel  
**Lab:** Lab 1 – Microsoft Sentinel Prerequisites  
**Task:** Task 3 of 3 — Assign the Security Administrator Role  
**Estimated Time:** ~5 minutes  
**Difficulty:** Beginner  

---

## 🎯 Objective

Grant the **Security Administrator** directory role to the **Admin** user account (`tadmin@tflabs4.onmicrosoft.com`) via **Microsoft Entra ID**. This role provides the necessary permissions for upcoming security configuration activities in Microsoft Sentinel and Microsoft Defender.

> ⚠️ **Important distinction:** This task assigns a **Microsoft Entra ID directory role** (identity-level), which is different from an **Azure RBAC role** (resource-level) assigned in Task 1. Both are required for a complete Sentinel deployment.

---

## ✅ Prerequisites

- [ ] Task 1 (Configure Permissions on Subscription) completed ✅
- [ ] Task 2 (Register Required Resource Providers) completed ✅
- [ ] You are logged into the [Azure Portal](https://portal.azure.com)
- [ ] Admin account has **Global Administrator** to assign Entra ID roles

---

## 📸 Step-by-Step Walkthrough

---

### ▶ Step 1 — Task Overview

The lab presents **Task 3 – Assign the Security Administrator Role** with the following description:

> *"In this task, we will grant the Security Administrator role to the Admin account which we are using, to ensure it has the required permissions for upcoming security configuration activities."*

Click **Start Task** to begin.

![Task 3 Start Screen](images/task3-step1-start.png)

---

### ▶ Step 2 — Navigate to Microsoft Entra ID

1. From the Azure Portal home page, look at the **Azure services** row.
2. Click on **Microsoft Entra ID** (the blue diamond icon).

![Select Microsoft Entra ID](images/task3-step2-entra-id.png)

> 💡 The guided tooltip instructs: *"Select Microsoft Entra ID."*  
> Microsoft Entra ID is the new name for Azure Active Directory (Azure AD) — it is the identity and access management service for your tenant.

---

### ▶ Step 3 — Select the Admin User

1. Microsoft Entra ID opens. Navigate to **Users** → **All users** from the left panel (or it may open directly to the Users list).
2. From the list of 10 users, locate and click on **Admin** (`tadmin@tflabs4.on...`).

![Select Admin User](images/task3-step3-select-admin.png)

> The guided tooltip confirms: *"From the list of users, Select Admin."*  
> Admin is shown as a **Member** type user with identity `tflabs4.onmicrosoft.com`.

---

### ▶ Step 4 — Open Assigned Roles

1. Inside the **Admin** user profile, look at the left navigation panel.
2. Click on **Assigned roles**.

![Open Assigned Roles](images/task3-step4-assigned-roles.png)

> The tooltip instructs: *"Click on Assigned roles to add a new role assignment to the Admin account."*  
> You can see the Admin user currently has **1** assigned role (Global Administrator), along with **2** Group memberships and **5** Assigned licenses.

---

### ▶ Step 5 — Click + Add Assignments

1. On the **Admin | Assigned roles** page, you can see the existing role: **Global Administrator**.
2. Click the **+ Add assignments** button in the top toolbar.

![Click Add Assignments](images/task3-step5-add-assignments.png)

> The tooltip prompts: *"Select + Add assignments."*  
> The Admin account currently only has the **Global Administrator** role — we need to add **Security Administrator** as well.

---

### ▶ Step 6 — Search for Security Administrator

1. A **Directory roles** panel slides in from the right.
2. In the search box, type `security Administrator`.
3. Two roles appear in the results:
   - **Cloud App Security Administrator** — manages Cloud App Security only
   - **Security Administrator** — broader role covering Entra ID and Office 365 security
4. Click the **checkbox** next to **Security Administrator**.

![Search and Select Security Administrator](images/task3-step6-search-role.png)

> The tooltip instructs: *"Click on the checkbox for Security Administrator."*

| Role | Description |
|---|---|
| Cloud App Security Administrator | Manages Cloud App Security product only |
| **Security Administrator ✅** | Can read security info, reports, and manage configuration in Entra ID and Office 365 |

---

### ▶ Step 7 — Click Add to Confirm

1. With **Security Administrator** checked (checkbox turns blue ✅), the **Add** button at the bottom of the panel activates.
2. Click **Add** to apply the role assignment.

![Click Add to Confirm](images/task3-step7-click-add.png)

> The tooltip guides: *"Click on the Add button to confirm and apply the role assignment."*

---

### ▶ Step 8 — Role Successfully Assigned

1. The Directory roles panel closes.
2. A green success notification appears in the top-right corner of the portal.
3. The **Assigned roles** list now shows two roles for the Admin user.

![Security Administrator Successfully Assigned](images/task3-step8-success.png)

```
✅ Successfully added assignment
Successfully added assignment 'Security Administrator'.
```

**Admin's assigned roles after this task:**

| Role | Resource Name | Resource Type | Assignment Path | Type |
|---|---|---|---|---|
| Global Administrator | Directory | Organization | Direct | Built-in |
| **Security Administrator** | **Directory** | **Organization** | **Direct** | **Built-in** |

---

### ▶ Step 9 — Task Complete

The lab displays a final confirmation overlay:

> *"The selected role is now assigned to the Admin user."*

Click **OK** to complete the task.

![Task 3 Complete](images/task3-step9-complete.png)

---

## 🏁 Lab 1 Complete — All 3 Tasks Done!

| Task | Description | Status |
|---|---|---|
| Task 1 | Configure Permissions on the Subscription | ✅ Complete |
| Task 2 | Register Required Resource Providers | ✅ Complete |
| Task 3 | Assign the Security Administrator Role | ✅ Complete |

---

## 🔍 Key Concept: Azure RBAC vs. Entra ID Roles

A common point of confusion in Sentinel deployments is the difference between these two role systems:

| | Azure RBAC (Task 1) | Entra ID Roles (Task 3) |
|---|---|---|
| **Scope** | Azure resources (subscriptions, RGs) | Identity & Microsoft 365 services |
| **Example role** | Contributor | Security Administrator |
| **Where to manage** | Subscription → Access control (IAM) | Entra ID → Users → Assigned roles |
| **Why needed** | Deploy & manage Azure resources | Read security data, configure Defender policies |

Both are required to fully operate Microsoft Sentinel.

---

## ➡️ What's Next

With all Lab 1 prerequisites complete, the environment is ready for **Lab 2 — Deploying Microsoft Sentinel** (creating a Log Analytics Workspace and enabling Sentinel).

---

## 📚 Additional Resources

- [Security Administrator role in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference#security-administrator)
- [Assign Microsoft Entra roles to users](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/manage-roles-portal)
- [Microsoft Sentinel roles and permissions](https://learn.microsoft.com/en-us/azure/sentinel/roles)
- [Difference between Azure RBAC and Entra ID roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/rbac-and-directory-admin-roles)

---

*Walkthrough documented by: **Reduan Islam Badhon***  
*Based on: Microsoft Partner Skilling Hub — Modernize and optimize your SOC deployment with Microsoft Sentinel*
