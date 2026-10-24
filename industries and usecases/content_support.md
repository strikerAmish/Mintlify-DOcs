### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / CUSTOMER SUPPORT`
* **Title:** AI infrastructure for customer support.
* **Description:** Customer resolution requires multi-session continuity, not just scripted replies. Build intelligent support copilots, smart ticket routing, and dynamic help centers on persistent, per-user memory — the critical infrastructure most support platforms still lack.
* **Feature List:**
  * **BASE:** Per-user isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Chat logs, emails, and calls instantly transcribed and tokenized with PII redaction.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT SUPPORT CONTEXT (01 - 05)`
* **Title:** Every ticket adds context.
* **Description:** Negentro's PiyApi remembers what matters across calls, emails, or live chats. By serving a perfectly curated, conflict-free payload, your support copilot avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of each individual customer's issue.

### Section 3: Why Support Needs Memory
* **Label:** `01 WHY SUPPORT NEEDS MEMORY`
* **Title:** Issue resolution only works if the system remembers the customer.
* **Description (Left):** Most support AI tools start every session with amnesia. A chatbot that can't recall a customer's previous complaints, ongoing technical issues, or subscription tier will never deliver true frustration-free support.
* **Description (Right):** If you're building next-generation support platforms, the foundational layer must be per-user memory that's isolated, persistent, and secure. Turn static ticket logs and help docs into a dynamic bitemporal graph that can be queried by meaning, resolving contradictions deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Triage & resolution copilots:** Adapt to each customer across channels — remembering what they've tried, what failed, and their exact configuration.
* **02 Ticket & history search:** Make complex support histories searchable by meaning, so an agent instantly finds the exact moment a workaround was applied.
* **03 Queryable knowledge bases:** Transform rigid FAQ pages and internal runbooks into an active knowledge store that a support agent can ask questions of directly.
* **04 Adaptive routing platforms:** Personalize the support journey for every user at scale, with each customer's context securely isolated in its own environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** Support problems, solved.
* **01 Resolution that needs memory:** A support agent must remember the customer across touchpoints — what their environment is, what is broken, and their previous interactions.
* **02 Per-customer isolation at scale:** A platform has millions of users, and each customer's memory record must remain strictly their own. PiyApi guarantees structural privacy, data tokenization, and optional geo-fencing for strict compliance.
* **03 Context locked in disjointed channels:** Support history is often trapped in unsearchable call transcripts. PiyApi enables timestamped semantic search so agents can jump straight to the moment the user explained the bug.
* **04 Runbooks that are hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and exact error codes), ensuring agents get the relevant fix even if phrasing differs.
* **Right Panel Labels:** `TICKET -> NEXT TICKET` | `01 TICKET` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT TICKET`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: Customer, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Customer Memory
* **Label:** `05 PERSISTENT CUSTOMER MEMORY`
* **Title:** Resolution that deepens per user.
* **Description:** A support platform should get better for each customer the longer they use it. A copilot answering a user for the first time has no context; but after a month powered by PiyApi's bitemporal graph, it deterministically knows their technical setup, recurring bugs, and subscription limits, tailoring every interaction accordingly.
* **Right Panel Steps:** `01 First ticket` | `02 Known setup` | `03 Recurring issues` | `04 Support history` | `05 Personalised next session`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy triage copilots and intelligent ticket routing using our full-pattern, multi-tenant memory architecture, ensuring per-user isolation and deep semantic search for support logs.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does a copilot know what a customer has already tried?
  * **A:** PiyApi remembers across channels. Each session's interactions are processed into memory scoped exclusively to that user, so the copilot knows what is fixed, what is broken, and what troubleshooting steps to skip.
* **FAQ 2:**
  * **Q:** How are different users kept separate at scale?
  * **A:** Negentro enforces strict per-user memory isolation at the infrastructure level. Every customer's context graph is structurally partitioned, ensuring zero data leakage, backed by privacy tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it extract data from long email chains and call logs?
  * **A:** Yes. PiyApi can extract knowledge from unstructured omnichannel support logs, mapping them semantically so agents can ask questions and find the exact reply where a promise was made.
* **FAQ 4:**
  * **Q:** What happens when a user updates their software or fixes an issue?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context—recognizing an upgrade—without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared troubleshooting data mix with a customer's private PII?
  * **A:** No. Global knowledge (like public help centers) is integrated seamlessly with personal memory, but private account details never pollute the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished Zendesk alternative or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the ticketing application, help desk, and copilot on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every customer a memory that grows with them.
  * **Description:** Build support systems that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
