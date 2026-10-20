# Learning Journey Showcase: Automated LinkedIn Posts with n8n

An n8n workflow that turns daily learning entries in a Google Sheet into professional LinkedIn posts using Google Gemini.

## Workflow

Google Sheets Trigger (every minute, new row) → Basic LLM Chain (Gemini summary) → LinkedIn Specialization (Gemini post) → Create a post (LinkedIn)

## How It Works

1. A new row is added to the Google Sheet with the day's learning entry.
2. Gemini summarizes the entry into a concise, professional summary.
3. Gemini converts the summary into an engaging LinkedIn post with a hook, key insights, a real-world reflection, hashtags and a closing question.
4. The post is published to LinkedIn automatically.

## Google Sheet Format

| Date | Topic/Module | What I Learned | Skills/Tools |
|---|---|---|---|
| 2026-10-18 | Prompt Engineering | Learned how to structure prompts with a clear role, context and output format. | Prompt Design, Google Gemini |

Column headers must match exactly, because the prompts read them by name.

## Setup

1. Import `workflow.json` into n8n.
2. Add credentials: Google Sheets OAuth2, Google Gemini (PaLM) API key, LinkedIn OAuth2.
3. Select your own Google Sheet and sheet tab in the trigger node.
4. Activate the workflow.

## Tech Stack

n8n, Google Gemini, Google Sheets API, LinkedIn API, OAuth 2.0
