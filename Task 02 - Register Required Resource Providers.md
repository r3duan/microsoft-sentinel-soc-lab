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

<img width="1777" height="852" alt="image" src="https://github.com/user-attachments/assets/64ba1807-4e91-45ed-9bc4-37fce9329aac" />


> 💡 The guided tooltip instructs: *"Click on Subscriptions."*

---

### ▶ Step 2 — Select Azure Subscription

1. On the Subscriptions page, click **Azure Subscription** from the list.

<img width="1785" height="859" alt="image" src="https://github.com/user-attachments/assets/69c36426-4ec5-40f8-ab6a-1591005cd1ee" />

> Both subscriptions (Azure Subscription and TFSUB001) are shown as **Active** under Tenant Root Group.


---

### ▶ Step 3 — Expand the Settings Menu

1. Inside the **Azure Subscription** blade, scroll down the left navigation panel.
2. Click on **Settings** to expand it.

<img width="1775" height="858" alt="image" src="https://github.com/user-attachments/assets/0270d948-0da0-4ae6-99df-de1ac2764f0d" />

> The tooltip guides: *"Expand Settings"* to reveal sub-options including Resource providers.


---

### ▶ Step 4 — Select Resource Providers

1. Under the expanded **Settings** section, click **Resource providers**.

![Select Resource Providers](images/task2-step4-resource-providers.png)

> The tooltip prompts: *"Select Resource providers."* This opens the full list of available and registered providers for this subscription.

<img width="1774" height="854" alt="image" src="https://github.com/user-attachments/assets/ea06ba2d-6403-45b4-b4e2-f5df8fe79298" />


---

### ▶ Step 5 — Check Microsoft.Insights (Already Registered)

1. In the **Search** box, type `Microsoft.insight`.
2. The result shows **microsoft.insights** with status: ✅ **Registered**.


> The lab tooltip confirms: *"Since Microsoft.insights is already registered we will now check Microsoft.web."* Click **Proceed**.




---

### ▶ Step 6 — Check Microsoft.Web (Already Registered)

1. Clear the search box and type `Microsoft.web`.
2. The result shows **Microsoft.Web** with status: ✅ **Registered**.

<img width="1781" height="857" alt="image" src="https://github.com/user-attachments/assets/8f825184-eae0-438c-9385-e894b5ca39b3" />



> The tooltip confirms: *"It is also registered. Click on the close icon."*  
> Both Microsoft.Insights and Microsoft.Web were pre-registered — no action needed for these.




---

### ▶ Step 7 — Search for Microsoft.SecurityInsights

1. Clear the search and type `Microsoft.SecurityInsights`.
2. The result shows **Microsoft.SecurityInsights** with status: ❌ **NotRegistered**.
3. Click the **radio button** to the left of the provider name to select it.

<img width="1568" height="758" alt="image" src="https://github.com/user-attachments/assets/ca154e24-21ea-4741-98e9-e63891341289" />


> ⚠️ **Microsoft.SecurityInsights** is the core resource provider for Microsoft Sentinel. It must be registered before Sentinel can be deployed.

---

### ▶ Step 8 — Select the Radio Button

1. Click the **radio button** next to **Microsoft.SecurityInsights** to select the row.

<img width="1568" height="758" alt="image" src="https://github.com/user-attachments/assets/05605758-f250-4787-b012-23a6638fdf73" />


> The tooltip instructs: *"Click on the radio button."* The row will be highlighted, activating the **Register** button in the toolbar.

---

### ▶ Step 9 — Click Register

1. With **Microsoft.SecurityInsights** selected, click the **Register** button at the top of the toolbar.

<img width="1568" height="755" alt="image" src="https://github.com/user-attachments/assets/8bf2976c-54b3-4af4-9a50-072d41d9abf7" />


> The tooltip guides: *"Click on Register."* The **Register** button becomes active (no longer greyed out) once the radio button is selected.

---

### ▶ Step 10 — Registration In Progress: Microsoft.SecurityInsights

1. After clicking Register, the status changes to 🔄 **Registering**.
2. A notification appears in the top-right corner confirming the registration has started.

<img width="1568" height="755" alt="image" src="https://github.com/user-attachments/assets/1fdcfeec-48fa-4a94-865c-13ef5909812c" />


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

<img width="1568" height="753" alt="image" src="https://github.com/user-attachments/assets/9f669b70-51dc-45fd-afee-866a765161eb" />


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

<img width="1568" height="753" alt="image" src="https://github.com/user-attachments/assets/fd0395fc-a038-432d-9b7a-b8037faa9ef2" />


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
