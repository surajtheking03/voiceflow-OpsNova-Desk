🧠 OpsNova Desk – Agent Jaanu (Final Guardrailed Version)

An agentic AI workflow built in Voiceflow, where Agent Jaanu evaluates internal requests, decides the correct operational action, and safely interacts with an external API to create support tickets when required.

This project focuses on reliability, guardrails, and decision-first AI design, rather than flashy responses.

🎯 Project Objective

To design an internal operations agent that:

Collects structured inputs with minimal ambiguity

Uses Prompt AI for controlled decision-making

Executes actions only when explicitly required

Handles API success, failure, and escalation safely

Always exits gracefully (no dead ends)

🏢 Dummy Brand

OpsNova Desk
A fictional internal support & operations platform.

⚠️ All APIs, endpoints, and workflows are for demonstration purposes only.

🤖 Meet Agent Jaanu

Agent Jaanu acts as a junior operations agent:

Reviews incoming requests

Assesses urgency and issue type

Decides between:

Create Ticket

Escalate

No Action

Never assumes success blindly

A little personality, yes —
but the behavior is strictly professional and deterministic.

🧱 Inputs Captured

All critical inputs are controlled to ensure stability:

User Name

Issue Type

Access Issue

Billing Issue

Feature Request

Other

Urgency Level

Low

Medium

High

Issue Description

Short free-text context (only where necessary)

Buttons and Set blocks are used wherever possible to reduce ambiguity.

🔁 High-Level Workflow
User Input
 → Structured Capture
 → Agent Jaanu (Prompt AI Decision)
    ├─ Create Ticket → API → Success / Failure Handling
    ├─ Escalate → Notify User → End
    └─ No Action → Inform User → End

🔗 External API Integration

When Agent Jaanu decides Create Ticket:

A POST request is sent to a webhook-style endpoint

Request data is passed as structured JSON

API success and failure paths are handled explicitly

This project prioritizes safe execution over optimistic assumptions.

🛡️ Guardrails & Safety Design

This workflow is guardrailed at multiple levels:

✔ Decision Guardrails

Prompt AI output is checked explicitly

Only known actions are allowed downstream

✔ API Guardrails

API calls are isolated to one controlled path

Success and failure are handled separately

Users are informed when something goes wrong

✔ User Experience Guardrails

No silent failures

Clear confirmation or escalation messaging

Retry option provided where applicable

🔐 Security & Protection Notes

This project uses a dummy webhook endpoint

No API keys or secrets are included

Authentication is intentionally out of scope

⚠️ Production Note

In real-world systems, webhook endpoints should be protected using:

API keys or bearer tokens

Secret headers

Signed payloads or IP allow-listing

This project focuses on agent design and orchestration, not backend security implementation.

🧠 What This Project Demonstrates

Agentic AI thinking (decision → action → validation)

Proper use of Prompt AI for judgment, not conversation

Safe external API orchestration

Failure-aware automation design

Clean, maintainable Voiceflow architecture

🏁 Final Note

Agent Jaanu may sound friendly,
but the workflow is strict, safe, and production-minded.

This project represents a shift from:

“I built a chatbot”
to
“I designed an agent that can be trusted.”

💙 Built by Suraj
with Agent Jaanu keeping things sane 😄