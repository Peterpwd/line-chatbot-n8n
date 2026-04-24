# 🚀 LINE Chatbot Automation (n8n)

AI-powered chatbot system for automating IT support requests from LINE Group and converting them into Jira tickets.

---

## 📌 Overview

This project is an automation workflow built with **n8n** that receives messages from a LINE Group, analyzes them using AI, validates required information, prevents duplicate cases, and automatically creates Jira tickets.

---

## ⚙️ Features

### 🔍 Smart Case Detection

* Detect messages with `#แจ้งเคส`
* Filter irrelevant messages
* Clean and normalize input text

### 🤖 AI Case Classification

* Classify case types such as:

  * SUGAR
  * WH (Warehouse)
  * PASSWORD
  * KIOSK
  * USER_IT
* Validate required fields
* Generate user-friendly reply messages

### 🔁 Duplicate Prevention

* Prevent duplicate cases within 10 minutes
* Uses Google Sheets as cache storage

### 🎫 Jira Integration

* Automatically create Jira tickets
* Map fields dynamically (priority, category, etc.)

### 📢 Notification System

* Send notification to IT LINE Group
* Show ticket info, user, and case details

---

## 🏗️ Architecture

```
LINE Messaging API
        ↓
Webhook (n8n)
        ↓
Message Filter + Regex
        ↓
AI Processing (Google Gemini)
        ↓
Validation + Duplicate Check
        ↓
Jira Ticket Creation
        ↓
LINE Notification (IT Team)
        ↓
Google Sheets (Logging)
```

---

## 🛠️ Tech Stack

* **Automation:** n8n
* **Language:** JavaScript (in workflow)
* **AI:** Google Gemini
* **APIs:**

  * LINE Messaging API
  * Google Sheets API
  * Jira API

---

## 📂 Project Structure

```
n8n-workflow/
  └── Line_Chatbot.json
```

---

## 🚀 Getting Started

### 1. Import Workflow

* Open n8n
* Import `Line_Chatbot.json`

### 2. Setup Credentials

Configure the following:

* LINE Messaging API Token
* Google Service Account
* Jira API

### 3. Activate Webhook

* Enable workflow
* Copy webhook URL
* Connect to LINE Bot

---

## 📌 Example Usage

```
#แจ้งเคส Reset Password AD: PPhunpipat
```

**Bot Response:**

```
✅ รับเคสเรียบร้อยแล้วครับ
📋 ประเภทเคส: PASSWORD
ทีมงานกำลังดำเนินการให้ครับ
```

---

## 🔒 Security Notes

* Do NOT upload credentials to repository
* Use environment variables instead
* Keep API tokens private

---

## 💡 Highlights

* Real-world IT Support Automation
* AI-powered text analysis
* Multi-system integration (LINE + Jira + Google Sheets)
* Backend logic with validation and deduplication

---

## 👨‍💻 Author

**Phuwadol Phunpipat**
IT Support (Application Support)
