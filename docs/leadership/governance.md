# Governance

## Overview

AI governance is the system of policies, roles, and processes that determine how AI is approved, deployed, monitored, and retired within an organization. Governance is not a compliance exercise — it is a risk management function.

---

## Core Governance Functions

### Approval

Who decides which AI use cases are permitted? A governance framework defines:

- The intake process for proposed AI applications
- The criteria used to evaluate risk
- The escalation path for high-risk or novel cases
- Time-to-decision targets (slow approval drives shadow AI)

### Risk Classification

Not all AI uses carry the same risk. A tiered system is practical:

| Tier | Description | Examples | Oversight |
|---|---|---|---|
| Low | Internal, reversible, low-stakes | Meeting summarization, drafting assistance | Self-service |
| Medium | External-facing or significant process impact | Customer service AI, document review | Team lead review |
| High | Regulated, consequential, or irreversible | Hiring, credit, medical decisions | Committee review |

### Monitoring

Deployed AI systems require ongoing oversight:

- Output quality monitoring (drift, degradation)
- Usage audits (who uses it, for what)
- Incident tracking and response
- Periodic reassessment of risk classification

### Retirement

AI systems should have defined criteria for retirement or replacement. Changes in the underlying model, data, or regulatory environment may require revisiting decisions.

---

## Governance Roles

| Role | Responsibility |
|---|---|
| AI Governance Committee | Policy, high-risk approvals, escalations |
| Business Unit AI Leads | Use case intake, local oversight |
| AI Risk/Compliance Team | Regulatory alignment, audit support |
| Engineering AI Team | Technical standards, security review |
| Legal/Privacy Counsel | Data use, contracts, liability |

---

## Common Governance Failures

- **Rubber-stamp committees** that approve everything without meaningful review
- **Governance-by-checklist** that produces documentation but not accountability
- **No post-deployment oversight** — governance stops at launch
- **Unclear accountability** — committee approval diffuses responsibility without assigning it

---

## Related

- [AI Policy](../governance/ai-policy.md)
- [Human Oversight](../governance/human-oversight.md)
- [AI Strategy](ai-strategy.md)
- [Compliance](../governance/compliance.md)
