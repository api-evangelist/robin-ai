# Robin AI (robin-ai)

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
