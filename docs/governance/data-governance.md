# Data Governance

## Overview

AI systems are only as good as the data they use. Data governance in an AI context covers how data is classified, managed, and controlled when it enters AI pipelines.

---

## Data Classification for AI

Most organizations have data classification policies. AI introduces new contexts where those classifications apply:

| Classification | Can be sent to external AI? | Conditions |
|---|---|---|
| Public | Yes | No conditions |
| Internal | Yes, with conditions | Approved tools, data processing agreement |
| Confidential | Only to approved systems | Strict DPA, security review |
| Regulated (PII, PHI, PCI) | Only where compliant | Specific legal requirements met |

Establish and communicate which classification applies to the data employees commonly work with.

---

## Data Lineage in AI Pipelines

Track where data comes from and where it goes:

- What sources feed the AI system?
- Is the data transformed or anonymized before use?
- What is retained (prompts, responses, embeddings)?
- Who has access to logs containing user data?

Lineage documentation supports audit, incident response, and regulatory requirements.

---

## Retrieval Access Control

For RAG systems, retrieval must respect access controls:

- A user querying an AI assistant should only receive information from documents they are authorized to access
- Access control must be enforced at the retrieval layer, not just at document storage
- Verify that multi-tenant RAG systems isolate data between tenants

This is a commonly missed gap in RAG implementations.

---

## Data Retention

AI systems generate new data (prompts, responses, embeddings, fine-tuning datasets). Apply retention policies:

- What is kept, for how long, and why
- When is data deleted
- Who can access retained AI interaction data

---

## Training Data Governance

If the organization fine-tunes models or contributes to training:

- What data was used, with what consent
- How is personal data handled in training sets
- What right of deletion or correction exists for training data subjects

---

## Related

- [Security and Privacy](../engineering/security-and-privacy.md)
- [Compliance](compliance.md)
- [AI Policy](ai-policy.md)
