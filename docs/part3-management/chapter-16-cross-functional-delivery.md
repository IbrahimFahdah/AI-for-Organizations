# Chapter 16: Cross-Functional AI Delivery

AI projects involve more functions than typical software projects: business units, data teams, engineering, legal, risk, and change management. Coordinating across these functions is a primary delivery challenge.

---

## Business and Technical Collaboration

The most common failure mode: technical teams build what they think was asked; business teams expected something different.

Prevent it:
- Business and technical owners jointly define success criteria before build starts
- Include business representatives in sprint reviews
- Demo on real-world tasks, not curated examples
- Document decisions and rationale as they are made

---

## Agile AI Delivery Models

Standard agile works for AI with adjustments:

| Standard Agile | AI Adaptation |
|---|---|
| User stories define acceptance | Add quality thresholds as acceptance criteria |
| Sprint demo shows features | Sprint demo includes quality metrics |
| Definition of done = deployed | Definition of done = deployed + monitored |
| Velocity measures throughput | Include evaluation cycle time |

Treat model evaluation as a first-class sprint activity, not a post-delivery check.

---

## Vendor Coordination

When AI involves external vendors:

- Define integration points and data formats before vendor contract is signed
- Include testing requirements in the contract (vendor must support evaluation on your data)
- Agree on incident escalation and response SLA
- Assign an internal owner for the vendor relationship

Vendor management without an internal owner drifts. Someone has to be accountable.

---

## Working with Data Teams

Data teams are often the bottleneck in AI projects:

- Involve data teams in use case assessment, not just after the decision is made
- Identify data dependencies early (what data is needed, in what format, with what freshness)
- Plan for data pipeline work in project timelines — it is usually underestimated
- Establish clear ownership of data quality for AI inputs

---

## AI Project Execution Models

Common models:

| Model | Description | Best For |
|---|---|---|
| Embedded | AI engineer on the business team | Deep integration, long-term product |
| Central + embed | Central AI team provides tooling; business team leads | Scaled deployment, shared platform |
| Vendor-led | Vendor delivers; internal team integrates | Speed, limited internal capacity |
| Center of Excellence | CoE provides expertise; business teams execute | Large organizations, governance needs |

---

## Key Takeaways

- Cross-functional alignment at project start is cheaper than misalignment discovered at delivery.
- Adapt agile to include evaluation as a first-class activity, not an afterthought.
- Data team involvement and timelines are consistently underestimated in AI projects.

**Common mistake:** Treating AI delivery as a pure engineering project; underinvesting in business alignment and change management.
