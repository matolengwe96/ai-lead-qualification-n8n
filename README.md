# AI Lead Qualification System (n8n)

Professional starter repository for an AI-powered lead qualification pipeline built in n8n.

## Summary

This project receives inbound leads, enriches and scores them with AI, applies qualification logic, records qualified leads in Google Sheets, and sends notifications to Slack and email.

## Workflow

Form -> AI -> JS -> IF -> Sheets -> Slack -> Email

## Repository Structure

```text
ai-lead-qualification-n8n/
|-- workflow.json
|-- README.md
|-- docs/
|   |-- architecture.md
|   `-- setup-guide.md
|-- screenshots/
|   |-- workflow.png
|   |-- slack-notification.png
|   `-- google-sheet.png
`-- data/
	`-- sample-leads.json
```

## Files

- workflow.json: Main n8n workflow export file.
- docs/architecture.md: Architecture overview and node-by-node flow.
- docs/setup-guide.md: Setup and import instructions.
- data/sample-leads.json: Example lead payloads for testing.
- screenshots/: Visual documentation assets.

## Quick Start

1. Clone this repository.
2. Import workflow.json into n8n.
3. Configure credentials for AI, Google Sheets, Slack, and Gmail.
4. Run a test execution with data/sample-leads.json.
5. Activate and monitor the workflow.

## License

Add your preferred license, such as MIT.
