# Question 1: JIRA Automation Rule

## 📌 Objective

Create a JIRA automation rule that:
- Uses a **trigger** (e.g., *Issue Created*, *Issue Transitioned*)
- Performs an **action**:
  - Assigns the issue to the QA Lead **OR**
  - Sends an email notification to the QA Lead

---

## ⚙️ Tools Used

- JIRA Cloud / Server
- Chrome / Firefox
- Screenshot Tool
- GitHub

---

## ⚡ Automation Rule Setup

### 🔹 Trigger Used
- **Type**: Issue Created  
- **Details**: This trigger initiates the rule whenever a new issue is created in the selected project.

### 🔹 Action Configured
Choose one or both of the following based on what you implemented:

#### Option A: Assign to QA Lead
- **Action Type**: Assign Issue
- **Assignee**: `QA_Lead_Username` or `QA Lead` role

#### Option B: Send Email Notification
- **Action Type**: Send Email
- **Recipients**: QA Lead Email (`qa.lead@example.com`)
- **Email Body**: Includes issue summary, description, and reporter info.

---

## 🧪 Testing & Execution

### Steps Taken:
1. Created a new issue in JIRA.
2. Verified that the automation rule was triggered.
3. Checked that the action (assignment/email) was completed.

---

## 📸 Screenshots

| Description | Screenshot |
|-------------|------------|
| Rule Configuration | ![Rule Config](screenshots/rule-configuration.png) |
| Trigger Setup | ![Trigger](screenshots/trigger-setup.png) |
| Action Setup | ![Action](screenshots/action-setup.png) |
| Rule Execution | ![Execution](screenshots/rule-execution.png) |

> **Note:** All screenshots are stored in the `screenshots/` folder.

---

## 📁 Files Included

- `README.md` (this file)
- `automation-rule-export.json` *(if export was possible)*
- `screenshots/` folder with all relevant images
- Any additional logs or proof of execution

---

## ✅ Status

- [x] Rule Created  
- [x] Trigger Configured  
- [x] Action Implemented  
- [x] Rule Tested  
- [x] Screenshots Captured  
- [x] GitHub Repo Prepared

---

## 📝 Notes

- This automation was created and tested using JIRA Cloud.
- All tasks were completed individually as per the assessment guidelines.
- No credentials or private information are shared in this submission.

```

---

### 📁 Recommended Folder Structure for GitHub

```
Tech-Assessment-[YourName]/
│
├── Question-1-JIRA-Automation/
│   ├── README.md
│   ├── automation-rule-export.json   (if available)
│   └── screenshots/
│       ├── rule-configuration.png
│       ├── trigger-setup.png
│       ├── action-setup.png
│       └── rule-execution.png
```

