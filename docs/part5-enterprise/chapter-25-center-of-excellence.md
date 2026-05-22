# Chapter 25: Creating an AI Center of Excellence

A Center of Excellence (CoE) is a shared organizational function that provides AI capability, standards, and governance to business units. Done well, it accelerates adoption and maintains consistency. Done poorly, it becomes a bottleneck that drives shadow AI.

---

## Governance Structures

The CoE needs authority and accountability, not just advisory status:

- **Approval authority** — can approve or reject AI deployments against defined criteria
- **Standard-setting** — defines technical and governance standards that business units follow
- **Exception handling** — governs deviations from standards
- **Escalation path** — final decision-maker when business unit and governance conflict

A CoE with only advisory authority will be ignored when business units feel urgency.

---

## Shared Services

What the CoE provides to business units:

| Service | Description |
|---|---|
| AI platform | Common infrastructure: gateway, RAG pipeline, evaluation tooling |
| Model access | Managed API access with cost tracking and controls |
| Governance support | Use case review, risk assessment templates |
| Evaluation frameworks | Shared test sets, scoring rubrics, benchmarking |
| Training and enablement | AI literacy programs, developer training |
| Tooling library | Vetted, reusable AI components |

---

## Standards and Frameworks

The CoE owns:

- **AI development standards** — how AI systems are built, tested, and deployed
- **Data standards** — classification, handling, access control for AI pipelines
- **Security standards** — prompt injection controls, logging, access management
- **Evaluation standards** — minimum quality thresholds before deployment
- **Vendor standards** — approved vendor list, procurement requirements

Standards must be practical. Comprehensive standards that are ignored are worse than minimal standards that are followed.

---

## Reusable Enterprise Capabilities

The CoE builds components that business units consume rather than rebuild:

- Shared document ingestion and RAG pipeline
- Centralized AI gateway with logging and cost attribution
- Common evaluation and benchmarking tooling
- Vetted integration patterns for common enterprise systems
- Internal model library (fine-tuned or hosted models)

---

## Key Takeaways

- A CoE without approval authority is an advisory committee; it will be bypassed.
- Shared services reduce duplicated engineering effort across business units.
- Standards only create value if they are practical and enforced consistently.

**Common mistake:** Staffing the CoE with governance and policy experts only, without engineers who can build shared platforms.
