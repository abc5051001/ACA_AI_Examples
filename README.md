# ACA AI integration showcase

Planning repository for a working AI demonstration for Alley Cat Allies (ACA), following separate website-improvement and SEO proposals. The audience is the CEO, CFO, and other nontechnical leaders.

The central story: **help staff review important correspondence, understand documents, and prepare supported decisions while keeping people in control.**

## Current state

Documentation only. No application, dependencies, cloud resources, mailbox connections, or deployed services are implemented. These documents define proposed behavior, not features that already work. Work on implementation should resume from [the session handoff](docs/SESSION_HANDOFF.md).

## Agreed direction

- Build a working local demo after this planning commit.
- Keep Gmail and Microsoft 365 / Outlook in scope; choose the first live connector later.
- Identify incoming email, extract attachments, use OCR when needed, and prepare a summary, reply, or review item.
- Focus the presentation on executive workflows rather than assuming routine public inquiries reach the CEO/CFO.
- Build document-grounded chat with a Claude SDK agent loop that can search, inspect evidence, and search again.
- Show the observable process, retrieved passages, and documents supporting the answer. A concise explanation of an action is distinct from a model's hidden internal reasoning.
- Use Langfuse to demonstrate the workflow, usage, cost where available, errors, and staff approval points.
- Consider Azure Blob Storage for originals and Azure AI Search for retrieval. These are proposed services, not provisioned resources or final hosting decisions.
- Demonstrate data protection in plain language, with fictional data first and an honest distinction between ACA-controlled hosting and external model processing.

## Recommended executive scenarios

| Scenario | Why it belongs with leadership | Proposed attachments |
| --- | --- | --- |
| Restricted donation / funding offer | Acceptance terms, spending limits, obligations, and mission fit may need CEO/CFO review | Gift letter or draft funding agreement PDF, budget spreadsheet, reporting schedule |
| Board finance packet | CEO/CFO need a reliable briefing and explanations of changes | Budget-versus-actual spreadsheet, finance memo PDF, program update |
| Invoice exception | Finance escalates missing approval, a possible duplicate, or a changed payment instruction | Invoice PDF or scan, purchase approval, prior invoice register |

These are plausible examples, not verified descriptions of ACA's inboxes or policies. The primary scenario and fixtures remain recommendations until the user confirms them. See [executive workflows](docs/EXECUTIVE_WORKFLOWS.md).

## Documents

- [Executive workflows and attachments](docs/EXECUTIVE_WORKFLOWS.md)
- [Proposed architecture and document-grounded chat](docs/ARCHITECTURE.md)
- [Data privacy, safety, and deployment choices](docs/PRIVACY_AND_SAFETY.md)
- [CEO/CFO demonstration script](docs/DEMO_SCRIPT.md)
- [Implementation phases and acceptance criteria](docs/IMPLEMENTATION_PLAN.md)
- [Session handoff and unresolved decisions](docs/SESSION_HANDOFF.md)

## Scope boundaries

Use fictional people, donors, vendors, messages, and internal policies. Public ACA materials may be used as separately labeled sources with their provenance preserved. Never present an invented policy, funding offer, financial result, or projected saving as an ACA fact.

Staff review replies and financial interpretations. The demo does not accept gifts, approve expenses, change bank details, execute payments, or make accounting entries. A future automatic email reply should be limited to a deliberately approved category such as receipt acknowledgment.

No real emails are to be sent during development. A request to build or commit this demo does not authorize connecting an executive mailbox, importing confidential records, or sending messages.

Planning baseline: October 30, 2026. Provider policies and service capabilities must be checked again during implementation.
