# LongMemEval Benchmark Content Extraction

This document compiles all content and references related to the **LongMemEval** benchmark extracted from the `cognee`, `exabase`, `mastra`, `mem0`, and `supermem` directories.

## 1. Mastra
*Mastra heavily focuses on LongMemEval, presenting a comprehensive deep-dive into their "Observational Memory" architecture and its performance.*

*   **Top Scores:** Mastra's Observational Memory (OM) achieved a state-of-the-art score of **94.87%** with `gpt-5-mini` on the LongMemEval benchmark. With `gemini-3-pro-preview`, it scored 93.27%, and with `gpt-4o`, it scored 84.23%.
*   **Dataset Specs:** They used the `longmemeval_s` dataset containing 500 questions across ~57M tokens of conversational data. Each question has ~50 sessions attached.
*   **Categories Evaluated:**
    *   `knowledge-update`: When a user's information changes, can the system track the update?
    *   `multi-session`: Synthesizing information scattered across multiple conversations (noted as the hardest category).
    *   `single-session-assistant`: Recalling what the assistant said.
    *   `single-session-preference`: Remembering user preferences stated in passing.
    *   `single-session-user`: Recalling what the user said.
    *   `temporal-reasoning`: Resolving relative time and ordering events.
*   **RAG vs OM:** Initially, Mastra tested standard RAG (Semantic Recall), hitting **80.05%** with `topK 20` using `gpt-4o`, which already beat Zep's claims that RAG doesn't work for agent memory. Their "Observational Memory" approach pushed this to ~95%.
*   **Comparison to Others:** Mastra provides a leaderboard placing their OM system at the top, followed by Hindsight (91.40%), Supermemory (85.20%), EmergenceMem (86.00%), and Zep (71.20%).
*   **Why LongMemEval over LoCoMo?** Mastra explicitly chose LongMemEval because it uses question-specific LLM-as-judge prompts (providing reproducibility) rather than LoCoMo's unreliable F1 similarity scoring.

## 2. Exabase
*Exabase references LongMemEval to establish a baseline of quality before pushing for higher-scale evaluations (BEAM).*

*   **Top Score:** Exabase's M-1 architecture achieved **96.4%** on LongMemEval, using `Gemini 3 Flash`.
*   **View on the Benchmark:** They note that LongMemEval evaluates using ~115,000 tokens of conversational history. They argue that at this scale, a context window can technically hold the entire corpus (meaning a naive "dump everything into context" approach could participate).
*   **Previous SOTA Comparison:** Exabase positions M-1 (96.4%) as beating the previous SOTA, which they identify as Mem0 (94.8%).
*   **Conclusion:** They used their LongMemEval results to prove that "retrieval architecture, and not model scale, that drives memory system quality," before moving on to the BEAM benchmark to test at the 1M and 10M token scales.

## 3. Mem0
*Mem0 references LongMemEval to showcase their strong retrieval performance and the benefits of their "Temporal Reasoning" feature.*

*   **Top Score:** Mem0 scores **94.4%** overall on LongMemEval. With the introduction of their "Temporal Reasoning" feature, this improved to **94.8%** at `top_50` retrieval.
*   **Temporal Reasoning Impact:** The addition of time-aware memory (understanding when facts were true) yielded an overall lift of +4.4 points. The biggest gain was seen in `multi-session` questions, jumping +11.2 points (from 82.0% to 93.2% at `top_50`).
*   **Benchmark Context:** Mem0 processed 500 questions across 6 categories, with a mean token usage of 6,787 tokens. 
*   **View on the Benchmark:** Mem0 describes LongMemEval as targeting "longer, multi-topic dialogs with more turns between the initial fact and the final probe," introducing "realistic distractions and a mix of structured facts and free text," compared to shorter tests like LoCoMo.

## 4. Supermemory
*Supermemory positions itself as a top-tier memory solution across multiple benchmarks, including LongMemEval.*

*   **Claims:** Supermemory explicitly states they are "State of the art on LongMemEval, LoCoMo and ConvoMem #1". 
*   **External Mentions:** According to Mastra's published leaderboard, Supermemory achieved **85.20%** (using `gemini-3-pro-preview`), **84.60%** (using `gpt-5`), and **81.60%** (using `gpt-4o`) on LongMemEval. 

## 5. Cognee
*Cognee mentions LongMemEval primarily as a benchmark used by competitors, while distinguishing its own focus.*

*   **Mentions:** Cognee notes that both **mem0** and **Zep** have run and published results on LongMemEval (and LoCoMo).
*   **View on the Benchmark:** Cognee positions itself against these benchmarks by stating that mem0 and Zep optimize for "retrieval speed and token size on short-session QA datasets" (like LoCoMo and LongMemEval). Cognee instead prefers to evaluate on the BEAM benchmark, arguing it is a "longer-horizon benchmark where evidence is scattered across many turns."
