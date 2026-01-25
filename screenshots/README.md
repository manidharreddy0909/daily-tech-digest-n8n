# Daily Tech Digest Automation (n8n + AI)

## Overview
An AI-powered automation that fetches the latest tech news, summarizes it using an AI agent, and sends a daily email digest automatically.

---

## Workflow Overview
![Workflow Overview](screenshots/workflow-overview.png)

---

## Data Source (RSS Feeds)
The workflow collects tech news from multiple RSS feeds.
![RSS Input](screenshots/rss-input.png)

---

## AI Summarization
An AI Agent processes and summarizes the news into concise, readable insights.
![AI Agent](screenshots/ai-agent.png)

---

## Final Output (Email Delivery)
The summarized tech digest is delivered via email automatically.
![Email Output](screenshots/email-output.png)

---

## Tech Stack
- n8n
- AI Agent (LLM)
- RSS Feeds
- Gmail API
- Cron / Schedule Trigger

---

## Key Learnings
- Building multi-step AI automations
- Cleaning and structuring data for AI
- Designing reliable scheduled workflows

---

## Future Improvements
- Topic-based personalization
- Slack / WhatsApp delivery
- Multi-language summaries
