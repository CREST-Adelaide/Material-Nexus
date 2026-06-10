# Example: Notebook Lab

Pattern used by **Agentic AI (LinkedIn Learning)** — Colab-ready notebooks with data and assets.

## Tree

```
labs/agentic-ai-first-system/
├── README.md
├── action_autonomy.ipynb
├── planning_autonomy.ipynb
├── .gitignore
├── data/
│   └── sops/
│       ├── sop_001_standard_returns.txt
│       ├── sop_002_damaged_items.txt
│       └── ...
└── assets/
    └── diagrams/
        └── autonomy-ladder.png
```

## Lab README Template

```markdown
# Agentic AI: Build Your First Agentic System

Hands-on lab for building router and planning agents.

## Notebooks

| Notebook | Chapter | Colab |
|----------|---------|-------|
| action_autonomy.ipynb | Ch 3 — Action autonomy | [Open in Colab](https://colab.research.google.com/github/org/repo/blob/main/labs/agentic-ai-first-system/action_autonomy.ipynb) |
| planning_autonomy.ipynb | Ch 4 — Planning autonomy | [Open in Colab](...) |

## Prerequisites
- OpenAI API key
- Basic Python

## Setup (Colab)
1. Open notebook link
2. Add `OPENAI_API_KEY` to Colab secrets
3. Run cells in order; stop at 🎬 chapter markers

## Data
Sample SOPs in `./data/sops/` — fictional customer support scenarios.

## What you'll build
- V1: Router agent (action autonomy)
- V2: Planning agent with retrieval
```

## .gitignore

```
.env
*.ipynb_checkpoints/
__pycache__/
outputs/
*.pkl
*.parquet
```

## When to use

- Primary deliverable is runnable code
- Course video references notebook chapter markers
- Sample data ships with repo (small files only)

## Large data

If datasets exceed ~10MB, host externally:

```markdown
## Data
Download from [Hugging Face](https://hf.co/datasets/...) and place in `./data/`.
```
