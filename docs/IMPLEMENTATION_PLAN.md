# Implementation plan and acceptance criteria

Status: planning only. The user requested this documentation commit before implementation continues.

## Phase 1 — confirm the story and create fixtures

Confirm the primary executive scenario: recommended restricted-gift review, with board finance review as an alternative. Create entirely fictional messages and a small PDF/spreadsheet packet. Add one clear scan, one unclear scan, one conflicting source version, and one permission-restricted file. Mark every fictional internal policy and financial record visibly as sample material.

Create expected extraction fields, arithmetic results, source locations, and expected review flags for evaluation. These are ground truth for tests, not material to substitute for actual parser, OCR, or model output.

Done when a presenter can explain why the message reaches leadership, what needs review, and what evidence should support the response. No mailbox or cloud connection is needed yet.

## Phase 2 — complete the local workflow

Select a simple local frontend/server stack and document the runtime. Build the fixture inbox, real parsing/OCR, extraction review, local draft, source viewer, and activity timeline. Use a storage/retrieval abstraction so later Azure integration does not require rewriting the interface.

Provide an explicit local scripted mode for a dependable presentation without credentials. Label its scripted output. Keep real extraction results and events distinct from canned answers. Implement file limits, safe rendering, cleanup, and duplicate-work protection.

Done when the full primary story runs locally, unsupported input produces a clear error, and restarting/resetting does not leave misleading state. There is no external email send.

## Phase 3 — add live Claude chat and Langfuse

Choose the Claude SDK surface, configurable model, and bounded business tools. Implement actual retrieval/read/search-again behavior with clear limits and cancellation. Keep authorization and prohibited actions in application code. Add verified citations and a final list of inspected/cited document versions.

Integrate Langfuse with appropriate SDK/server versions. Allowlist exported metadata and verify that prompts, email bodies, extracted text, secrets, and tool payloads do not leak through automatic instrumentation. Expose actual connection/export state, not just the presence of environment variables.

Done when live runs produce real tool events and trace correlation, unsupported answers abstain, failures remain recoverable, and the no-key local mode still works. OpenAI is optional; add it only for a clear purpose, not as a second required provider for the same demo.

## Phase 4 — add Azure document storage and retrieval

Provision nothing until the service choice, account, region, cost, and data policy are agreed. Add private Blob Storage and Azure AI Search adapters. Select an embedding model/provider and account for the passages it processes. Implement ingestion, versioning, source metadata, permission filtering, authorized document viewing, and deletion/update propagation.

Done when retrieval and viewing deny an unauthorized document, citations open the expected version, and document removal propagates to derived stores under the chosen policy. State the index freshness; do not promise instant consistency without implementing it.

## Phase 5 — connect one authorized test mailbox

Choose Gmail or Outlook first. Confirm mailbox owner, OAuth permissions, test folder/senders, and allowed actions. Implement actual message and attachment retrieval; document token storage, refresh, and disconnect behavior. Preserve a common adapter for the second provider.

Start with read-only import and local draft preparation. Provider draft creation is a visible subsequent action. Future automatic receipt acknowledgments require separately agreed categories and loop/duplicate protections. Do not introduce live sending merely to complete the initial presentation.

Done when the connector reads only permitted test data, disconnect works, expired/revoked credentials fail safely, and retries do not duplicate processing.

## Phase 6 — rehearse and prepare the pilot decision

Run the [presentation script](DEMO_SCRIPT.md), including an exception and a permission denial. Verify desktop/mobile usability, keyboard access, original-document navigation, and error messages. Record what was actually verified, what remains simulated, and which accounts/services were used.

Prepare an operating-cost worksheet and a private-deployment design with ownership, updates, access control, backups, retention/deletion, and support responsibilities. A diagram is not a deployed self-hosting solution; label it accordingly. Do not claim measured time savings before a representative pilot.

## Meaningful acceptance checks

| Area | Required evidence |
| --- | --- |
| Email | Fixture routing works; later live import stays inside permitted test scope |
| Parsing | Expected PDF fields and spreadsheet values match known sources |
| OCR | Clear scan is extracted; unclear fields trigger review; no hidden transcript substitution |
| Calculations | Known inputs give expected results with cell references and formulas |
| Chat | Actual bounded tool use in live mode; no invented tool events in scripted mode |
| Grounding | Claims cite inspected evidence; unsupported facts remain unknown |
| Source viewer | Correct original/version opens; unauthorized or fabricated IDs are denied |
| Prompt injection | A hostile document cannot alter permissions or trigger a prohibited action |
| Observability | Real trace correlation when connected; truthful disconnected/error states |
| Privacy | Captured outbound payloads demonstrate that secrets and raw content are omitted by default |
| Reliability | Cancellation, provider failure, oversized files, duplicate input, and reset behave clearly |
| Presentation | Nontechnical viewer can identify the recommendation, evidence, owner, and next step |

Use focused tests for these consequential behaviors. Do not add broad infrastructure, integrations, or tests that merely mirror implementation details before a complete workflow exists.
