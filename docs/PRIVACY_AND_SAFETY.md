# Privacy and safety proposal

Status: intended controls and presentation guidance, not verified protections in a working system. No current compliance certification or zero-retention agreement is claimed.

## Explain the choices in plain language

"We can choose where ACA's documents and activity records are stored, control who can access them, and limit what is sent to a model. If we use an external model, that provider still processes the selected information. Its contractual terms and the exact service configuration matter."

| Option | What ACA could control | What still needs verification |
| --- | --- | --- |
| Fictional cloud demo | Which sample documents and metadata are sent | Account configuration, logging, provider processing |
| ACA-controlled application and data services | App hosting, document access, storage, deletion, and optionally Langfuse | External model/embedding/OCR terms; cloud operators and backups |
| Application plus locally hosted model | Model processing can also remain inside the selected environment | Model quality, operations, hardware, licenses, security, residual network egress |

Azure Blob Storage and Azure AI Search are managed cloud services, not a fully self-hosted stack. A self-hosting proposal should separately cover application hosting, private file/object storage, a local search/vector service, OCR, Langfuse and its supported dependencies, and optionally a locally served model. Self-hosting shifts operational responsibility to ACA or its operator. It does not guarantee security by itself.

## Account for every copy

| Data destination | Proposed handling |
| --- | --- |
| Gmail / Microsoft 365 | Dedicated test inbox for demo; original email remains under mailbox retention |
| Downloaded files / temporary OCR images | Private temporary storage, bounded lifetime, cleanup after failures |
| Original document storage | Private access, version identity, explicit retention policy |
| Extracted text / search chunks / embeddings | Treat as sensitive derived copies with matching permissions and deletion rules |
| Model requests and outputs | Minimum necessary selected context; verify provider terms and features |
| Langfuse and application logs | Minimal metadata by default; redact before export; never log tokens or secrets |
| Browser state and exports | Avoid sensitive browser persistence; protect downloads and clear demo state |
| Backups | Separate retention and restore procedure; explain that active deletion may not erase backups immediately |

Before a real pilot, choose retention periods with ACA, test deletion across these destinations, and document exceptions. Do not invent a legally required retention period for ACA.

## Model-provider retention

OpenAI API training use, abuse-monitoring logs, and stored application state are separate matters. `store: false` alone is not proof of zero retention. OpenAI's additional retention controls require approval, and endpoint/feature limitations apply. Use the [official OpenAI data controls documentation](https://developers.openai.com/api/docs/guides/your-data) for the exact planned request path.

Anthropic zero-retention arrangements also require eligibility and approval; the covered products, selected models, and exceptions matter. Do not transfer a retention claim from an API account to a consumer subscription or assume every model has identical terms. See [Anthropic's zero-retention scope](https://privacy.claude.com/en/articles/8956058-i-have-a-zero-data-retention-agreement-with-anthropic-what-products-does-it-apply-to).

These providers are options, not evidence that ACA already has an agreement. Choose and validate account, model, endpoint, features, regions, OCR/embedding providers, and logging before using confidential records. Check the terms again when implementation begins.

## Application controls to demonstrate

- A source file cannot issue instructions to the application. Email, attachments, and retrieved text are untrusted content. Reject attempts to override policy, reveal secrets, or send information elsewhere.
- Permission checks run before search, document reading, and document viewing. Test with at least two roles and one restricted document.
- Low-quality OCR, ambiguous dates, missing fields, and conflicting versions lead to review, not invented certainty. Confidence scores are a signal, not proof of correctness.
- Citations must resolve to documents and passages actually available to the user. A citation is evidence to inspect, not an automatic factual guarantee.
- Numeric results come from validated data and deterministic calculations. Staff still decide financial treatment and approval.
- The model cannot send unrestricted email, accept a gift, authorize spending, change payment details, or create accounting entries.
- Future automatic acknowledgments require an allowlisted category, a dedicated permitted mailbox, idempotency, automated-message detection, rate limits, and a stop switch. A trusted-looking sender is not sufficient authorization for a sensitive action.
- Secrets remain on the server and outside Git. Cloud exports use an explicit field allowlist; check instrumentation so prompts and tool outputs are not captured accidentally.

Langfuse supports masking before transmission; masking rules still need testing, and content omission is preferable when content is unnecessary. See [Langfuse data masking](https://langfuse.com/self-hosting/security/data-masking).

## What leadership should see

Demonstrate one missing-field exception, one unsupported question, and one inaccessible source. Show that staff can inspect the evidence and stop a proposed action. Explain the current mode and destinations in a small data-flow view; do not display a generic "100% safe" or "zero retention" badge without verified evidence.
