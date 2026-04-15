# 🧪 Lab Walkthrough – Task 1: Configure Permissions on the Subscription

**Course:** Modernize and Optimize Your SOC Deployment with Microsoft Sentinel  
**Lab:** Lab 1 – Microsoft Sentinel Prerequisites  
**Task:** Task 1 of 2 — Configure Permissions on the Subscription  
**Estimated Time:** ~5 minutes  
**Difficulty:** Beginner  

---

## 🎯 Objective

Assign the **Contributor** role to the **Admin** user at the **Azure Subscription** scope using Azure Identity and Access Management (IAM). This grants the account sufficient privileges to deploy and configure Microsoft Sentinel resources in subsequent tasks.

---

## ✅ Prerequisites

Before starting this task, confirm the following:

- [ ] You are logged into the [Azure Portal](https://portal.azure.com) as a Global Administrator or User Access Administrator
- [ ] You have access to the **Contoso Labs4** tenant (`tflabs4.onmicrosoft.com`)
- [ ] At least one active subscription is visible (e.g., **Azure Subscription**)

---

## 📸 Step-by-Step Walkthrough

---

### ▶ Step 1 — Navigate to Subscriptions

**What to do:**
1. Open the [Azure Portal](https://portal.azure.com) — you will land on the Home page.
2. Under **Azure services**, locate and click the **Subscriptions** icon (yellow key icon).

**What you see:**  
A hover tooltip appears over the Subscriptions icon with options to "Learn more with Copilot" and "Free training from Microsoft."

> 💡 **Tip:** You can also type `Subscriptions` in the search bar at the top (shortcut: `G+/`) and select it from the results.

---

### ▶ Step 2 — Select the Target Subscription

**What to do:**
1. The Subscriptions list will load, showing all subscriptions your account has access to.
2. In this environment, you will see two subscriptions: **Azure Subscription** and **TFSUB001**.
3. Click on **Azure Subscription**.

**What you see:**  
A green guided tooltip appears prompting: *"Select Azure Subscription"*. Both subscriptions show **Account admin** as the role and **Active** status under the Tenant Root Group.

> ⚠️ **Note:** If you don't see a subscription, click **Switch directories** — you may be in the wrong Azure AD tenant.

---

### ▶ Step 3 — Open Access Control (IAM)

**What to do:**
1. After opening the **Azure Subscription** blade, look at the left-side navigation panel.
2. Click on **Access control (IAM)**.

**What you see:**  
A guided tooltip explains: *"Click on IAM to assign a new role to the subscription using Identity and Access Management (IAM)."*

> 📌 **Why IAM?** Azure IAM (Role-Based Access Control / RBAC) is the mechanism for controlling who can do what on Azure resources. Assigning a role here applies it at the subscription scope, meaning it cascades down to all resource groups and resources within.

---

### ▶ Step 4 — Open the Add Dropdown

**What to do:**
1. On the **Access control (IAM)** page, click the **+ Add** dropdown button in the top toolbar.

**What you see:**  
The green tooltip guides you: *"Click the + Add dropdown."* The dropdown will expand to reveal options including **Add role assignment**, **Add co-administrator**, etc.

---

### ▶ Step 5 — Select "Add Role Assignment"

**What to do:**
1. From the expanded **+ Add** dropdown, click **Add role assignment**.

**What you see:**  
The tooltip confirms: *"Select Add role assignment."* The **Add role assignment** option is highlighted with a red border for easy identification.

---

### ▶ Step 6 — Choose the Privileged Administrator Roles Tab

**What to do:**
1. The **Add role assignment** wizard opens, starting on the **Role** tab.
2. You will see two sub-tabs: **Job function roles** and **Privileged administrator roles**.
3. Click on the **Privileged administrator roles** tab.

**What you see:**  
The tooltip instructs: *"Select the Privileged administrator roles tab."* The Job function roles tab is selected by default.

> ℹ️ **Understanding the difference:**
> - **Job function roles** = Narrowly scoped roles for specific services (e.g., `Security Reader`, `Log Analytics Contributor`)
> - **Privileged administrator roles** = Broad built-in roles: **Owner**, **Contributor**, **Reader**

---

### ▶ Step 7 — Select the Contributor Role

**What to do:**
1. On the **Privileged administrator roles** tab, you will see a list of roles.
2. Click on **Contributor** to select it (it will highlight in blue).

**What you see:**  
The tooltip confirms: *"Select Contributor."* You can see its description: *"Grants full access to manage all resources, but does not allow you to assign roles in Azure RBAC..."*

| Role | Type | Category |
|------|------|----------|
| Owner | BuiltInRole | General |
| **Contributor** ✅ | BuiltInRole | General |

> ⚠️ **Azure warns:** *"Can a job function role with less access be used instead?"* — For production, always evaluate if a narrower role is appropriate.

---

### ▶ Step 8 — Click Next to Proceed to Members

**What to do:**
1. With **Contributor** selected, click the **Next** button at the bottom of the page.

**What you see:**  
The tooltip says: *"Select Next."* This takes you to the **Members** tab of the wizard.

---

### ▶ Step 9 — Select the Member to Assign

**What to do:**
1. On the **Members** tab, verify **Assign access to** is set to `User, group, or service principal`.
2. Click **+ Select members**.
3. A **Select members** panel slides in from the right side.
4. In the search box, search for `Admin` or scroll to find **Admin** (`tadmin@tflabs4.onmicrosoft.com`).
5. Click on **Admin** to select them — they will be highlighted in blue.
6. Click the **Select** button at the bottom of the panel.

**What you see:**  
The guided tooltip says: *"Select Admin."* The member list shows multiple users in the tenant. After selecting, the member will appear in the Members table below.

---

### ▶ Step 10 — Review and Assign

**What to do:**
1. Click **Review + assign** to move to the final confirmation step.
2. Review the role assignment summary:
   - **Role:** Contributor
   - **Scope:** Azure Subscription
   - **Member:** Admin (tadmin@tflabs4.onmicrosoft.com)
3. Click **Review + assign** again to finalize.

**What you see:**  
A green success notification appears in the top-right corner of the Azure Portal:

```
✅ Added Role assignment
Admin was added as Contributor for Azure Subscription.
```

A new guided tooltip also appears, saying:
> *"We will proceed to next task to register the required resource providers."*

---

## 🏁 Task Complete!

**Summary of what was accomplished:**

| Item | Value |
|------|-------|
| Role Assigned | Contributor |
| Assigned To | Admin (tadmin@tflabs4.onmicrosoft.com) |
| Scope | Azure Subscription (Contoso Labs4) |
| Result | ✅ Role assignment successful |

---

## 🔍 Verification Steps (Optional)

To confirm the assignment was applied:
1. Stay on the **Access control (IAM)** page.
2. Click the **Role assignments** tab.
3. Filter by **Admin** user or the **Contributor** role.
4. Confirm **Admin** appears with **Contributor** at the **Subscription** scope.

---

## ➡️ Next Step

Proceed to **Task 2 – Register Required Resource Providers** to prepare the Azure subscription for Microsoft Sentinel deployment.

---

## 📚 Additional Resources

- [Azure built-in roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)
- [Assign Azure roles using the Azure portal](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal)
- [Microsoft Sentinel roles and permissions](https://learn.microsoft.com/en-us/azure/sentinel/roles)
- [Best practices for Azure RBAC](https://learn.microsoft.com/en-us/azure/role-based-access-control/best-practices)

---

*Walkthrough documented by: **Reduan Islam Badhon***  
*Based on: Microsoft Partner Skilling Hub — Modernize and optimize your SOC deployment with Microsoft Sentinel*
