# Human Oversight

## Overview

Human oversight is the set of mechanisms by which people monitor, review, and can intervene in AI system behavior. It is a requirement in regulated contexts and a risk management practice in all others.

---

## Why Oversight Cannot Be Optional

AI systems fail in ways that are unpredictable, probabilistic, and sometimes invisible until consequences accumulate. Without oversight mechanisms:

- Errors propagate at scale before detection
- Accountability is unclear when something goes wrong
- Regulatory requirements in many sectors cannot be met
- Systemic biases compound without correction

---

## Oversight Mechanisms

### Pre-Deployment Review

Before deploying an AI system:
- Risk assessment against classification criteria
- Technical review of accuracy, failure modes, and bias
- Legal and compliance sign-off where required
- Approval by designated authority

### Human-in-the-Loop

For high-stakes decisions, require a human to review AI output before it takes effect.

**Spectrum of human involvement:**

| Level | Description | When to Use |
|---|---|---|
| Full automation | AI acts without human review | Low-stakes, high-volume, reversible |
| Human review on flag | AI flags uncertain cases for review | Medium-stakes |
| Human confirmation | Human approves before action | High-stakes or irreversible |
| AI assists human | Human makes decision, AI provides input | Highest-stakes, regulated decisions |

### Ongoing Monitoring

Post-deployment oversight:
- Output quality monitoring and alerting
- Regular human review of sampled outputs
- Incident tracking and root cause analysis
- Periodic reassessment of risk classification

### Appeal and Correction

When AI decisions affect individuals, there must be:
- A way for affected parties to contest the decision
- A human who can review the AI's decision
- A process to correct errors and update records

This is a legal requirement in many jurisdictions for automated decision-making.

---

## Accountability Assignment

Oversight requires clear accountability:

- Who is notified when monitoring thresholds are breached?
- Who decides to halt or roll back an AI system?
- Who is responsible for outcomes when AI output is wrong?
- Who owns the ongoing review cadence?

Committees can approve; individuals must be accountable.

---

## Related

- [Governance](../leadership/governance.md)
- [AI Policy](ai-policy.md)
- [Compliance](compliance.md)
- [Operational Risks](../operations/operational-risks.md)
