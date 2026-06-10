# Contributing Material

Guidelines for adding or updating content in a material share repo.

---

## Before You Add Content

1. Decide **which section** it belongs in (`courses/`, `guides/`, `labs/`, `research/`, `interview-prep/`)
2. Check if similar content exists — extend rather than duplicate
3. Pick the **course pattern** (chapter / day / week / part) and stick to it

---

## Adding a New Course

1. Create folder: `courses/your-course-name/`
2. Add `README.md` with:
   - Title, authors, one-paragraph pitch
   - Who it's for / prerequisites
   - Unit index (linked list of chapters/days/weeks)
   - External links (video, certification, community)
3. Add content units following [NAMING.md](./NAMING.md)
4. Add entry to **root README.md** under Courses section
5. Open PR with summary of what's included

---

## Adding a Standalone Guide

1. Create `guides/your-topic.md` OR `guides/your-topic/README.md` if multi-file
2. Link from root README under Guides
3. Keep guides focused — if it grows past ~8 sections, consider promoting to `courses/`

---

## Adding a Lab

1. Create `labs/your-lab-name/`
2. README must include:
   - Colab/open link (if notebook)
   - Required API keys / env vars
   - Step-by-step run order
3. Add `.gitignore` for checkpoints and secrets
4. No large binaries — link externally

---

## Adding Research Curation

1. Paper lists → `research/papers/YYYY/{month}_list.md`
2. Multi-file reports → `research/reports/report-slug/` with own README
3. Include date updated at top of list files

---

## Pull Request Checklist

- [ ] Files follow [NAMING.md](./NAMING.md)
- [ ] New folder has README if it's a course/lab/report
- [ ] Root README updated with link
- [ ] Internal links are relative and tested
- [ ] Images optimized (<500KB where possible)
- [ ] No secrets, API keys, or personal data
- [ ] License-compatible content (original or properly attributed)

---

## Style Notes

- Write markdown for GitHub rendering (avoid exotic HTML)
- Use `##` headings consistently; one H1 per file (the title)
- Code blocks with language tags: ` ```python ` 
- Prefer tables for structured comparisons; keep them narrow
- Emoji in headings: optional, but be consistent within a course
