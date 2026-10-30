# Session handoff

Last updated: October 30, 2026.

## User objective

Build a working local AI integration showcase for ACA, aimed at the CEO/CFO, alongside separate website and SEO improvement proposals. Start by committing the README and planning Markdown so work can continue across sessions.

The user's latest instruction is documentation first. Do not resume application implementation merely because earlier messages authorized a working demo. Continue from these plans when the user asks to proceed.

## Confirmed preferences

- Keep both Gmail and Outlook in the proposal; decide the first connector later.
- Eventually build a working local demo, not just a written proposal.
- Identify incoming messages, parse attachments with OCR where needed, and prepare summaries, replies, or review items.
- Reconsider the recipient and attachments so the story actually fits executive work at a nonprofit.
- Use Claude SDK integration and an agent loop for document-grounded chat.
- Show the observable process, source-file access, and the documents supporting the final answer.
- Consider blob storage and Azure AI Search for document access and retrieval.
- Use Langfuse to showcase the workflow.
- Explain value, oversight, cost, and privacy for nontechnical leadership.
- Show a path to private/self-hosted deployment and accurate provider-retention choices.

## Recommended decisions, not yet confirmed

Primary story: a development colleague forwards a fictional restricted gift offer to the CEO/CFO for review. Alternative/additional story: an internal board finance packet. A scanned invoice exception is a useful OCR example. Do not treat these recommendations as confirmed ACA workflows.

Use a local fixture mode, with a distinct live-model mode and separately configured test-mailbox connection. Keep replies in review. Azure services are candidates, not mandatory initial dependencies. OpenAI may be an optional provider for a distinct task; Claude is the requested chat/agent integration.

The exact Claude SDK surface, frontend/backend stack, model, embedding provider, hosting, runtime, OCR engine, cloud accounts, budget, and primary scenario are not selected. There is no agreed implementation schedule or measured ROI.

## Actual repository state at planning time

The repository was empty, on `main`, with no commits before this documentation work. The earlier conversation reported starter files and a dependency install, but the filesystem inspection for this handoff found neither application files nor an installed dependency tree. Treat the checked-in tree as authoritative: this baseline contains documentation and Git hygiene only.

A Git remote named `origin` exists. Its target, credentials, and access were not validated. A local commit and a remote push are separate outcomes; check `git status` and `git log` to confirm the result. Do not assume remote synchronization occurred.

The session did not find a Git user name/email in the checked configuration. If needed, the planning commit can use a clearly identified agent author through command-scoped Git settings without changing the user's global identity.

## Local environment observations

- Workspace: `C:\Users\shawn\Desktop\ACA_AI_Examples`.
- Related website project: `C:\Users\shawn\Desktop\ACADemo.com\aca-demo`; it was read for context only and should not be modified as part of this repository's work.
- PowerShell is the available shell. At inspection, `node` and `npm` were not on PATH and the Windows Python alias did not run.
- A portable Node runtime was found at `C:\Users\shawn\Desktop\ACADemo.com\.tools\node-v24.22.0-win-x64\node.exe`. This is a machine-specific observation, not a portable project prerequisite.
- No project or ancestor `AGENTS.md` was found in the inspected path. Recheck instructions in future sessions.
- No secrets or mailbox contents were read. No live emails were sent, cloud resources provisioned, or app deployments performed.

## Next session

1. Read `README.md` and these documents, then inspect the Git tree and current instructions.
2. Confirm the recommended executive story or accept a user-selected alternative. Choose the first packet and define expected results.
3. Implement Phase 1 and Phase 2 of [the plan](IMPLEMENTATION_PLAN.md) only when the user resumes implementation.
4. Keep no-key examples truthful, preserve staff review, and verify authorization before connecting external services or introducing real records.

## Presentation language

The user wants to show the "reasoning process." Meet that need through actual searches, source reads, concise action explanations, evidence gaps, and citations. Do not claim access to a complete hidden chain of thought. Likewise, distinguish proposed protections from controls actually implemented and tested.
