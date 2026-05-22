# Evaluation and Testing

## Overview

AI systems cannot be tested the same way traditional software is tested. There is no single correct output to assert against — outputs are probabilistic, context-dependent, and often evaluated on dimensions like quality and appropriateness rather than correctness.

---

## Evaluation Types

### Unit-Level Evaluation

Test individual prompts or components in isolation.

- Define a set of representative inputs with expected output characteristics
- Run the prompt and score the output against the criteria
- Track pass rate over time and across model versions

### End-to-End Evaluation

Test the full system: retrieval, generation, post-processing, and output.

- Use representative user queries
- Score final outputs for accuracy, relevance, format compliance
- Include edge cases, adversarial inputs, and common failure modes

### Regression Testing

Ensure changes to prompts, models, or retrieval don't degrade known-good cases.

- Maintain a curated regression test set
- Run before any deployment change
- Track performance trends, not just pass/fail

---

## Evaluation Metrics

| Dimension | Measurement Approach |
|---|---|
| Factual accuracy | Human review, automated fact-checking |
| Retrieval recall (RAG) | Ground truth retrieval tests |
| Format compliance | Structured output parsing, regex |
| Instruction following | Rubric-based scoring |
| Refusal appropriateness | Human review of refusal rate |
| Latency | P95 response time |
| Cost | Token consumption per query |

---

## LLM-as-Judge

For dimensions that are difficult to measure with rules, use a separate LLM to evaluate outputs.

```
Evaluate the following response for factual accuracy and completeness.
Rate on a scale of 1–5 and explain your rating.

Question: [question]
Expected answer: [reference answer]
Model response: [response to evaluate]
```

**Limitations:**
- Biases toward longer, more confident-sounding responses
- May not catch subtle factual errors
- Performance depends on the judge model's own capabilities

Use LLM-as-judge as one signal, not the only signal.

---

## Human Evaluation

Human evaluation is the gold standard for quality assessment but is expensive and slow.

- Use for initial calibration and setting standards
- Use for periodic audits of automated evaluation reliability
- Use for high-stakes use cases where quality requirements are critical

---

## Test Data Management

- Keep test sets separate from training/fine-tuning data
- Maintain test set freshness — add new cases as failure modes are discovered
- Do not use production data directly in test sets without anonymization

---

## Related

- [Observability](observability.md)
- [RAG Systems](rag-systems.md)
- [AI Agents](ai-agents.md)
