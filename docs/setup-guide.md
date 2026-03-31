# Setup Guide

## Prerequisites

- Running n8n instance (cloud or self-hosted)
- OpenAI API access
- Google account with Sheets access
- Slack workspace with an app or bot token
- Gmail account for outbound email

## Import Workflow

1. Open n8n.
2. Go to **Workflows** -> **Import from File**.
3. Select `workflow.json` from this repository.
4. Save the imported workflow.

## Configure Credentials

Set up credentials in n8n for:

- OpenAI
- Google Sheets
- Slack
- Gmail

Then map each credential in the corresponding node.

## Test with Sample Data

1. Open `data/sample-leads.json`.
2. Use one sample object as your form/webhook payload.
3. Execute the workflow manually.
4. Verify outputs in Google Sheets, Slack, and Gmail.

## Recommended Next Steps

- Add environment variables for thresholds and channel IDs.
- Add non-qualified branch handling (archive, CRM, or nurture email).
- Add global error trigger and alerts.
