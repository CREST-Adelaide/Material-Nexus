# Material Share Repo Guide

A reference structure for GitHub repos that publish **courses, guides, research curations, interview prep, and notebooks** — inspired by patterns from [awesome-generative-ai-guide](https://github.com/aishwaryanr/awesome-generative-ai-guide).

Use this repo as a **blueprint**, not a rigid spec. Pick the layout that matches your content type.

---

## Quick Start

1. Read [docs/STRUCTURE.md](./docs/STRUCTURE.md) — top-level layout and when to use each folder
2. Pick an example from [examples/](./examples/) that matches your content
3. Copy the matching skeleton from [templates/](./templates/)
4. Follow [docs/NAMING.md](./docs/NAMING.md) for file and folder names
5. Wire everything into your root `README.md` (hub page)

---

## Recommended Top-Level Layout

```
your-material-repo/
├── README.md                 # Hub: what this repo is + links to everything
├── LICENSE.md
├── CONTRIBUTING.md           # Optional but recommended for community repos
│
├── courses/                  # Full structured learning paths (rename from free_courses if you prefer)
│   ├── ai-evals-for-everyone/
│   ├── applied-llms-mastery-2024/
│   └── openclaw-mastery/
│
├── guides/                   # Standalone roadmaps, 101s, tool lists (not full courses)
│   ├── rag-roadmap.md
│   ├── agents-101.md
│   └── favourite-tools.md
│
├── labs/                     # Notebooks + sample data (hands-on, runnable)
│   └── agentic-ai-first-system/
│
├── research/                 # Curated papers, reports, trend tables
│   ├── papers/
│   │   ├── 2024/
│   │   └── 2025/
│   └── reports/
│
├── interview-prep/           # Q&A, flashcards, mock scenarios
│
└── assets/                   # Shared images/diagrams used across multiple sections (optional)
```

### Why this split?

| Folder | Put here when… | Avoid putting here… |
|--------|----------------|---------------------|
| `courses/` | Multi-part curriculum with its own README, progression, and completion path | One-off blog-style guides |
| `guides/` | Single-topic references, roadmaps, glossaries | Full 10-day or 10-week curricula |
| `labs/` | Jupyter notebooks, sample datasets, Colab-ready code | Pure markdown theory |
| `research/` | Time-stamped or versioned external content (papers, reports) | Original course content |
| `interview-prep/` | Hiring-focused Q&A and drills | General learning material |

---

## Course Layout Patterns

Pick **one** pattern per course. Do not mix day-based and chapter-based naming inside the same course.

### Pattern A — Chapter-based (best for conceptual courses)

```
courses/ai-evals-for-everyone/
├── README.md                 # Course landing: overview, cert link, chapter index
├── chapters/
│   ├── 01_wth_are_ai_evals.md
│   ├── 02_model_vs_product_evaluations.md
│   └── 10_glossary_of_terms.md
├── images/
│   └── chapter_01/
└── slides.html               # Optional companion deck
```

### Pattern B — Day-based (best for bootcamps / build-along)

```
courses/openclaw-mastery/
├── README.md
├── FAQ.md
├── getting-started.md
├── days/
│   ├── day-01-install-secure/
│   │   ├── learn.md          # Theory
│   │   ├── build.md          # Hands-on steps
│   │   └── agent-instructions-finalize-setup.md  # Optional automation prompts
│   └── day-02-give-it-a-soul/
│       ├── learn.md
│       └── build.md
└── diagrams/
```

### Pattern C — Week-based (best for semester-style courses)

```
courses/applied-llms-mastery-2024/
├── README.md
├── week01_foundations.md
├── week02_prompting.md
├── week03_finetuning.md
└── img/
```

### Pattern D — Part/series (best for crash courses, blog series)

```
courses/agentic-ai-crash-course/
├── README.md
├── part1_what_are_ai_agents.md
├── part2_agent_architecture.md
└── part9_real_world_systems.md
```

### Pattern E — Notebook lab (best for code-first courses)

```
labs/agentic-ai-first-system/
├── README.md                 # Colab links, prerequisites, chapter break markers
├── action_autonomy.ipynb
├── planning_autonomy.ipynb
├── data/
│   └── sops/
├── assets/
│   └── diagrams/
└── .gitignore                # Ignore large outputs, .env, checkpoints
```

---

## Root README Rules (Hub Page)

Your root `README.md` is the **table of contents for the entire repo**. Keep it scannable:

1. **One-line pitch** — what learners get
2. **Featured content** — 5–8 links max, newest first
3. **Announcements** — time-sensitive updates (collapsible or dated section)
4. **Sections by category** — Courses | Guides | Research | Interview Prep | Labs
5. **External links** — certification forms, YouTube playlists, course websites
6. **Contribution note** — link to CONTRIBUTING.md if open to PRs

Do **not** duplicate full course content in the root README. Link to each course's own `README.md`.

---

## Naming Conventions (summary)

| Thing | Convention | Example |
|-------|------------|---------|
| Course folder | `kebab-case`, include year if versioned | `applied-llms-mastery-2024` |
| Chapter files | `NN_snake_topic.md` (zero-padded) | `03_evaluation_building_blocks.md` |
| Day folders | `day-NN-short-slug` | `day-06-tame-your-inbox` |
| Week files | `weekNN_topic.md` | `week4_RAG.md` |
| Part files | `partN_topic.md` | `part1_what_are_ai_agents.md` |
| Images | under `images/`, `img/`, or `diagrams/` per course — pick one | `images/chapter_03/diagram.png` |
| Research papers | `research/papers/YYYY/month_list.md` | `2024/january_list.md` |

Full details: [docs/NAMING.md](./docs/NAMING.md)

---

## What to Improve vs. Legacy Patterns

If you're migrating from a repo like `awesome-generative-ai-guide`, consider:

| Legacy | Recommended |
|--------|-------------|
| `free_courses/` | `courses/` (clearer intent) |
| `resources/` (mixed guides + labs) | Split into `guides/` and `labs/` |
| `research_updates/` | `research/` with `papers/` and `reports/` subfolders |
| Mixed folder casing (`Applied_LLMs_Mastery_2024`) | Consistent `kebab-case` for new content |
| Course with no README | Every course/lab gets its own landing README |
| Giant root README (300+ lines) | Hub links only; detail lives in section READMEs |

You don't need to rename everything at once. **New content follows the new rules; migrate old content when you touch it.**

---

## Examples

| Example | Path | Use when |
|---------|------|----------|
| Hub repo | [examples/hub-repo/](./examples/hub-repo/) | Multi-category material collection |
| Chapter course | [examples/course-chapter-based/](./examples/course-chapter-based/) | 101-style conceptual course |
| Day course | [examples/course-day-based/](./examples/course-day-based/) | Bootcamp / daily build-along |
| Week course | [examples/course-week-based/](./examples/course-week-based/) | Long-form structured program |
| Standalone guides | [examples/standalone-guides/](./examples/standalone-guides/) | Roadmaps, tool lists, glossaries |
| Research curation | [examples/research-curated/](./examples/research-curated/) | Paper lists, state-of-X reports |
| Interview prep | [examples/interview-prep/](./examples/interview-prep/) | Q&A banks |
| Notebook lab | [examples/notebook-lab/](./examples/notebook-lab/) | Colab/Jupyter hands-on |

---

## Templates

Copy-ready skeletons live in [templates/](./templates/):

- `templates/hub-repo/` — empty repo with folder stubs
- `templates/course-chapter/` — chapter-based course starter
- `templates/course-day/` — day-based course starter

---

## Docs

- [STRUCTURE.md](./docs/STRUCTURE.md) — full layout reference
- [NAMING.md](./docs/NAMING.md) — naming and file conventions
- [CONTRIBUTING.md](./docs/CONTRIBUTING.md) — how to add or update material

---

## License

This guide is provided as-is for structuring your own repos. Adapt freely.
# Material-Nexus
