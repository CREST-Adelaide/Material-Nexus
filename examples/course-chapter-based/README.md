# Example: Chapter-Based Course

Pattern used by **AI Evals for Everyone** — numbered chapters, images per chapter, optional slides.

## Tree

```
courses/ai-evals-for-everyone/
├── README.md
├── chapters/
│   ├── 01_wth_are_ai_evals.md
│   ├── 02_model_vs_product_evaluations.md
│   ├── 03_evaluation_building_blocks.md
│   ├── 04_building_reference_datasets.md
│   ├── 05_building_evaluation_metrics.md
│   ├── 06_production_challenge.md
│   ├── 07_production_monitoring_strategies.md
│   ├── 08_evaluation_process.md
│   ├── 09_common_misconceptions.md
│   └── 10_glossary_of_terms.md
├── images/
│   ├── header_image.jpg
│   ├── sample_certificate.png
│   ├── chapter_9/
│   └── chapter_10/
└── slides.html                    # optional
```

## Course README Template

```markdown
# AI Evals for Everyone

![Header](./images/header_image.jpg)

Beginner-friendly 101 on AI evaluation.

**Authors:** Name One & Name Two

## Get Certified
1. Read all chapters (or watch videos)
2. Take the [assessment](https://example.com/quiz)
3. Receive certificate

## Chapters
1. [WTH are AI Evals?](./chapters/01_wth_are_ai_evals.md)
2. [Model vs Product Evaluations](./chapters/02_model_vs_product_evaluations.md)
...
10. [Glossary](./chapters/10_glossary_of_terms.md)

## Who Should Take This
- AI engineers, PMs, data scientists
```

## Chapter File Template

```markdown
# Chapter 3: The Evaluation Framework

**Learning objectives**
- Understand the core building blocks of eval systems
- Distinguish offline vs online evaluation

---

(content)

---

## Key takeaways
- ...

**Next:** [Chapter 4 — Building Reference Datasets](./04_building_reference_datasets.md)
```

## When to use

- Conceptual / theory-heavy courses
- Certification paths with linear progression
- Content also published as YouTube playlist (link in README)
