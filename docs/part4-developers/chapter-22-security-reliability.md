# Chapter 22: Security, Reliability, and Governance

AI systems have distinct security and reliability failure modes that standard software practices do not cover. Build these in from the start.

---

## Prompt Injection Risks

Prompt injection is the primary attack surface unique to LLM applications. An attacker embeds instructions in content the model processes — documents, emails, user inputs, web pages — that attempt to override system behavior.

**Mitigations:**
- Treat all external content as untrusted; never combine privileged instructions with untrusted input in a way that allows override
- Validate and sanitize inputs before passing to the model
- Never allow model output to directly trigger sensitive actions without validation
- Apply output filtering before using AI responses in consequential operations
- Use a separate, privileged system prompt that cannot be overridden by user input

---

## Hallucination Mitigation

Hallucination cannot be eliminated, but its impact can be controlled:

| Technique | Effect |
|---|---|
| RAG with citations | Ground responses in source documents; show the source |
| Temperature reduction | More deterministic output; less creative, less wrong |
| Structured output | Constrain output format; easier to validate |
| Post-generation fact checking | Automated verification against known facts |
| Human review for high-stakes outputs | Final check before consequential action |
| Explicit uncertainty instructions | Prompt model to say "I don't know" vs. guess |

---

## AI Testing Strategies

Testing AI requires a different approach than testing deterministic software:

- **Functional tests** — does the system handle common cases correctly?
- **Adversarial tests** — does it handle edge cases, malformed inputs, and injection attempts?
- **Regression tests** — do prompt or model changes break previously-working cases?
- **Quality benchmarks** — does output quality meet defined thresholds at scale?
- **Security tests** — can prompt injection succeed; does PII appear in outputs?

Maintain a curated test set. Run it before every deployment change.

---

## Monitoring and Observability

What to monitor in production:

- **Latency** (p50, p95, p99) — user experience and SLA compliance
- **Error rate** — API failures, timeouts, invalid outputs
- **Output quality** — automated scoring against quality rubric
- **Cost** — token consumption; alert on unexpected spikes
- **Refusal rate** — unexpected changes signal model or prompt issues
- **User feedback** — thumbs down, corrections, re-queries

Alert on thresholds; review trends weekly.

---

## Compliance Engineering

Technical controls that support compliance:

- **Audit logging** — every prompt, response, user, timestamp (with PII handling policy)
- **Data classification enforcement** — prevent high-classification data from reaching unauthorized AI systems
- **Access control at retrieval** — users only retrieve documents they are authorized to see
- **Output scanning** — detect and redact PII or sensitive patterns before returning to users
- **Model version tracking** — log which model version produced each output for reproducibility

---

## Key Takeaways

- Prompt injection is the highest-priority AI security risk; treat external content as untrusted.
- Hallucination mitigation is a system design problem, not a prompt wording problem.
- Compliance controls (logging, access control, output scanning) must be built in, not added later.

**Common mistake:** Treating security review as a pre-launch checklist item rather than an ongoing engineering discipline.
