# Architecture

## Workflow Path

Form -> OpenAI -> JavaScript -> IF -> Google Sheets -> Slack -> Gmail

## Step-by-Step Design

1. **Form (Trigger)**
   - Captures incoming lead details from a web form or webhook.
   - Typical fields: name, email, company, role, company size, budget, message.

2. **OpenAI (Lead Analysis)**
   - Scores lead quality based on fit and intent.
   - Produces structured output such as `lead_score`, `qualification_reason`, and `priority`.

3. **JavaScript (Normalization)**
   - Cleans and standardizes model output.
   - Converts free-form values into predictable keys for routing and storage.

4. **IF (Decision Gate)**
   - Applies a qualification threshold (example: score >= 70).
   - Routes qualified and non-qualified leads to different branches.

5. **Google Sheets (Logging)**
   - Appends qualified lead records for team visibility and reporting.
   - Stores key metadata including score, source, and timestamp.

6. **Slack (Internal Alert)**
   - Sends real-time notifications to sales or operations channels.
   - Includes lead summary and score to support fast response.

7. **Gmail (External Follow-Up)**
   - Sends a follow-up or confirmation email to qualified leads.
   - Can be templated by score band or lead segment.

## Data Flow Notes

- Input data is enriched by AI before business rules are applied.
- Routing logic is centralized in the IF node for transparency.
- Storage and notifications are decoupled to keep the workflow maintainable.

## Operational Considerations

- Keep API keys in n8n credential manager only.
- Add retry/error handling as a next iteration.
- Add audit fields for debugging (run ID, processing timestamp, model version).
