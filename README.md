# AlphaSense (alphasense)

AlphaSense is an AI-powered market intelligence and search platform used by hedge funds, banks, corporates, consulting firms, and law firms to accelerate research and decision-making. The platform unifies 500M+ public and private documents - SEC filings, broker research from 1,500+ firms, news, earnings call transcripts, internal company content, and 260,000+ Tegus expert call transcripts (Tegus was acquired in December 2023 for ~$930M) - behind a generative search and agent layer (GenSearch, Deep Research, Workflow Agents). The developer surface is gated, enterprise-only, and is split across two contracts: an Agent API for embedding GenSearch / Deep Research / MCP tools into customer AI agents, and a set of Utility APIs (Search, Brokers, Companies, Watchlist, Trends, User, Download, Ingestion) for direct programmatic access. Both are exposed over a single OAuth 2.0-protected GraphQL endpoint at https://api.alpha-sense.com/gql, with a companion REST Ingestion API for Enterprise Intelligence customers. AlphaSense Enterprise Intelligence Private Cloud ships with a public Go CLI (AlphaSense-Engineering/privatecloud-cli) for installing and validating the Kubernetes-hosted environment in a customer's own VPC.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/alphasense/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=alphasense-api-evangelist&utm_content=repo)

## Type

- **x-type:** company

## Tags

- Market Intelligence, Financial Research, Search, Generative AI, AI Agents, Expert Calls, Document Intelligence, Enterprise Intelligence, MCP, GraphQL

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

| API | Description |
|---|---|
| AlphaSense Agent API | GraphQL surface that wraps GenSearch (auto / fast / thinkLonger / deepResearch), Workflow Agents, and Document Search behind /gql for customer-built AI agents. |
| AlphaSense Search API | GraphQL search over 500M+ filings, broker research, news, transcripts, and Tegus expert calls. |
| AlphaSense Ingestion API | REST surface for pushing customer-owned internal documents into Enterprise Intelligence. |
| AlphaSense Companies API | Company resolution (ticker / name / CIK / ISIN) and metadata. |
| AlphaSense Brokers API | Reference data for the 1,500+ broker research firms whose content is licensed by AlphaSense. |
| AlphaSense Watchlist API | CRUD for user watchlists of companies, tickers, and saved queries. |
| AlphaSense Trends API | Keyword / theme frequency time-series. |
| AlphaSense User API | User profile and entitlement operations. |
| AlphaSense Download / Export API | Bulk export of documents and reports. |
| AlphaSense Authentication API | OAuth 2.0 password-grant /auth endpoint plus x-api-key header. |
| AlphaSense MCP Server | Model Context Protocol surface for GenSearch, ThinkLonger, and Deep Research as agent tools. |
| AlphaSense Private Cloud CLI | Go-based CLI for installing and validating Enterprise Intelligence Private Cloud on a customer Kubernetes cluster. |

## Common Properties

