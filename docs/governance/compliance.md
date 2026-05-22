# Compliance

## Overview

AI compliance requirements vary by jurisdiction, industry, and use case. This page provides an orientation to major regulatory frameworks, not legal advice. Organizations should engage legal counsel for jurisdiction-specific requirements.

---

## Regulatory Landscape

### EU AI Act

The EU AI Act classifies AI systems by risk and imposes requirements accordingly:

| Risk Level | Examples | Requirements |
|---|---|---|
| Unacceptable | Social scoring, real-time biometric surveillance | Prohibited |
| High | Hiring, credit, education access, critical infrastructure | Conformity assessment, transparency, human oversight |
| Limited | Chatbots, AI-generated content | Disclosure requirements |
| Minimal | Spam filters, AI in video games | No specific requirements |

Organizations deploying AI in the EU or to EU citizens should assess where their systems fall and what obligations apply.

### GDPR and Privacy Regulations

When AI systems process personal data:
- Legal basis for processing must be established
- Data subject rights (access, deletion, portability) apply to AI-processed data
- Automated decision-making with significant effects requires human review options
- Data protection impact assessments may be required

Similar frameworks apply in California (CCPA), Brazil (LGPD), Canada (PIPEDA), and others.

### Sector-Specific Regulation

| Sector | Relevant Frameworks |
|---|---|
| Financial services | Fair lending laws, model risk management (SR 11-7), MiFID II |
| Healthcare | HIPAA, FDA AI/ML guidance |
| Employment | Equal employment opportunity laws, anti-discrimination |
| Education | FERPA, student data protection |

---

## Model Risk Management

For organizations in regulated financial services, model risk management frameworks (e.g., US Federal Reserve SR 11-7) apply to AI models used in material decisions.

Requirements typically include:
- Model documentation and validation
- Independent review
- Ongoing performance monitoring
- Inventory and governance

---

## Compliance Integration

Compliance should be built into AI governance processes, not bolted on after deployment:

- Include compliance review in the AI use case approval process
- Document compliance assessment for each deployed system
- Maintain an AI inventory with compliance status
- Review compliance status when regulations change or systems are updated

---

## Related

- [AI Policy](ai-policy.md)
- [Data Governance](data-governance.md)
- [Human Oversight](human-oversight.md)
- [Governance](../leadership/governance.md)
