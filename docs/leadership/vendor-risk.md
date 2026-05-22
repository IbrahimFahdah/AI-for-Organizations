# Vendor Risk

## Overview

AI vendors introduce risks that differ in kind from traditional software vendors. The opacity of models, the pace of change, and the dependency on external infrastructure create specific vulnerabilities that procurement and risk teams need to understand.

---

## Categories of Vendor Risk

### Model Risk

AI model behavior can change across versions without warning. A model update by a vendor can:

- Change output quality or format
- Shift political or content moderation behavior
- Break integrations that depend on specific output patterns

**Mitigation:** Pin to specific model versions where possible. Test across model updates before applying them in production. Include change notification requirements in contracts.

### Data Risk

When data is sent to a third-party AI vendor, questions arise:

- Is the data used to train the vendor's models?
- Who has access to data at the vendor?
- Is the data retained, and for how long?
- Does sending data violate privacy regulations or customer agreements?

**Mitigation:** Review data processing terms carefully. Prefer vendors with opt-out of training data use. Apply data minimization — send only what is necessary.

### Concentration Risk

Dependence on a single AI vendor creates fragility. If the vendor:

- Changes pricing significantly
- Experiences an outage
- Deprecates a model or service
- Is acquired or changes terms

...the organization may have limited options.

**Mitigation:** Design for abstraction where feasible. Maintain awareness of alternatives. Avoid deep integration that makes switching prohibitively expensive.

### Longevity Risk

AI startups fail. Models get deprecated. Services get shut down. Consider:

- What is the vendor's financial stability?
- What happens to your data if the vendor closes?
- Is there an exit plan?

---

## Vendor Due Diligence Questions

- What are the data processing terms, and can we negotiate them?
- Can we pin to a specific model version?
- What is the SLA for uptime and incident response?
- What is the deprecation policy for models and APIs?
- How are security vulnerabilities disclosed and remediated?
- Is there a third-party security audit available?

---

## Related

- [Procurement](procurement.md)
- [Security and Privacy](../engineering/security-and-privacy.md)
- [AI Hype vs Reality](../fundamentals/ai-hype-vs-reality.md)
