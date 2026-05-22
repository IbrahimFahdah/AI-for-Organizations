# Workflow Integration

## Overview

Integrating AI into a workflow means changing how work gets done, not just adding a new tool. Effective integration requires understanding the existing workflow, identifying where AI creates genuine leverage, and designing the human-AI interaction pattern deliberately.

---

## Integration Patterns

### Augmentation

AI assists a human performing a task. The human retains decision authority.

**Examples:** AI drafts an email; human reviews and sends. AI summarizes a document; human reads and decides.

**When to use:** High-stakes decisions, novel situations, regulated contexts, low error tolerance.

### Routing

AI classifies or routes work, humans handle it.

**Examples:** AI categorizes support tickets by type; agents handle each category. AI flags anomalies; analysts investigate.

**When to use:** High volume, repetitive classification with human handling downstream.

### Automation

AI completes a task end-to-end with no human in the loop for each instance.

**Examples:** AI generates a structured report from data. AI responds to a narrow class of inquiries.

**When to use:** Low-stakes, high-volume, well-defined tasks with strong evaluation criteria. Requires monitoring for drift.

### Hybrid (Human-in-the-Loop)

AI completes work; humans review a sample or high-risk cases.

**Examples:** AI processes 95% of claims automatically; human reviews flagged cases.

**When to use:** Where full automation is possible for most cases but exceptions require judgment.

---

## Integration Design Steps

1. **Map the current workflow.** Document each step, who does it, how long it takes, and what errors occur.
2. **Identify leverage points.** Where is the volume highest? Where do errors have the most impact? Where is the work most repetitive?
3. **Select an integration pattern.** Match the pattern to the stakes and reliability of the AI system.
4. **Design the handoff.** Define exactly how AI output is presented to human reviewers. Unclear handoffs cause errors.
5. **Define failure modes.** What happens when AI output is wrong or unavailable? The fallback must be designed, not discovered.
6. **Measure before and after.** See [ROI and Value](../leadership/roi-and-value.md).

---

## Common Integration Mistakes

- Inserting AI into a process without changing the process (automation without redesign)
- Designing for the happy path only — ignoring what happens when AI fails
- No feedback loop to improve the AI system based on downstream errors
- Optimizing the AI step while the bottleneck is elsewhere in the workflow

---

## Related

- [Process Redesign](process-redesign.md)
- [Employee Adoption](employee-adoption.md)
- [Observability](../engineering/observability.md)
