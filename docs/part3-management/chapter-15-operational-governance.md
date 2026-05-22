# Chapter 15: Operational Governance and Risk Management

Governance approved the deployment. Operational governance keeps it running within acceptable risk bounds after go-live.

---

## Operational Controls

Controls are the mechanisms that keep AI systems behaving within defined parameters:

| Control type | Example |
|---|---|
| Input controls | Blocked prompt patterns, data classification checks before processing |
| Output controls | PII scanning, format validation, content filtering |
| Rate controls | Limits on automated action volume per time period |
| Escalation controls | Routing low-confidence outputs to human review |
| Audit controls | Logging all AI actions for review |

Define controls before deployment. Retrofitting them is harder and more disruptive.

---

## Compliance Execution

Policy compliance requires more than a policy document:

- **Training** — staff know what the policy requires
- **Controls** — technical enforcement where feasible
- **Monitoring** — evidence that policy is being followed
- **Audit trail** — logs sufficient to investigate incidents
- **Review cycle** — policy updated as AI systems and regulations change

The compliance question is not "do we have a policy?" — it is "can we demonstrate compliance?"

---

## Responsible AI Operations

Daily operations should include:

- Monitoring output quality metrics and reviewing alerts
- Reviewing a sample of AI outputs (not just flagged ones)
- Tracking and triaging user-reported issues
- Escalating systemic quality problems to product/engineering

This is ongoing work, not a quarterly checkbox.

---

## Audit Readiness

An AI system that cannot be audited should not be deployed in regulated contexts. Audit readiness requires:

- An AI inventory with system documentation
- Logs that can reconstruct what the system did and why
- Evidence of pre-deployment testing and validation
- Records of governance approvals
- Post-deployment performance data

---

## Risk Mitigation Processes

For each identified risk (see [Chapter 4](../part1-foundations/chapter-04-responsible-ai.md)):

- Define a mitigation control
- Assign an owner
- Set a monitoring threshold
- Define the response when the threshold is breached

Risk without a mitigation owner is risk that will be managed reactively, after an incident.

---

## Key Takeaways

- Operational governance is the ongoing practice; policy governance is the framework.
- Compliance requires training, controls, monitoring, and audit trails — not just a document.
- Every identified risk needs a named owner and a defined response threshold.

**Common mistake:** Treating governance review as a deployment prerequisite only; stopping governance at go-live.
