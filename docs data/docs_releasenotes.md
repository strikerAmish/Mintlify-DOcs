# PiyAPI - Release Notes Documentation

## 1. Top Configuration
* **Breadcrumb:** `Release Notes`
* **Action:** `[Copy page]`

## 2. Left Sidebar Navigation
* **RELEASE NOTES**
  * Highlights
  * SDKs & Tools
  * Platform
* **FILTER BY**
  * All
  * Product
  * SDK
  * Integration
  * Plugin
  * Infrastructure

## 3. Right Sidebar Navigation ("On this page")
* Highlights
* SDK & Tools
* Platform
* August 2026
* July 2026
* June 2026

---

# Highlights

Platform updates, infrastructure improvements, and SDK releases.

> **Note:** Sample content — illustrative release notes for demonstration purposes.

*(Search and Filter Bar: `All updates` | `Search release notes...` | `2026` | `All`)*

## August 2026

### PiyAPI Coding Agent Plugin launches for VS Code
`2026-08-24` | `Agent Plugin` | **HIGHLIGHT**

The VS Code plugin provides persistent project memory directly within the editor. The extension surfaces prior decisions, architectural conventions, and working context across isolated coding sessions.

* **Automatic memory**: Captures working context in the background without manual tagging.
* **Scoped recall**: Restricts `memory.search` to the current `project_id` to prevent cross-repo leakage.
* **Inline suggestions**: Injects relevant past fixes directly into the diff view.

> **Developer preview.** Available to design partners; general availability targeted for Q4.

`[View documentation →]`

### Python SDK v4.2 — batched writes and async memory client
`2026-08-19` | `SDK`

A new `AsyncMemoryClient` and batched write support designed for high-throughput Python applications.

* **Batch API**: Write up to 500 memories per request, reducing round trips by 90%.
* **AsyncClient**: Mirrors the synchronous client API for `asyncio` compatibility.

`[Migration guide →]`

### Project vs. personal memory scoping
`2026-08-14` | `Memory`

Memory queries and writes can now be strictly scoped to prevent crossover between shared project data and private user context.

* **Scope param**: Pass `scope=project` or `scope=user` on every write and query operation.
* **Isolation guarantee**: Hard boundary enforced at the storage layer, keyed by `user_id` and `project_id`.

> [!WARNING]
> **Migration note.** Existing memories default to `scope=user`. Update your endpoints if your application expects shared project context.

### REST API v1.3 — richer filtering on /v1/memories
`2026-08-07` | `API`

The `/v1/memories` endpoint now supports compound filtering and date constraints.

* **Filter operators**: Native support for `AND`/`OR` grouping structures.
* **Session filter**: Restrict retrieval results to a specific `session_id` for conversation-level boundaries.

---

## July 2026

### Native MCP support across the platform
`2026-07-29` | `Platform` | **HIGHLIGHT**

Native Model Context Protocol (MCP) support allows compatible clients to read and write memory directly to the PiyAPI engine.

* **MCP server**: A single-line installation exposes native memory tools to the host environment.
* **Tool discovery**: Hosts automatically detect `search`, `add`, and `update` tools.

`[View documentation →]`

### TypeScript SDK v3.0 — full type-safe memory client
`2026-07-22` | `SDK`

The SDK has been entirely rewritten with strict TypeScript definitions, tree-shakeable exports, and Edge runtime support.

* **Edge-ready**: Executes in Vercel Edge and Cloudflare Workers environments with zero polyfills.
* **Breaking change**: `client.memories.add()` now returns a strictly typed `Memory` object instead of raw JSON.

`[Migration guide →]`

### LangChain and LlamaIndex memory adapters
`2026-07-16` | `Open Source`

Native memory backends are now available as drop-in replacements for the primary open-source agent frameworks.

* **LangChain**: Implements `BaseMemory` with persistent cross-session state retention.
* **LlamaIndex**: Distributed as a zero-config `ChatMemoryBuffer` replacement.

### UX Pilot AI and Google Gemini embedding support
`2026-07-09` | `Provider`

PiyAPI now supports UX Pilot AI and Google Gemini as dense vector embedding providers, alongside OpenAI.

* **Provider config**: Configure via the `embedding_provider` project setting or explicitly per API call.

### Vector retrieval latency reduced by 40%
`2026-07-02` | `Infrastructure`

The core retrieval index was re-architected to reduce p95 query latency globally.

* **HNSW tuning**: Dynamic index parameters based on real-time collection size.
* **Result caching**: Repeated `memory.search` requests utilizing identical filters are now served directly from cache.

---

## June 2026

### PiyAPI Memory Platform — general availability
`2026-06-26` | `Product` | **HIGHLIGHT**

The core persistent memory infrastructure is now generally available with SLA-backed uptime and strict tenant isolation.

* **GA SLA**: 99.9% uptime commitment across all production tiers.
* **Isolation model**: All memory records are strictly namespaced by `project_id` and `user_id`.

`[View documentation →]`

### PiyAPI CLI 1.0
`2026-06-19` | `Developer Tools`

Inspect, seed, and debug memory indices directly from the terminal.

* **piyapi tail**: Streams live memory writes matching a specific `project_id`.
* **piyapi seed**: Executes bulk imports from JSONL files for localized testing workflows.

### Dashboard: memory graph visualizer
`2026-06-12` | `Platform`

A visual interface for exploring relationships between memories, filterable by recency, category, and user entity.

* **Graph view**: Renders topological semantic clusters directly from the production dataset.

> **Developer preview.** Enable via the feature flags section in project settings.

### Slack and Zendesk connectors
`2026-06-05` | `Integration`

Automatically index support conversations and team messages into scoped customer memory.

* **Zendesk sync**: Resolved tickets are parsed and converted to memories keyed by `user_id`.
* **Slack app**: Available via the Slack App Directory; requires channel authorization to begin indexing.

### REST API rate limits raised for Pro tier
`2026-06-01` | `API`

Pro workspaces receive a 5x increase to the global request ceiling across all memory endpoints.

* **New limit**: 5,000 requests per minute per project on the REST API.

---

**Footer Actions:** `[Suggest edits]` | `[Raise issue]`

**Footer Navigation:** `← PREVIOUS: API Reference` | `NEXT: SDK & Tools →`

---

> **Editor's Note: Navbar & Content Adjustments**
> * **Right Sidebar ("On this page")**: The Figma design had `SDK & Tools` and `Platform` underneath `Highlights`, but the main content only spans chronological updates. I retained `SDK & Tools` and `Platform` in the markdown sidebar to perfectly match the Figma, representing logical sub-pages.
> * **Footer Navigation**: Added a `← PREVIOUS: API Reference` link to correctly connect the global documentation workflow.
> * **Content Typo Fix**: Corrected a redundant Figma sentence regarding UX Pilot AI to accurately state that Gemini and UX Pilot are supported alongside OpenAI.
