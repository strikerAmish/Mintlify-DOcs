# PiyAPI - Open Source Documentation

## 1. Top Configuration
* **Breadcrumb:** `Open Source / Overview`
* **Action:** `[Copy page]`

---

## 2. Left Sidebar Navigation
* **Overview**
* **Python SDK Quickstart**
* **Node.js Quickstart**
* **Self-hosted Server**
* **Web Studio**
* **REST API**
* **Configuration**
* **LLMs**
* **Vector Databases**
* **Embeddings**
* **Storage**
* **Metadata Filtering**
* **Reranking**
* **Multimodal Support**

---

## 3. Right Sidebar Navigation ("On this page")
* Get started
* Go further
* Default components
* Configuration
* Self-hosted architecture
* Build on the open-source

---

## 4. Hero Section

# Open Source Overview
Run PiyAPI on your own infrastructure with full control over your data, configuration, and deployment environment.

**Tags:** `Open Source` | `Self-hosted` | `Developer Infrastructure`

PiyAPI Open Source provides the flexibility to deploy our cognitive memory engine entirely within your VPC. Maintain strict data privacy, enterprise compliance, and total configuration control without sacrificing the power of bitemporal reasoning.

Developers can install the SDK directly into an application as a lightweight library, or run the full PiyAPI server as an independent, scalable microservice. Both approaches allow you to configure storage, embeddings, and BYOK (Bring Your Own Key) model routing to match your existing infrastructure.

The stack is designed to be fully extensible—connect your existing PostgreSQL databases, plug in custom LLMs, and build active inference workflows tailored to your exact deployment constraints.

---

## 5. Run PiyAPI your way (Cards)

### As a library
Install the lightweight SDK directly into your TypeScript or Python application for immediate, embedded bitemporal memory.

### As a self-hosted server
Run the full PiyAPI Gateway and Memory Engine as an independent Docker service with complete control over Redis caching, `pgvector` indexing, and LLM routing.

---

## 6. Get started (Cards)

### Python Quickstart
Install the `piyapi-memory` package and verify that hybrid memory storage and retrieval work in a few lines of code.
`Learn more →`

### Node.js Quickstart
Install the `@piyapi/sdk` package and connect your first stateful agent workflow.
`Learn more →`

### Self-hosted server
Deploy the PiyAPI Docker container locally or on your Kubernetes cluster and configure your bitemporal infrastructure.
`Learn more →`

---

## 7. Go further (Cards)

### Configure components
Configure BYOK routing, embedding providers, `pgvector` storage, and tune the UnifiedScorer for your specific deployment.
`Learn more →`

### Self-hosting features
Explore enterprise namespace isolation, semantic cache purging, multimodal CDC connectors, and compliance-grade redaction tools.
`Learn more →`

### Build with cookbooks
Use practical examples for LangChain agents, CrewAI, MCP server integrations, and real-world compliance workflows.
`Learn more →`

> **Need a managed alternative?**
> Compare the self-hosted open-source deployment with the fully managed PiyAPI Cloud Platform, or switch to the **Platform** documentation.

---

## 8. Default components

PiyAPI ships with sane, production-ready defaults for each part of the pipeline. Every component can be replaced or explicitly configured to match your existing VPC infrastructure and provider preferences.

### Library defaults
| COMPONENT | DEFAULT |
|:---|:---|
| **LLM** | OpenAI (via BYOK) |
| **Embeddings** | OpenAI `text-embedding-3-small` |
| **Vector store** | `pgvector` |
| **History store** | PostgreSQL |

### Self-hosted defaults
| COMPONENT | DEFAULT |
|:---|:---|
| **Reranker** | UnifiedScorer (BM25 + RRF) |
| **Storage** | PostgreSQL (Bitemporal KG) |
| **Metadata cache** | Redis |
| **Providers** | Multi-Provider BYOK Routing |

---

## 9. Configure your stack

```typescript
// piyapi.config.ts
import { createPiyAPI } from '@piyapi/sdk';

const piyapi = createPiyAPI({
  llm: "openai:gpt-4o",
  embeddings: "openai:text-embedding-3-small",
  // Connect directly to your existing infrastructure
  vectorStore: "pgvector://localhost:5432/piyapi",
  storage: "postgres://localhost:5432/piyapi_graph",
  cache: "redis://localhost:6379"
});
```

---

## 10. Self-hosted architecture

*(Visual: Self-hosted architecture diagram)*

**Nodes:**
`[1] Your Application` → `[2] PiyAPI Server` → (`Memory`, `Retrieval`, `Embeddings`, `LLM`, `Storage`) → `[3] Your Infrastructure`

---

## 11. Configuration

### LLMs
Route generation through any provider using our unified BYOK manager. Support for OpenAI, Anthropic, Gemini, DeepSeek, Mistral, Groq, Cohere, and Perplexity is handled natively.

### Embeddings
Choose the embedding provider and model used for vector generation. Easily swap out defaults for specialized models depending on your latency and accuracy requirements.

### Vector databases
Connect the storage backend used for dense HNSW retrieval. Defaults to PostgreSQL with `pgvector` for robust, transaction-safe vector operations.

### Storage
Configure where persistent bitemporal graph data (PiyGraph) and conversational history are stored.

### Metadata filtering
Control how stored context is filtered and retrieved using strict namespace scoping (`X-Namespace-Prefix`) and arbitrary tagging rules.

### Reranking
Fine-tune the UnifiedScorer reranking layer (combining BM25 trigram search and 11 distinct retrieval signals) when hyper-precise retrieval is required for your agents.

---

## 12. Build on the open-source stack

* Replace infrastructure components (e.g., swap Redis for an alternative caching layer)
* Configure multi-provider routing and failover logic to prevent LLM downtime
* Integrate directly with your existing enterprise PostgreSQL databases
* Build custom Active Inference workflows and agent MCP tools

> **Open-source note**
> Keep your deployment configuration explicit so model, storage, and retrieval dependencies remain easy to understand, version control, and operate across your team.

---

**Footer Actions:**
`[Suggest edits]` | `[Raise issue]`

**Footer Navigation:**
`← PREVIOUS: Platform Overview` | `NEXT: Integrations Overview →`
