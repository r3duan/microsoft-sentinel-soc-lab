# 🛡️ Modernize and Optimize Your SOC Deployment with Microsoft Sentinel

> **Course:** Modernize and optimize your SOC deployment with Microsoft Sentinel  
> **Platform:** Microsoft Partner Skilling Hub (LevelUp)  
> **Level:** Intermediate | **Duration:** 6 hours | **Cost:** Free  

---

## 📋 Overview

This repository documents the hands-on lab walkthroughs for the **Microsoft Sentinel SOC Deployment** course. It covers deploying, configuring, and optimizing Microsoft Sentinel using the unified experience within the Microsoft Defender portal. Labs are designed to help technical teams operationalize an AI-ready SOC with improved visibility and integrated Defender workflows.

---

## 🗂️ Lab Index

| Lab | Task | Description | Status |
|-----|------|-------------|--------|
| Lab 1 | Task 1 | Configure Permissions on the Subscription | ✅ Documented |
| Lab 1 | Task 2 | Register Required Resource Providers | 🔜 Coming Soon |

---

## 🔐 Lab 1 – Setting Up Microsoft Sentinel Prerequisites

### Task 1: Configure Permissions on the Subscription

**Objective:** Assign the **Contributor** role to the Admin user on the Azure Subscription using Identity and Access Management (IAM). This ensures the account has sufficient privileges to deploy and manage Microsoft Sentinel resources.

**Prerequisites:**
- Access to the [Azure Portal](https://portal.azure.com)
- An active Azure Subscription (e.g., `Contoso Labs4 / tflabs4.onmicrosoft.com`)
- Global Administrator or User Access Administrator permissions

---

### 📝 Step-by-Step Instructions

#### Step 1 – Navigate to Subscriptions
1. Open the [Azure Portal](https://portal.azure.com).
2. From the **Azure services** section on the home page, click **Subscriptions**.

> 💡 You can also search for "Subscriptions" in the top search bar (shortcut: `G+/`).

---

#### Step 2 – Select the Target Subscription
1. On the Subscriptions page, you will see a list of available subscriptions.
2. Click on **Azure Subscription** (the primary subscription used for this lab).

> ⚠️ Subscriptions are filtered by RBAC permissions. If you don't see your subscription, click **Switch directories**.

---

#### Step 3 – Open Access Control (IAM)
1. Inside the **Azure Subscription** blade, locate the left-hand navigation menu.
2. Click on **Access control (IAM)**.

> 📌 IAM is where all role-based access control (RBAC) configurations are managed for the subscription scope.

---

#### Step 4 – Add a Role Assignment
1. On the **Access control (IAM)** page, click the **+ Add** dropdown button in the top toolbar.
2. Select **Add role assignment** from the dropdown.

---

#### Step 5 – Select the Role
1. On the **Add role assignment** wizard, go to the **Role** tab.
2. Switch from **Job function roles** to the **Privileged administrator roles** tab.
3. From the list, select **Contributor**.

> ℹ️ The **Contributor** role grants full access to manage all Azure resources but does **not** allow assigning roles to others in Azure RBAC.

4. Click **Next** to proceed to the Members tab.

---

#### Step 6 – Assign to a Member
1. On the **Members** tab, confirm **Assign access to** is set to `User, group, or service principal`.
2. Click **+ Select members**.
3. In the **Select members** panel that appears on the right, search for and select **Admin** (`tadmin@tflabs4.onmicrosoft.com`).
4. Click **Select** to confirm.

---

#### Step 7 – Review and Assign
1. Click **Review + assign** to review your settings.
2. Confirm the role assignment and click **Review + assign** again to finalize.

✅ **Success:** A notification will appear confirming — *"Admin was added as Contributor for Azure Subscription."*

---

### 🎯 Expected Outcome

After completing Task 1:
- The **Admin** user has been granted the **Contributor** role at the **Azure Subscription** scope.
- The environment is now ready for registering required resource providers in **Task 2**.

---

## 🔗 References

- [Azure RBAC Documentation](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview)
- [Microsoft Sentinel Documentation](https://learn.microsoft.com/en-us/azure/sentinel/)
- [Add or remove Azure role assignments](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal)
- [Microsoft Partner Skilling Hub](https://partner.microsoft.com/en-us/training/assets)

---

## 👤 Author

**Reduan Islam Badhon**  
Microsoft Partner Skilling Hub – SOC Modernization Lab Series  

---

## 📄 License

This documentation is for educational purposes, based on the Microsoft Partner Skilling Hub course content.
