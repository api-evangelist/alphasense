# AlphaSense (alphasense)

AlphaSense is an AI-powered market intelligence and search platform used by hedge funds, banks, corporates, consulting firms, and law firms to accelerate research and decision-making. The platform unifies 500M+ public and private documents - SEC filings, broker research from 1,500+ firms, news, earnings call transcripts, internal company content, and 260,000+ Tegus expert call transcripts (Tegus was acquired in December 2023 for ~$930M) - behind a generative search and agent layer (GenSearch, Deep Research, Workflow Agents). The developer surface is gated, enterprise-only, and is split across two contracts: an Agent API for embedding GenSearch / Deep Research / MCP tools into customer AI agents, and a set of Utility APIs (Search, Brokers, Companies, Watchlist, Trends, User, Download, Ingestion) for direct programmatic access. Both are exposed over a single OAuth 2.0-protected GraphQL endpoint at https://api.alpha-sense.com/gql, with a companion REST Ingestion API for Enterprise Intelligence customers. AlphaSense Enterprise Intelligence Private Cloud ships with a public Go CLI (AlphaSense-Engineering/privatecloud-cli) for installing and validating the Kubernetes-hosted environment in a customer's own VPC.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/alphasense/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/alphasense/refs/heads/main/apis.yml)

## Tags

- Market Intelligence
- Financial Research
- Search
- Generative AI
- AI Agents
- Expert Calls
- Document Intelligence
- Enterprise Intelligence
- MCP
- GraphQL

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### AlphaSense Agent API

GraphQL surface for embedding AlphaSense intelligence into customer AI agents. Wraps GenSearch (auto / fast / thinkLonger / deepResearch modes), Workflow Agents (pre-built and custom), and the Document Search API behind a single OAuth 2.0 + API-key-protected /gql endpoint. Returns markdown-formatted answers with inline citations to the underlying AlphaSense source documents (filings, transcripts, broker research, Tegus calls). Designed for agentic workflows that need first-result in under five minutes.

