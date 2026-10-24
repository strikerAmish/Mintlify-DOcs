### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / FINANCE`
* **Title:** AI infrastructure for finance & accounting.
* **Description:** Financial automation requires strict statefulness, not just scale. Build intelligent procurement copilots, smart invoice reconciliation, and queryable ledgers on persistent, per-client memory — the critical infrastructure required for compliance-heavy financial pipelines.
* **Feature List:**
  * **BASE:** Per-client isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Invoices and receipts instantly parsed and tokenized with PII redaction.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT FINANCIAL CONTEXT (01 - 05)`
* **Title:** Every transaction adds context.
* **Description:** Negentro's PiyApi remembers what matters across quarters, years, or fiscal periods. By serving a perfectly curated, conflict-free payload, your financial copilot avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of each individual client's financial state.

### Section 3: Why Finance Needs Memory
* **Label:** `01 WHY FINANCE NEEDS MEMORY`
* **Title:** Financial automation only works if the system remembers the ledger.
* **Description (Left):** Most AI tools start every session with amnesia. A procurement agent that can't recall a vendor's pricing history, previous invoices, or budget constraints will never deliver reliable financial automation.
* **Description (Right):** If you're building next-generation fintech platforms, the foundational layer must be per-client memory that's isolated, persistent, and secure. Turn static receipts and ledgers into a dynamic bitemporal graph that can be queried by meaning, resolving financial contradictions deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Procurement copilots:** Adapt to each client across fiscal cycles — remembering preferred vendors, budget limits, and spending patterns.
* **02 Invoice & receipt search:** Make complex transactional histories searchable by meaning, so an accountant instantly finds the exact moment an expense was authorized.
* **03 Queryable financial regulations:** Transform tax codes and compliance manuals into an active knowledge store that an agent can ask questions of directly.
* **04 Adaptive accounting platforms:** Personalize the financial journey for every user at scale, with each client's financial context securely isolated in its own environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** Financial problems, solved.
* **01 Reconciliation that needs memory:** An accounting agent must remember the client across periods — what was paid, what is pending, and their tax classifications.
* **02 Per-client isolation at scale:** A platform has thousands of businesses, and each company's memory record must remain strictly their own. PiyApi guarantees structural privacy, data tokenization, and optional geo-fencing for strict compliance.
* **03 Data locked in unstructured PDFs:** Financial history is often trapped in unsearchable invoices. PiyApi enables timestamped semantic search so accountants can jump straight to the original receipt.
* **04 Tax codes that are hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and entity overlap), ensuring you get the relevant regulatory clause even if phrasing differs.
* **Right Panel Labels:** `TRANSACTION -> NEXT TRANSACTION` | `01 TRANSACTION` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT TRANSACTION`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: Client, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Client Memory
* **Label:** `05 PERSISTENT CLIENT MEMORY`
* **Title:** Intelligence that deepens per client.
* **Description:** A fintech platform should get better for each business the longer they use it. An agent meeting a client for the first time has no context; but after a fiscal year powered by PiyApi's bitemporal graph, it deterministically knows their recurring expenses, vendor terms, and baseline cash flow, tailoring every interaction accordingly.
* **Right Panel Steps:** `01 First transaction` | `02 Known vendors` | `03 Recurring expenses` | `04 Financial history` | `05 Personalised next period`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy accounting and procurement copilots using our full-pattern, multi-tenant memory architecture, ensuring per-client isolation and deep semantic search for financial documents.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does a copilot know a client's financial history?
  * **A:** PiyApi remembers across sessions. Each session's interactions are processed into memory scoped exclusively to that client, so the copilot knows their budget, pending invoices, and past transactions.
* **FAQ 2:**
  * **Q:** How are different businesses kept separate at scale?
  * **A:** Negentro enforces strict per-client memory isolation at the infrastructure level. Every company's context graph is structurally partitioned, ensuring zero data leakage, backed by privacy tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it extract data from scanned receipts and invoices?
  * **A:** Yes. PiyApi can extract knowledge from unstructured financial documents, mapping them semantically so accountants can ask questions and find the exact line item where an expense is located.
* **FAQ 4:**
  * **Q:** What happens when a vendor updates their pricing or terms?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared regulatory knowledge mix with a client's private ledger?
  * **A:** No. Global knowledge (like tax codes and compliance rules) is integrated seamlessly with personal memory, but private financial data never pollutes the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished accounting product or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the fintech application, UI, and copilot on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every client a memory that grows with them.
  * **Description:** Build financial systems that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
