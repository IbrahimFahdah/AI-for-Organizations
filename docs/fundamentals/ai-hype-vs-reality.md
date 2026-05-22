# AI Hype vs Reality

## Overview

Every major AI capability announcement is followed by a wave of organizational interest, vendor promises, and implementation projects — many of which fail quietly. This section provides a framework for separating what AI systems can reliably do from what they are claimed to do.

---

## What AI Systems Actually Do

Modern AI systems, including large language models and multimodal models, are statistical systems trained on large datasets. They:

- **Generate plausible outputs** — not verified outputs
- **Match patterns** — they do not reason in the human sense
- **Degrade outside their training distribution** — novel situations produce unreliable results
- **Hallucinate** — confidently produce false information when uncertain

This is not a deficiency to be fixed in the next release. It is a structural property of how these systems work.

---

## Common Overclaims

### "AI understands your business"

AI models do not understand anything. They predict tokens. A model that produces accurate-sounding answers about your industry has seen similar text during training — it does not have domain knowledge in a meaningful sense.

**Implication:** Never deploy AI outputs without validation mechanisms proportional to the stakes involved.

### "AI will replace [role]"

Wholesale role replacement by AI is rare in practice. What happens more commonly: tasks within roles shift, workflows change, and the skills required for a role evolve. Headcount reductions from AI have occurred, but they are typically in high-volume, narrow-task functions.

**Implication:** Focus AI planning on task-level analysis, not job-level replacement.

### "AI is improving exponentially"

Capability improvements are real but uneven. Some benchmarks improve rapidly; real-world reliability, consistency, and trustworthiness improve more slowly. The gap between benchmark performance and production performance is significant.

**Implication:** Evaluate AI for your specific use case, not general benchmark scores.

---

## Useful Mental Models

### The 80/20 Problem

AI often handles 80% of a task well and 20% poorly — and the 20% is unpredictable. For many applications, this is not good enough. Knowing where the 80% ends matters more than celebrating the 80%.

### Automation Bias

People tend to over-trust automated outputs. When AI is in the loop, human reviewers often become less rigorous, not more. This is well-documented in medical, legal, and financial contexts.

### The Demo Gap

AI demos are curated. Production deployments face messy inputs, edge cases, ambiguous requests, and adversarial users. Evaluating AI from demos systematically overestimates production performance.

---

## Questions to Ask Vendors

- What is the error rate on your specific task type, not aggregate benchmarks?
- How does performance degrade on edge cases or unusual inputs?
- What happens when the model is wrong — how does the system fail?
- What is the latency and cost at production volume?
- What data is used to train or fine-tune this model, and who owns it?

---

## Related

- [Organizational Readiness](organizational-readiness.md)
- [AI Adoption Failures](ai-adoption-failures.md)
- [Vendor Risk](../leadership/vendor-risk.md)
