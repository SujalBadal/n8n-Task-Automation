# TweetBurner AI 🤖🔥

TweetBurner AI is an n8n-powered smart workflow that fetches tweets, processes them, and generates savage, witty, and viral roast replies using Google Gemini AI — all within the n8n chat interface.

---

## 🧠 Features

- 🔗 Fetch tweets via Twitter API (via custom HTTP request).
- 🧹 Cleans and formats tweets with a Code node.
- 🤖 Powered by Google Gemini AI (via LangChain Agent).
- 🗯️ Replies with brutal, sarcastic one-liners to tweet content.
- 💬 Works entirely inside the n8n Chat UI (not Telegram).
- 🔍 Can access SerpAPI if needed for external tools.

---

## 🚀 Workflow Overview

1. **Trigger**: n8n ChatTrigger node waits for user input.
2. **HTTP Request**: Pulls tweets based on static query.
3. **Code Node**: 
   - Extracts tweets
   - Removes duplicates
   - Formats timestamps
4. **AI Agent**:
   - Prompt: “You are a savage and sarcastic Twitter expert bot...”
   - Generates short and funny roast replies.
5. **Gemini AI**: Acts as the brain behind the responses.
6. **n8n Chat Interface**: Displays the reply.

---

## 🛠️ Technologies Used

- [n8n.io](https://n8n.io/)
- LangChain Integration
- Google Gemini (via PaLM API)
- SerpAPI (Optional Tool)
- Custom Code Node (JavaScript)

---

## 💬 Sample Prompt (used internally)

```txt
You are a savage and sarcastic Twitter expert bot. 
Given the tweet below, write a short, witty, and brutal one-liner reply. 
Make it sound like a viral roast.

Tweet:
"{{ $json.content }}"

Reply only with the one-liner. No explanations. No extra formatting.
