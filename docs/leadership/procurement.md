# Procurement

## Overview

AI procurement differs from standard software procurement in several important ways: the product is a black box, performance is probabilistic, and the market is moving fast enough that standard multi-year contracts may lock organizations into obsolete approaches.

---

## Procurement Principles

### Evaluate on Your Data, Not Benchmarks

Standard AI benchmarks measure average-case performance across generic tasks. Your use case is specific. Before committing:

- Run the vendor's system against representative samples of your actual data
- Measure the specific quality attributes that matter to your use case
- Compare multiple vendors on the same test set

### Define Acceptance Criteria Before Procurement

Agree on what "good enough" means before signing. This includes:

- Minimum accuracy or quality thresholds
- Latency requirements
- Availability/SLA requirements
- Data handling requirements

Having these defined in advance gives grounds for renegotiation or exit if the vendor fails to deliver.

### Contract Considerations

| Clause | Why It Matters |
|---|---|
| Data processing terms | Defines how your data is used and stored |
| Model version pinning | Protects against unwanted updates |
| Deprecation notice period | Time to adapt when services end |
| Audit rights | Ability to verify compliance claims |
| Exit/data return | What happens when the contract ends |
| Liability limits | Who bears cost of AI errors |

### Avoid Lock-In

- Prefer vendors with standard APIs over proprietary integrations
- Build abstraction layers in your own systems so the vendor can be swapped
- Assess switching cost explicitly before signing long-term commitments

---

## Evaluation Process

1. Define use case requirements and acceptance criteria
2. Shortlist vendors based on capability and market position
3. Issue RFI/RFP with specific technical and contractual requirements
4. Run parallel pilots on your own data
5. Evaluate total cost of ownership, not just licensing
6. Negotiate key contract terms
7. Establish monitoring and review cadence post-award

---

## Related

- [Vendor Risk](vendor-risk.md)
- [Vendor Evaluation Framework](../frameworks/vendor-evaluation-framework.md)
- [AI Strategy](ai-strategy.md)
