### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / LEGAL`
* **Title:** AI infrastructure for legal & compliance.
* **Description:** Legal reasoning requires perfect recall, not just semantic similarity. Build intelligent contract analysis copilots, smart case law search, and dynamic legal libraries on persistent, per-client memory — the critical infrastructure required for rigorous legal workflows.
* **Feature List:**
  * **BASE:** Per-client isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Contracts and case files instantly transcribed and tokenized with PII redaction.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT LEGAL CONTEXT (01 - 05)`
* **Title:** Every document adds context.
* **Description:** Negentro's PiyApi remembers what matters across briefs, contracts, or entire cases. By serving a perfectly curated, conflict-free payload, your legal copilot avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of each individual legal matter.

### Section 3: Why Legal Needs Memory
* **Label:** `01 WHY LEGAL NEEDS MEMORY`
* **Title:** Case analysis only works if the system remembers the facts.
* **Description (Left):** Most legal AI tools start every session with amnesia. A contract analysis feature that can't recall previously negotiated clauses, opposing counsel arguments, or specific entity relationships will never deliver true legal utility.
* **Description (Right):** If you're building next-generation LegalTech platforms, the foundational layer must be per-matter memory that's isolated, persistent, and secure. Turn static case files and contracts into a dynamic bitemporal graph that can be queried by meaning, resolving contradictions deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Case analysis copilots:** Adapt to each legal matter across sessions — remembering key entities, timelines, and established facts.
* **02 Contract & brief search:** Make complex legal content searchable by meaning, so an attorney instantly finds the exact moment a clause was introduced.
* **03 Queryable precedent libraries:** Transform case law, regulations, and statutes into an active knowledge store that a paralegal agent can ask questions of directly.
* **04 Adaptive compliance platforms:** Personalize the compliance monitoring for every client at scale, with each firm's legal context securely isolated in its own environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** Legal problems, solved.
* **01 Case strategy that needs memory:** A legal copilot must remember the matter across sessions — what was argued, what was dismissed, and the relationships between entities.
* **02 Per-matter isolation at scale:** A platform has thousands of legal cases, and each client's memory record must remain strictly their own. PiyApi guarantees structural privacy, data tokenization, and optional geo-fencing for strict compliance.
* **03 Evidence locked in unstructured files:** Discovery content is often trapped in unsearchable formats. PiyApi enables timestamped semantic search so lawyers can jump straight to the relevant exhibit.
* **04 Statutes that are hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and entity overlap), ensuring you get the exact legal provision even if phrasing differs.
* **Right Panel Labels:** `DOCUMENT -> NEXT DOCUMENT` | `01 DOCUMENT` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT DOCUMENT`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: Client, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Legal Memory
* **Label:** `05 PERSISTENT LEGAL MEMORY`
* **Title:** Analysis that deepens per case.
* **Description:** A LegalTech platform should get better for each case the longer it's analyzed. A copilot scanning a brief for the first time has no context; but after a discovery phase powered by PiyApi's bitemporal graph, it deterministically knows the key players, recurring disputes, and timeline of events, tailoring every interaction accordingly.
* **Right Panel Steps:** `01 First document` | `02 Known entities` | `03 Recurring disputes` | `04 Case timeline` | `05 Personalised next brief`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy contract analysis and legal copilots using our full-pattern, multi-tenant memory architecture, ensuring per-matter isolation and deep semantic search for case files.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does a copilot know what facts have already been established?
  * **A:** PiyApi remembers across documents. Each session's interactions are processed into memory scoped exclusively to that legal matter, so the copilot knows what is settled, what is disputed, and what needs research.
* **FAQ 2:**
  * **Q:** How are different clients kept separate at scale?
  * **A:** Negentro enforces strict per-client memory isolation at the infrastructure level. Every matter's context graph is structurally partitioned, ensuring zero data leakage, backed by privacy tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it extract data from scanned legal exhibits?
  * **A:** Yes. PiyApi can extract knowledge from unstructured PDFs and evidence files, mapping them semantically so attorneys can ask questions and find the exact page where a fact is located.
* **FAQ 4:**
  * **Q:** What happens when a law changes or a fact is overturned?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context—recognizing that a ruling was overturned—without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared case law mix with a client's private case facts?
  * **A:** No. Global knowledge (like statutes and precedents) is integrated seamlessly with personal memory, but private case strategies never pollute the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished legal product or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the LegalTech application, UI, and copilot on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every legal matter a memory that grows with it.
  * **Description:** Build legal systems that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
