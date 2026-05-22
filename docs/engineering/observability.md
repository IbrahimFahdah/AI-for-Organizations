# Observability

## Overview

AI systems require observability beyond standard application monitoring. Model behavior is probabilistic and can degrade in ways that are invisible to infrastructure metrics. You need to observe what the model is doing, not just that it is running.

---

## What to Monitor

### Infrastructure Layer

Standard application metrics apply:
- Latency (p50, p95, p99)
- Error rates (API errors, timeouts)
- Cost (token consumption, API spend)
- Throughput (requests per second)

### Model Output Layer

This is where AI observability differs:

- **Output quality scores:** Automated metrics run against model outputs
- **Refusal rate:** How often the model declines to answer
- **Output length distribution:** Sudden changes indicate behavior change
- **Format compliance:** For structured output tasks, how often is the format correct
- **Hallucination proxy metrics:** Citation accuracy, factual consistency checks

### User Behavior Layer

- **Thumbs up/down rates:** Direct user feedback
- **Correction rate:** How often users edit AI outputs
- **Abandon rate:** How often users stop after seeing AI output
- **Re-query rate:** How often users rephrase after an unsatisfying answer

---

## Logging Requirements

Log enough to reconstruct what happened when something goes wrong:

| What to Log | Why |
|---|---|
| Full prompt (sanitized) | Reproduce issues |
| Model response | Audit, debugging |
| Model version and parameters | Reproduce issues after updates |
| Latency and token counts | Cost attribution, performance |
| User ID (hashed if needed) | Incident investigation |
| Upstream request context | Trace through the system |

**Warning:** Prompts may contain sensitive data. Apply data classification policies before logging.

---

## Evaluation Pipelines

One-time evaluation is not enough. Run automated evaluation on a sample of live traffic:

1. **Sample** a representative set of production requests
2. **Score** outputs with an automated judge (often another model, or rule-based checks)
3. **Alert** when quality drops below threshold
4. **Review** flagged outputs with human analysts

This is sometimes called "LLM-as-judge" evaluation. It is approximate but scalable.

---

## Tracing for Agents

Agent systems require distributed tracing that captures:
- Each tool call (input, output, latency)
- Each model call (prompt, response, version)
- The reasoning chain between steps
- Total cost and latency per agent run

---

## Tools and Frameworks

- **LangSmith, Langfuse, Arize:** Purpose-built LLM observability
- **OpenTelemetry:** Standard tracing, works with custom instrumentation
- **Prometheus + Grafana:** Infrastructure metrics

---

## Related

- [AI Agents](ai-agents.md)
- [Evaluation and Testing](evaluation-and-testing.md)
- [Operational Risks](../operations/operational-risks.md)
