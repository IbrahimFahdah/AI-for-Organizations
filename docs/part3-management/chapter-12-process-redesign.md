# Chapter 12: Redesigning Processes for AI

AI inserted into an unchanged process usually produces marginal gains. The bigger opportunity — and the bigger challenge — is redesigning the process around what AI makes possible.

---

## Human + AI Workflows

The most effective AI deployments redesign the division of labor between humans and AI:

| Task type | AI role | Human role |
|---|---|---|
| High-volume, repetitive | Primary executor | Exception handler |
| Judgment-intensive | Input provider / first draft | Decision maker |
| Novel or complex | Research assistant | Full owner |
| High-stakes, irreversible | Advisory input | Final authority |

Design the workflow before deploying the AI.

---

## Operational Redesign

Steps to redesign a process for AI:

1. **Map the current process** — every step, owner, time, and error rate
2. **Identify the constraint** — what limits throughput or quality
3. **Determine AI's role** — where does AI change the constraint, not just one step around it
4. **Redesign the workflow** — adjust steps, roles, and review mechanisms
5. **Test with a pilot group** — validate before rolling out
6. **Measure the delta** — compare to baseline

---

## Automation Boundaries

Not every step in a process should be automated. Define explicit automation boundaries:

- What is automated end-to-end
- What requires human confirmation before execution
- What AI should never do (irreversible actions, regulated decisions)

Automation without boundaries creates liability when AI acts beyond its scope.

---

## Escalation Models

Every AI workflow needs an escalation path:

```
AI handles standard case
    → Low-confidence output? → Human review
    → Edge case detected?    → Human review
    → Error reported?        → Incident response
    → System unavailable?    → Manual fallback
```

Design escalation before deployment. Do not discover it during an incident.

---

## AI-Assisted Decision Flows

For decisions where AI provides input but humans decide:

- Present AI output with confidence indicators, not just answers
- Show the sources or reasoning behind the output
- Make it easy to override and record why
- Track override rates — high override = AI isn't working; zero override = humans aren't reviewing

---

## Key Takeaways

- AI in an unchanged process improves one step; AI in a redesigned process improves the system.
- Automation boundaries must be explicit — especially for irreversible actions.
- Design escalation paths before deployment, not after incidents.

**Common mistake:** Optimizing the AI component of a workflow while the bottleneck is elsewhere in the process.
