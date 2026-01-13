 # Daily AI Tech Digest n8n Workflow

An automated n8n workflow that fetches the latest technology news from major RSS feeds, summarizes the content using OpenAI's GPT models into plain English, and delivers a daily digest via Gmail.

## How it Works
1. **Schedule Trigger**: The process initiates automatically every day at 7:00 AM.
2. **Data Acquisition**: The workflow pulls the latest articles from TechCrunch, Engadget, Wired, and The Verge.
3. **Data Aggregation**: All news snippets from the previous 24 hours are collected into a single dataset.
4. **AI Processing**: An AI Agent processes the raw text to remove technical jargon and create a simplified summary.
5. **Format Conversion**: The summary is converted from Markdown to HTML to ensure proper email formatting.
6. **Email Delivery**: The final digest is sent to a specified Gmail address.

## Setup Instructions

### 1. Prerequisites
- An active n8n instance (Cloud or Self-hosted).
- OpenAI API credentials.
- Gmail account with OAuth2 or App Password configured in n8n.

### 2. Import the Workflow
- Download the `workflow.json` file from this repository.
- In n8n, click on **Workflows** > **Import from File** and select the JSON.

### 3. Configure Credentials
You will need to set up two connections in n8n:
- **OpenAI API**: Create a new credential and paste your API key. (Note: The workflow is currently set to use gpt-5-mini; you may need to update this to gpt-4o-mini in the node settings).
- **Gmail API**: Connect your Google account to the "Send a message" node.

### 4. Personalize
- **Email Address**: Open the last node ("Send a message") and change the "Send To" field from the placeholder to your own email.
- **RSS Feeds**: Edit the "Edit Fields" node if you want to add or remove news sources.

## Nodes Used
- Schedule Trigger: Automates the daily run.
- RSS Feed Read: Scrapes news data.
- AI Agent: Brain of the operation using LangChain.
- Markdown Node: Formats the text for emails.
- Gmail Node: Delivery system.

---
Built with n8n.
 
