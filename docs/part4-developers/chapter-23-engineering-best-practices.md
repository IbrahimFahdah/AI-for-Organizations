# Chapter 23: Enterprise AI Engineering Best Practices

Practices that distinguish production-grade AI engineering from prototype AI engineering.

---

## Human-Centered AI Design

The most technically correct AI system fails if it does not fit how people work.

- **Design for the failure case** — what does the user see when AI is wrong? This matters more than the success case.
- **Show uncertainty** — a system that expresses confidence calibration is more trustworthy than one that never hedges.
- **Make correction easy** — override and feedback mechanisms should be zero-friction.
- **Explain on demand** — high-stakes outputs need accessible reasoning, not just results.
- **Test with real users on real tasks** — lab evals and production differ significantly.

---

## Responsible AI Development

Build responsible AI into the development process, not as a post-hoc review:

- Include bias and fairness checks in the definition of done for consequential decisions
- Run adversarial tests before every deployment
- Document known limitations in system documentation
- Include an "intended use" and "out of scope use" specification for every AI component
- Require security review before any agent that takes external actions

---

## Cost Optimization

AI API costs are token-based and compound quickly at scale.

| Technique | Typical Saving |
|---|---|
| Prompt compression | 20–50% (remove redundant instructions) |
| Response caching | 30–80% (for repeated or similar queries) |
| Smaller model for simpler tasks | 50–90% (route to cheaper model by task type) |
| Batch API for async processing | 40–50% (most providers offer batch discounts) |
| Context window management | 10–30% (summarize long conversations rather than passing full history) |

Instrument cost per request from day one. Surprises happen at scale.

---

## AI DevOps and MLOps

Treat AI system components like software: version controlled, tested, deployed via CI/CD.

- **Prompt versioning** — prompts are code; store in git, test before deployment
- **Model version pinning** — explicit model versions in config; changes require testing
- **Evaluation in CI** — run quality benchmarks as part of the deployment pipeline
- **Feature flags** — roll out prompt or model changes to a percentage of traffic
- **Rollback** — define rollback criteria and test the rollback procedure

---

## Reusable AI Architecture Patterns

Patterns worth centralizing rather than rebuilding per project:

- **AI gateway** — central proxy for all model API calls with logging, rate limiting, cost tracking
- **RAG pipeline** — shared document ingestion, chunking, embedding, and retrieval infrastructure
- **Evaluation framework** — shared test sets, scoring rubrics, and benchmark tooling
- **Prompt library** — versioned, tested prompts for common tasks
- **Output parsers** — reliable structured output extraction

---

## Key Takeaways

- Design for the failure case first; success paths take care of themselves.
- Cost optimization requires instrumentation from day one — you cannot optimize what you cannot measure.
- Centralize reusable components; rebuild only what genuinely requires customization.

**Common mistake:** Rebuilding the same pipeline infrastructure in every project team because there is no shared platform.
