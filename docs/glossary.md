# Glossary

---

**Agent / AI Agent**
An AI system that autonomously executes multi-step tasks by selecting and invoking tools, observing results, and adjusting its approach. Distinguished from single-turn AI by its ability to take sequences of actions.

**Automation Bias**
The tendency for humans to over-trust automated system outputs, reducing the rigor of their own review. Well-documented in contexts where AI is in the loop for consequential decisions.

**Chunking**
The process of splitting source documents into smaller units for indexing in a RAG system. Chunk size and overlap strategy affect retrieval quality.

**Context Window**
The maximum amount of text (measured in tokens) that a language model can process in a single interaction. Inputs exceeding the context window are truncated.

**Data Drift**
A shift in the statistical distribution of real-world data relative to the data used to train an AI model. Can degrade model performance over time without any change to the model itself.

**Embedding**
A numerical vector representation of text (or other data) produced by an embedding model. Semantically similar texts have similar embeddings. Used in vector search for RAG systems.

**Evaluation (Evals)**
The process of systematically measuring AI system performance. Includes automated metrics, LLM-as-judge scoring, and human review.

**Fine-Tuning**
Adapting a pre-trained model to a specific task or domain by continuing training on task-specific data. Produces a customized model version.

**Foundation Model**
A large AI model trained on broad data, intended as a base for many downstream applications. Examples: GPT-4, Claude, Llama, Gemini.

**Grounding**
Providing an AI model with factual context (retrieved documents, database results, real-time data) to reduce hallucination and improve accuracy.

**Guardrails**
Constraints applied to AI system inputs or outputs to enforce safety, policy, or quality requirements. Can be implemented in the prompt, as post-processing filters, or via specialized models.

**Hallucination**
When an AI model generates confident, plausible-sounding output that is factually incorrect. A structural property of language models, not a bug that will be fully eliminated.

**Human-in-the-Loop (HITL)**
A system design where humans review or approve AI outputs before they take effect. Degree of involvement ranges from sampling to full review.

**LLM (Large Language Model)**
A neural network trained on large text datasets to predict and generate text. The underlying technology behind most contemporary AI assistants and coding tools.

**Model Risk**
The risk that an AI model produces incorrect, biased, or unstable outputs that cause financial, legal, or reputational harm. Formally defined in financial services regulation.

**Multimodal**
AI systems that process multiple types of input — text, images, audio, video — rather than text alone.

**Prompt**
The input text provided to a language model. Includes the system prompt (instructions), conversation history, and user query.

**Prompt Engineering**
The practice of designing and refining prompts to improve model output quality, consistency, and safety.

**Prompt Injection**
An attack in which malicious content in text processed by an AI system (documents, emails, web pages) attempts to override the system prompt or redirect model behavior.

**RAG (Retrieval-Augmented Generation)**
An architecture that retrieves relevant documents at query time and includes them in the model prompt, grounding responses in specific source material rather than model memory alone.

**Reranking**
A step in RAG pipelines that re-scores initially retrieved documents for relevance to the specific query. Improves precision at the cost of additional latency.

**Shadow AI**
Informal use of consumer AI tools by employees outside of organizational oversight. A risk vector for data leakage and policy violation.

**System Prompt**
The instruction set provided to an AI model before user interaction. Defines the model's role, behavior constraints, and context.

**Temperature**
A parameter controlling the randomness of language model output. Lower temperature produces more deterministic, predictable output; higher temperature produces more varied output.

**Token**
The unit of text that language models process. Roughly 3/4 of an English word. Models are priced by token consumption.

**Vector Store / Vector Database**
A database optimized for storing and searching vector embeddings. Enables semantic similarity search used in RAG systems.

**Zero-Shot / Few-Shot**
Prompting strategies. Zero-shot: the model responds without examples. Few-shot: the prompt includes example input-output pairs to guide the model's behavior.
