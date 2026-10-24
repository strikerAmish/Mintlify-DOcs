### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / HEALTHCARE`
* **Title:** AI infrastructure for healthcare.
* **Description:** Patient care requires context, not just scale. Build intelligent triage copilots, smart medical record search, and dynamic care platforms on persistent, per-patient memory — the critical infrastructure required for HIPAA-compliant AI workflows.
* **Feature List:**
  * **BASE:** Per-patient isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Medical notes and PDFs instantly transcribed and tokenized with PHI redaction.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT PATIENT CONTEXT (01 - 05)`
* **Title:** Every visit adds context.
* **Description:** Negentro's PiyApi remembers what matters across days, weeks, or years. By serving a perfectly curated, conflict-free payload, your copilot avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of each individual patient's history.

### Section 3: Why Healthcare Needs Memory
* **Label:** `01 WHY HEALTHCARE NEEDS MEMORY`
* **Title:** Triage and care only work if the system remembers the patient.
* **Description (Left):** Most medical AI tools start every session with amnesia. A triage feature that can't recall a patient's chronic conditions, previous symptoms, or contraindications will never deliver safe, personalized care.
* **Description (Right):** If you're building next-generation health platforms, the foundational layer must be per-patient memory that's isolated, persistent, and secure. Turn static medical records into a dynamic bitemporal graph that can be queried by meaning, resolving contradictions deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Triage copilots:** Adapt to each patient across visits — remembering their baseline health, recent procedures, and ongoing symptoms.
* **02 Medical record search:** Make complex patient histories searchable by meaning, so a clinician instantly finds the exact moment a diagnosis was recorded.
* **03 Queryable medical libraries:** Transform clinical guidelines and research papers into an active knowledge store that a copilot can ask questions of directly.
* **04 Adaptive care platforms:** Personalize the care journey for every user at scale, with each patient's medical context securely isolated in its own HIPAA-ready environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** Healthcare problems, solved.
* **01 Triage that needs memory:** A copilot that adapts must remember the patient across visits — what they've tried, what failed, and their medical history.
* **02 Per-patient isolation at scale:** A platform has thousands of patients, and each person's memory record must remain strictly their own. PiyApi guarantees structural privacy, PHI tokenization, and optional geo-fencing for strict compliance.
* **03 Records locked in PDFs:** Medical history is often trapped in unsearchable scans. PiyApi enables timestamped semantic search so clinicians can jump straight to the moment a test result was filed.
* **04 Clinical literature that's hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and entity overlap), ensuring you get the relevant clinical guideline even if phrasing differs.
* **Right Panel Labels:** `VISIT -> NEXT VISIT` | `01 VISIT` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT VISIT`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: Patient, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Patient Memory
* **Label:** `05 PERSISTENT PATIENT MEMORY`
* **Title:** Care that deepens per patient.
* **Description:** A healthcare platform should get better for each patient the longer they use it. A copilot meeting a patient for the first time has no context; but after a year powered by PiyApi's bitemporal graph, it deterministically knows their chronic conditions, recurring symptoms, and baseline health, tailoring every interaction accordingly.
* **Right Panel Steps:** `01 First visit` | `02 Known conditions` | `03 Recurring symptoms` | `04 Medical history` | `05 Personalised next visit`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy triage and healthcare copilots using our full-pattern, multi-tenant memory architecture, ensuring per-patient isolation and deep semantic search for clinical records.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does a copilot know a patient's medical history?
  * **A:** PiyApi remembers across visits. Each session's interactions are processed into memory scoped exclusively to that patient, so the copilot knows their baseline, ongoing treatments, and past symptoms.
* **FAQ 2:**
  * **Q:** How is HIPAA compliance handled at scale?
  * **A:** Negentro enforces strict per-patient memory isolation at the infrastructure level. Every patient's context graph is structurally partitioned, ensuring zero data leakage, backed by PHI tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it extract data from scanned medical PDFs?
  * **A:** Yes. PiyApi can extract knowledge from unstructured medical records and scans, mapping them semantically so clinicians can ask questions and find the exact page where a result is located.
* **FAQ 4:**
  * **Q:** What happens when a patient is cured of a past condition?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared medical knowledge mix with a patient's private PHI?
  * **A:** No. Global knowledge (like clinical guidelines) is integrated seamlessly with personal memory, but personal PHI and visit notes never pollute the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished medical product or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the healthcare application, UI, and copilot on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every patient a memory that grows with them.
  * **Description:** Build healthcare systems that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
