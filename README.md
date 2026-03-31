# AI Lead Qualification System (n8n)

An end-to-end n8n automation that qualifies inbound leads with OpenAI, routes them by priority, stores outcomes in Google Sheets, alerts the team in Slack, and sends immediate Gmail follow-up for high-priority leads.

## Project Overview

This workflow converts raw form submissions into structured, actionable lead records. It reduces manual triage work and helps teams respond faster to leads that are most likely to convert.

## Business Problem Solved

Sales and operations teams often lose time manually reviewing every lead. This project automates qualification so the team can:

- prioritize high-intent leads quickly
- standardize lead scoring and status assignment
- keep a clean record of outcomes in Google Sheets
- trigger immediate internal and external notifications

## Workflow Architecture

Form -> OpenAI -> JavaScript -> IF -> Google Sheets -> Slack -> Gmail

## Features

- Form capture with standardized lead fields
- AI-based lead scoring and qualification summary
- JavaScript normalization for status, tag, and tiers
- Conditional routing for priority vs non-priority leads
- Structured append-row logging in Google Sheets
- Slack alert for priority leads
- Gmail notification for priority leads

## Setup Instructions

1. Clone the repository.
2. Import [workflow.json](workflow.json) into n8n.
3. Add credentials for OpenAI, Google Sheets, Slack, and Gmail.
4. Replace template placeholders in the workflow with your environment values.
5. Test with [data/sample-leads.json](data/sample-leads.json).

## Example Outputs

- Google Sheets row with lead profile, AI summary, score, status, and metadata
- Slack message posted to the leads channel for priority leads
- Gmail notification sent for high-priority lead follow-up

## Screenshots

- Workflow editor: [screenshots/workflow.png](screenshots/workflow.png)
- Slack notification: [screenshots/slack-notification.png](screenshots/slack-notification.png)
- Google Sheets output: [screenshots/google-sheet.png](screenshots/google-sheet.png)

## Repository Structure

```text
ai-lead-qualification-n8n/
├── workflow.json
├── README.md
├── LICENSE
├── docs/
│   ├── architecture.md
│   ├── setup-guide.md
│   ├── github-metadata.md
│   └── release-checklist.md
├── screenshots/
│   ├── workflow.png
│   ├── slack-notification.png
│   └── google-sheet.png
└── data/
    └── sample-leads.json
```

## Author

Matole Lengwe

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
