# Robin AI (robin-ai)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Robin AI is a London-headquartered legal intelligence platform founded in 2019 by former Clifford Chance disputes lawyer Richard Robinson and machine learning researcher James Clough. The platform automates contract review, drafting, search, obligation tracking, and structured extraction for enterprise legal teams via a Microsoft Word add-in, a web workspace, and a public REST API. Robin AI shipped on Anthropic's Claude models (Claude 3 entered the stack in March 2024) and processed 500k+ documents for customers including KPMG, PwC, Pfizer, GE, UBS, and PepsiCo, advertising 80% faster contract review and 3-second clause search. The company's public-facing Robin Legal Intelligence Platform API (openapi 3.1.0, version 0.2.0-dev, base URL https://api.robinai.com, X-API-Key auth) exposes Documents, Templates, Tables, Properties, and Groups — the Tables API is the flagship extraction surface that turns unstructured legal text into clean structured data tables for CLMs, CRMs, ERPs, BI dashboards, and risk engines. NOTE Robin AI collapsed in late 2025 after failing to close a $50M funding round; the managed services arm was acquired by Scissero in December 2025 and the engineering team was acqui-hired by Microsoft in January 2026 to strengthen Word's legal AI capabilities. This profile documents the API surface as it was published at robinai.com/robin-api.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/robin-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/robin-ai/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Legal
- LegalTech
- Contract Review
- Contract Analysis
- Contract Lifecycle Management
- CLM
- Document Extraction
- Structured Data
- Legal AI
- Artificial Intelligence
- Word Add-In
- Playbook
- Redlining
- Obligation Tracking
- Anthropic
- Claude

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Robin Legal Intelligence Platform API

Public REST API for Robin AI's Legal Intelligence Platform. Exposes the Tables extraction engine, Documents store, reusable extraction Templates, custom document Properties, and organizational Groups. All requests authenticate with an X-API-Key header against https://api.robinai.com. JSON responses use cursor pagination via `limit` and `starting_after`, support ISO 8601 date-range filters, and include clickable Citations linking extracted answers back to the originating contract span. The Tables endpoints are the primary surface for high-volume contract analytics — create a Table from a Template and a set of Document IDs, build it, then page through the Results to load structured answers into CLMs, CRMs, ERPs, BI dashboards, or risk engines.

- **Human URL:** [https://robinai.com/robin-api](https://robinai.com/robin-api)
- **Base URL:** `https://api.robinai.com`

#### Tags

- Contracts
- Documents
- Tables
- Templates
- Properties
- Groups
- Extraction
- Legal AI

#### Properties

- [Documentation](https://robinai.com/robin-api)
- [Documentation](https://robinai.com/news-and-resources/blog/introducing-robins-tables-api-unlock-structured-data-from-legal-documents)
- [OpenAPI](openapi/robin-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/robin-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/robin-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/robin-ai-document-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/robin-ai-table-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/robin-ai-template-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/robin-ai-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

## Common Properties

- [Website](https://robinai.com)
- [Portal](https://robinai.com/robin-api)
- [Documentation](https://robinai.com/robin-api)
- [Documentation](https://robinai.com/news-and-resources/blog/introducing-robins-tables-api-unlock-structured-data-from-legal-documents)
- [Documentation](https://robinai.com/news-and-resources/robin-university/legal-intelligence-platform-an-ai-powered-hub-for-all-your-legal-data)
- [Documentation](https://robinai.com/news-and-resources/robin-university/how-to-streamline-your-contract-review-with-robin-ai)
- [Documentation](https://robinai.com/news-and-resources/guides-reports/legal-ai-buyers-guide)
- [Sign Up](https://app.robinai.com)
- [Sign Up](https://robinai.com/demo)
- [Pricing](https://robinai.com/pricing)
- [Plans](plans/robin-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/robin-ai-rate-limits.yml)
- [Fin Ops](finops/robin-ai-finops.yml)
- [Trust Center](https://security.robinai.com)
- [Privacy Policy](https://robinai.com/privacy)
- [Terms of Service](https://robinai.com/terms)
- [Blog](https://robinai.com/news-and-resources/blog)
- [Newsroom](https://robinai.com/news-and-resources)
- [Careers](https://robinai.com/company/careers)
- [Company](https://robinai.com/company)
- [Contact](https://robinai.com/contact)
- [Support](https://robinai.com/help)
- [LinkedIn](https://www.linkedin.com/company/robinai)
- [Twitter](https://twitter.com/Robin_LegalAI)
- [YouTube](https://www.youtube.com/@robinaichannel)
- [GitHub Organization](https://github.com/ai-robin)
- [Marketplace](https://aws.amazon.com/marketplace/reviews/reviews-list/prodview-zvgmcfv4tqtma)
- [Marketplace](https://marketplace.microsoft.com/en-in/product/office/WA200006060)
- [Integration](https://robinai.com/robin-api)
- [Customers](undefined)
- [Partners](undefined)
- [Certifications](undefined)
- [Office](undefined)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Company Status](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
