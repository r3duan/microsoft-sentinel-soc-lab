# Getting Started with Microsoft Sentinel: Configuring Azure Subscription Permissions

**Published by:** Reduan Islam Badhon  
**Series:** Modernize and Optimize Your SOC with Microsoft Sentinel  
**Tags:** `Azure` `Microsoft Sentinel` `IAM` `RBAC` `SOC` `Security` `Cloud`

---

When building a modern Security Operations Center (SOC) on Azure, getting your permissions model right from day one is non-negotiable. Before you can deploy Microsoft Sentinel, connect data sources, or configure analytics rules, the accounts doing that work need the right level of access at the right scope.

In this first post of my lab walkthrough series — based on the **Microsoft Partner Skilling Hub course: Modernize and Optimize Your SOC Deployment with Microsoft Sentinel** — I'll walk you through **Task 1: Configure Permissions on the Subscription**. It's a foundational step, but one that trips up many practitioners who skip the RBAC planning phase.
<img width="1918" height="933" alt="image" src="https://github.com/user-attachments/assets/98decb3c-1ded-46b8-9e45-c3d38262d7ae" />


---

## Why Subscription-Level Permissions Matter for Sentinel

Microsoft Sentinel is deployed into a **Log Analytics workspace**, which lives inside a **Resource Group**, which lives inside a **Subscription**. When you're setting up a new Sentinel environment, you need to be able to create and configure resources across all of those layers.

The **Contributor** role at the subscription scope is a common starting point for lab environments. It grants full ability to create and manage Azure resources without the elevated privilege of being able to assign roles to others. Think of it as the "do everything except grant access" role.

For production environments, Microsoft recommends using the principle of least privilege — scoping roles to the minimum necessary and using dedicated Sentinel-specific roles like `Microsoft Sentinel Contributor`. But for this lab, Contributor at the subscription scope gets us up and running quickly.

---

## What We're Doing in Task 1

**Goal:** Assign the Contributor role to the Admin user (`tadmin@tflabs4.onmicrosoft.com`) on the **Azure Subscription** using Azure RBAC through the IAM blade.

**Environment:** Contoso Labs4 tenant (`tflabs4.onmicrosoft.com`)

---

## The Walkthrough

### 1. Find Your Subscription

From the Azure portal home, navigate to **Subscriptions**. You'll see the subscriptions your account has RBAC access to manage. In this lab environment, we have two: **Azure Subscription** and **TFSUB001**. We'll be working with **Azure Subscription**.

<img width="1836" height="931" alt="image" src="https://github.com/user-attachments/assets/f29b1888-4bfb-435a-8563-a6a9420534d6" />


> **Pro Tip:** If you don't see your subscription, you may be looking in the wrong directory. Use the **Switch directories** link to check.

### 2. Open IAM on the Subscription

Click into **Azure Subscription**, then select **Access control (IAM)** from the left navigation. This blade is your central control panel for all RBAC operations at this scope — you can view current role assignments, check access for specific users, and add or remove assignments.

<img width="1776" height="853" alt="image" src="https://github.com/user-attachments/assets/111c5db2-628a-459d-a5f2-1b6c61a67651" />


### 3. Add a Role Assignment

Click **+ Add → Add role assignment**. The wizard that opens walks you through three steps: Role, Members, and Review + assign.

<img width="1775" height="854" alt="image" src="https://github.com/user-attachments/assets/11d9c19e-92ac-4e9d-9e40-995062f0841e" />


### 4. Choose the Right Role

On the **Role** tab, switch to the **Privileged administrator roles** tab. Here you'll find the three classic Azure built-in roles:

| Role | What It Does |
|------|-------------|
| **Owner** | Full access + can assign roles to others |
| **Contributor** | Full resource management, no role assignments |
| **Reader** | View-only access to everything |

Select **Contributor** and click **Next**.

<img width="1778" height="858" alt="image" src="https://github.com/user-attachments/assets/c1783255-0f63-4d77-a733-d6b3a349b3f6" />


### 5. Select the Member

On the **Members** tab, the assignment type defaults to **User, group, or service principal** — which is what we want. Click **+ Select members**, search for **Admin**, and select `tadmin@tflabs4.onmicrosoft.com`. Click **Select** to add them.

<img width="1775" height="848" alt="image" src="https://github.com/user-attachments/assets/ae002439-29a9-4a51-8702-e8d0a12f4fb7" />



### 6. Review and Confirm

Click **Review + assign** twice to commit the change. Within seconds, you should see a green notification in the top-right corner:

> ✅ *"Admin was added as Contributor for Azure Subscription."*


<img width="1775" height="848" alt="image" src="https://github.com/user-attachments/assets/e286c881-60ba-4f7a-84df-aff6d6b905fa" />




Task 1 is complete.

---

## Key Takeaways

**RBAC is foundational.** Before any Sentinel deployment activity can happen, the right permissions need to be in place. Skipping this step leads to cryptic "Authorization failed" errors later in the process.

**Scope matters.** We assigned the role at the **subscription scope**, which means the Admin user now has Contributor access to everything in that subscription. In production, you'd likely scope this more narrowly — to a resource group or even a specific workspace.

**IAM is your audit trail too.** The Role assignments tab in IAM gives you a full view of who has what access. Make it a habit to review this periodically as part of your SOC hygiene.

---

## What's Next

With permissions configured, the lab moves to **Task 2: Register Required Resource Providers** — ensuring the Azure subscription is ready to provision the specific resource types that Microsoft Sentinel depends on.

Stay tuned for the next post in this series.

---

## About This Series

This series documents my hands-on progress through the **Microsoft Partner Skilling Hub** course: *Modernize and optimize your SOC deployment with Microsoft Sentinel*. All lab walkthroughs are based on real simulated environments provided through the LevelUp platform.

**Connect:** Share your own Sentinel deployment experiences in the comments or on LinkedIn!

---

*© Reduan Islam Badhon — Educational content based on Microsoft Partner training materials.*
