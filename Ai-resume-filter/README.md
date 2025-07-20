# 🤖 AI-Powered Resume Rejection Mailer (n8n + Google Gemini)

This project is an automated resume evaluation and rejection email sender built using **n8n** and **Google Gemini (PaLM 2.5 Flash)**.

It analyzes resumes submitted via chatbot, checks for **Node.js** knowledge, and sends a **rejection email** automatically if the candidate doesn’t qualify.

---

## 🧠 How It Works

1. 📩 A resume is submitted via chat (e.g., Telegram or web form).
2. 🧠 **Google Gemini AI** analyzes the input to check if the candidate knows Node.js.
3. ✅ If YES → No email is sent (assumed selected).
4. ❌ If NO → Gemini generates a rejection email body.
5. 📤 Email is automatically sent to the candidate using **Gmail integration**.

---

## 🔗 Tools Used

- [n8n.io](https://n8n.io) – No-code workflow automation tool
- Google Gemini (PaLM 2.5 Flash) – AI reasoning engine
- LangChain + n8n Langchain nodes
- Gmail (OAuth2 integration)

---

## 📸 Workflow Preview

![Workflow Preview](./selection-rejection-workflow.png)
