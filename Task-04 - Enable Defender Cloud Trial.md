# 🧪 Lab Walkthrough – Task 4: Enable the Trial for Microsoft Defender for Cloud

**Course:** Modernize and Optimize Your SOC Deployment with Microsoft Sentinel  
**Lab:** Lab 1 – Microsoft Sentinel Prerequisites  
**Task:** Task 4 of 4 — Enable the Trial for Microsoft Defender for Cloud  
**Estimated Time:** ~10 minutes  
**Difficulty:** Beginner  

---

## 🎯 Objective

Activate the **Microsoft Defender for Cloud trial** to access advanced security features and monitoring capabilities for the Azure environment. This trial enables comprehensive cloud-native protection including Cloud Security Posture Management (CSPM), Cloud Workload Protection Platform (CWPP), and Defender for APIs.

> 💡 **Why this matters:** Microsoft Defender for Cloud provides crucial visibility into your security posture, vulnerability assessment, threat protection, and compliance monitoring — all essential for a modern SOC deployment.

---

## ✅ Prerequisites

- [ ] Task 1 (Configure Permissions on Subscription) completed ✅
- [ ] Task 2 (Register Required Resource Providers) completed ✅
- [ ] Task 3 (Assign the Security Administrator Role) completed ✅
- [ ] You are logged into the [Azure Portal](https://portal.azure.com)
- [ ] Admin account has appropriate permissions to enable Defender plans

---

## 📸 Step-by-Step Walkthrough

---

### ▶ Step 1 — Task Overview

The lab presents **Task 4 – Enable the Trial for Microsoft Defender for Cloud** with the following description:

> *"In this task, we will activate the Microsoft Defender for Cloud trial to access advanced security features and monitoring capabilities for our environment."*

Click **Start Task** to begin.

![Task 4 Overview - Start Task button visible](screenshot-placeholder)

**What you'll enable:**
- Cloud Security Posture Management (CSPM)
- Cloud Workload Protection Platform (CWPP)
- Defender for APIs
- 30-day free trial for premium features

---

### ▶ Step 2 — Open the Hamburger Menu and Navigate to Microsoft Defender for Cloud

1. From the Azure Portal home page, click the **hamburger menu** (three horizontal lines) in the top-left corner.
2. From the navigation menu that appears, scroll down and select **Microsoft Defender for Cloud**.

![Hamburger menu with tooltip: "Click on the hamburger menu and navigate to Microsoft Defender for Cloud"](screenshot-placeholder)

> 💡 The guided tooltip instructs: *"Click on the hamburger menu and navigate to Microsoft Defender for Cloud."*  
> Microsoft Defender for Cloud is Azure's native cloud security solution, formerly known as Azure Security Center and Azure Defender.

---

### ▶ Step 3 — Select Microsoft Defender for Cloud from the Left Panel

1. With the left navigation panel expanded, locate **Microsoft Defender for Cloud** in the list.
2. Click on **Microsoft Defender for Cloud** to open the service.

![Left navigation menu showing Microsoft Defender for Cloud highlighted](screenshot-placeholder)

**You should see the following services in the menu:**
- Home
- Dashboard
- All services
- ⭐ Favorites section
  - All resources (Resource Manager)
  - Resource groups (Resource Manager)
  - App Services
  - Function App
  - Azure SQL Database
  - Azure Cosmos DB
  - Virtual machines
  - Load balancers
  - Storage accounts
  - Virtual networks
  - Microsoft Entra ID
  - Monitor
  - Advisor
  - **Microsoft Defender for Cloud** ← Select this

---

### ▶ Step 4 — Click Setup in the Overview Page

1. Microsoft Defender for Cloud opens to the **Overview** page.
2. In the left navigation panel, you'll see options like Overview, **Setup**, Recommendations, Attack path analysis, Security alerts, Inventory, etc.
3. Click on **Setup** in the left menu.

![Microsoft Defender for Cloud Overview page with tooltip: "Click Setup"](screenshot-placeholder)

> The tooltip guides: *"Click Setup."*

**Current Overview page shows:**
- **Subscriptions:** Showing 2 subscriptions
- **Exposed resources:** -- (not yet configured)
- **Attack paths:** --
- **Security alerts:** --
- **Security posture:** 0 Critical recommendations, 0 Attack paths, 0/0 Overdue recommendations
- Total secure score: 0%

---

### ▶ Step 5 — Expand Management to Go to Environment Settings

1. On the **Setup** page, you'll see the section titled **"Connect your environments to Defender for Cloud"**.
2. The page shows:
   - *"Protect cloud-native applications from code to runtime."*
   - *"Complete your Azure workloads onboarding and protect additional cloud environments."*
3. Look at the left navigation panel under the expanded **General** section.
4. Expand the **Management** section.
5. Click on **Environment settings**.

![Setup page with tooltip: "Expand Management to go to Environment settings"](screenshot-placeholder)

> The tooltip instructs: *"Expand Management to go to Environment settings."*

**Environment options displayed:**
- **Microsoft Azure:** 0 onboarded, All eligible subscriptions are onboarded
- **Amazon Web Services:** 0 onboarded, [Onboard >]
- **Google Cloud Platform:** 0 onboarded, [Onboard >]
- **Additional environments:** [Explore environments >]

---

### ▶ Step 6 — Select Environment Settings from the Management Menu

1. With the **Management** section expanded, click on **Environment settings**.

![Left panel showing Management expanded with Environment settings highlighted and tooltip: "Select Environment settings"](screenshot-placeholder)

**Management section contains:**
- 🌐 **Environment settings** ← Click this
- 🔄 Workflow automation

---

### ▶ Step 7 — Click on the Dropdown for Tenant Root Group

1. The **Environment settings** page opens, showing your Azure organizational structure.
2. You'll see:
   - **Azure subscriptions:** 2
   - **AWS accounts:** 0
   - **GCP projects:** 0
   - **GitHub connectors:** 0
   - **AzureDevOps connectors:** 0
   - **GitLab connectors:** 0
   - **Docker Hub:** 0
   - **JFrog:** 0
3. Under the **Name** column, you'll see the hierarchy starting with **Azure** (collapsed).
4. Click the **dropdown arrow** (▷) next to **Tenant Root Group (2 of 2 subscriptions)** to expand it.

![Environment settings page with tooltip: "Click on the dropdown for Tenant Root Group"](screenshot-placeholder)

> The tooltip guides: *"Click on the dropdown for Tenant Root Group."*

---

### ▶ Step 8 — Select Azure Subscription

1. After expanding the Tenant Root Group, you'll see the subscriptions listed beneath it.
2. You should see:
   - 💛 **Azure Subscription** (0/0 plans)
   - 💛 **TFSUB001** (0/0 plans) 
3. Click on **Azure Subscription**.

![Expanded tenant hierarchy showing Azure Subscription with tooltip: "Select Azure Subscription"](screenshot-placeholder)

> The tooltip instructs: *"Select Azure Subscription."*

**Note:** Both subscriptions show **0/0 plans** enabled, indicating no Defender plans are currently active.

---

### ▶ Step 9 — Click on Enable All Plans Button

1. The **Settings | Defender plans** page opens for the Azure Subscription.
2. At the top of the page, you'll see:
   - **Save** button (grayed out)
   - **Settings & monitoring** tab
   - Blue info banner: *"After February 5, 2025, The Defender for Storage classic per-transaction plan will no longer be available for new storage accounts and subscriptions."*
   - **Enable all plans** button (white button)
   - Notice: *"30 days free trial is available for some of your plans"*
3. Click the **Enable all plans** button.

![Settings Defender plans page with tooltip: "Click on Enable all plans button"](screenshot-placeholder)

> The tooltip guides: *"Click on Enable all plans button."*

**Current plan status shown:**

**Cloud Security Posture Management (CSPM)**
| Plan | Pricing | Resource quantity | Monitoring coverage | Status |
|------|---------|-------------------|---------------------|--------|
| Foundational CSPM | Free | - | ✅ Full | Off/On toggle |
| Defender CSPM | $5/Billable resource/Month | 0 resources | ✅ Full | Off |

**Cloud Workload Protection (CWPP)**
| Plan | Pricing | Resource quantity | Monitoring coverage | Status |
|------|---------|-------------------|---------------------|--------|
| Servers | Plan 2 ($15/Server/Month) | 0 servers | ✅ Full | Off |
| App Service | $15/instance/Month | 0 instances | ✅ Full | Off |

---

### ▶ Step 10 — Select Microsoft Defender for APIs Plan 1

1. After clicking **Enable all plans**, a **Plan selection** panel slides in from the right.
2. The panel shows **APIs** plan options with the header: *"Defender for APIs helps you gain visibility into business-critical APIs. You can investigate and improve security posture, prioritize vulnerability fixes, and detect against the top OWASP API threats."*
3. **Plan details** section shows four benefits with green checkmarks:
   - ✅ Unified inventory of all APIs published within Azure API Management
   - ✅ Monitor API traffic against top OWASP API threats through ML-based and threat intelligence-based detection
   - ✅ Security insights including identifying unauthenticated, inactive/dormant, and externally exposed APIs
   - ✅ Classifies APIs that receive or respond with sensitive data
4. You'll see four plan options:
   - ⚪ **Microsoft Defender for APIs Plan 1** — $200/month - 1 million API calls, Overages: $0.0002/API call
   - ⚪ Microsoft Defender for APIs Plan 2 — $700/month - 5 million API calls, Overages: $0.00014/API call
   - ⚪ Microsoft Defender for APIs Plan 3 — $5,000/month - 50 million API calls, Overages: $0.0001/API call
   - ⚪ Microsoft Defender for APIs Plan 4 — $7,000/month - 100 million API calls, Overages: $0.00007/API call
5. Select the radio button for **Microsoft Defender for APIs Plan 1**.

![Plan selection panel with tooltip: "Select Microsoft Defender for APIs Plan 1"](screenshot-placeholder)

> The tooltip instructs: *"Select Microsoft Defender for APIs Plan 1."*

---

### ▶ Step 11 — Click Save Button (First Time)

1. With **Microsoft Defender for APIs Plan 1** selected (radio button filled with blue dot ●), the **Save** button at the bottom of the panel becomes active.
2. Click the **Save** button.

![Plan selection panel showing Plan 1 selected with tooltip: "Click Save button"](screenshot-placeholder)

> The tooltip guides: *"Click Save button."*

---

### ▶ Step 12 — Select Save Again in the Defender Plans Page

1. The Plan selection panel closes.
2. You're back on the **Settings | Defender plans** page.
3. Notice that the **Defender CSPM** plan status now shows **On** (purple toggle switched to the right).
4. A green tooltip appears pointing to the **Save** button at the top of the page.
5. Click the **Save** button at the top of the page to finalize the configuration.

![Settings page with Defender CSPM enabled and tooltip: "Select Save again"](screenshot-placeholder)

> The tooltip instructs: *"Select Save again."*

**Updated plan status:**

**Cloud Security Posture Management (CSPM)**
| Plan | Pricing | Resource quantity | Monitoring coverage | Status |
|------|---------|-------------------|---------------------|--------|
| Foundational CSPM | Free | - | ✅ Full | Off/On |
| Defender CSPM | $5/Billable resource/Month | 0 resources | ✅ Full | **On** 🟣 |

**Cloud Workload Protection (CWPP)**
| Plan | Pricing | Resource quantity | Monitoring coverage | Status |
|------|---------|-------------------|---------------------|--------|
| Servers | Plan 2 ($15/Server/Month) | 0 servers | ✅ Full | **On** 🟣 |
| App Service | $15/instance/Month | 0 instances | ✅ Full | **On** 🟣 |

---

### ▶ Step 13 — Task Complete — Trial Enabled

1. After clicking Save, a confirmation dialog appears with the message:

> *"In this task, we have enabled the Microsoft Defender for Cloud trial."*

2. Additionally, a notification banner appears in the top-right corner:

> 🟢 **Defender for APIs Onboarding Recommendation Available. Select here t...**  
> *"To complete onboarding for Defender for APIs, you will need to select which Azure API Management APIs to onboard for security coverage by remediating the onboarding recommendation linked in the notification title above."*

3. Click **OK** to complete the task.

![Final confirmation dialog showing task completion](screenshot-placeholder)

---

## 🏁 Lab 1 Complete — All 4 Tasks Done!

| Task | Description | Status |
|---|---|---|
| Task 1 | Configure Permissions on the Subscription | ✅ Complete |
| Task 2 | Register Required Resource Providers | ✅ Complete |
| Task 3 | Assign the Security Administrator Role | ✅ Complete |
| Task 4 | Enable the Trial for Microsoft Defender for Cloud | ✅ Complete |

---

## 🔍 What You've Enabled

By completing this task, you've activated the following Microsoft Defender for Cloud capabilities:

### **1. Cloud Security Posture Management (CSPM)**
- **Foundational CSPM** (Free): 
  - Asset discovery
  - Continuous assessment
  - Security recommendations for posture hardening
  - Secure score measurement
- **Defender CSPM** ($5/billable resource/month):
  - Agentless vulnerability scanning
  - Data-aware security posture
  - Cloud security graph
  - Advanced threat hunting
  - Attack path analysis

### **2. Cloud Workload Protection Platform (CWPP)**
- **Servers Protection** (Plan 2 - $15/server/month):
  - Threat detection for VMs
  - Just-in-time VM access
  - File integrity monitoring
  - Adaptive application controls
  - Network map
- **App Service Protection** ($15/instance/month):
  - Runtime threat protection
  - Vulnerability assessment
  - Web application firewall recommendations

### **3. Defender for APIs** (Plan 1 - $200/month for 1M calls)
- Unified API inventory
- OWASP API threat detection
- Sensitive data classification
- Unauthenticated API identification

---

## 💰 Trial Period Information

**Free Trial Details:**
- **Duration:** 30 days
- **Coverage:** Most Defender plans are free during the trial period
- **After trial:** You can choose to:
  - Continue with paid plans (automatic if not canceled)
  - Disable specific plans
  - Keep only Foundational CSPM (always free)

**Important:** Set a calendar reminder to review your Defender plans before the 30-day trial ends to avoid unexpected charges.

---

## 📊 What's Next After Task 4

Now that your environment has:
- ✅ Proper RBAC permissions (Task 1)
- ✅ Required resource providers registered (Task 2)
- ✅ Security Administrator role assigned (Task 3)
- ✅ Microsoft Defender for Cloud trial enabled (Task 4)

You're ready to proceed to **Lab 2 — Deploying Microsoft Sentinel**, where you will:
1. Create a Log Analytics Workspace
2. Enable Microsoft Sentinel
3. Configure data connectors
4. Set up analytics rules

---

## 🔧 Post-Configuration Recommendations

### **Immediate Next Steps:**
1. **Complete API Onboarding**
   - Navigate to the recommendation from the notification
   - Select which Azure API Management APIs to protect
   - Apply security coverage

2. **Review Security Recommendations**
   - Go to **Defender for Cloud → Recommendations**
   - Review the initial security posture assessment
   - Prioritize recommendations by severity

3. **Configure Security Policies**
   - Navigate to **Environment settings → Azure Subscription → Security policies**
   - Review and customize regulatory compliance standards
   - Enable/disable specific policy initiatives

4. **Set Up Email Notifications**
   - Go to **Settings → Email notifications**
   - Configure recipients for security alerts
   - Set notification severity thresholds

### **Monitoring Your Trial:**
- Go to **Defender for Cloud → Defender plans**
- Click "Settings & monitoring" tab
- Monitor resource coverage and costs
- Review which resources are protected

---

## 🛡️ Understanding the Defender Plans

### **Foundational CSPM (Free — Always Available)**
**What it does:**
- Discovers all your Azure resources
- Assesses them against Azure Security Benchmark
- Provides security recommendations
- Calculates a secure score

**Who should use it:** Everyone — it's free and provides essential security posture visibility.

---

### **Defender CSPM (Paid — Trial Enabled)**
**What it adds:**
- **Attack path analysis** — Visualize how attackers could exploit weaknesses
- **Cloud security graph** — Understand relationships between resources and risks
- **Agentless scanning** — No agents needed for vulnerability detection
- **Data-aware security** — Discover and protect sensitive data

**Who should use it:** Organizations needing advanced threat modeling and comprehensive vulnerability management.

---

### **Workload Protection Plans (Paid — Trial Enabled)**

#### **Servers (VMs)**
- Real-time threat detection
- Behavioral analytics
- Integration with Microsoft Defender for Endpoint
- File integrity monitoring
- Adaptive application controls

#### **App Service**
- Runtime protection for web apps
- Detection of suspicious activities
- Integration with web application firewall

#### **Defender for APIs**
- API inventory and classification
- Detection of top OWASP API threats
- Sensitive data exposure alerts
- Inactive/shadow API discovery

---

## 📚 Additional Resources

- [Microsoft Defender for Cloud Documentation](https://learn.microsoft.com/en-us/azure/defender-for-cloud/)
- [Defender for Cloud Pricing](https://azure.microsoft.com/en-us/pricing/details/defender-for-cloud/)
- [CSPM vs CWPP — What's the Difference?](https://learn.microsoft.com/en-us/azure/defender-for-cloud/concept-cloud-security-posture-management)
- [Defender for APIs Overview](https://learn.microsoft.com/en-us/azure/defender-for-cloud/defender-for-apis-introduction)
- [Azure Security Benchmark](https://learn.microsoft.com/en-us/security/benchmark/azure/)
- [Managing and responding to security alerts](https://learn.microsoft.com/en-us/azure/defender-for-cloud/managing-and-responding-alerts)

---

## 🎓 Key Takeaways

✅ **You've successfully enabled enterprise-grade cloud security** with Microsoft Defender for Cloud  
✅ **30-day free trial** gives you time to evaluate all premium features  
✅ **Foundational CSPM remains free** even after trial — always keep it enabled  
✅ **Multiple protection layers** — posture management + workload protection + API security  
✅ **Integration with Sentinel** — Defender alerts will feed into your SIEM for centralized security operations  

---

## ⚠️ Common Issues and Troubleshooting

### **Issue: "Enable all plans" button is grayed out**
**Solution:** Ensure you have the appropriate permissions. You need one of:
- Owner role on the subscription
- Contributor role on the subscription
- Security Admin role in Microsoft Entra ID

### **Issue: Plans not showing as "On" after clicking Save**
**Solution:** 
- Wait 1-2 minutes for the changes to propagate
- Refresh the page
- Check if you received any error notifications

### **Issue: "Plan selection panel doesn't appear"**
**Solution:**
- Check your browser's popup blocker
- Try a different browser (Edge or Chrome recommended)
- Clear browser cache

### **Issue: Trial already consumed**
**Solution:**
- Each Azure subscription gets one 30-day trial
- If previously used, you'll need to enable paid plans
- Contact Microsoft Support to request trial extension for training purposes

---

## 🎯 Quiz — Test Your Knowledge

**Question 1:** What's the difference between Foundational CSPM and Defender CSPM?  
<details>
<summary>Click to reveal answer</summary>
Foundational CSPM (free) provides basic security posture assessment, recommendations, and secure score. Defender CSPM (paid) adds advanced features like attack path analysis, cloud security graph, agentless vulnerability scanning, and data-aware security posture.
</details>

**Question 2:** How long is the Microsoft Defender for Cloud trial period?  
<details>
<summary>Click to reveal answer</summary>
30 days
</details>

**Question 3:** Which Defender plan helps detect OWASP API threats?  
<details>
<summary>Click to reveal answer</summary>
Microsoft Defender for APIs
</details>

**Question 4:** Do you need to install agents for Defender CSPM vulnerability scanning?  
<details>
<summary>Click to reveal answer</summary>
No — Defender CSPM uses agentless scanning technology
</details>

---

*Walkthrough documented by: **Reduan Islam Badhon***  
*Based on: Microsoft Partner Skilling Hub — Modernize and optimize your SOC deployment with Microsoft Sentinel*  
*Task 4 of 4 — Lab 1 Prerequisites*
