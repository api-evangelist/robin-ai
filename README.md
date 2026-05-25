# Robin AI

> London-headquartered legal AI platform for enterprise contract review, drafting, search, obligation tracking, and bulk structured extraction. Powered by Anthropic's Claude models and shipped as a Microsoft Word add-in, a web workspace, and a public REST API at `api.robinai.com`.

API Evangelist profile of **Robin AI** — the Legal Intelligence Platform founded in 2019 by Richard Robinson (ex-Clifford Chance) and James Clough. At its peak Robin served 13 Fortune 500 customers and major private equity firms including **KPMG, PwC, Pfizer, GE, UBS, and PepsiCo**, processed 500,000+ documents, and advertised 80% faster contract review with 3-second clause search.

## Status (as of May 2026)

Robin AI **collapsed in late 2025** after failing to close a $50M funding round. The wind-down played out across two transactions:

- **December 2025** — The managed services arm was acquired by **Scissero**.
- **January 2026** — **Microsoft acqui-hired the engineering team** to strengthen Word's legal AI capabilities.

The Robin API surface (`api.robinai.com`) and product documentation at [robinai.com/robin-api](https://robinai.com/robin-api) remain published, but live availability beyond the wind-down period is uncertain. This profile preserves the API design as it was shipped to enterprise customers.

## The API

| | |
|---|---|
| **Spec** | OpenAPI 3.1.0, version `0.2.0-dev` |
| **Base URL** | `https://api.robinai.com` |
| **Auth** | `X-API-Key` header |
| **Pagination** | `limit` (1–1000, default 100) + `starting_after` cursor |
| **Filters** | ISO 8601 date ranges (`created_*`, `updated_*`), name, status, group |
| **Citations** | Every Tables answer carries a clickable Citation back to the source span |

Five top-level resource families:

| Resource | Surface |
|---|---|
| **Documents** | Upload (multipart), list with property filters, fetch, attach typed Properties |
| **Tables** | Bulk extraction jobs — create from a Template + Documents, build, cancel, list Results |
| **Templates** | Reusable, ordered prompt sets with typed `answer_format` (text_summary, number_currency, date, boolean, list, …) |
| **Properties** | Typed custom property definitions (string, number, currency, date-time, boolean) |
| **Groups** | Organizational containers — personal, private, public, report_public, report_private |

## What's in this repo

| Path | Contents |
|---|---|
| [`apis.yml`](apis.yml) | APIs.json provider record for Robin AI |
| [`openapi/robin-ai-openapi.yml`](openapi/robin-ai-openapi.yml) | Full OpenAPI 3.1 spec for the v1 Legal Intelligence Platform API |
| [`json-schema/`](json-schema/) | JSON Schemas for Document, Table, and Template resources |
| [`json-structure/`](json-structure/) | JSON Structure description of the Document resource |
| [`json-ld/robin-ai-context.jsonld`](json-ld/robin-ai-context.jsonld) | Linked-data context mapping Robin terms to schema.org |
| [`examples/`](examples/) | Request/response examples for Create Document, Create Table, List Table Results |
| [`capabilities/contract-extraction.yaml`](capabilities/contract-extraction.yaml) | Naftiko capability: upload → template → table → build → poll → results |
| [`capabilities/document-management.yaml`](capabilities/document-management.yaml) | Naftiko capability: upload, tag, and search documents |
| [`rules/robin-ai-rules.yml`](rules/robin-ai-rules.yml) | Spectral ruleset enforcing Robin's `/v1/` prefix, typed-ID, and cursor-pagination conventions |
| [`vocabulary/robin-ai-vocabulary.yml`](vocabulary/robin-ai-vocabulary.yml) | Domain vocabulary — resources, statuses, answer formats, legal concepts |
| [`plans/robin-ai-plans-pricing.yml`](plans/robin-ai-plans-pricing.yml) | API Commons Plans — Word Add-In, Workspace, API Access, AWS Marketplace |
| [`rate-limits/robin-ai-rate-limits.yml`](rate-limits/robin-ai-rate-limits.yml) | API Commons Rate Limits — documented 429/402 envelopes, cursor caps |
| [`finops/robin-ai-finops.yml`](finops/robin-ai-finops.yml) | FOCUS-aligned mapping of Robin's chargeable dimensions |

## Tags

`Legal` · `LegalTech` · `Contract Review` · `Contract Analysis` · `Contract Lifecycle Management` · `CLM` · `Document Extraction` · `Structured Data` · `Legal AI` · `Artificial Intelligence` · `Word Add-In` · `Playbook` · `Redlining` · `Obligation Tracking` · `Anthropic` · `Claude`

## Links

- Website — <https://robinai.com>
- API docs — <https://robinai.com/robin-api>
- Tables API launch post — <https://robinai.com/news-and-resources/blog/introducing-robins-tables-api-unlock-structured-data-from-legal-documents>
- Web app — <https://app.robinai.com>
- Trust Center — <https://security.robinai.com>
- GitHub org — <https://github.com/ai-robin>
- AWS Marketplace — <https://aws.amazon.com/marketplace/reviews/reviews-list/prodview-zvgmcfv4tqtma>
- Microsoft AppSource (Word Add-In) — <https://marketplace.microsoft.com/en-in/product/office/WA200006060>
- Microsoft acqui-hire coverage — [Artificial Lawyer](https://www.artificiallawyer.com/2026/01/09/microsoft-to-acqui-hire-robin-ai-tech-team/), [Legal IT Insider](https://legaltechnology.com/2026/01/12/microsoft-hires-raft-of-robin-ai-engineers-to-bolster-its-word-team/)

Maintained by [Kin Lane](https://apievangelist.com) · part of the [API Evangelist](https://apievangelist.com) catalog.
