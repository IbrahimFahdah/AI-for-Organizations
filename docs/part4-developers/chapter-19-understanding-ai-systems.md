# Chapter 19: Understanding AI Systems

Building reliable AI systems requires understanding how the underlying technology works — not just how to call the API.

---

## Machine Learning Foundations

ML models learn statistical patterns from labeled data. Key concepts every AI engineer needs:

- **Training vs inference** — training is expensive and offline; inference is real-time and cheap by comparison
- **Overfitting** — model memorizes training data, fails on new inputs
- **Distribution shift** — real-world data diverges from training data over time
- **Embeddings** — dense vector representations of text, images, or other data; the foundation of semantic search

---

## Large Language Models

LLMs are transformer-based models trained on large text corpora to predict the next token. What this means in practice:

- They generate plausible continuations, not verified facts
- Longer context improves performance, up to the context window limit
- Temperature controls output randomness (lower = more deterministic)
- System prompts are instructions; user messages are inputs — this distinction matters for security

Model scale does not linearly predict task performance. Evaluate on your specific task.

---

## AI Architectures

| Pattern | Description | Use Case |
|---|---|---|
| Direct API | App calls model API directly | Simple, low-volume |
| Gateway | Internal proxy mediates all AI calls | Enterprise, multi-model |
| RAG | Retrieval + generation | Knowledge-grounded Q&A |
| Agent | Model controls multi-step execution | Complex, multi-tool tasks |
| Fine-tuned | Custom model for specific domain | High-volume, narrow tasks |

---

## APIs and Integrations

Most AI capabilities are consumed via HTTP APIs with JSON. Core concepts:

- **Prompt** — the input sent to the model (system + messages)
- **Completion** — the model's response
- **Tokens** — the unit of input/output; cost and context limits are token-based
- **Streaming** — receive response tokens incrementally rather than waiting for full response
- **Function/tool calling** — structured mechanism for model to request execution of defined functions

---

## Enterprise AI Platforms

Managed AI platforms (Azure OpenAI, AWS Bedrock, GCP Vertex AI) offer:
- Data residency within your cloud account
- Integration with existing IAM and networking
- Managed endpoints for common models
- Usage logging and cost attribution

Trade-off: higher cost per token vs. proprietary API; more compliance controls vs. less flexibility.

---

## Key Takeaways

- LLMs generate plausible text; production systems need evaluation pipelines to catch failures.
- Architecture choice (RAG, agent, fine-tuned) is a product decision, not just a technical one.
- Token economics affect system design — context window limits and cost per token are first-class constraints.

**Common mistake:** Treating the model as the system. The model is one component; retrieval, prompting, evaluation, and monitoring are equally important.
