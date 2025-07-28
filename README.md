# 🤖 n8n No-Code AI FAQ Bot

A modern, **no-code AI-powered FAQ chatbot** using [n8n](https://n8n.io/), Google Sheets, and Gemini AI — inspired by [Vibhor Choudhary's #BuildInPublic Day 9](https://www.linkedin.com/posts/vibhor-choudhary_buildinpublic-day9-30daysofai-activity-7348953339792891905-P0y5) during the #30DaysOfAI challenge.

<img width="600" height="600" alt="n8n logo" src="https://github.com/user-attachments/assets/5e25ab36-9a80-46af-a45e-a5cbc422f4d2" />


---

## 🚀 Features

- **No-Code Setup:** Deploy instantly with drag-and-drop n8n workflow import.
- **Live FAQ Editing:** FAQs stored in Google Sheets—edit and add answers in real time!
- **Conversational AI:** Gemini (Google) generates accurate, helpful, natural responses.
- **Flexible Triggers:** Webhook/chat-trigger ready for website, app, Slack, or WhatsApp.
- **Easy to Extend:** Modify logic, add memory, or connect with more services.

---

## 🛠️ Quick Start

1. **Clone this repository**
2. **Import Workflow**
   - In n8n, go to Workflows > Import > Select `FAQ Bot.json`
3. **Configure Google Sheets**
   - Set up Google Sheets credentials via n8n; link your Sheet with FAQs.
4. **Configure Gemini**
   - Obtain a Gemini API key, add to n8n Gemini node.
5. **Test Your Bot!**
   - Trigger through chat/webhook node and get responses.
6. **Customize**
   - Edit prompt templates or improve memory and logic as you wish.

---

## 📄 Example Google Sheet Format

| Question                 | Answer                                      |
|--------------------------|---------------------------------------------|
| What is n8n?             | An open-source workflow automation tool.    |
| How does Gemini work?    | It's an LLM that generates conversational AI replies.|

* ## Sample Google Sheet: https://docs.google.com/spreadsheets/d/1gCvK0b-sAEGcKkoAHKdHbENsB9MVZCxNCyO8H7DUR3Q/edit?usp=sharing *

---

## 🌟 Inspiration / Credit

> "Built during the #30daysofAI challenge, this project shows how non-developers can automate FAQ responses by blending n8n (no-code automation), Gemini (AI LLM), and Google Sheets as a backend—a simple, scalable, and cost-effective AI support tool."  
> — Inspired by Vibhor Choudhary's [LinkedIn post](https://www.linkedin.com/posts/vibhor-choudhary_buildinpublic-day9-30daysofai-activity-7348953339792891905-P0y5)

---

## 📝 Requirements

- [n8n](https://n8n.io/) (self-hosted or cloud)
- A Google Account (Google Sheets API enabled)
- [Gemini API access](https://ai.google.dev/)
- Webhook endpoint for chat/message input

---

## 📊 How It Works

1. **User Sends a Question** to a webhook or chat trigger.
2. **n8n Workflow** fetches relevant FAQ from Google Sheets.
3. **Gemini Node** generates a conversational answer if FAQ is missing or needs contextualization.
4. **Reply Sent** back to the user/channel.

---

## 🔒 Security & Best Practices

- **Never commit credentials.** Use environment variables or n8n's credential store.
- **Follow n8n security guidelines** for workflows that process user input.

---

## 🤝 Contribution

- **Fork and PR:** Improvements welcome—add new nodes, refine prompts, create docs!
- **Discuss:** File issues for feature requests or bugs.
- **Community:** Tag #BuildInPublic and #n8nFAQ on social to share your results.

---

## 🪪 License

[MIT License](./LICENSE)

---

## 🖼️ Screenshots / Docs

Place screenshots or further documentation in [`/docs/`](docs/).

--- 
