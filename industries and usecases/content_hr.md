### Section 1: Hero
* **Breadcrumb:** `INDUSTRIES / HR`
* **Title:** AI infrastructure for HR & recruiting.
* **Description:** Effective recruiting requires tracking candidates across long, multi-stage journeys. Build intelligent onboarding copilots, smart resume search, and dynamic talent pools on persistent, per-candidate memory — the critical infrastructure most HR products still lack.
* **Feature List:**
  * **BASE:** Per-candidate isolation, zero-leakage, constant time O(1) retrieval latency.
  * **MEMORY:** Deterministic conflict resolution using the PiyGraph bitemporal architecture.
  * **EXTRACT:** Resumes and interviews instantly transcribed and tokenized with PII redaction.
  * **DEEP SEARCH:** Hybrid search fusing dense vector HNSW and BM25 trigrams via our UnifiedScorer Engine.
* **Buttons:** `Start building` | `Read the docs`

### Section 2: Context Introduction
* **Subtitle:** `PERSISTENT CANDIDATE CONTEXT (01 - 05)`
* **Title:** Every interaction adds context.
* **Description:** Negentro's PiyApi remembers what matters across screening calls, interviews, or onboarding weeks. By serving a perfectly curated, conflict-free payload, your HR copilot avoids the "Lost in the Middle" phenomenon and token-heavy context stuffing, responding with a progressively deeper understanding of each individual candidate.

### Section 3: Why HR Needs Memory
* **Label:** `01 WHY HR NEEDS MEMORY`
* **Title:** Recruiting only works if the system remembers the candidate.
* **Description (Left):** Most recruiting tools start every session with amnesia. An interviewing copilot that can't recall a candidate's previous answers, salary expectations, or specific skill gaps will never deliver a seamless candidate experience.
* **Description (Right):** If you're building next-generation HR platforms, the foundational layer must be per-candidate memory that's isolated, persistent, and secure. Turn static resumes and interview notes into a dynamic bitemporal graph that can be queried by meaning, resolving contradictions deterministically.

### Section 4: What You Can Build
* **Label:** `02 WHAT YOU CAN BUILD`
* **Title:** Four shapes, one infrastructure.
* **01 Interviewing copilots:** Adapt to each candidate across rounds — remembering what they've discussed, where they excel, and their career goals.
* **02 Resume & talent search:** Make complex candidate pools searchable by meaning, so a recruiter instantly finds the exact moment a specific skill was mentioned.
* **03 Queryable company wikis:** Transform onboarding manuals and HR policies into an active knowledge store that a new hire can ask questions of directly.
* **04 Adaptive onboarding platforms:** Personalize the first 90 days for every new hire at scale, with each employee's progress securely isolated in its own environment.

### Section 5: Product Architecture
* **Label:** `03 PRODUCT ARCHITECTURE`
* **Title:** HR problems, solved.
* **01 Recruiting that needs memory:** A screening agent must remember the candidate across touchpoints — what they know, what they lack, and their cultural fit.
* **02 Per-candidate isolation at scale:** A platform has thousands of applicants, and each person's memory record must remain strictly their own. PiyApi guarantees structural privacy, PII tokenization, and optional geo-fencing for strict compliance.
* **03 Interviews locked in video and audio:** Screening content is often trapped in unsearchable Zoom recordings. PiyApi enables timestamped semantic search so recruiters can jump straight to the moment a candidate answered a technical question.
* **04 Resumes that are hard to search:** Implement hybrid search that evaluates 11 signals in a single pass (including recency decay and entity overlap), ensuring recruiters get the relevant candidate even if job titles differ.
* **Right Panel Labels:** `INTERVIEW -> NEXT INTERVIEW` | `01 INTERVIEW` | `02 CONTEXT` | `03 MEMORY` | `04 NEXT INTERVIEW`

### Section 6: Architecture Diagram
* **Label:** `04 ARCHITECTURE`
* **Title:** The infrastructure underneath.
* *(Keep the diagram exactly as is, the labels perfectly describe the PiyApi flow: Candidate, Session, Context Engine, Extract, Search, Knowledge, Retrieval System).*

### Section 7: Persistent Candidate Memory
* **Label:** `05 PERSISTENT CANDIDATE MEMORY`
* **Title:** Intelligence that deepens per hire.
* **Description:** An HR platform should get better for each candidate the longer they interact with it. A copilot meeting an applicant for the first time has no context; but after a screening phase powered by PiyApi's bitemporal graph, it deterministically knows their technical strengths, recurring questions, and optimal placement, tailoring every interview accordingly.
* **Right Panel Steps:** `01 First screen` | `02 Known strengths` | `03 Salary expectations` | `04 Interview history` | `05 Personalised final round`

### Section 8: Get Started
* **Label:** `06 GET STARTED`
* **Title:** Start with the use case that fits.
* **Description:** Deploy recruiting and onboarding copilots using our full-pattern, multi-tenant memory architecture, ensuring per-candidate isolation and deep semantic search for talent pools.
* **Buttons:** `Start building` | `Read the docs ->` | `Talk to us ->`

### Section 9: Frequently Asked Questions
* **Label:** `07 QUESTIONS`
* **Title:** Frequently asked.
* **FAQ 1:**
  * **Q:** How does an agent know what a candidate has already been asked?
  * **A:** PiyApi remembers across rounds. Each session's interactions are processed into memory scoped exclusively to that candidate, so the copilot knows what technical skills are validated and what needs probing.
* **FAQ 2:**
  * **Q:** How are different applicants kept separate at scale?
  * **A:** Negentro enforces strict per-candidate memory isolation at the infrastructure level. Every applicant's context graph is structurally partitioned, ensuring zero data leakage, backed by privacy tokenization and real-world token economics.
* **FAQ 3:**
  * **Q:** Can it transcribe and search video interviews?
  * **A:** Yes. PiyApi can extract knowledge from audio and video transcripts, mapping them semantically so recruiters can ask questions and find the exact timestamp where an answer is located.
* **FAQ 4:**
  * **Q:** What happens when a candidate updates their resume or skills?
  * **A:** PiyApi features Deterministic Conflict Resolution via its bitemporal graph. It structurally segregates when a fact becomes true from when it was ingested, overriding outdated context—recognizing a newly acquired certification—without injecting LLM hallucinations.
* **FAQ 5:**
  * **Q:** Does shared company policy mix with an employee's private feedback?
  * **A:** No. Global knowledge (like HR handbooks) is integrated seamlessly with personal memory, but private performance reviews and notes never pollute the shared global knowledge base.
* **FAQ 6:**
  * **Q:** Is this a finished ATS product or something I build on?
  * **A:** PiyApi is the foundational memory API and infrastructure layer, delivering O(1) constant time latency. We provide the memory intelligence; you build the HR application, ATS, and copilot on top.

### Section 10: Footer
* **Label:** `08 MORE SOLUTIONS`
* **Title:** Explore other industries.
* **Grid Options:** *(Education, Healthcare, Finance, Legal, HR, Media, SaaS, Ecommerce, Consulting, Customer Support)*
* **Bottom CTA:**
  * **Label:** `START BUILDING`
  * **Title:** Give every candidate a memory that grows with them.
  * **Description:** Build HR systems that remember context, retrieve knowledge, and personalize every interaction with Negentro's PiyApi.
  * **Buttons:** `Start building` | `Explore the docs`
