# *LongMemEval Benchmark Results*

*At **Negentro**, we believe that a truly intelligent AI agent requires a memory layer that doesn't just store information, but actively tracks evolving facts, cross-session nuances, and temporal shifts. To prove the capabilities of **PiyApi**, our advanced memory layer, we rigorously evaluate it against the industry-standard **LongMemEval** benchmark.*

## *Why LongMemEval?*

*While many memory benchmarks test simple factual recall within short conversational windows, production AI agents face much messier reality. Users change their minds, facts update over time, and crucial information is often scattered across dozens of disjointed sessions.*

*We test PiyApi against LongMemEval because it reflects real-world complexity. Using a rigorous dataset of 500 questions spanning ~57M tokens of conversational data, LongMemEval is widely recognized as one of the most comprehensive benchmarks for evaluating long-term interactive memory. It challenges the memory layer to perform across six critical categories:*

* ***Information Extraction (IE):** Recalling specific information from extensive interactive histories, including details mentioned by either the user or the assistant.*
* ***Multi-Session Reasoning (MR):** Synthesizing information across multiple history sessions to answer complex questions that involve aggregation and comparison.*
* ***Knowledge Updates (KU):** Recognizing changes in the user's personal information and updating knowledge of the user dynamically over time.*
* ***Temporal Reasoning (TR):** Showing awareness of the temporal aspects of user information, including explicit time mentions and timestamp metadata.*
* ***Abstention (ABS):** Identifying questions seeking unknown information (not mentioned in the history) and correctly abstaining or answering "I don't know".*

---

## PiyApi's Performance on LongMemEval

PiyApi was designed from the ground up to solve the exact challenges that LongMemEval tests. By moving beyond naive RAG (Retrieval-Augmented Generation) and implementing true contextual and temporal understanding, PiyApi delivers industry-leading accuracy.

### Overall Score

🏆 **Overall Accuracy: [YOUR_OVERALL_SCORE]%** (Model: [MODEL_NAME_USED, e.g., gpt-4o])

*This places PiyApi [YOUR_COMPETITIVE_POSITION, e.g., at the state-of-the-art frontier / among the top 3 memory architectures globally], outperforming traditional vector-search approaches while maintaining a highly efficient token footprint.*

### Accuracy by Question Type

We believe in transparency across every memory capability. Here is how PiyApi breaks down across LongMemEval's rigorous categories:

| Category                          | PiyApi Accuracy    | Industry Context                                                                                                  |
| :-------------------------------- | :----------------- | :---------------------------------------------------------------------------------------------------------------- |
| **Information Extraction**  | **[SCORE]%** | *[Optional note, e.g., Proves high-fidelity recall of granular facts buried in massive histories.]*             |
| **Multi-Session Reasoning** | **[SCORE]%** | *[Optional note, e.g., Showcases our graph-linking ability to connect dots across months of disjointed chats.]* |
| **Knowledge Updates               |                    |                                                                                                                   |

```

```

** | **[SCORE]%** | *[Optional note, e.g., Demonstrates PiyApi's ability to seamlessly override outdated facts without hallucinating.]* |
| **Temporal Reasoning**            | **[SCORE]%** | *[Optional note, e.g., Proves PiyApi understands the difference between past states and current realities.]*        |
| **Abstention**                    | **[SCORE]%** | *[Optional note, e.g., Ensures the agent never hallucinates when facts aren't present.]*                            |

---

## What This Means for Your AI Agents

Benchmark scores only matter if they translate to better user experiences. PiyApi's high performance on LongMemEval means that when you integrate Negentro's memory layer into your application, you get:

1. **Durable Context:** Your agents won't suffer from "context rot." They will remember a user's dietary restrictions from six months ago just as clearly as a prompt from six seconds ago.
2. **Lower Latency & Cost:** By retrieving the exact *right* memory rather than stuffing the context window with raw chat history, PiyApi drastically reduces LLM token costs and latency.
3. **Conflict Resolution:** When a user says "Actually, I moved to London," PiyApi correctly updates the state rather than holding two conflicting locations as equally true.

### Reproduce Our Results

We believe in open evaluation. You can review our evaluation methodology, prompts, and run the benchmark against PiyApi yourself.

[Link to Benchmark Runner / GitHub Repo] | [Read our Evaluation Methodology Blog Post]

---

*Curious how PiyApi stacks up in other scenarios? Explore our results on the [BEAM Benchmark] and [LoCoMo].*
