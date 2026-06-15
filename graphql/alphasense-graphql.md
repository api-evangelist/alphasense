# AlphaSense GraphQL API

GraphQL surface for embedding AlphaSense intelligence into customer AI agents. Wraps GenSearch (auto / fast / thinkLonger / deepResearch modes), Workflow Agents (pre-built and custom), and the Document Search API behind a single OAuth 2.0 + API-key-protected /gql endpoint. Returns markdown-formatted answers with inline citations to the underlying AlphaSense source documents (filings, transcripts, broker research, Tegus calls). Designed for agentic workflows that need first-result in under five minutes.

## AlphaSense Agent API

**Endpoint:** https://api.alpha-sense.com

**Documentation:** https://developer.alpha-sense.com/agent-api/quickstart

**References:**

- Documentation: https://developer.alpha-sense.com/agent-api/quickstart
- Authentication: https://developer.alpha-sense.com/api/getting-started

## AlphaSense Search API

GraphQL search over the full AlphaSense content library (500M+ documents spanning SEC filings, broker research from 1,500+ firms, news, earnings call transcripts, and Tegus expert interviews). Supports keyword and semantic filters, date presets, document-type filters, watchlists, and smart synonyms. Operates against the same OAuth-protected /gql endpoint as the Agent API. Used to drive in-app search and retrieval flows that do not need agentic answer synthesis.

**Endpoint:** https://api.alpha-sense.com

**Documentation:** https://developer.alpha-sense.com/api/getting-started

**References:**

- Documentation: https://developer.alpha-sense.com/api/getting-started
