# Chapter 21: Data and Infrastructure

AI systems depend on data pipelines, vector stores, and compute infrastructure. Choices made here determine cost, latency, reliability, and maintainability.

---

## Data Pipelines

AI pipelines ingest, transform, and serve data to models. Key concerns:

- **Freshness** — how recent is the data the model sees?
- **Quality** — garbage in, garbage out applies doubly to AI
- **Lineage** — can you trace where data came from and where it went?
- **Access control** — does the pipeline enforce who can see what?

Common failure: data pipelines built for the pilot that cannot handle production volume or freshness requirements.

---

## Vector Databases

Vector databases store and search embedding vectors for RAG systems.

| Database | Deployment | Notes |
|---|---|---|
| pgvector | Self-hosted (Postgres extension) | Simple, SQL-compatible, good for moderate scale |
| Chroma | Local / self-hosted | Easy to get started; less mature for production |
| Weaviate | Self-hosted / cloud | Rich filtering, good hybrid search |
| Pinecone | Managed cloud | Simple ops, higher cost at scale |
| Qdrant | Self-hosted / cloud | Fast, good filtering, growing ecosystem |

Choice depends on scale, existing infrastructure, and hybrid (keyword + semantic) search needs.

---

## Model Hosting

| Option | Complexity | Privacy | Cost at Scale |
|---|---|---|---|
| Third-party API | Low | Lower | Variable / high |
| Cloud-hosted (own VPC) | Medium | Higher | Medium |
| Self-hosted open source | High | Highest | Lower at volume |

Self-hosting requires GPU infrastructure and model serving expertise. Operational overhead is significant. Only justified at high volume or high data sensitivity.

---

## Cloud AI Services

Major cloud providers offer managed AI platforms:

| Provider | Service | Notes |
|---|---|---|
| Azure | Azure OpenAI | OpenAI models in your Azure tenant |
| AWS | Bedrock | Multiple model providers, good AWS integration |
| GCP | Vertex AI | Google models + third party; strong MLOps tooling |

These offer data residency, logging, and IAM integration at the cost of higher per-token pricing vs. direct API.

---

## Scalability and Performance

Design for production load from the start:

- **Caching** — identical or semantically similar requests; reduces cost and latency
- **Async processing** — for non-real-time tasks, queue requests rather than blocking
- **Batch APIs** — many providers offer lower-cost batch endpoints for offline processing
- **Horizontal scaling** — stateless inference servers scale horizontally
- **Context management** — long conversations accumulate tokens; implement summarization or truncation

---

## Key Takeaways

- Data pipeline quality and freshness are often the production AI bottleneck, not model quality.
- Vector database choice should match scale, hybrid search needs, and existing infrastructure.
- Caching is the highest-ROI performance optimization for most AI applications.

**Common mistake:** Building the data pipeline for the demo dataset; discovering it cannot scale to production volume after go-live.
