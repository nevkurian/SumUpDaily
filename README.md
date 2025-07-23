# SumUpDaily

An automated daily news summarizer built using **n8n**, **Groq LLM**, and a free **News API**, that delivers concise, AI-generated news summaries directly to user inboxes. Users can subscribe via a Google Form, and the system runs entirely on free-tier tools.

---

## 🚀 Features

- 🔁 **Automated Workflow** — Runs daily via n8n Cron node
- 🌐 **News Fetching** — Uses News API to get top 10 headlines further limited to 5
- 🧠 **AI Summarization** — Summarizes each article using Groq’s LLM (e.g., Mixtral)
- 📩 **Email Delivery** — Sends the digest to all subscribers via Gmail
- 📝 **User Subscription** — Simple Google Form integrated with Google Sheets

---

## 📦 Tech Stack

| Tool         | Purpose                            |
|--------------|------------------------------------|
| [n8n](https://n8n.io/)        | Workflow automation              |
| [Groq](https://groq.com/)     | LLM for text summarization       |
| [Newsdata.io](https://newsdata.io/) or News API | Fetch latest headlines           |
| Google Sheets | Store subscriber emails           |
| Google Forms  | User subscription form            |
| Gmail         | Email delivery to users           |

---

## 🔄 Workflow Overview

```text
[Cron Trigger – Daily at 6 AM]
         ↓
[Fetch top headlines from News API]
         ↓
[Limit to top 5 articles]
         ↓
[Groq LLM: Summarize each article]
         ↓
[Format summaries into a daily digest]
         ↓
[Read subscriber emails from Google Sheets]
         ↓
[Send email digest to each subscriber]
