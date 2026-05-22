# AI Strategy

## Overview

An AI strategy defines how an organization will use AI to achieve its goals — and, equally, what it will not do with AI. Without a strategy, AI investment fragments into disconnected pilots and vendor contracts that do not compound.

---

## What a Strategy Is Not

- A list of AI tools to evaluate
- A commitment to "be AI-first"
- A vendor roadmap adopted as internal strategy
- A one-time document produced for a board presentation

---

## Strategy Components

### 1. Problem Portfolio

Identify and prioritize the specific problems AI should address. A good problem for AI has:

- High volume or frequency (automation leverage)
- Clear correctness criteria (evaluability)
- Available training data or prompt examples
- Acceptable cost of error (risk tolerance)

Rank problems by strategic value and feasibility. Not every high-value problem is high-feasibility.

### 2. Capability Build vs Buy

For each priority problem, decide whether to:

- **Buy:** Use an existing AI product or API (faster, less control)
- **Build:** Develop custom models or systems (slower, more control)
- **Augment:** Integrate AI into existing tools via APIs or plugins

Most organizations should default to buy for first deployments and build only where differentiation or data control justifies the cost.

### 3. Sequencing

AI capabilities build on each other. Data infrastructure enables analytics, which enables supervised models, which enables generative applications. Sequence investments so each layer supports the next.

### 4. Risk Appetite

Define explicit risk tolerances for AI errors. Different applications have different stakes:

- Internal productivity tools: higher tolerance for errors
- Customer-facing systems: lower tolerance, human review required
- Regulated decisions (credit, hiring, medical): may require specific compliance approaches

### 5. Governance Model

Specify who approves AI use cases, who monitors deployed systems, and who owns outcomes. See [Governance](governance.md).

---

## Strategy Pitfalls

- **Centralized-only strategy:** Central AI teams that do not engage with business units produce strategy documents that do not affect practice.
- **Decentralized-only strategy:** Business units acting independently produce inconsistent risk profiles and duplicated costs.
- **Horizon mismatch:** Board-level strategy operates on 3-5 year horizons; AI moves faster. Build in review cadences (quarterly minimum).

---

## Related

- [Governance](governance.md)
- [ROI and Value](roi-and-value.md)
- [AI Readiness Framework](../frameworks/ai-readiness-framework.md)
