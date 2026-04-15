# 🧪 Lab Walkthrough – Task 2: Register Required Resource Providers

**Course:** Modernize and Optimize Your SOC Deployment with Microsoft Sentinel  
**Lab:** Lab 1 – Microsoft Sentinel Prerequisites  
**Task:** Task 2 of 2 — Register Required Resource Providers  
**Estimated Time:** ~10 minutes  
**Difficulty:** Beginner  

---

## 🎯 Objective

Verify and register the four required Azure Resource Providers needed for Microsoft Sentinel deployment:

| Resource Provider | Purpose |
|---|---|
| **Microsoft.Insights** | Azure Monitor & diagnostics |
| **Microsoft.Web** | App Service & Logic Apps host |
| **Microsoft.SecurityInsights** | Microsoft Sentinel core service |
| **Microsoft.Logic** | Logic Apps for SOAR playbooks |

---

## ✅ Prerequisites

- [ ] Task 1 (Configure Permissions) completed successfully
- [ ] Admin user has **Contributor** role on the Azure Subscription
- [ ] You are logged into the [Azure Portal](https://portal.azure.com)

---

## 📸 Step-by-Step Walkthrough

---

### ▶ Step 1 — Navigate to Subscriptions

1. From the Azure Portal home page, click **Subscriptions** under **Azure services**.

![Navigate to Subscriptions](images/task2-step1-subscriptions.png)

> 💡 The guided tooltip instructs: *"Click on Subscriptions."*

---

### ▶ Step 2 — Select Azure Subscription

1. On the Subscriptions page, click **Azure Subscription** from the list.

![Select Azure Subscription](images/task2-step2-select-subscription.png)

> Both subscriptions (Azure Subscription and TFSUB001) are shown as **Active** under Tenant Root Group.

---

### ▶ Step 3 — Expand the Settings Menu

1. Inside the **Azure Subscription** blade, scroll down the left navigation panel.
2. Click on **Settings** to expand it.

![Expand Settings](images/task2-step3-expand-settings.png)

> The tooltip guides: *"Expand Settings"* to reveal sub-options including Resource providers.

---

### ▶ Step 4 — Select Resource Providers

1. Under the expanded **Settings** section, click **Resource providers**.

![Select Resource Providers](images/task2-step4-resource-providers.png)

> The tooltip prompts: *"Select Resource providers."* This opens the full list of available and registered providers for this subscription.

---

### ▶ Step 5 — Check Microsoft.Insights (Already Registered)

1. In the **Search** box, type `Microsoft.insight`.
2. The result shows **microsoft.insights** with status: ✅ **Registered**.

![Microsoft.Insights Already Registered](images/task2-step5-insights-registered.png)

> The lab tooltip confirms: *"Since Microsoft.insights is already registered we will now check Microsoft.web."* Click **Proceed**.

---

### ▶ Step 6 — Check Microsoft.Web (Already Registered)

1. Clear the search box and type `Microsoft.web`.
2. The result shows **Microsoft.Web** with status: ✅ **Registered**.

![Microsoft.Web Already Registered](images/task2-step6-web-registered.png)

> The tooltip confirms: *"It is also registered. Click on the close icon."*  
> Both Microsoft.Insights and Microsoft.Web were pre-registered — no action needed for these.

---

### ▶ Step 7 — Search for Microsoft.SecurityInsights

1. Clear the search and type `Microsoft.SecurityInsights`.
2. The result shows **Microsoft.SecurityInsights** with status: ❌ **NotRegistered**.
3. Click the **radio button** to the left of the provider name to select it.

![Microsoft.SecurityInsights NotRegistered - Select Radio Button](images/task2-step7-securityinsights-select.png)

> ⚠️ **Microsoft.SecurityInsights** is the core resource provider for Microsoft Sentinel. It must be registered before Sentinel can be deployed.

---

### ▶ Step 8 — Select the Radio Button

1. Click the **radio button** next to **Microsoft.SecurityInsights** to select the row.

![Click Radio Button](images/task2-step8-radio-button.png)

> The tooltip instructs: *"Click on the radio button."* The row will be highlighted, activating the **Register** button in the toolbar.

---

### ▶ Step 9 — Click Register

1. With **Microsoft.SecurityInsights** selected, click the **Register** button at the top of the toolbar.

![Click Register](images/task2-step9-click-register.png)

> The tooltip guides: *"Click on Register."* The **Register** button becomes active (no longer greyed out) once the radio button is selected.

---

### ▶ Step 10 — Registration In Progress: Microsoft.SecurityInsights

1. After clicking Register, the status changes to 🔄 **Registering**.
2. A notification appears in the top-right corner confirming the registration has started.

![SecurityInsights Registering](images/task2-step10-securityinsights-registering.png)

```
ℹ️ Subscription Registering Resource Provider
Registering resource provider 'microsoft.securityinsights'
for subscription 'f70fe291-ff3a-427a-b9c1-70eb35b1a59c'
```

> Registration typically takes 1–3 minutes. You can click **Refresh** to check the current status.

---

### ▶ Step 11 — Registration In Progress: Microsoft.Logic

1. The lab automatically proceeds to register **Microsoft.Logic** as well.
2. Search for `Microsoft.logic` and repeat the same process: select the radio button → click **Register**.
3. The status changes to 🔄 **Registering**.

![Microsoft.Logic Registering](images/task2-step11-logic-registering.png)

```
ℹ️ Subscription Registering Resource Provider
Registering resource provider 'microsoft.logic'
for subscription 'f70fe291-ff3a-427a-b9c1-70eb35b1a59c'
```

> **Microsoft.Logic** is required for **Automation Playbooks** in Microsoft Sentinel (SOAR capabilities).

---

### ▶ Step 12 — Task Complete: All Providers Verified

1. After all registrations are confirmed, the lab displays a summary overlay.
2. A green success notification confirms **Microsoft.Logic** was successfully registered.

![Task 2 Complete - All Providers Registered](images/task2-step12-complete.png)

```
✅ Subscription Registering Resource Provider
Successfully registered resource provider: 'microsoft.logic'
for subscription: 'f70fe291-ff3a-427a-b9c1-70eb35b1a59c'
```

**Summary from the lab overlay:**
> *"In this task, we verified that the following resource providers are registered and available:"*
> - ✅ Microsoft.Web
> - ✅ Microsoft.SecurityInsights
> - ✅ Microsoft.Logic
> - ✅ Microsoft.Insight

Click **OK** to complete the task.

---

## 🏁 Task Complete!

| Resource Provider | Status |
|---|---|
| Microsoft.Insights | ✅ Was already Registered |
| Microsoft.Web | ✅ Was already Registered |
| Microsoft.SecurityInsights | ✅ Newly Registered |
| Microsoft.Logic | ✅ Newly Registered |

---

## 🔍 Why These Providers Matter

| Provider | Used For |
|---|---|
| **Microsoft.Insights** | Log Analytics diagnostics & metrics |
| **Microsoft.Web** | Hosting backend for Logic Apps |
| **Microsoft.SecurityInsights** | The Sentinel service itself — cannot deploy without this |
| **Microsoft.Logic** | SOAR playbooks / automated incident response |

---

## ➡️ Next Step

With permissions and resource providers configured, the environment is fully prepared for **Lab 2 — Deploying Microsoft Sentinel**.

---

## 📚 Additional Resources

- [Azure Resource Providers and types](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resource-providers-and-types)
- [Microsoft.SecurityInsights resource provider](https://learn.microsoft.com/en-us/azure/templates/microsoft.securityinsights)
- [Prerequisites for deploying Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/prerequisites)

---

*Walkthrough documented by: **Reduan Islam Badhon***  
*Based on: Microsoft Partner Skilling Hub — Modernize and optimize your SOC deployment with Microsoft Sentinel*
