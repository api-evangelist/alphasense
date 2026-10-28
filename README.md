# AlphaSense

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

AlphaSense is an AI-powered market intelligence and search platform used by hedge funds, banks, corporates, consulting firms, and law firms to accelerate research and decision-making. The platform unifies 500M+ public and private documents - SEC filings, broker research from 1,500+ firms, news, earnings call transcripts, internal company content, and 260,000+ Tegus expert call transcripts (Tegus was acquired in December 2023 for ~$930M) - behind a generative search and agent layer (GenSearch, Deep Research, Workflow Agents). The developer surface is gated, enterprise-only, and is split across two contracts: an Agent API for embedding GenSearch / Deep Research / MCP tools into customer AI agents, and a set of Utility APIs (Search, Brokers, Companies, Watchlist, Trends, User, Download, Ingestion) for direct programmatic access. Both are exposed over a single OAuth 2.0-protected GraphQL endpoint at https://api.alpha-sense.com/gql, with a companion REST Ingestion API for Enterprise Intelligence customers. AlphaSense Enterprise Intelligence Private Cloud ships with a public Go CLI (AlphaSense-Engineering/privatecloud-cli) for installing and validating the Kubernetes-hosted environment in a customer's own VPC.

**Areas:** Market Intelligence · Financial Research · Search · Generative AI · AI Agents · Expert Calls · Document Intelligence · Enterprise Intelligence · MCP · GraphQL

## AlphaSense on APIs.io

