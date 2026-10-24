### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / SAAS & DEV TOOLS`
* **Title:** AI infrastructure for developer tools.
* **Description:** Coding agents require deterministic statefulness, not just larger context windows. Build intelligent coding copilots, smart repository search, and dynamic documentation on persistent, per-developer memory — the critical infrastructure needed to prevent hallucinations on massive codebases.
* **Feature List:**
  * **BASE:** Per-developer isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Codebases, PRs, and tickets instantly parsed and tokenized.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT DEVELOPER CONTEXT (01 - 05)`
* **Title:** Every commit adds context.
* **Description:** Negentro's PiyApi remembers what matters across pull requests, sprint boards, or architectural changes. By serving a perfectly curated, conflict-free payload, your coding agent avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of your specific codebase.

### Section 3: Why Dev Tools Need Memory
* **Label:** `01 WHY DEV TOOLS NEED MEMORY`
* **Title:** Coding agents only work if they remember the architecture.
* **Description (Left):** Most AI coding tools start every session with amnesia. An agent that can't recall why a specific design pattern was chosen, which microservices interact, or what broke in the last PR will never deliver true engineering autonomy.
* **Description (Right):** If you're building next-generation developer tools, the foundational layer must be per-repository memory that's isolated, persistent, and secure. Turn static code and scattered Jira tickets into a dynamic bitemporal graph that can be queried by meaning, resolving version contradictions deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Stateful coding agents:** Adapt to the codebase across sprints — remembering architectural decisions, active bugs, and deployment constraints.
* **02 Repository & PR search:** Make complex enterprise codebases searchable by meaning, so an engineer instantly finds where a specific logic pattern was implemented.
* **03 Queryable technical specs:** Transform architecture documents, API specs, and Slack threads into an active knowledge store that an agent can ask questions of directly.
* **04 Adaptive developer onboarding:** Personalize the ramp-up for every new engineer, with each developer's learning context securely isolated in its own environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** Engineering problems, solved.
* **01 Autonomy that needs memory:** A coding agent must remember the system across deployments — what APIs changed, what was deprecated, and the current state of production.
* **02 Per-repository isolation at scale:** A platform hosts thousands of codebases, and each organization's memory record must remain strictly their own. PiyApi guarantees structural privacy, data tokenization, and optional geo-fencing for strict IP compliance.
* **03 Context locked in fragmented tools:** Engineering history is often trapped in unsearchable PR comments. PiyApi enables timestamped semantic search so agents can jump straight to the exact rationale for a code change.
* **04 Code that is hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and exact alphanumeric tokens), ensuring you get the exact function even if the variable names differ.
* **Right Panel Labels:** `COMMIT -> NEXT COMMIT` | `01 COMMIT` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT COMMIT`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: Developer, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Developer Memory
* **Label:** `05 PERSISTENT DEVELOPER MEMORY`
* **Title:** Intelligence that deepens per repo.
* **Description:** A developer tool should get better for each codebase the longer it runs. An agent analyzing a repo for the first time has no context; but after a sprint powered by PiyApi's bitemporal graph, it deterministically knows the core utilities, recurring edge cases, and preferred syntax, tailoring every PR accordingly.
* **Right Panel Steps:** `01 First commit` | `02 Known architecture` | `03 Recurring bugs` | `04 Deployment history` | `05 Personalised next PR`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy stateful coding agents and repository search using our full-pattern, multi-tenant memory architecture, ensuring per-repo isolation and deep semantic search for code and documentation.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does a coding agent know what APIs are currently active?
  * **A:** PiyApi remembers across commits. Each session's interactions are processed into memory scoped exclusively to that codebase, so the agent knows what is deprecated, what is stable, and what is planned.
* **FAQ 2:**
  * **Q:** How is proprietary IP kept separate at scale?
  * **A:** Negentro enforces strict per-org memory isolation at the infrastructure level. Every repository's context graph is structurally partitioned, ensuring zero data leakage, backed by tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it extract context from Slack threads and Jira tickets?
  * **A:** Yes. PiyApi can extract knowledge from unstructured technical discussions, mapping them semantically so engineers can ask questions and find the exact decision point where a trade-off was made.
* **FAQ 4:**
  * **Q:** What happens when a library is updated or a function is refactored?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context—recognizing a refactor—without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared open-source knowledge mix with a company's private repo?
  * **A:** No. Global knowledge (like public API docs) is integrated seamlessly with internal memory, but private proprietary code never pollutes the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished IDE plugin or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the DevTool, IDE plugin, and coding agent on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every codebase a memory that grows with it.
  * **Description:** Build developer tools that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
