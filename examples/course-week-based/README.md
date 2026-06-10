# Example: Week-Based Course

Pattern used by **Applied LLMs Mastery 2024** — one markdown file per week, flat structure.

## Tree

```
courses/applied-llms-mastery-2024/
├── README.md                      # optional; can rely on root hub README
├── week1_part1_foundations.md
├── week2_prompting.md
├── week3_finetuning_llms.md
├── week4_RAG.md
├── week5_tools_for_LLM_apps.md
├── week6_llm_evaluation.md
├── week7_build_llm_app.md
├── week8_deployment.md
├── week9_case_studies.md
├── week10_research_trends.md
├── week11_foundations.md          # bonus week if needed
└── img/
    └── week4-rag-diagram.png
```

## Week File Template

```markdown
# Week 4: RAG (Retrieval-Augmented Generation)

**Release date:** Feb 5, 2024

## This week you will learn
- What RAG is and when to use it
- Key components: retriever, embedder, generator
- Advanced RAG patterns

## Readings
- (links)

## Content

### Understanding RAG
...

### Key components
...

## Exercises
1. Build a minimal RAG pipeline with ...

## Homework / Project
Extend last week's app with retrieval.

## Next week
[Week 5 — Tools for LLM Apps](./week5_tools_for_LLM_apps.md)
```

## When to use

- Cohort courses (10–12 weeks)
- Content drops on a schedule
- Each week is self-contained enough to read standalone

## Tip

If a week splits into multiple sessions, use `week1_part1_` / `week1_part2_` — still sorts correctly.
