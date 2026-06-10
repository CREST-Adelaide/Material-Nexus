# Naming Conventions

Consistent names make repos sortable, linkable, and grep-friendly.

---

## Folders

| Scope | Format | Good | Bad |
|-------|--------|------|-----|
| Top-level section | `kebab-case`, plural noun | `courses`, `interview-prep` | `FreeCourses`, `InterviewPrep` |
| Course / lab | `kebab-case`, include year if versioned | `applied-llms-mastery-2024` | `Applied_LLMs_Mastery_2024` |
| Day unit | `day-NN-short-slug` | `day-06-tame-your-inbox` | `Day6`, `day6_inbox` |
| Research year | `YYYY` | `2024`, `2025` | `24`, `year-2024` |
| Report project | `kebab-case` | `state-of-ai-2025` | `StateOfAI2025Report` |

**NN** = zero-padded two digits (`01`, `09`, `10`).

---

## Markdown Files

| Type | Format | Example |
|------|--------|---------|
| Chapter | `NN_snake_case_topic.md` | `03_evaluation_building_blocks.md` |
| Week | `weekNN_topic.md` | `week4_RAG.md` |
| Part | `partN_topic.md` | `part1_what_are_ai_agents.md` |
| Day theory | `learn.md` | (fixed name inside day folder) |
| Day practice | `build.md` | (fixed name inside day folder) |
| Agent prompts | `agent-instructions-{action}.md` | `agent-instructions-finalize-setup.md` |
| Standalone guide | `kebab-case-topic.md` | `rag-roadmap.md` |
| Paper list | `{month}_list.md` | `january_list.md` |
| FAQ | `FAQ.md` or `faq.md` | pick one per repo, stay consistent |

---

## Images & Assets

```
courses/my-course/
├── images/              # Preferred name (pick ONE per course)
│   ├── header.jpg       # Course banner
│   ├── sample-cert.png
│   └── chapter_03/      # Group by chapter/day if many files
│       └── diagram.png
```

Alternatives: `img/`, `diagrams/` — acceptable, but don't mix all three in one course.

**File names:** `kebab-case` or `snake_case`, lowercase, descriptive.

```
hero-image.png          ✓
Chapter3_Final_v2.PNG   ✗
```

---

## Sorting Rules

GitHub and file browsers sort lexicographically. Design names so **logical order = alphabetical order**.

| Content | Trick |
|---------|-------|
| Chapters 1–10 | Zero-pad: `01_`, `02_`, … `10_` |
| Days 1–10 | Zero-pad in folder: `day-01-`, `day-02-` |
| Weeks 1–10 | Zero-pad: `week01_`, `week02_` |
| Parts | `part1_`, `part2_` (single digit OK if <10 parts) |
| Months | Full month name: `january_list.md` not `1_list.md` |

---

## Titles vs. Slugs

- **Folder/file slug:** short, URL-safe, no spaces — `ai-evals-for-everyone`
- **Display title:** in README H1 — "AI Evals for Everyone"
- **Don't encode** punctuation in slugs: avoid `what's`, use `what-is` or `whats`

---

## Versioning

When releasing a new edition:

```
courses/applied-llms-mastery-2024/   # frozen
courses/applied-llms-mastery-2025/   # new cohort
```

Don't overwrite in place if people link to the old URL. Add a note in the old README: "Superseded by [2025 edition](../applied-llms-mastery-2025/)."

---

## Reserved / Special Files

| File | Location | Notes |
|------|----------|-------|
| `README.md` | Every major folder | Required |
| `LICENSE.md` | Repo root | Required for public repos |
| `CONTRIBUTING.md` | Repo root | Recommended |
| `.gitignore` | Repo root + labs | Ignore secrets, checkpoints |
| `slides.html` | Course root | Optional single-file deck |
