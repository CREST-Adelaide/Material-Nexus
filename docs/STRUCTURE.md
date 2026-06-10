# Repository Structure Reference

This document defines the canonical layout for **material share repos** — GitHub repositories whose primary purpose is publishing educational content, not application code.

---

## Design Principles

1. **Discoverability first** — a newcomer lands on root README and finds content in ≤30 seconds
2. **One README per deliverable** — every course, lab, and major report has its own landing page
3. **Predictable depth** — max 4 levels of nesting for markdown content (`repo/courses/name/chapters/file.md`)
4. **Separation by intent** — courses ≠ guides ≠ research ≠ labs ≠ interview prep
5. **Stable URLs** — use folder names you won't rename; put version/year in the name upfront

---

## Top-Level Folders

### `courses/`

Full learning paths with explicit progression (chapters, days, weeks, or parts).

**Required per course:**
- `README.md` — overview, audience, prerequisites, index of units, external links (cert, video)
- At least 3 content units (chapters/days/weeks/parts)

**Optional per course:**
- `FAQ.md`
- `images/` or `diagrams/`
- `slides.html` or `slides/` for presentation decks
- `getting-started.md` for setup that spans the whole course

**Do not put here:**
- Single markdown files (those belong in `guides/`)
- Runnable notebooks without a course wrapper (those belong in `labs/`)

---

### `guides/`

Standalone reference material — no implied start-to-finish path.

Examples:
- `rag-roadmap.md` — "learn RAG in 3 days"
- `agents-101-guide.md` — intro explainer
- `favourite-ai-tools.md` — curated tool list
- `llm-lingo/` — glossary series (folder of related short entries)

**Structure options:**

```
guides/
├── rag-roadmap.md              # Single file
├── securing-agentic-systems.md
└── llm-lingo/                  # Mini-collection
    ├── README.md
    ├── term-autoregressive.md
    └── term-context-window.md
```

---

### `labs/`

Hands-on, runnable content: Jupyter notebooks, sample datasets, starter code.

**Required per lab:**
- `README.md` — Colab/local run instructions, API keys needed, prerequisites
- At least one `.ipynb` or runnable script

**Recommended:**
```
labs/my-lab/
├── README.md
├── notebook.ipynb
├── data/           # Small sample data only; link to external storage for large files
├── assets/         # Diagrams referenced in notebook
└── .gitignore      # outputs/, .env, __pycache__, .ipynb_checkpoints
```

**Large files:** Do not commit datasets >10MB. Link to Hugging Face, GDrive, or S3 in README.

---

### `research/`

Curated third-party content and original research summaries.

```
research/
├── papers/
│   ├── 2024/
│   │   ├── january_list.md
│   │   └── march_list.md
│   └── 2025/
│       └── january_list.md
├── reports/
│   └── state-of-ai-2025/
│       ├── README.md
│       ├── sections/
│       ├── images/
│       ├── styles.css
│       └── script.js
└── tables/
    └── ai-evaluation-2025-table.md
```

**Naming:** Year folders for papers; slug folders for multi-file reports.

---

### `interview-prep/`

Hiring-focused content, kept separate so learners don't confuse it with courses.

```
interview-prep/
├── README.md
├── 60-gen-ai-questions.md
└── img/
```

---

### `assets/` (optional, repo-wide)

Shared branding, badges, or diagrams used across multiple sections. Prefer **course-local** `images/` when assets are course-specific.

---

## Root Files

| File | Purpose |
|------|---------|
| `README.md` | Hub / table of contents |
| `LICENSE.md` | Content license (CC-BY, MIT, etc.) |
| `CONTRIBUTING.md` | How to submit fixes or new material |
| `.gitignore` | Ignore notebook checkpoints, `.env`, large outputs |

---

## Course Internal Structures (pick one)

### Chapter-based

Best for: conceptual courses, certification paths, glossary-heavy content.

```
courses/my-course/
├── README.md
├── chapters/
│   ├── 01_introduction.md
│   ├── 02_core_concepts.md
│   └── 10_glossary.md
└── images/
    ├── header.jpg
    └── chapter_02/
        └── diagram.png
```

**Chapter file template sections:**
1. Title + learning objectives
2. Body content
3. Key takeaways
4. Next chapter link

---

### Day-based

Best for: bootcamps, "build something each day", agent-guided setup.

```
courses/my-bootcamp/
├── README.md
├── FAQ.md
├── days/
│   └── day-03-connect-service/
│       ├── learn.md    # What & why (theory)
│       └── build.md    # How (hands-on)
└── diagrams/
```

**Optional:** `agent-instructions-*.md` files referenced by prompts in `build.md` (keep prefix consistent: `agent-instructions-` or `claw-instructions-`).

---

### Week-based

Best for: semester-length programs, cohort courses.

```
courses/my-program-2024/
├── README.md
├── week01_foundations.md
├── week02_advanced-topic.md
└── img/
```

Each week file is self-contained: objectives, reading, exercises, homework link.

---

### Part-based

Best for: crash courses, blog-to-repo migrations, shorter series.

```
courses/my-crash-course/
├── README.md
├── part1_intro.md
├── part2_deep-dive.md
└── part5_wrap-up.md
```

Parts don't need to be numbered contiguously if some are optional.

---

## README Hierarchy

```
Root README.md          → links to categories + featured items
  └── courses/X/README  → course overview + unit index
        └── chapters/   → individual .md files (no README needed per chapter)
  └── labs/Y/README     → run instructions + notebook links
  └── research/Z/README → report overview (for multi-file reports)
```

**Rule:** If a folder has 3+ files and represents a "product" (course, lab, report), it gets a README.

---

## Linking Conventions

- Use **relative links** inside the repo: `[Chapter 1](../chapters/01_intro.md)`
- Root README links use paths from repo root: `courses/my-course/README.md`
- External cert/quiz/video links go in course README, not buried in chapter 7
- Anchor links in long hub READMEs for GitHub TOC: `## Courses` etc.

---

## Anti-Patterns (avoid)

| Anti-pattern | Why it's bad | Fix |
|--------------|--------------|-----|
| Everything in root README | Unmaintainable, bad SEO | Hub + section READMEs |
| `resources/` junk drawer | Guides, labs, courses mixed | Split by intent |
| Inconsistent naming (`Applied_LLMs` vs `ai-evals`) | Hard to navigate | kebab-case for folders |
| No zero-padding (`chapter_1.md`) | Sort order breaks | `01_`, `02_`, … |
| Images in random paths | Broken links on move | One `images/` per course |
| 500-line single markdown | Hard to review/edit | Split into chapters/parts |
| Binary blobs in git | Slow clones | External hosting + link |

---

## Migration Checklist

When restructuring an existing repo:

- [ ] Add section READMEs before moving files (redirect notes if URLs are public)
- [ ] Update all internal links
- [ ] Keep old paths as symlinks or leave a stub markdown with "moved to X" for 1 release cycle
- [ ] Update root README hub links
- [ ] Verify Colab/badge URLs if notebooks moved
