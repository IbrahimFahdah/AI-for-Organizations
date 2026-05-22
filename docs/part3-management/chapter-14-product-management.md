# Chapter 14: Product Management in the AI Era

Managing AI-powered products requires adapting standard product management practices to handle probabilistic behavior, non-deterministic outputs, and the unique challenge of evaluating quality at scale.

---

## AI Product Lifecycle

AI products have an additional phase compared to traditional software:

1. **Define** — problem, users, success criteria
2. **Evaluate** — is AI the right solution; which approach
3. **Build** — model selection, integration, evaluation pipeline
4. **Validate** — test with real users on real tasks
5. **Deploy** — production with monitoring
6. **Operate** — ongoing quality management, model updates, drift detection
7. **Iterate** — improve based on production data

The operate phase is ongoing and resource-intensive. Scope it before you commit to building.

---

## Defining AI Requirements

Traditional requirements: "The system shall do X when Y."
AI requirements: "The system should perform X on cases like Y at quality level Z, with defined handling for cases outside that scope."

Key additions:
- **Quality threshold** — what accuracy/quality is acceptable
- **Scope boundaries** — what the system is and is not for
- **Fallback behavior** — what happens when AI confidence is low
- **Prohibited outputs** — what the system must never produce

---

## Managing Probabilistic Systems

AI systems do not have a correct/incorrect binary — they have quality distributions. Product implications:

- Define quality in terms of distributions, not single outputs
- Measure quality continuously in production, not just during testing
- Accept that perfect accuracy is not achievable; define acceptable error rates instead
- Design the user experience to handle uncertainty (show confidence, allow override)

---

## Feedback Loops and Iteration

AI products improve through feedback. Build feedback mechanisms into the product:

- Explicit feedback (thumbs up/down, correction, rating)
- Implicit feedback (override rate, re-query rate, abandon rate)
- Periodic human review of sampled outputs

Feedback is only valuable if there is a process to act on it. A feedback button with no downstream review is noise.

---

## AI User Experience Considerations

UX for AI differs from traditional software UX:

- **Calibrate expectations** — users who expect perfection will reject useful AI
- **Show uncertainty** — "I'm not confident" is better than a confident wrong answer
- **Make override easy** — users should be able to correct AI without friction
- **Explain when needed** — for consequential outputs, show why the AI said what it said
- **Design for failure** — the unhappy path is more important in AI than in traditional software

---

## Key Takeaways

- The operate phase of an AI product is as important as the build phase — plan for it.
- Define quality in terms of distributions and thresholds, not binary pass/fail.
- Feedback loops only create value if someone acts on the feedback.

**Common mistake:** Treating AI product development as finished at launch; ignoring the ongoing quality management required.
