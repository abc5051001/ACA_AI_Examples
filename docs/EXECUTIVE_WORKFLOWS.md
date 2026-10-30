# Executive workflows and attachment design

## How a nonprofit operates

A nonprofit pursues a mission and needs income, staff, programs, financial controls, and oversight to sustain that work. It may receive donations, grants, or other income; not every organization has the same funding model. A board oversees the organization, executive leadership directs its work, and finance helps manage budgets, cash, reporting, and controls. Development staff manage fundraising and donor relationships; program staff carry out mission work. In smaller organizations, one person may cover several functions.

An important distinction is whether a donor limits how a contribution may be used. Money in an account should not automatically be treated as available for any expense. Financial management and board oversight therefore make useful executive demonstration themes. This is a general operating model, not a finding about ACA's staffing or accounting. See the [National Council of Nonprofits' financial management resources](https://www.councilofnonprofits.org/running-nonprofit/administration-and-financial-management/financial-management) and [Minnesota Council of Nonprofits' financial management guidance](https://minnesotanonprofits.org/resources-tools/principles-practices-for-nonprofit-excellence/financial-management).

ACA's public [frequently asked questions](https://www.alleycat.org/about/frequently-asked-questions-faq/) describes its mission and public cat-care resources. That supports a mission-relevant presentation; it does not establish its private email routing, approval policies, or grant operations. Do not assume ACA operates as a local adoption shelter or that a particular executive personally processes routine inquiries.

## Which messages would reach a CEO or CFO?

Usually the executive relevance comes from a relationship, decision, exception, or deadline. A message might arrive directly, be copied to leadership, or be forwarded by a development or finance colleague. Invoices often reach accounts payable first; routine donor questions usually reach development or support first. The demo should represent that routing instead of treating every incoming message as executive correspondence.

| Message | Likely initial owner in a typical organization | Executive reason to review | Attachment examples |
| --- | --- | --- | --- |
| Major donor offers support with conditions | Development | Mission fit, acceptance terms, restrictions | Gift letter PDF, proposed budget XLSX |
| Funder requests a report or agreement review, if applicable | Development / program lead | Obligations, deadlines, commitments | Funding agreement PDF, reporting template DOCX, budget XLSX |
| Finance sends a board briefing draft | Finance lead / CFO | Financial position, variances, board questions | Finance memo PDF, budget-versus-actual XLSX, program update PDF |
| Invoice has an approval or payment exception | Accounts payable / finance | Resolve an exception within delegated authority | Invoice PDF/scan, purchase approval, invoice register CSV |
| Audit team asks for supporting records | Finance | Coordinate review and accountable responses | Request list XLSX, draft management letter PDF |
| Partner proposes a significant collaboration | Program lead / CEO | Strategy, capacity, commitments | Proposal PDF, draft memorandum DOCX |

The last two are optional extensions, not initial implementation requirements. Neither public practice nor AI classification establishes an actual ACA executive's authority.

## Recommended primary story: a restricted gift offer

Use a fictional development colleague forwarding a fictional donor's proposed gift to the CEO and CFO: "Can you review the conditions and what we need to clarify before replying?" This is a decision-oriented review, not a generic inquiry.

Proposed fixture packet:

- `gift-offer.pdf`: a proposed $25,000 gift for a fictional Community Cat Care Pilot, with a January 1–March 31, 2027 use period and a report due April 15, 2027. Sample terms allow sterilization services and transport, and exclude equipment purchases.
- `proposed-budget.xlsx`: the draft use of funds, with clearly labeled totals and categories.
- `gift-review-policy.pdf`: a fictional, versioned demonstration policy describing review roles. It must carry "Sample policy — not an ACA policy."
- `program-plan.pdf`: the fictional scope and intended activities, without representing a real ACA commitment.

AI extracts the offer amount, purpose, dates, restrictions, reporting obligations, and ambiguities with page/cell references. It retrieves the sample review policy, flags unresolved questions, and drafts a response for staff review. An offered gift is not received cash, an accepted award, or unrestricted revenue. The system must not turn a proposed offer into a financial commitment.

Suggested follow-up: "What should we clarify before accepting this offer, and which documents support that recommendation?" The answer should distinguish explicit terms, derived observations, and missing information. The proposed fixture terms are illustrative, not accounting or legal guidance.

## Complementary story: prepare a board finance briefing

An internal finance colleague sends a draft packet to the CFO, with the CEO copied, asking for review before a board meeting. This makes fewer assumptions about external grant funding than a funder-specific workflow.

Use a synthetic budget-versus-actual XLSX, a finance memo PDF, and a program narrative. AI summarizes the largest changes and identifies questions. Arithmetic is performed by a deterministic calculation tool over parsed cells, with period, units, formulas, and source cells visible. The language model explains the calculation rather than inventing it. This is an optional second scenario after the first complete workflow.

## Attachment exception: a scanned invoice

Use a fictional vendor invoice and purchase approval. A clear scan demonstrates actual OCR; a deliberately unclear copy demonstrates staff review. Retain a human-authored expected transcript for evaluation, but do not pass that transcript off as OCR output.

Extract vendor, invoice number, invoice date, line items, total, currency, and due date only when supported. Label unreadable fields as unknown. A matching invoice number/vendor in a supplied register is a possible duplicate requiring review, not proof of fraud. A payment-instruction change must never trigger an automated bank-detail update.

## Questions for ACA discovery

Before introducing real data, establish which workflow occurs frequently, who receives it, what the actual attachments look like, who can approve a response, and what systems hold authoritative records. Confirm whether grants received, grants issued, restricted gifts, or other funding categories are relevant. These questions should refine the pilot; they need not block building fictional fixtures.
