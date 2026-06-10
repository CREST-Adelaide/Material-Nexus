# Example: Hub Repo (Multi-Category Material Collection)

This mirrors a repo like `awesome-generative-ai-guide` — one GitHub repo as the central hub for many content types.

## Full Tree

```
awesome-genai-hub/                    # or your-domain-hub
├── README.md                         # Hub: featured links + section index
├── LICENSE.md
├── CONTRIBUTING.md
│
├── courses/
│   ├── ai-evals-for-everyone/        # → see course-chapter-based example
│   ├── openclaw-mastery/             # → see course-day-based example
│   ├── applied-llms-mastery-2024/    # → see course-week-based example
│   └── agentic-ai-crash-course/      # → part-based (part1_, part2_, …)
│
├── guides/
│   ├── genai-roadmap.md
│   ├── rag-roadmap.md
│   ├── agents-roadmap.md
│   ├── agents-101-guide.md
│   ├── securing-agentic-ai-systems.md
│   ├── favourite-ai-tools.md
│   └── llm-lingo/
│       └── README.md
│
├── labs/
│   └── agentic-ai-first-system/      # → see notebook-lab example
│
├── research/
│   ├── papers/
│   │   ├── 2024/
│   │   │   ├── january_list.md
│   │   │   └── march_list.md
│   │   └── 2025/
│   │       └── january_list.md
│   ├── reports/
│   │   └── state-of-ai-2025/
│   └── tables/
│       └── ai-evaluation-2025-table.md
│
└── interview-prep/
    ├── README.md
    └── 60-gen-ai-questions.md
```

## Root README Skeleton

```markdown
# Awesome GenAI Hub

One-stop repo for courses, guides, research, and interview prep.

## Featured
- [OpenClaw Mastery](courses/openclaw-mastery/README.md) — NEW
- [AI Evals for Everyone](courses/ai-evals-for-everyone/README.md)

## Courses
| Course | Description |
|--------|-------------|
| [Applied LLMs Mastery 2024](courses/applied-llms-mastery-2024/) | 10-week LLM applications |
| [AI Evals for Everyone](courses/ai-evals-for-everyone/) | Evaluation 101 + cert |

## Guides
- [5-day GenAI Roadmap](guides/genai-roadmap.md)
- [RAG Roadmap](guides/rag-roadmap.md)

## Research
- [Best papers — Jan 2025](research/papers/2025/january_list.md)
- [State of AI 2025 Report](research/reports/state-of-ai-2025/README.md)

## Interview Prep
- [60 GenAI Questions](interview-prep/60-gen-ai-questions.md)

## Labs
- [Agentic AI First System](labs/agentic-ai-first-system/README.md)
```

## Mapping from `awesome-generative-ai-guide`

| Current path | Recommended path |
|--------------|------------------|
| `free_courses/` | `courses/` |
| `resources/*.md` (guides) | `guides/` |
| `resources/agentic_ai_course_lil/` | `labs/agentic-ai-first-system/` |
| `research_updates/` | `research/` |
| `interview_prep/` | `interview-prep/` |
