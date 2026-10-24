### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / MEDIA`
* **Title:** AI infrastructure for media & entertainment.
* **Description:** Asset management requires multimodal context, not just keyword tags. Build intelligent search copilots, smart video archiving, and dynamic content libraries on persistent, per-tenant memory — the critical infrastructure most media platforms still lack.
* **Feature List:**
  * **BASE:** Per-tenant isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Audio, video, and scripts instantly transcribed and tokenized into semantically searchable text.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT MEDIA CONTEXT (01 - 05)`
* **Title:** Every asset adds context.
* **Description:** Negentro's PiyApi remembers what matters across scripts, dailies, or podcast episodes. By serving a perfectly curated, conflict-free payload, your media copilot avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of your entire content catalog.

### Section 3: Why Media Needs Memory
* **Label:** `01 WHY MEDIA NEEDS MEMORY`
* **Title:** Asset management only works if the system understands the content.
* **Description (Left):** Most media AI tools start every session with amnesia. A video search feature that can't recall what happens in an earlier episode, identify recurring characters, or track story arcs will never deliver true utility to editors or viewers.
* **Description (Right):** If you're building next-generation media platforms, the foundational layer must be per-tenant memory that's isolated, persistent, and secure. Turn static video and audio into a dynamic bitemporal graph that can be queried by meaning, resolving timeline contradictions deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Editorial copilots:** Adapt to the production pipeline — remembering script changes, shoot locations, and actor availabilities.
* **02 Video & audio search:** Make complex multimedia content searchable by meaning, so an editor instantly finds the exact timestamp a quote was spoken.
* **03 Queryable asset libraries:** Transform raw footage, B-roll, and podcast recordings into an active knowledge store that a producer can ask questions of directly.
* **04 Adaptive content platforms:** Personalize the discovery journey for every viewer at scale, with each user's viewing context securely isolated in its own environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** Media problems, solved.
* **01 Production that needs memory:** An editorial copilot must remember the project across sessions — what was cut, what is pending, and the overarching narrative.
* **02 Per-tenant isolation at scale:** A platform hosts thousands of creators, and each project's memory record must remain strictly their own. PiyApi guarantees structural privacy, data tokenization, and optional geo-fencing for strict compliance.
* **03 Assets locked in video and audio:** Media history is often trapped in unsearchable raw files. PiyApi enables timestamped semantic search so editors can jump straight to the exact frame.
* **04 Scripts that are hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and entity overlap), ensuring you get the relevant scene even if the dialogue differs slightly.
* **Right Panel Labels:** `PROJECT -> NEXT PROJECT` | `01 ASSET` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT ASSET`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: User/Creator, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Media Memory
* **Label:** `05 PERSISTENT MEDIA MEMORY`
* **Title:** Intelligence that deepens per project.
* **Description:** A media platform should get better for each creator the longer they use it. A copilot scanning a script for the first time has no context; but after a production cycle powered by PiyApi's bitemporal graph, it deterministically knows the characters, recurring themes, and preferred pacing, tailoring every interaction accordingly.
* **Right Panel Steps:** `01 First script` | `02 Known characters` | `03 Recurring themes` | `04 Production history` | `05 Personalised editing`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy media search and editorial copilots using our full-pattern, multi-tenant memory architecture, ensuring per-project isolation and deep semantic search for video and audio.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does a copilot know what happened in previous episodes?
  * **A:** PiyApi remembers across transcripts. Each session's interactions are processed into memory scoped exclusively to that series or project, so the copilot knows established lore, character traits, and plot points.
* **FAQ 2:**
  * **Q:** How are different creators kept separate at scale?
  * **A:** Negentro enforces strict per-tenant memory isolation at the infrastructure level. Every project's context graph is structurally partitioned, ensuring zero data leakage, backed by privacy tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it transcribe and search raw video?
  * **A:** Yes. PiyApi can extract knowledge from audio and video, mapping them semantically so editors can ask questions and find the exact timestamp where an event occurs.
* **FAQ 4:**
  * **Q:** What happens when a script is rewritten or a scene is cut?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context—recognizing a rewrite—without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared metadata mix with a creator's private project?
  * **A:** No. Global knowledge is integrated seamlessly with personal memory, but private scripts and unreleased footage never pollute the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished media player or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the streaming application, CMS, and copilot on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every creator a memory that grows with them.
  * **Description:** Build media systems that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
