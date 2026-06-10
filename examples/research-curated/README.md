# Example: Research Curation

For paper lists, trend tables, and multi-file interactive reports.

## Tree

```
research/
├── papers/
│   ├── 2024/
│   │   ├── january_list.md
│   │   ├── february_list.md
│   │   └── march_list.md
│   └── 2025/
│       └── january_list.md
├── tables/
│   ├── agentic-search-retrieval-table.md
│   └── ai-evaluation-2025-table.md
└── reports/
    └── state-of-ai-2025/
        ├── README.md
        ├── index.html              # or single-page app entry
        ├── styles.css
        ├── script.js
        ├── sections/
        │   ├── 00-opening.html
        │   ├── 02-model-layer.html
        │   └── 07-closing.html
        └── images/
            └── resources/
```

## Monthly Paper List Template

```markdown
# Best GenAI Papers — January 2025

*Last updated: 2025-02-01*

| Paper | Authors | Why it matters | Link |
|-------|---------|----------------|------|
| Title | A, B | One-line summary | [arXiv](url) |

## Honorable mentions
- ...
```

## Multi-File Report README

```markdown
# State of AI 2025 Report

Interactive report on model, infra, and application layers.

## View
- [Open report](./index.html) (GitHub Pages)
- Or browse [sections](./sections/)

## Structure
- `sections/` — HTML slides/sections
- `images/` — assets
```

## When to use

- Content is **curated external** work (papers, links)
- Time-based organization (month/year)
- Original reports with HTML/CSS/JS assets

## Don't

- Mix original course chapters into `research/`
- Commit huge PDFs — link to arXiv/PDF hosts
