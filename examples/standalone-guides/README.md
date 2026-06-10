# Example: Standalone Guides

For roadmaps, tool lists, security guides, glossaries — content without a formal course progression.

## Tree

```
guides/
├── genai-roadmap.md               # "Learn GenAI in 5 days"
├── rag-roadmap.md                 # "Learn RAG in 3 days"
├── agents-roadmap.md
├── agents-101-guide.md
├── securing-agentic-ai-systems.md
├── favourite-ai-tools.md
├── 60-ai-projects.md
└── llm-lingo/                     # multi-file glossary
    ├── README.md
    ├── autoregressive.md
    └── context-window.md
```

## Single-File Guide Template

```markdown
# 5-Day GenAI Roadmap

A practical path from zero to building with LLMs.

## Day 1 — Foundations
- Read: ...
- Try: ...

## Day 2 — Prompting
...

## Resources
- [Course: Applied LLMs](../courses/applied-llms-mastery-2024/week1_part1_foundations.md)
```

## Mini-Collection (Glossary) Template

```
guides/llm-lingo/
├── README.md          # Index of all terms
├── term-a.md
└── term-b.md
```

```markdown
# LLM Lingo

Plain-English definitions for common LLM terms.

| Term | Link |
|------|------|
| Autoregressive | [term](./autoregressive.md) |
| Context window | [term](./context-window.md) |
```

## When to use

- Content is reference, not certification
- No fixed "start here → finish here" path
- Promote to `courses/` if you add 8+ sequential units and a cert
