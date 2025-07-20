# 📬 Telegram HTML Validator & Email Notifier (n8n Workflow)

This n8n automation monitors a Telegram bot for incoming messages, checks if the message content is valid HTML using a Langchain-powered AI (Google Gemini 2.5), and sends an email alert if the message contains **invalid HTML**.

---

## 🔧 Features

- ✅ Listens for new messages on Telegram
- 🧠 Uses **Langchain Agent + Gemini 2.5 Flash model** to analyze the content
- 🕵️ Checks if the message is valid HTML (`YES` or `NO`)
- 📧 Sends an email to a configured Gmail address if the message is **not valid HTML**

---

## 🧩 Workflow Components

| Node | Purpose |
|------|---------|
| **Telegram Trigger** | Listens for incoming messages |
| **Google Gemini Chat Model** | Provides AI capabilities via Gemini |
| **Langchain AI Agent** | Validates HTML using system prompt |
| **If Node** | Checks if the AI returned `"YES"` |
| **Gmail Node** | Sends an email alert if content is invalid |
| **Google Gemini (PaLM) API Credential** | Authenticates AI agent calls |

---

## 📝 System Prompt Logic

The system message instructs the AI to:
> “Analyze the incoming data to check if it's valid HTML or not. If it's valid return `YES`, else return `NO`.”

---

## 📤 Output Behavior

| AI Output | Action |
|-----------|--------|
| `YES` | Nothing happens |
| `NO` | Email is sent with subject: `invalid` and message: `invalid html code` |

---

## ⚙️ Setup Instructions

1. **Create a Telegram Bot** and connect it to the Telegram Trigger node.
2. **Add Google Gemini API credentials** under `Credentials` in n8n.
3. **Connect Gmail OAuth2** for the email sender.
4. **Configure Email Settings**:
   - Edit the **Gmail node** to set the recipient email.
5. Deploy or test in **n8n editor**.

