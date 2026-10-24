### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / ECOMMERCE`
* **Title:** AI infrastructure for ecommerce & retail.
* **Description:** Personalized shopping requires deep preference tracking, not just generic recommendations. Build intelligent shopping copilots, smart product search, and stateful cart-recovery agents on persistent, per-shopper memory — the critical infrastructure most retail products still lack.
* **Feature List:**
  * **BASE:** Per-shopper isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Catalogs and user reviews instantly parsed and tokenized with PII redaction.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT SHOPPER CONTEXT (01 - 05)`
* **Title:** Every purchase adds context.
* **Description:** Negentro's PiyApi remembers what matters across seasons, sales, or abandoned carts. By serving a perfectly curated, conflict-free payload, your shopping copilot avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of each individual shopper's taste.

### Section 3: Why Ecommerce Needs Memory
* **Label:** `01 WHY ECOMMERCE NEEDS MEMORY`
* **Title:** Personalised retail only works if the system remembers the shopper.
* **Description (Left):** Most retail AI tools start every session with amnesia. A shopping assistant that can't recall a user's sizing, brand preferences, or previous returns will never deliver true personalization.
* **Description (Right):** If you're building next-generation ecommerce platforms, the foundational layer must be per-shopper memory that's isolated, persistent, and secure. Turn static product catalogs into a dynamic bitemporal graph that can be queried by meaning, resolving preference changes deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Shopping copilots:** Adapt to each user across visits — remembering their style, budget, and sizing constraints.
* **02 Semantic product search:** Make vast inventory catalogs searchable by meaning, so a shopper instantly finds the exact item even using unconventional descriptions.
* **03 Stateful cart-recovery:** Transform abandoned sessions into active knowledge, allowing agents to seamlessly resume a conversation exactly where the user left off.
* **04 Adaptive storefronts:** Personalize the browsing journey for every user at scale, with each shopper's preference context securely isolated in its own environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** Retail problems, solved.
* **01 Recommendations that need memory:** A shopping assistant must remember the user across sessions — what they bought, what they returned, and how their style evolves.
* **02 Per-shopper isolation at scale:** A platform has millions of shoppers, and each user's memory record must remain strictly their own. PiyApi guarantees structural privacy, data tokenization, and optional geo-fencing for strict compliance.
* **03 Catalogs locked in rigid tags:** Inventory is often trapped in unsearchable category trees. PiyApi enables semantic search so shoppers can query by exact look and feel.
* **04 Inventory that is hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and entity overlap), ensuring shoppers get the relevant SKU even if their phrasing differs.
* **Right Panel Labels:** `VISIT -> NEXT VISIT` | `01 VISIT` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT VISIT`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: Shopper, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Shopper Memory
* **Label:** `05 PERSISTENT SHOPPER MEMORY`
* **Title:** Personalisation that deepens per user.
* **Description:** An ecommerce platform should get better for each shopper the longer they use it. A copilot meeting a user for the first time has no context; but after a season powered by PiyApi's bitemporal graph, it deterministically knows their exact fit, favored brands, and optimal price points, tailoring every interaction accordingly.
* **Right Panel Steps:** `01 First visit` | `02 Known sizes` | `03 Brand affinities` | `04 Purchase history` | `05 Personalised next session`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy shopping copilots and semantic search using our full-pattern, multi-tenant memory architecture, ensuring per-shopper isolation and deep search for retail catalogs.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does a copilot know what a shopper has already viewed or bought?
  * **A:** PiyApi remembers across sessions. Each session's interactions are processed into memory scoped exclusively to that user, so the copilot knows what they own, what they want, and what needs avoiding.
* **FAQ 2:**
  * **Q:** How are different shoppers kept separate at scale?
  * **A:** Negentro enforces strict per-shopper memory isolation at the infrastructure level. Every user's context graph is structurally partitioned, ensuring zero data leakage, backed by privacy tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it extract knowledge from user reviews?
  * **A:** Yes. PiyApi can extract sentiment and facts from unstructured product reviews, mapping them semantically so shoppers can ask questions about fit and durability directly.
* **FAQ 4:**
  * **Q:** What happens when a shopper changes their style or size?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context—recognizing a change in preference—without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared catalog data mix with a shopper's private cart?
  * **A:** No. Global knowledge (like product specs) is integrated seamlessly with personal memory, but private purchase history never pollutes the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished storefront or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the ecommerce application, UI, and copilot on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every shopper a memory that grows with them.
  * **Description:** Build ecommerce systems that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