- **Human URL:** [https://developer.alpha-sense.com/agent-api/quickstart](https://developer.alpha-sense.com/agent-api/quickstart)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- GraphQL
- Generative AI
- Agents
- GenSearch
- Deep Research

#### Properties

- [Documentation](https://developer.alpha-sense.com/agent-api/quickstart)
- [Authentication](https://developer.alpha-sense.com/api/getting-started)
- [OpenAPI](openapi/alphasense-agent-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/alphasense-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/alphasense-gensearch-conversation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/alphasense-citation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/alphasense-workflow-agent-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/alphasense-gensearch-conversation-structure.json)
- [JSON Structure](json-structure/alphasense-citation-structure.json)
- [JSON Structure](json-structure/alphasense-workflow-agent-structure.json)
- [Example](examples/alphasense-gensearch-conversation-example.json)
- [Example](examples/alphasense-citation-example.json)
- [Example](examples/alphasense-workflow-agent-example.json)

### AlphaSense Search API

GraphQL search over the full AlphaSense content library (500M+ documents spanning SEC filings, broker research from 1,500+ firms, news, earnings call transcripts, and Tegus expert interviews). Supports keyword and semantic filters, date presets, document-type filters, watchlists, and smart synonyms. Operates against the same OAuth-protected /gql endpoint as the Agent API. Used to drive in-app search and retrieval flows that do not need agentic answer synthesis.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- GraphQL
- Search
- Documents
- Retrieval

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [OpenAPI](openapi/alphasense-utility-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/alphasense-document-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/alphasense-document-structure.json)
- [Example](examples/alphasense-document-example.json)
- [Example](examples/alphasense-tegus-document-example.json)

### AlphaSense Ingestion API

REST surface (`/services/i/ingestion-api/v1/...`) used by Enterprise Intelligence customers to push their own internal documents - research notes, board decks, CRM exports, meeting transcripts - into AlphaSense so the same GenSearch and Deep Research layer can answer over external market intelligence and internal company content together. Available on SaaS (https://api.alpha-sense.com) and Private Cloud (customer-hosted domain) deployments.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- REST
- Ingestion
- Enterprise Intelligence
- Internal Content

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [OpenAPI](openapi/alphasense-utility-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/alphasense-ingestion-job-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/alphasense-ingestion-job-structure.json)
- [Example](examples/alphasense-ingestion-job-example.json)

### AlphaSense Companies API

GraphQL operations for resolving and enriching companies in the AlphaSense entity graph - ticker / name / CIK / ISIN lookup, parent / subsidiary relationships, sector and industry tagging, and references that join into Search and GenSearch filters.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- Companies
- Entities
- Reference Data

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [OpenAPI](openapi/alphasense-utility-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/alphasense-company-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/alphasense-company-structure.json)
- [Example](examples/alphasense-company-example.json)

### AlphaSense Brokers API

Lookup and metadata for the 1,500+ broker research firms whose content AlphaSense licenses. Resolves broker identifiers used by the Search API and exposes coverage signals for analysts filtering by source.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- Brokers
- Research
- Reference Data

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [OpenAPI](openapi/alphasense-utility-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/alphasense-broker-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/alphasense-broker-structure.json)
- [Example](examples/alphasense-broker-example.json)

### AlphaSense Watchlist API

Create, read, update, and delete user watchlists - persisted bundles of companies, tickers, and saved searches that drive personalized alerts, digests, and re-ranked Search results.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- Watchlists
- Personalization
- Alerts

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [OpenAPI](openapi/alphasense-utility-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/alphasense-watchlist-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/alphasense-watchlist-structure.json)
- [Example](examples/alphasense-watchlist-example.json)

### AlphaSense Trends API

Time-series operations for theme, keyword, and topic frequency across the document corpus - the back end behind AlphaSense's Trend visualisations and competitive-intelligence dashboards.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- Trends
- Analytics
- Time Series

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [Postman Collection](collections/alphasense-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AlphaSense User API

User and account management operations covering profile, preferences, session, and entitlement metadata for integrating the AlphaSense experience into a host application or single-sign-on flow.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- Users
- Accounts
- Identity

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [Postman Collection](collections/alphasense-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AlphaSense Download / Export API

Bulk export and download operations for documents, search results, and report PDFs - used to push AlphaSense content into downstream data warehouses, vaults, and BI tools.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- Downloads
- Export
- Bulk

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [Postman Collection](collections/alphasense-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AlphaSense Authentication API

OAuth 2.0 password-grant token endpoint at POST /auth. Clients submit email, password, client_id, and client_secret together with an x-api-key header to receive a bearer token used on every subsequent Agent or Utility API call. The same flow works against SaaS (https://api.alpha-sense.com) and Private Cloud (https://{your-domain}/) base URLs.

- **Human URL:** [https://developer.alpha-sense.com/api/getting-started](https://developer.alpha-sense.com/api/getting-started)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- Authentication
- OAuth 2.0
- Token

#### Properties

- [Documentation](https://developer.alpha-sense.com/api/getting-started)
- [OpenAPI](openapi/alphasense-agent-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/alphasense-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/alphasense-auth-token-example.json)

### AlphaSense MCP Server

Model Context Protocol surface that lets MCP-aware AI clients (Claude, Cursor, ChatGPT-style desktop hosts, in-house agent frameworks) call GenSearch, ThinkLonger, and Deep Research as tools without writing a bespoke GraphQL integration. The MCP server brokers the OAuth flow and enforces the customer's Agent API entitlement.

- **Human URL:** [https://developer.alpha-sense.com/agent-api/quickstart](https://developer.alpha-sense.com/agent-api/quickstart)
- **Base URL:** `https://api.alpha-sense.com`

#### Tags

- MCP
- Model Context Protocol
- Agents
- Tools

#### Properties

- [Documentation](https://developer.alpha-sense.com/agent-api/quickstart)
- [Postman Collection](collections/alphasense-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AlphaSense Private Cloud CLI

Go-based CLI (AlphaSense-Engineering/privatecloud-cli, Apache-2.0-ish "Other" license) used by Enterprise Intelligence Private Cloud customers to bootstrap and validate the Kubernetes cluster that hosts AlphaSense inside their own cloud account. Ships `check` and `install` commands that lay down Crossplane and platform namespaces, generate the required ServiceAccounts, Roles, ClusterRoles, and Pods, and reconcile against per-version compatibility matrices.

- **Human URL:** [https://github.com/AlphaSense-Engineering/privatecloud-cli](https://github.com/AlphaSense-Engineering/privatecloud-cli)
- **Base URL:** `https://github.com/AlphaSense-Engineering/privatecloud-cli`

#### Tags

- CLI
- Private Cloud
- Kubernetes
- Enterprise Intelligence

#### Properties

- [GitHub Repository](https://github.com/AlphaSense-Engineering/privatecloud-cli)
- [Release Notes](https://github.com/AlphaSense-Engineering/privatecloud-cli/releases)
- [Postman Collection](collections/alphasense-agent-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-agent-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/alphasense-utility-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/alphasense-utility-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.alpha-sense.com/)
- [Developer Portal](https://developer.alpha-sense.com/)
- [Documentation](https://developer.alpha-sense.com/)
- [Getting Started](https://developer.alpha-sense.com/api/getting-started)
- [Quickstart](https://developer.alpha-sense.com/agent-api/quickstart)
- [Authentication](https://developer.alpha-sense.com/api/getting-started)
- [GitHub Organization](https://github.com/AlphaSense-Engineering)
- [Trust Center](https://trust.alpha-sense.com/)
- [Support](https://help.alpha-sense.com/)
- [LinkedIn](https://www.linkedin.com/company/alphasense)
- [Plans](plans/alphasense-plans-pricing.yml)
- [Rate Limits](rate-limits/alphasense-rate-limits.yml)
- [Fin Ops](finops/alphasense-finops.yml)
- [Spectral Rules](rules/alphasense-rules.yml)
- [Vocabulary](vocabulary/alphasense-vocabulary.yml)
- [JSON-LD](json-ld/alphasense-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)
- [L L Ms Txt](https://developer.alpha-sense.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
