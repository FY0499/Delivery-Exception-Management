# Delivery Exception Management

I built this n8n workflow to monitor delivery records, analyze orders that may have delivery issues, and use AI to identify likely causes, classify severity, and recommend the next action.

## How it works

1. A scheduled trigger retrieves delivery records from Google Sheets.
2. The AI agent reviews the order ID, customer, order date, latest shipment update, and notes.
3. Google Gemini identifies the likely cause of the delay, assigns a severity level, and decides whether the case needs immediate escalation.
4. JavaScript structures the AI response with the related order and customer details.
5. The workflow checks the escalation condition and sends a Telegram alert when immediate attention is needed.

## Main features

- Scheduled delivery status monitoring.
- AI-based delivery issue analysis.
- Severity classification (Low, Medium, or Critical).
- Suggested actions for delivery exceptions.
- Telegram alerts for cases requiring escalation.

## Technologies

n8n, Google Sheets, Google Gemini, JavaScript, AI Agent, Telegram, and Schedule Trigger.

## Setup

Import [workflow.json](./workflow.json) into n8n, configure your Google Sheets, Gemini, and Telegram credentials, then connect your delivery tracking sheet and make sure it includes the order, customer, date, latest update, and notes fields.
