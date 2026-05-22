# AI for Organizations

A practitioner's guide to adopting, deploying, and governing AI in enterprise and institutional settings.

This repository contains the source for a documentation-first book published via [GitHub Pages](https://pages.github.com/) using [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

## Scope

The guide covers:

- **Fundamentals** — separating AI reality from hype and assessing organizational readiness
- **Leadership** — strategy, governance, ROI measurement, and vendor management
- **Operations** — workflow integration, change management, and employee adoption
- **Engineering** — architecture, RAG systems, agents, security, and evaluation
- **Governance** — policy, data governance, compliance, and human oversight
- **Case Studies** — documented real-world deployments with lessons learned
- **Frameworks** — reusable readiness, maturity, and vendor evaluation frameworks

## Local Development

```bash
pip install mkdocs-material
mkdocs serve
```

Visit `http://localhost:8000` to preview the site.

## Publishing

The site deploys automatically to GitHub Pages on every push to `main` via the included GitHub Actions workflow.

Manual deploy:

```bash
mkdocs gh-deploy
```

## Repository Layout

```
docs/          Published content (source of truth)
drafts/        Work in progress — not published
research/      References, source links, raw statistics
prompts/       Editorial and diagram generation prompts
presentations/ Slide decks and workshop materials
```

## Contributing

See [docs/about.md](docs/about.md) for the writing style guide and contribution process.

## License

See [LICENSE](LICENSE).
