# 🤖 Inbox Zero Butler – Smart Email Sorting Agent for Runner

A submission for the [Runner H-AI Agent Prompting Challenge](https://dev.to/devteam/join-the-runner-h-ai-agent-prompting-challenge-10000-in-prizes-for-20-winners-30ki).

## 🧠 Overview
This project features an intelligent email-sorting prompt designed for use with the [Runner AI Agent](https://runner.dev). The agent parses raw email content and classifies each email into one of several contextual folders based on **intent**, **urgency**, and **tone** — helping users reach *Inbox Zero* faster.

[](/AI%20Email%20Sorting%20Flowchart.png)

## 🚀 What It Does
Given a raw email, the agent:
1. Understands the email’s **intent** (e.g., a support request, a task, a newsletter, etc.)
2. **Classifies** it into one of six smart categories
3. **Explains** the reasoning
4. Optionally: Suggests a next step or reply draft

## 🗃️ Supported Categories
- **Support Request**
- **Newsletter**
- **Calendar Event / Meeting Note**
- **Actionable Task**
- **Follow-Up Needed**
- **Spam / Promotion**

## 📝 Prompt Design (Core)

```prompt
You are Inbox Zero Butler, an AI agent that helps users categorize and triage their email inbox.

Task:
- Read the raw email provided.
- Classify it into one of the following:
  1. Support Request
  2. Newsletter
  3. Calendar Event / Meeting
  4. Actionable Task
  5. Follow-Up Needed
  6. Spam / Promotion

- Output the following:
  1. Category
  2. Reason (brief explanation of your decision)
  3. Suggested Action (optional – short and helpful)

---

Email:
"Hey, just checking if the refund for Order #1245 has been processed. I haven’t seen an update yet."

---

Your Output:
Category: Support Request
Reason: The sender is following up on a past order and expects a resolution.
Suggested Action: Tag this as a high-priority support ticket and notify the finance team.
```