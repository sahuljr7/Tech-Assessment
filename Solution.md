# ✅ Solution: How to Implement JIRA Automation Rule

## 🎯 Goal

Create an automation rule that performs the following:

* **Trigger**: When an issue is created (or transitioned)
* **Action**:

  * Option A: Assign the issue to the **QA Lead**
  * Option B: Send an **email notification** to the QA Lead

You can implement either or both actions depending on your needs.

---

## 🛠️ Prerequisites

* You must have **JIRA Project Administrator** or **JIRA System Admin** permissions.
* A defined **QA Lead** user or email address.

---

## 🔄 Step-by-Step Implementation in JIRA

### Step 1: Access Automation Settings

1. Navigate to your JIRA project.
2. In the left sidebar, click on **Project Settings**.
3. Scroll down and click **Automation** (for JIRA Cloud)
   *(For JIRA Server, this might be under "Project Automation" or “Project Rules”)*

---

### Step 2: Create a New Rule

1. Click **Create Rule** or **Add Rule**.

---

### Step 3: Set the Trigger

1. Choose a trigger:

   * Click **"Issue Created"** (or **"Issue Transitioned"** if you want it on workflow changes).
2. Click **Save**.

---

### Step 4: Add an Action

#### **Option A: Assign to QA Lead**

1. Click **New Action** → Select **Assign Issue**.
2. In the "Assignee" field, select:

   * A specific user (e.g., `qa.lead.username`)
     OR
   * Use smart value: `{{project.lead}}` or assign to a user in a custom field.
3. Click **Save**.

---

#### **Option B: Send Email Notification**

1. Click **New Action** → Select **Send Email**.
2. In the **To** field:

   * Enter QA Lead email (e.g., `qa.lead@example.com`)
     OR use a JIRA group (e.g., `qa-team`)
3. Subject:

   * `New Issue Created: {{issue.key}} - {{issue.summary}}`
4. Body:

   ```text
   A new issue has been created:

   - Key: {{issue.key}}
   - Summary: {{issue.summary}}
   - Reporter: {{issue.reporter.displayName}}
   - Description: {{issue.description}}

   View it here: {{issue.url}}
   ```
5. Click **Save**.

---

### Step 5: Name and Save the Rule

1. Click **Publish Rule**.
2. Name it something clear, like:
   `Assign to QA Lead on Issue Create` or `Notify QA on New Issues`

---

### Step 6: Test the Rule

1. Go to your project and create a new issue.
2. Watch for:

   * Issue being assigned to QA Lead
     **or**
   * QA Lead receiving an email notification
3. Check **Rule Audit Log** to verify execution.

---

## 📸 Screenshot Suggestions

Capture and save the following for documentation:

1. Rule Overview
2. Trigger Configuration
3. Action (Assign or Email) Configuration
4. Audit Log / Rule Execution
5. Email Received (if applicable)
6. Issue Assigned in JIRA (if applicable)

---

## 🔄 Optional: Export the Rule (JIRA Cloud)

1. Go to the automation rule list.
2. Click the three dots next to your rule.
3. Select **Export rule** → Save the JSON file.
4. Add it to your GitHub repository.

---

## 🧠 Tips

* Use **Smart Values** (`{{issue.fields.summary}}`, `{{issue.url}}`, etc.) for dynamic content.
* Add **Conditions** to apply the rule only for certain issue types, priorities, or labels.
* You can **combine actions** (assign + email) in a single rule.

---
