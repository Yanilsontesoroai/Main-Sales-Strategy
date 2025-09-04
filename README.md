# 📧 Main Sales Strategy v2 – Automated B2B Email Outreach (n8n)

This repository contains the n8n workflows that power Tesoro AI's automated B2B outreach system. It generates personalized recruitment emails based on live company insights and sends them via Gmail, while managing opt-in/out flows and tracking metadata through Google Sheets.

---

## 🔁 Workflow Structure

### 🧩 Main Workflow: `Main Sales Strategy v2`
Controls the overall logic, routes to sub-workflows and form handlers.

### 🔧 Sub-workflow 1: `Generated Email`
- Uses Google Gemini (Palm API) to gather company and role-specific information.
- Feeds vector stores for tone and content alignment.
- Generates full email content (subject, greeting, body, CTA, signature).

### 📤 Sub-workflow 2: `Send Email`
- Formats the generated content into responsive HTML.
- Sends the email via Gmail.
- Logs the thread ID and contact metadata into a Google Sheet.

### 📋 Form Branches
- Embedded in the email footer for opt-out and contact follow-up.
- Routes user input to update preferences and CRM logic.

---

## 🔑 Features

- ✅ AI-generated content based on live company data
- ✅ Custom tone and structure based on ICP (CEO, CTO, HR)
- ✅ Gmail integration with threading
- ✅ Google Sheets as lead database
- ✅ HTML email templates
- ✅ Opt-out / contact forms via n8n Forms

---

## ⚙️ Technologies Used

- [n8n](https://n8n.io) - Workflow automation
- Google Sheets API
- Gmail API (OAuth2)
- Google Palm API (Gemini)
- LangChain Vector Store

---

## 📂 Files Included

- `Main Sales Strategy v2.json` – Core workflow
- `Generated Email.json` – Sub-workflow for email generation
- `Send Email.json` – Sub-workflow for email delivery

---

## 👤 Maintainer

**Yanilson Moreno**   
[tesoroai.com](https://www.tesoroai.com)


