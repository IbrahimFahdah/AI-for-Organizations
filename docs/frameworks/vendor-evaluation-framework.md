# Vendor Evaluation Framework

## Overview

A structured framework for evaluating AI vendors across technical, commercial, and risk dimensions. Use this before any significant AI vendor commitment.

---

## Evaluation Dimensions

### 1. Technical Capability

Score each criterion 1–5.

| Criterion | Weight | Score | Weighted |
|---|---|---|---|
| Performance on your specific task (tested, not claimed) | 25% | | |
| Latency at target volume | 10% | | |
| Output consistency and reliability | 15% | | |
| Model versioning and stability | 10% | | |
| API quality and documentation | 10% | | |
| Fine-tuning or customization capability | 5% | | |
| Evaluation tooling provided | 5% | | |
| **Technical Total** | **80%** | | |

### 2. Security and Privacy

| Criterion | Weight | Score | Weighted |
|---|---|---|---|
| Data not used for training (opt-out available) | 30% | | |
| SOC 2 Type II or equivalent certification | 20% | | |
| Data residency options | 20% | | |
| Incident response and breach notification | 15% | | |
| Penetration testing and vulnerability disclosure | 15% | | |
| **Security Total** | **100%** | | |

### 3. Commercial Terms

| Criterion | Weight | Score | Weighted |
|---|---|---|---|
| Pricing transparency and predictability | 25% | | |
| Contract flexibility (no excessive lock-in) | 20% | | |
| Deprecation notice period (minimum 12 months) | 20% | | |
| SLA and uptime commitments | 20% | | |
| Exit and data return terms | 15% | | |
| **Commercial Total** | **100%** | | |

### 4. Vendor Stability

| Criterion | Weight | Score | Weighted |
|---|---|---|---|
| Financial health / funding runway | 30% | | |
| Customer references (similar use case) | 25% | | |
| Regulatory track record | 25% | | |
| Product roadmap alignment | 20% | | |
| **Stability Total** | **100%** | | |

---

## Evaluation Process

1. **Define requirements** — acceptance criteria, non-negotiables, priorities
2. **Shortlist** — identify 2–4 vendors for evaluation
3. **Issue RFI** — request responses to standard questions
4. **Run parallel tests** — same test set, same evaluation criteria across vendors
5. **Score independently** — multiple evaluators score independently before comparing
6. **Reference checks** — speak with existing customers in similar contexts
7. **Contract review** — legal and procurement review of terms
8. **Decision and documentation** — record rationale for audit trail

---

## Red Flags

- Refuses to allow testing on your own data before commitment
- Cannot provide performance data beyond aggregate benchmarks
- No clear data processing agreement
- Model version pinning not available
- Deprecation policy vague or short

---

## Related

- [Enterprise AI Strategy](../part2-leadership/chapter-06-enterprise-ai-strategy.md)
- [Security and Reliability](../part4-developers/chapter-22-security-reliability.md)
