# Diagram Prompts

Prompts for generating Mermaid diagrams used in this guide.

---

## Architecture Diagrams

```
Generate a Mermaid flowchart showing [ARCHITECTURE PATTERN].

Requirements:
- Left-to-right layout (LR)
- Label each node clearly
- Show data flow direction
- Include error/failure paths if relevant
- Use subgraphs to group related components

Output only the Mermaid code block, no explanation.
```

---

## Decision Trees

```
Generate a Mermaid flowchart for a decision tree that helps a reader decide [DECISION].

Inputs to consider: [list of factors]
Outcomes: [list of outcomes]

Format as a top-down (TD) flowchart.
Use diamond shapes for decision nodes.
Keep labels short (under 8 words per node).
```

---

## Process Flows

```
Generate a Mermaid sequence diagram showing [PROCESS].

Actors: [list of actors/systems]
Show: the sequence of messages/actions
Include: error cases where relevant

Output only the Mermaid code block.
```

---

## Maturity Models

```
Generate a Mermaid diagram showing a progression from [LEVEL 1] to [LEVEL N].

For each level include:
- Level name
- 2-3 key characteristics

Use a left-to-right layout. Each level should be a distinct node.
```
