# 🚀 AI-Based Email Support Automation (n8n + PostgreSQL)

## 📌 Overview

This project is an **automated customer support system** built using **n8n** that processes incoming emails and intelligently classifies them into:

- **FEEDBACK**
- **ISSUE (Support Requests)**

The system extracts key information, applies AI-based classification, and stores structured issue data in a **PostgreSQL database** for tracking and analysis.

---

## ⚙️ Features

### 📥 Email Automation
- Reads incoming emails using IMAP/Gmail Trigger
- Automatically processes new messages

---

### 🧠 AI Classification (2 Stages)

#### Stage 1 — Email Type Detection
- Classifies emails into:
  - **FEEDBACK**
  - **ISSUE**

#### Stage 2 — Issue Categorization
- Categorizes issues into:
  - BILLING  
  - PRODUCT  
  - ACCOUNT  
  - PAYMENT  
  - ABUSE  
  - OTHER  

- Also generates:
  - Confidence score  
  - Short issue summary  

---

### 🧾 Data Extraction
Extracts structured fields:
- Ticket ID  
- Customer Name  
- Customer Email  
- Subject  
- Body Text  
- Timestamp  

---

### 🗄️ PostgreSQL Integration

All issues are stored in a **tickets table** with:

- `ticket_id`  
- `customer_email`  
- `customer_name`  
- `subject`  
- `body_text`  
- `category`  
- `confidence`  
- `summary`  
- `status`  
- `created_at`  

---

### ✉️ Automated Responses
- Sends acknowledgment emails for:
  - Feedback  
  - Issues  

---

## 🔁 Workflow
Email Trigger
   ↓
Preprocessing (JavaScript)
   ↓
LLM Classifier 1 (Feedback vs Issue)
   ↓
IF Node

FEEDBACK:
   → Store / Acknowledge

ISSUE:
   → LLM Classifier 2 (Category + Summary)
   → Store in PostgreSQL
   → Send acknowledgment email