Everything profiled for AlphaSense is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/alphasense/](https://apis.io/providers/alphasense/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [AlphaSense Trends API](https://apis.io/apis/alphasense/trends-api/) — Time-series operations for theme, keyword, and topic frequency across the document corpus - the back end behind AlphaSense's Trend visualisations and…
- [AlphaSense User API](https://apis.io/apis/alphasense/user-api/) — User and account management operations covering profile, preferences, session, and entitlement metadata for integrating the AlphaSense experience into a…
- [AlphaSense Download / Export API](https://apis.io/apis/alphasense/download-api/) — Bulk export and download operations for documents, search results, and report PDFs - used to push AlphaSense content into downstream data warehouses,…
- [AlphaSense MCP Server](https://apis.io/apis/alphasense/mcp-server/) — Model Context Protocol surface that lets MCP-aware AI clients (Claude, Cursor, ChatGPT-style desktop hosts, in-house agent frameworks) call GenSearch,…
- [AlphaSense Private Cloud CLI](https://apis.io/apis/alphasense/privatecloud-cli/) — Go-based CLI (AlphaSense-Engineering/privatecloud-cli, Apache-2.0-ish "Other" license) used by Enterprise Intelligence Private Cloud customers to bootstrap…
- [AlphaSense Authentication API](https://apis.io/apis/alphasense/alphasense-authentication-api/) — OAuth 2.0 token exchange for the AlphaSense platform.
- [AlphaSense GenSearch API](https://apis.io/apis/alphasense/alphasense-gensearch-api/) — Generative-search mutations and conversation polling for AlphaSense GenSearch.
- [AlphaSense Ingestion API](https://apis.io/apis/alphasense/alphasense-ingestion-api/) — Push customer-owned content into Enterprise Intelligence.
- [AlphaSense Search API](https://apis.io/apis/alphasense/alphasense-search-api/) — Document search across the AlphaSense corpus (500M+ documents).

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [AlphaSense GraphQL API](https://apis.io/graphqls/alphasense/alphasense-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [alphasense](https://apis.io/servers/alphasense/alphasense/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Alphasense Agentic Access](https://apis.io/agentic-access/alphasense/alphasense-agentic-access/)

#### JSON Schema (8)

The data models the API reads and writes.

- [Broker](https://apis.io/schemas/alphasense/alphasense-broker/)
- [Citation](https://apis.io/schemas/alphasense/alphasense-citation/)
- [Company](https://apis.io/schemas/alphasense/alphasense-company/)
- [Document](https://apis.io/schemas/alphasense/alphasense-document/)
- [GenSearchConversation](https://apis.io/schemas/alphasense/alphasense-gensearch-conversation/)
- [IngestionJob](https://apis.io/schemas/alphasense/alphasense-ingestion-job/)
- [Watchlist](https://apis.io/schemas/alphasense/alphasense-watchlist/)
- [WorkflowAgent](https://apis.io/schemas/alphasense/alphasense-workflow-agent/)

#### JSON Structure (8)

Data models expressed in JSON Structure.

- [Alphasense Broker Structure](https://apis.io/json-structure/alphasense/alphasense-broker-structure/)
- [Alphasense Citation Structure](https://apis.io/json-structure/alphasense/alphasense-citation-structure/)
- [Alphasense Company Structure](https://apis.io/json-structure/alphasense/alphasense-company-structure/)
- [Alphasense Document Structure](https://apis.io/json-structure/alphasense/alphasense-document-structure/)
- [Alphasense Gensearch Conversation Structure](https://apis.io/json-structure/alphasense/alphasense-gensearch-conversation-structure/)
- [Alphasense Ingestion Job Structure](https://apis.io/json-structure/alphasense/alphasense-ingestion-job-structure/)
- [Alphasense Watchlist Structure](https://apis.io/json-structure/alphasense/alphasense-watchlist-structure/)
- [Alphasense Workflow Agent Structure](https://apis.io/json-structure/alphasense/alphasense-workflow-agent-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Alphasense Context](https://apis.io/jsonld/alphasense/alphasense-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Alphasense Vocabulary](https://apis.io/vocabularies/alphasense/alphasense-vocabulary/)

#### Examples (10)

Example requests and responses.

- [Alphasense Auth Token Example](https://apis.io/examples/alphasense/alphasense-auth-token-example/)
- [Alphasense Broker Example](https://apis.io/examples/alphasense/alphasense-broker-example/)
- [Alphasense Citation Example](https://apis.io/examples/alphasense/alphasense-citation-example/)
- [Alphasense Company Example](https://apis.io/examples/alphasense/alphasense-company-example/)
- [Alphasense Document Example](https://apis.io/examples/alphasense/alphasense-document-example/)
- [Alphasense Gensearch Conversation Example](https://apis.io/examples/alphasense/alphasense-gensearch-conversation-example/)
- [Alphasense Ingestion Job Example](https://apis.io/examples/alphasense/alphasense-ingestion-job-example/)
- [Alphasense Tegus Document Example](https://apis.io/examples/alphasense/alphasense-tegus-document-example/)
- [Alphasense Watchlist Example](https://apis.io/examples/alphasense/alphasense-watchlist-example/)
- [Alphasense Workflow Agent Example](https://apis.io/examples/alphasense/alphasense-workflow-agent-example/)

#### Collections (28)

Postman and Open Collection request collections.

- [AlphaSense Agent API](https://apis.io/collections/alphasense/open-alphasense-agent-api/)
- [AlphaSense Agent Authentication API](https://apis.io/collections/alphasense/open-alphasense-authentication-api/)
- [AlphaSense Agent Authentication Brokers API](https://apis.io/collections/alphasense/open-alphasense-brokers-api/)
- [AlphaSense Agent Authentication Companies API](https://apis.io/collections/alphasense/open-alphasense-companies-api/)
- [AlphaSense Agent Authentication Deep Research API](https://apis.io/collections/alphasense/open-alphasense-deep-research-api/)
- [AlphaSense Agent Authentication Document Search API](https://apis.io/collections/alphasense/open-alphasense-document-search-api/)
- [AlphaSense Agent Authentication Download API](https://apis.io/collections/alphasense/open-alphasense-download-api/)
- [AlphaSense Agent Authentication GenSearch API](https://apis.io/collections/alphasense/open-alphasense-gensearch-api/)
- [AlphaSense Agent Authentication Ingestion API](https://apis.io/collections/alphasense/open-alphasense-ingestion-api/)
- [AlphaSense Agent Authentication Search API](https://apis.io/collections/alphasense/open-alphasense-search-api/)
- [AlphaSense Agent Authentication Trends API](https://apis.io/collections/alphasense/open-alphasense-trends-api/)
- [AlphaSense Agent Authentication User API](https://apis.io/collections/alphasense/open-alphasense-user-api/)
- [AlphaSense Utility APIs](https://apis.io/collections/alphasense/open-alphasense-utility-api/)
- [AlphaSense Agent Authentication Watchlist API](https://apis.io/collections/alphasense/open-alphasense-watchlist-api/)
- [AlphaSense Agent Authentication Workflow Agents API](https://apis.io/collections/alphasense/open-alphasense-workflow-agents-api/)
- [AlphaSense Agent Authentication API](https://apis.io/collections/alphasense/postman-alphasense-authentication-api/)
- [AlphaSense Agent Authentication Brokers API](https://apis.io/collections/alphasense/postman-alphasense-brokers-api/)
- [AlphaSense Agent Authentication Companies API](https://apis.io/collections/alphasense/postman-alphasense-companies-api/)
- [AlphaSense Agent Authentication Deep Research API](https://apis.io/collections/alphasense/postman-alphasense-deep-research-api/)
- [AlphaSense Agent Authentication Document Search API](https://apis.io/collections/alphasense/postman-alphasense-document-search-api/)
- [AlphaSense Agent Authentication Download API](https://apis.io/collections/alphasense/postman-alphasense-download-api/)
- [AlphaSense Agent Authentication GenSearch API](https://apis.io/collections/alphasense/postman-alphasense-gensearch-api/)
- [AlphaSense Agent Authentication Ingestion API](https://apis.io/collections/alphasense/postman-alphasense-ingestion-api/)
- [AlphaSense Agent Authentication Search API](https://apis.io/collections/alphasense/postman-alphasense-search-api/)
- [AlphaSense Agent Authentication Trends API](https://apis.io/collections/alphasense/postman-alphasense-trends-api/)
- …and 3 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [AlphaSense — jsonschema rules](https://apis.io/rules/alphasense/alphasense-jsonschema-spectral-rules/)
- [AlphaSense API Rules](https://apis.io/rules/alphasense/alphasense-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Alphasense Authentication](https://apis.io/security/alphasense/alphasense-authentication/)
- [Alphasense Domain Security](https://apis.io/security/alphasense/alphasense-domain-security/)
- [Alphasense Trust Center](https://apis.io/security/alphasense/alphasense-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Alphasense Plans Pricing](https://apis.io/plans/alphasense/alphasense-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Alphasense Rate Limits](https://apis.io/rate-limits/alphasense/alphasense-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Alphasense Finops](https://apis.io/finops/alphasense/alphasense-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.alpha-sense.com/)
- [Documentation](https://developer.alpha-sense.com/)
- [Getting started](https://developer.alpha-sense.com/api/getting-started)
- [Support](https://help.alpha-sense.com/)
- [Blog](https://www.alpha-sense.com/newsroom/)
- [Trust centre](https://trust.alpha-sense.com/)
- [GitHub](https://github.com/AlphaSense-Engineering)

## API Evangelist rating

**Kin Score 42.8** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 64.3 |
| Contract governance | 23.5 |
| Operational transparency | 26.3 |
| Developer ergonomics | 51.2 |
| Access clarity | 15.8 |

**Agent readiness 45.2** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 20.0** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/alphasense/](https://apis.io/providers/alphasense/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for AlphaSense: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/alphasense/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
