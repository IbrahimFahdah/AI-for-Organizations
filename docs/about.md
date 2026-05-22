# About This Guide

## Purpose

This guide exists to help practitioners — not researchers or vendors — make sound decisions about AI in organizational contexts.

It prioritizes:

- Evidence over enthusiasm
- Tradeoffs over recommendations
- Specificity over generality
- Actionable guidance over theoretical frameworks

---

## Writing Style Guide

### Voice and Tone

- **Direct.** State what is true, not what sounds good.
- **Specific.** Name the tradeoff, not just the concept.
- **Neutral.** Avoid vendor advocacy, promotional language, or hype.
- **Grounded.** Back claims with evidence, documented examples, or explicit acknowledgment of uncertainty.

### What to Avoid

- Filler phrases: "AI is transforming…", "in today's rapidly changing landscape…"
- Unsupported superlatives: "the best approach", "the most important factor"
- False precision: statistics cited without source or context
- Passive voice where active is clearer

### Formatting Conventions

- Use H2 (`##`) for main sections within a page, H3 (`###`) for subsections.
- Use tables for comparisons and tradeoffs.
- Use admonition blocks for warnings, notes, and tips:

```
!!! warning "Title"
    Content here.

!!! note
    Content here.

!!! tip
    Content here.
```

- Use Mermaid for diagrams:

```
    ```mermaid
    flowchart LR
        A --> B
    ```
```

- Code blocks should specify language for syntax highlighting.
- Prefer numbered lists for sequential steps, bullet lists for unordered sets.

### File Naming

- Lowercase, hyphen-separated: `ai-strategy.md`, `data-governance.md`
- No spaces, no underscores in filenames

### Linking

- Use relative links: `[Governance](../governance/ai-policy.md)`
- Link to specific sections where relevant: `[ROI](../leadership/roi-and-value.md#defining-value)`

---

## Contribution Process

1. Open an issue describing the addition or correction.
2. Draft content in `drafts/unfinished/` first.
3. Submit a pull request with the final content moved to the appropriate `docs/` path.
4. All content is reviewed for accuracy, tone, and formatting before merge.

---

## License

Content is licensed under CC BY 4.0. You may reuse, adapt, and redistribute with attribution.
