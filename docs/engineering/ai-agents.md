# AI Agents

## Overview

AI agents are systems in which a language model controls a multi-step process — selecting tools, taking actions, and adjusting based on results. Agents extend single-turn AI interactions to longer-horizon tasks.

---

## What Makes a System an Agent

An agent has some combination of:

- **Tool use:** The model can invoke functions, APIs, or external services
- **Memory:** The model retains context across steps
- **Planning:** The model decomposes tasks into sub-tasks
- **Feedback loops:** The model observes results and adjusts

A simple chatbot is not an agent. A system that receives a task, searches the web, drafts a document, checks it against criteria, and revises it is an agent.

---

## Agent Patterns

### ReAct (Reason + Act)

The model alternates between reasoning about what to do and taking an action. After each action, it observes the result and reasons again.

```
Thought: I need to find the current policy document.
Action: search("policy document Q4 2025")
Observation: [results returned]
Thought: The second result looks relevant. I'll retrieve it.
Action: retrieve(url)
...
```

### Tool-Calling Agents

The model selects from a defined set of tools. Tools are functions the model can call with structured parameters. The function executes in the environment and returns a result.

Common tools: web search, document retrieval, code execution, API calls, database queries.

### Multi-Agent Systems

Multiple specialized agents collaborate on a task. A coordinator agent delegates to specialist agents and synthesizes results.

**Caution:** Multi-agent systems are significantly harder to debug and monitor than single agents.

---

## Architectural Considerations

### Tool Design

- Tools should have clear, narrow contracts
- Tool descriptions must be precise — the model's tool selection depends on them
- Tools should return structured output the model can parse
- Tools should have timeouts and error handling

### State Management

Agents need memory of prior steps. Options:

- **In-context memory:** Everything in the prompt (simple, limited by context window)
- **External memory:** Store prior steps and retrieve relevant ones (scalable, adds retrieval complexity)

### Human-in-the-Loop

For high-stakes agent actions (sending emails, modifying data, making purchases), insert human approval steps. The cost of a wrong autonomous action is often higher than the cost of a confirmation step.

---

## Risk Profile

Agents are higher-risk than single-turn AI systems:

- **Compounding errors:** Early mistakes propagate through subsequent steps
- **Unintended side effects:** Agents can take actions with real-world consequences
- **Prompt injection:** External content processed by an agent can attempt to hijack its behavior
- **Runaway loops:** Agents can get stuck in retry loops with real resource consumption

**Default to conservative tool permissions.** Agents should have access to only the tools they need.

---

## Related

- [AI Architecture](ai-architecture.md)
- [Security and Privacy](security-and-privacy.md)
- [Observability](observability.md)
- [Evaluation and Testing](evaluation-and-testing.md)
