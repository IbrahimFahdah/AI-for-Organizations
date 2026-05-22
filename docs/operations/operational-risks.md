# Operational Risks

## Overview

AI systems introduce operational risks that differ from traditional software. Standard monitoring and incident response processes need to be adapted.

---

## Risk Categories

### Output Quality Degradation

AI model performance can degrade over time due to:
- Data drift (the real-world distribution shifts from training data)
- Model updates by the vendor
- Changes in upstream data pipelines
- Adversarial inputs

**Mitigation:** Continuous output quality monitoring. See [Observability](../engineering/observability.md).

### Automation Errors at Scale

A bug in traditional software produces one wrong output per execution. An AI error in a high-volume automated pipeline can produce thousands of wrong outputs before detection.

**Mitigation:** Statistical sampling with human review. Anomaly detection on output distributions. Hard limits on automated action rates.

### Dependency Failures

AI systems depend on:
- External model APIs (vendor availability)
- Data pipelines feeding the model
- Downstream systems consuming outputs

Each dependency is a failure point.

**Mitigation:** Circuit breakers. Graceful degradation paths. SLA monitoring for upstream dependencies.

### Feedback Loop Corruption

When AI outputs influence the data used to evaluate or retrain the AI, feedback loops can form. The system trains on its own outputs and drifts.

**Mitigation:** Keep human-labeled evaluation sets that are not contaminated by model outputs. Monitor for distribution shift in training data.

### Prompt Injection

For AI systems that process external text (emails, documents, user input), malicious content can attempt to override system instructions.

**Mitigation:** Input sanitization. Privileged/unprivileged context separation in prompts. Human review of high-stakes outputs. See [Security and Privacy](../engineering/security-and-privacy.md).

---

## Operational Risk Framework

| Risk | Likelihood | Impact | Mitigation Priority |
|---|---|---|---|
| Output quality degradation | High | Medium–High | Monitor continuously |
| Vendor API outage | Medium | High | Fallback/circuit breaker |
| Automation errors at scale | Low–Medium | High | Sampling + rate limits |
| Prompt injection | Medium | Medium–High | Input controls |
| Data pipeline failure | Medium | High | Pipeline monitoring |
| Feedback loop corruption | Low | High | Evaluation set hygiene |

---

## Incident Response

Define before deployment:

- Who is alerted when AI output quality drops below threshold
- Who decides to halt automated processing
- What the manual fallback process is
- How incidents are documented and reviewed

---

## Related

- [Observability](../engineering/observability.md)
- [Security and Privacy](../engineering/security-and-privacy.md)
- [Workflow Integration](workflow-integration.md)
