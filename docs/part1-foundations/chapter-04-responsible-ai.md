# Chapter 4: Responsible AI, Risk, and Governance

Responsible AI is not a values exercise — it is risk management. The organizations that treat it seriously avoid the failures that generate regulatory scrutiny, reputational damage, and legal liability.

---

## Data Privacy

AI systems that process personal data are subject to privacy regulations (GDPR, CCPA, and sector-specific rules). Key obligations:

- Establish a legal basis for using personal data in AI pipelines
- Apply data minimization — send only what is necessary
- Honor data subject rights (access, deletion, correction)
- Document what data flows into which AI systems

The most common gap: employees sending personal data to external AI tools without realizing it violates privacy policy.

---

## Security Risks

AI introduces specific security threats beyond standard software vulnerabilities:

- **Prompt injection** — malicious content in documents or inputs attempts to redirect AI behavior
- **Data exfiltration** — AI outputs may inadvertently reveal sensitive information
- **Training data leakage** — vendor models may surface private data from training

See [Chapter 22](../part4-developers/chapter-22-security-reliability.md) for engineering controls.

---

## Bias and Fairness

AI systems can encode and amplify biases present in training data. In consequential decisions — hiring, lending, benefits eligibility — this creates both legal exposure and genuine harm.

Practical steps:
- Test model outputs across demographic subgroups before deployment
- Apply higher scrutiny to AI used in regulated decision contexts
- Establish a clear process for investigating bias complaints

---

## Regulatory Considerations

| Framework | Scope | Key Requirement |
|---|---|---|
| EU AI Act | EU market | Risk classification; high-risk systems require conformity assessment |
| GDPR | Personal data | Automated decision rights; impact assessments |
| US sector rules | Finance, healthcare, employment | Model risk management, anti-discrimination |

Regulatory requirements are jurisdiction- and use-case-specific. This is context, not legal advice.

---

## Human Oversight

Every deployed AI system should have:

- A named accountable owner
- Defined criteria for when a human must review AI output
- A process for correcting errors
- A mechanism for affected parties to contest AI decisions

Automation does not eliminate accountability — it concentrates it.

---

## Responsible AI Frameworks

Useful reference frameworks:

- [NIST AI Risk Management Framework](https://www.nist.gov/artificial-intelligence) — structured risk management
- [EU AI Act risk tiers](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689) — regulatory classification
- [Google PAIR Guidebook](https://pair.withgoogle.com/) — human-centered AI design

Adopt a framework as a starting point, not a compliance checklist.

---

## Key Takeaways

- Responsible AI is a risk discipline, not a PR exercise.
- Privacy, security, bias, and oversight each require concrete controls — not just policies.
- Governance needs to be designed before deployment, not after an incident.

**Common mistake:** Publishing an AI ethics statement without a governance process behind it.