- [Website](https://www.alpha-sense.com/)
- [DeveloperPortal](https://developer.alpha-sense.com/)
- [Documentation](https://developer.alpha-sense.com/)
- [GettingStarted](https://developer.alpha-sense.com/api/getting-started)
- [Quickstart](https://developer.alpha-sense.com/agent-api/quickstart)
- [Authentication](https://developer.alpha-sense.com/api/getting-started)
- [GitHubOrganization](https://github.com/AlphaSense-Engineering)
- [TrustCenter](https://trust.alpha-sense.com/)
- [Support](https://help.alpha-sense.com/)
- [LinkedIn](https://www.linkedin.com/company/alphasense)
- [Plans](plans/alphasense-plans-pricing.yml) - API Commons Plans 0.1
- [RateLimits](rate-limits/alphasense-rate-limits.yml) - API Commons Rate Limits 0.1
- [FinOps](finops/alphasense-finops.yml) - FOCUS-aligned FinOps Framework 1.0
- [SpectralRules](rules/alphasense-rules.yml)
- [Vocabulary](vocabulary/alphasense-vocabulary.yml)
- [JSONLD](json-ld/alphasense-context.jsonld)

## Features

| Name | Description |
|------|-------------|
| Generative Search (GenSearch) | Multi-agent search-and-answer layer over 500M+ documents with auto, fast, ThinkLonger, and Deep Research reasoning modes. |
| Deep Research | Long-horizon agent that decomposes a research question, plans steps, searches filings / transcripts / broker research / Tegus, and returns a markdown report with inline citations. |
| Workflow Agents | Pre-built and custom agents addressable by id for repeatable research tasks (earnings prep, competitor scan, KOL mapping). |
| Tegus Expert Insights | 260,000+ private expert-call transcripts and on-demand expert interviews, integrated post-acquisition (Dec 2023, ~$930M). |
| Enterprise Intelligence | Search the generative layer over a customer's internal documents alongside the external AlphaSense corpus. |
| Enterprise Intelligence Private Cloud | Customer-hosted Kubernetes deployment for regulated buyers; managed via the public privatecloud-cli. |
| Financial Data | Structured financial datasets and 4,000+ pre-built financial models integrated with the search layer. |
| Smart Synonyms | Domain-tuned query expansion mapping tickers, jargon, and industry terms to the right document language. |
| Inline Citations | Every GenSearch / Deep Research answer ships with traceable citations back to the underlying document, page, and span. |

## Use Cases

| Name | Description |
|------|-------------|
| Sell-Side Investment Banking | Pitch prep, comparables analysis, M&A target screening, and earnings-call review. |
| Hedge Fund Research | Idea generation, thesis monitoring, and competitive tracking across filings, broker research, and Tegus expert calls. |
| Private Equity Diligence | Industry primers, KOL identification, and management-quality assessment. |
| Asset Management | Coverage scaling across long-tail names and themes. |
| Venture Capital | Market sizing, founder background, and category-comp scans. |
| Corporate Strategy & CI | Competitor surveillance, market-trend tracking, and board-pack preparation. |
| Consulting Engagements | Engagement primers, hypothesis testing, and expert sourcing. |
| Law Firm Research | Litigation research, regulatory landscape mapping, and matter intelligence. |
| Agentic Research Automation | Programmatic GenSearch / Deep Research calls from customer-built agents over the Agent API or MCP server. |

## Integrations

| Name | Description |
|------|-------------|
| Snowflake | Push and query AlphaSense-derived content alongside the customer's warehouse via Enterprise Intelligence ingestion + export. |
| Microsoft 365 / SharePoint | Pull internal documents from SharePoint / Microsoft 365 into Enterprise Intelligence for unified search. |
| Tegus Expert Network | Native integration with the Tegus expert-call transcript library and on-demand expert services. |
| BamSEC | SEC filing search and analytics (acquired) folded into the unified index. |
| Canalyst | Pre-built financial models and equity datasets (acquired). |
| Sentieo | Document search and financial workflow (acquired). |
| Cerebras Systems | 2025 partnership accelerating inference for AlphaSense's generative-AI layer. |
| Model Context Protocol (MCP) Clients | Any MCP-aware host (Claude, Cursor, in-house agent frameworks) can call GenSearch / ThinkLonger / Deep Research as tools. |
| Kubernetes (Private Cloud) | Customer-managed Kubernetes (EKS / GKE / AKS) provisioned via the privatecloud-cli. |

## Solutions

| Name | Description |
|------|-------------|
| AlphaSense Platform | Core SaaS search and intelligence product for the full customer base. |
| Enterprise Intelligence | Search + GenSearch across both the AlphaSense external corpus and customer internal documents. |
| Enterprise Intelligence Private Cloud | Same product, deployed into the customer's own Kubernetes cluster for compliance-bound buyers. |
| Tegus Expert Insights | Expert-call transcript library and on-demand expert services from the Tegus side. |
| Tegus Expert Call Services | Concierge sourcing and scheduling of one-off expert interviews. |
| Generative Search Suite | GenSearch + Deep Research + Workflow Agents bundle for AI-led research workflows. |
| Agent API + MCP | Embedding contract for customers building their own agents over the AlphaSense corpus. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [AlphaSense Agent API](openapi/alphasense-agent-api-openapi.yml)
- [AlphaSense Utility APIs](openapi/alphasense-utility-api-openapi.yml)

### JSON Schema

- [Document](json-schema/alphasense-document-schema.json)
- [Company](json-schema/alphasense-company-schema.json)
- [Broker](json-schema/alphasense-broker-schema.json)
- [Watchlist](json-schema/alphasense-watchlist-schema.json)
- [GenSearchConversation](json-schema/alphasense-gensearch-conversation-schema.json)
- [Citation](json-schema/alphasense-citation-schema.json)
- [IngestionJob](json-schema/alphasense-ingestion-job-schema.json)
- [WorkflowAgent](json-schema/alphasense-workflow-agent-schema.json)

### JSON Structure

- [Document](json-structure/alphasense-document-structure.json)
- [Company](json-structure/alphasense-company-structure.json)
- [Broker](json-structure/alphasense-broker-structure.json)
- [Watchlist](json-structure/alphasense-watchlist-structure.json)
- [GenSearchConversation](json-structure/alphasense-gensearch-conversation-structure.json)
- [Citation](json-structure/alphasense-citation-structure.json)
- [IngestionJob](json-structure/alphasense-ingestion-job-structure.json)
- [WorkflowAgent](json-structure/alphasense-workflow-agent-structure.json)

### JSON-LD

- [AlphaSense JSON-LD Context](json-ld/alphasense-context.jsonld)

### Examples

- [Document (filing)](examples/alphasense-document-example.json)
- [Document (Tegus expert call)](examples/alphasense-tegus-document-example.json)
- [Company](examples/alphasense-company-example.json)
- [Broker](examples/alphasense-broker-example.json)
- [Watchlist](examples/alphasense-watchlist-example.json)
- [GenSearch Conversation](examples/alphasense-gensearch-conversation-example.json)
- [Citation](examples/alphasense-citation-example.json)
- [Ingestion Job](examples/alphasense-ingestion-job-example.json)
- [Workflow Agent](examples/alphasense-workflow-agent-example.json)
- [Auth Token Response](examples/alphasense-auth-token-example.json)

## Capabilities

Naftiko capabilities organized as self-contained per-tag definitions. Each file ships both REST and MCP exposers.

| Capability | API Surface | Tools | Persona |
|----------|--------------|-------|---------|
| [Agent API - Authentication](capabilities/agent-api-authentication.yaml) | Agent API | 1 | AI Engineer |
| [Agent API - GenSearch](capabilities/agent-api-gensearch.yaml) | Agent API | 2 | AI Engineer / Buy-Side Analyst |
| [Agent API - Deep Research](capabilities/agent-api-deep-research.yaml) | Agent API | 2 | AI Engineer / Buy-Side Analyst |
| [Agent API - Workflow Agents](capabilities/agent-api-workflow-agents.yaml) | Agent API | 2 | AI Engineer |
| [Utility API - Search](capabilities/utility-api-search.yaml) | Utility API | 1 | Buy-Side Analyst |
| [Utility API - Companies](capabilities/utility-api-companies.yaml) | Utility API | 2 | Buy-Side Analyst |
| [Utility API - Watchlist](capabilities/utility-api-watchlist.yaml) | Utility API | 4 | Sell-Side Banker |
| [Utility API - Ingestion](capabilities/utility-api-ingestion.yaml) | Utility API | 2 | Enterprise Intelligence Admin |

## Vocabulary

- [AlphaSense Vocabulary](vocabulary/alphasense-vocabulary.yml) - Unified taxonomy mapping 12 resources, 13 actions, 6 workflows, and 7 personas across operational (OpenAPI) and capability (Naftiko) dimensions.

## Rules

- [AlphaSense Spectral Rules](rules/alphasense-rules.yml) - 17 rules across info, servers, paths, operations, security, schemas, and tags enforcing AlphaSense API conventions.

## Plans

AlphaSense does not publish self-serve plan pricing. Commercial terms are negotiated per customer:

- **AlphaSense Platform (Named-Seat Enterprise)** - Annual named-seat subscription.
- **Tegus Expert Insights (Add-On)** - Subscription access to the Tegus library.
- **Tegus Expert Call Services (Concierge)** - Per-call or pre-purchased pack.
- **Enterprise Intelligence (Add-On)** - Per-document ingestion and per-GB storage.
- **Enterprise Intelligence Private Cloud** - Annual platform fee plus seats and ingestion.
- **Agent API + MCP (Embedding Contract)** - Platform fee plus per-credit GenSearch / Deep Research consumption.

The Private Cloud CLI is free; cost begins at the platform subscription line.

## Rate Limits

- GenSearch / Deep Research credit pool sized per-customer contract; 429 on exhaustion.
- Per-customer burst throttling on the shared /gql endpoint (numeric ceiling not published).
- Ingestion throughput is contracted; large initial loads scheduled with Solutions Engineering.
- Bearer tokens are short-lived; clients must refresh against /auth.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
