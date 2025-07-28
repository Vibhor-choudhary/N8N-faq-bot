# 📚 Documentation

## 🛠️ Setup Guides

### 1. Prerequisites
- Ensure you have [n8n](https://n8n.io/) installed (self-hosted or cloud).
- Google Account with Sheets API enabled.
- Access to [Gemini API](https://ai.google.dev/).
- This repository cloned locally or forked on GitHub.

### 2. Installation & Configuration

#### Clone and Import Workflow
```bash
git clone https://github.com/your-username/n8n-faq-bot.git
cd n8n-faq-bot
```
- In n8n, go to Workflows → Import, and select `workflows/FAQ-Bot.json`.

#### Set Up Google Sheets Integration
- In n8n, open Credentials → Create new → Google Sheets.
- Authorize with your Google Account.
- Link a spreadsheet (see below for example format).

#### Set Up Gemini Integration
- In n8n, add a Gemini API node.
- Paste your Gemini API credentials, or create new credentials in n8n.

#### Final Setup
- Connect chat/webhook entry points as desired.
- Modify workflow as needed for your platform (Slack, WhatsApp, website, etc.).

### 3. Troubleshooting

- **Credential Issues:** Ensure API credentials are added in n8n and not hard-coded.
- **No Response:** Check if the workflow is active and Google Sheet is shared properly.
- **API Limits:** Verify you are not exceeding Gemini or Google Sheets usage quotas.
- For advanced support, check n8n logs or raise an issue in this repo.

---

## 📡 API Documentation

If you extend the bot with additional APIs (e.g., Telegram, Discord, OpenAI):

### Example: Adding a Telegram Integration

#### Endpoint
- Webhook entry at `/webhook/telegram-faq`
- Accepts: JSON payload with `chat_id` and `message`.

#### Example Request
```json
{
  "chat_id": "123456789",
  "message": "What is n8n?"
}
```

#### Example Response
```json
{
  "reply": "n8n is an open-source workflow automation tool."
}
```

#### Error Codes
- `401 Unauthorized`: Invalid or missing API key.
- `404 Not Found`: Endpoint incorrect.
- `500 Internal Server Error`: Problem processing request.

**Tip:** For each new API, document:
- Endpoint URLs
- Required parameters
- Example requests/responses
- Error codes and troubleshooting steps

---

## 💡 Examples & Use Cases

### 1. Google Sheet Example Format

| Question        | Answer                               |
|-----------------|--------------------------------------|
| What is n8n?    | An open-source workflow tool.        |
| Who made this?  | Inspired by #30DaysOfAI, Vibhor C.   |

### 2. Workflow Use Case

- **Slack FAQ Bot:** Set up the webhook trigger node to listen to Slack slash commands. Route queries to the FAQ workflow for instant answers in Slack.
- **WhatsApp Support:** Integrate with Twilio WhatsApp, forwarding messages to n8n for FAQ automation.
- **Website Widget:** Connect chat widget to n8n webhook, enabling automated customer FAQ on your site.

---

_Contributions to documentation are welcome! Add your guides and API integrations to make this bot even more powerful._ 