# PiyAPI - Get Started Documentation

## 1. Top Configuration
* **Breadcrumb:** `Docs / Get Started`
* **Action:** `[Copy page]`

---

## 2. Left Sidebar Navigation
* **Get Started**
  * Quickstart
  * Building Agents
  * Workflows
  * Infrastructure
* **Platform**
* **Open Source**
* **Integrations**

---

## 3. Right Sidebar Navigation ("On this page")
* Quickstart
* Agents
* Workflows
* Integrations
* Examples
* Infrastructure

---

## 4. Hero Section

# Build with PiyAPI
Build persistent intelligence into your AI applications with PiyAPI's bitemporal memory, context, and developer infrastructure.

**Buttons:** `Get Started` | `API Reference`

---

## 5. Developer Grid (6 Cards)

### Quickstart
Initialize your PiyGraph. Learn how to create, store, and retrieve your first bitemporal facts with O(1) constant time latency.
```javascript
piyapi.memory.add({
  fact: "User prefers Dark Mode",
  valid_at: "2026-10-04",
  user_id: "u_1029"
})
```

### Agents
Add state to your AI agent. Give your agents persistent context across sessions with Deterministic Conflict Resolution to prevent hallucinations.
*(Visual: AI Agent → PiyGraph Memory → UnifiedScorer → Conflict-Free Payload)*

### Workflows
Retrieve context with UnifiedScorer. Build workflows that fuse dense vector HNSW and BM25 trigrams to retrieve exactly what the model needs.
```javascript
1. const payload = await retrieve(UnifiedScorer);
2. resolveConflicts(payload);
3. generateResponse();
```

### Integrations
Use PiyAPI with your framework. Connect PiyAPI to your existing stack using our native SDKs and agentic framework plugins.
*(Tags: Next.js | Python | LangChain | Node.js | LlamaIndex | Vercel AI)*

### Examples
Deploy a working Copilot. Start from production-ready examples of stateful coding agents, customer triage bots, and EdTech tutors.
```javascript
const client = new PiyApi(API_KEY);
client.agent.deploy(edTechTutor_Config);
```

### Infrastructure
Host on your own infrastructure. Understand VPC peering, data tokenization, and strict per-tenant isolation for enterprise compliance.
*(Visual: Application → VPC Peering → PiyAPI Core → Your Secure DB)*

---

**Footer Actions:**
`[Suggest edits]` | `[Raise issue]`

**Footer Navigation:**
`NEXT: Platform →`
