# PiyAPI - Platform Documentation

## 1. Top Configuration
* **Breadcrumb:** `Platform / Platform Overview`
* **Action:** `[Copy page]`

---

## 2. Left Sidebar Navigation
* **Overview**
* **Core Concepts**
  * Persistent Memory
  * Context Assembly
  * Hybrid Retrieval
  * PiyGraph Knowledge
* **Architecture**
* **Clients & SDKs**

---

## 3. Right Sidebar Navigation ("On this page")
* Core Concepts
* Architecture
* Initialize the Client
* Store and Retrieve Context
* How PiyAPI Works
* What's Next?

---

## 4. Hero Section

# Platform Overview
Everything you need to build, manage, and scale persistent intelligence with PiyAPI.

PiyAPI provides the infrastructure for persistent intelligence across AI applications.

The platform manages memory, context, and retrieval as distinct layers, allowing applications to store relevant information and recall it precisely when needed rather than relying on ephemeral session state.

This document introduces the core building blocks of PiyAPI and describes how they compose into a working system for AI agents and applications.

---

## 5. Core Concepts (Grid)

### Persistent Memory
Long-term storage referenced via `memory_id`. Backed by the **Unified 8-Operator Surface** (`store`, `retrieve`, `update`, `delete`, `merge`, `summarize`, `pin`, `verify`).

### Context
Assembled data passed via `context` object. Token-budget-aware context assembly for LLM system prompts via `POST /api/v1/context/retrieve`.

### Users & Sessions
Scoped via `user_id` identifiers. Enterprise multi-tenancy enforced via strict namespace isolation (`X-Namespace-Prefix` header) and automated PHI/PII privacy redaction.

### Retrieval
Query via `client.search()`. Hybrid search engine combining dense vector similarity (HNSW via `pgvector`) and BM25 trigram full-text search, fused using Reciprocal Rank Fusion (`RRF_K=30`).

### Knowledge
Structured domain data accessible through `knowledge.query()`. PiyGraph Knowledge Graph tracking real-world validity (`valid_at`) separately from system recording time (`system_at`).

---

## 6. Architecture

*(Visual: Request Pipeline Diagram)*

**Nodes:**
`Application` → `PiyAPI Gateway` → (`Memory Engine`, `Cognitive Engine`, `Integrations`) → `Vector Substrate (pgvector + Redis)`

> **Platform Note**
> PiyAPI separates persistent memory from the application logic so your AI system can retrieve relevant context when it needs it.

**System Architecture:**
```
┌────────────────────────────────────────────────────────────┐
│                      CLIENT LAYER                           │
│  TypeScript SDK  │  Python SDK  │  MCP Server  │  cURL     │
└──────────────────────────────┬─────────────────────────────┘
                                │
                                ▼
┌────────────────────────────────────────────────────────────┐
│          PIYAPI REST GATEWAY (api.piyapi.cloud)             │
│     Namespace Scoping  │  Rate Limiter  │  Auth & BYOK Guard│
└──────────────────────────────┬─────────────────────────────┘
                                │
              ┌─────────────────┼─────────────────┐
              ▼                 ▼                  ▼
    ┌─────────────────┐ ┌───────────────┐ ┌───────────────┐
    │  MEMORY ENGINE  │ │ COGNITIVE ENG.│ │ INTEGRATIONS  │
    │ • 8-Operators   │ │ • Hybrid RAG  │ │ • BYOK Mgr    │
    │ • Bitemporal    │ │ • PiyGraph KG │ │ • 12 CDC Conn │
    │ • Branching     │ │ • UnifiedScrr │ │ • 30 MCP Tools│
    └─────────────────┘ └───────────────┘ └───────────────┘
                                │
┌────────────────────────────────────────────────────────────┐
│               DATA & VECTOR SUBSTRATE                       │
│    PostgreSQL + pgvector  │  Bitemporal KG  │  Redis Cache  │
└────────────────────────────────────────────────────────────┘
```

---

## 7. Initialize the Client

**Tabs:** `JavaScript` | `Python` | `cURL`

**JavaScript (`@piyapi/sdk`)**
```javascript
import { PiyAPIClient } from '@piyapi/sdk';

const client = new PiyAPIClient({
  apiKey: process.env.PIYAPI_API_KEY || 'sk_live_...'
});
```

**Python (`piyapi-memory`)**
```python
from piyapi_memory import PiyAPIClient

client = PiyAPIClient(api_key="sk_live_your_key_here")
```

**cURL**
```bash
curl -s https://api.piyapi.cloud/api/v1/verify \
  -H "Authorization: Bearer sk_live_..."
# Response: {"status":"valid","key_id":"...","scopes":["memory:read","memory:write"]}
```

---

## 8. Store and Retrieve Context

**Steps:**
1. Create or initialize the client
2. Send conversational information
3. Store relevant memory
4. Retrieve context when needed
5. Pass retrieved context to the model

**Store a memory** (`example.js`)
```javascript
const memory = await client.memories.create({
  content: 'User prefers dark mode UI and works primarily with React and TypeScript.',
  tags: ['preferences', 'tech-stack'],
  metadata: { source: 'onboarding_chat', user_id: 'usr_9918' }
});
```

**Retrieve via Hybrid Search** (`example.js`)
```javascript
const results = await client.search({
  query: 'What frontend framework does the user prefer?',
  limit: 5,
  min_score: 0.25
});
```

**Response:**
```json
{
  "query": "What frontend framework does the user prefer?",
  "total": 1,
  "results": [
    {
      "id": "8a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
      "content": "User prefers dark mode UI and works primarily with React and TypeScript.",
      "score": 0.892,
      "vector_score": 0.854,
      "bm25_score": 0.931
    }
  ]
}
```

> **Tip**
> Use retrieval selectively so your application only sends relevant context to the model. Configure `min_score` (default `0.25`) and `alpha` (vector vs BM25 blend, default `0.7`) for precise control over retrieval quality.

---

## 9. How PiyAPI Works

| # | Step | Description |
|:--|:--|:--|
| **01** | **Capture** | Conversational or event data enters the system via API, SDK, or one of 12 native CDC connectors (Google Drive, Notion, GitHub, Slack, Jira, Gmail, and more). |
| **02** | **Store** | Relevant information is persisted as memory in PostgreSQL + `pgvector`, tagged and indexed for instant retrieval. |
| **03** | **Retrieve** | The UnifiedScorer evaluates 11 signals in a single pass — including vector similarity, BM25 text score, recency decay, entity overlap, contradiction penalty, and pin weight. |
| **04** | **Compose context** | Retrieved memory is assembled into a token-budget-aware context payload via `POST /api/v1/context/retrieve`. |
| **05** | **Generate response** | Context is passed to the model for output. Route through BYOK to use your own OpenAI, Anthropic, Gemini, or DeepSeek keys natively. |

---

## 10. What's Next? (Cards)

* **Explore the architecture →**
  Understand how PiyGraph, bitemporal `valid_at`/`system_at` tracking, and Speculative Memory Branching are structured.

* **Store your first memory →**
  Create and persist your first record using `POST /api/v1/memories` or the TypeScript SDK.

* **Build an AI agent →**
  Wire up memory and context using our MCP Server (`@piyapi/mcp-server` — 30 tools, 3 resources, 3 prompts).

* **Explore the API →**
  Browse the full REST reference and OpenAPI JSON spec at `https://api.piyapi.cloud/docs/raw/openapi.json`.

---

**Footer Actions:**
`[Suggest edits]` | `[Raise issue]`

**Footer Navigation:**
`← PREVIOUS: Get Started` | `NEXT: Open Source →`
